---
layout: post
title: Multi-target Makefiles
date: '2009-06-22 22:02:00'
---


I learned a really cool trick with gnu make the other day. I’ve started work on a little game engine based on OpenGL and OpenGL ES targetting Android (of course), the PowerVR simulator for ES 1.1 and 2.0, as well as Linux and Windows desktops. When I first set up the Makefile, I had five different target binaries and I hooked it into the CDT as a Makefile project with five different configs that called make with the right target. Worked fine.

But switching back and forth between each of the configs in order to test an idea was a pain. The CDT does have a Build All Configs menu item but it’s a pain to fire that up since it’s like three levels deep. I got to digging around the gnu make manual in hopes that something would jump out and bite me to make things simpler. And, it did!

Gnu make has a couple of interesting features that help. One, you can create a multi-line macros that take parameters (define … endef) much like the C preprocessor. You can then call ‘eval’ on the resulting string to have that string parsed into the Makefile. That’s awesome on it’s own. But, the second great feature is the ability to define variables on a per target basis. That allows you, for example, to have different CFLAGS settings for different targets.

So combining these features, I’ve been able to set up my builds to generate my library in five subdirectories under lib and objects under obj, all from the same sources. I tried this with a native app at work and I’ve also figured out how to add target specific sources to the mix. What a lifesaver.

Unfortunately, there are gotchas in CDT-land. With each source file compiled by five different compiler and option combinations, it gets pretty confused about what’s what. But the guesses it’s making aren’t so bad and it really drives you to keep the target specifics to a minimum.

To give you an idea of what it looks like, here is the relavent fragment from the makefile for my engine right now. I also just noticed the nice way it does source/header file dependencies using -MD of the gcc compiler and gnu make’s include. Now if I can get the CDT to generate me a SOURCES list automatically…

  
all: android pvr11lx pvr20lx linux mingw  
  
define PLATFORM_rules  
$(1)_OBJS = $$(SOURCES:src/%.cpp=obj/$(1)/%.o)  
$(1)_LIB = lib/$(1)/libdasEngine.a  
  
$(1): $$($(1)_LIB)  
  
$$($(1)_LIB): $$($(1)_OBJS)  
 @mkdir -p lib/$(1)  
 $$(TOOL_PREFIX)ar rc $$@ $$^  
  
obj/$(1)/%.o: src/%.cpp  
 @mkdir -p obj/$(1)  
 $$(TOOL_PREFIX)g++ $$(CFLAGS) -DDAS_PLATFORM_$(1) -MD -o $$@ -c $$  
-include $$($(1)_OBJS:%.o=%.d)  
endef  
  
android: TOOL_PREFIX = arm-none-eabi-  
android: CFLAGS += $(ANDROID_INCLUDE) -DANDROID -fno-exceptions -fno-rtti  
android: $(eval $(call PLATFORM_rules,android))   
  
pvr11lx: CFLAGS += -m32 -I$(HOME)/gl/powervr/1.1/include  
pvr11lx: $(eval $(call PLATFORM_rules,pvr11lx))  
  
pvr20lx: CFLAGS += -m32 -I$(HOME)/gl/powervr/2.0/include  
pvr20lx: $(eval $(call PLATFORM_rules,pvr20lx))  
  
linux: $(eval $(call PLATFORM_rules,linux))  
  
mingw: TOOL_PREFIX = i686-pc-mingw32-  
mingw: $(eval $(call PLATFORM_rules,mingw))


