---
layout: post
title: EclipseCon 2018 and the New CDT
author: Doug Schaefer
date: 2018-10-29 00:00:00 -0400
tags:
- eclipse-preview
---
EclipseCon for me is many things. It's a chance to meet face to face with my fellow CDT contributors. It's an opportunity to run things by each other that may feel awkward over the mailing list or conference calls. It's a chance to get a good feel for what's happening in the rest of the Eclipse IDE and the rest of the Eclipse ecosystem. And it's a chance to hang out with my brothers and sisters in the community and have a few laughs over a few beers going too late into the night but ready to get to work the next morning. It's the best.

This year was special for another reason. The Eclipse IDE is changing. The world of IDEs is changing. A new generation is upon us. And, no, it's not any particular IDE. Nor is it [my fictional Eclipse Two IDE](https://cdtdoug.ca/2017/02/16/what-is-two-much-more-than-yet-another-eclipse-ide.html) :). And believe it or not, it does involve and give a new lease on life to the old workhorse most of us simply call Eclipse. It's a new architecture for all IDEs and the Eclipse community is taking a leadership role in adopting that architecture. Talks on the topic were everywhere at EclipseCon.

<img src="https://code.visualstudio.com/assets/docs/extensions/example-debuggers/extensibility-architecture.png" style="display: block; margin: auto; height: 200px">

Of course I'm talking about the Language Server Protocol and the Debug Adapter Protocol. They were introduced by Microsoft for Visual Studio Code but are also open for adoption by any IDE. It allows users to chose the front end that gives them the best user experience while giving access to the language and debug features they expect from all IDEs. It allows IDE builders to work together on those features and it allows platform vendors to not only help with that and but also give their users and customers choice.

<img src="https://cdtdoug.ca/images/cdt_logo_icon_0.png" style="display: block; margin: auto; height: 120px; background: white">

For the CDT, we've been monitoring the clang/LLVM based language servers closely. clangd has industry momentum but is missing some key features. cquery has a ton of features including extensions to the LSP but has a relatively small community. CDT is working on support for both by leveraging the common Eclipse LSP4E plugins and the Generic editor. We have a long way to go before these services reach parity with the current CDT, but working with this larger community, I'm confident we'll get there. And it will solve our problem of keeping up with the ever evolving C++ language standard thanks to the great work that goes into clang.

On the debug side, we've seen a few open source gdb debug adaptors, but none of them are really suitable to the general CDT audience. So to help with that, my collegues at QNX will work with others in the community to build a debug adapter as a part of the CDT. This will be our first foray into the JavaScript/TypeScript world as an Eclipse project. We've built up a tonne of expertise on gdb/IDE integrations over the years and I think we can do a pretty good job of it. And of course we'll make it available for any IDE to use, which in turn means we're open to any help other IDE providers can offer.

The biggest benefit of this new component architecture is to allow users choice. For CDT, we're going to turn that on it's ear a bit. For us, it's also about sharing our expertise with other IDEs. Our first step down that road will be to produce a set of Visual Studio Code extensions first for our debug adapter to ensure a seamless experience on par with CDT. Depending on what happens on the language server side, we may also produce one for LSP to help integrate clangd which may need to be forked to properly handle gcc-based environments or add features the clangd community aren't interested in.

Our committment has always been to provide the best open tooling for C/C++ developers. For many, many years, that was Eclipse. This new architecture opens the door for alternatives and as the C/C++ community spreads their wings into this new world, we, the CDT contributors, will be there for them.