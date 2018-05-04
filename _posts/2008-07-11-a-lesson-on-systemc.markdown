---
layout: post
title: A lesson on SystemC
date: '2008-07-11 12:19:00'
---


Here’s a quick look at an example of [SystemC](http://www.systemc.org/home) code, you’re traditional NAND gate:

  
SC_MODULE(my_nand) {  
 sc_in<bool> a, b;  
 sc_out<bool> f;  
  
 void run() {  
 f = !(a && b);  
 }  
  
 SC_CTOR(my_nand) {  
 SC_METHOD(run);  
 sensitive }  
};  
</bool></bool>

It looks like some of hardware description languages I’ve seen such as [Verilog](http://en.wikipedia.org/wiki/Verilog). It lets you model inputs and outputs and a process here named *run* that takes the inputs *a* and *b* and does a nand to produce the output *f*. And it’s all continuous. The module will change the output value as the input values change.

The crazy thing is that this is C++ code. SystemC is a collection of header files that define the templated classes, such as *sc_in*, and some macros, such as *SC_MODULE*, as well as a runtime library that models the continuous nature of electronic signals and calls the process methods, such as *run* in our example, to execute the behaviors at the right time. Very cool use of C++ IMHO.

Now [UML Action Semantics](http://research.cs.queensu.ca/~stl/internal/uml2/bibtex/ref_action.html) isn’t that much different than the behavior and structure modeled here. You have actions that have input pins and output pins and a behavior that runs when all the input pins are ready. All actions run in parallel. It’s a discrete event system as opposed to continuous, as software tends to be as opposed to hardware. But I wonder whether we can use C++ in a similar way to program action semantics.

With a runtime that uses the underlying OS threading system supporting multi-core systems to run the actions in parallel as much as possible and the familiarity of C++ and existing C++ tools, like the CDT :), but used to program a paradigm very different than traditional sequential C, it has me intrigued…


