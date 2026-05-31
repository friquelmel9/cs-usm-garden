---
{"dg-publish":true,"permalink":"/01-atomic/computer-science/copy-constructor/","tags":["cs/oop","university/INF201","cs/lang/cpp"],"dg-note-properties":{"tags":["cs/oop","university/INF201","cs/lang/cpp"]}}
---

# Copy Constructor
In [[C++\|C++]], a copy [[01-atomic/computer-science/Constructor\|Constructor]] is a special kind of constructor used for creating new [[01-atomic/computer-science/Object\|Object]] as a copy of another. 

Normally the [[Compiler\|Compiler]] creates a copy constructor for each [[01-atomic/computer-science/Class\|Class]], however, an used-defined is commonly needed when [[Pointer\|Pointer]] it's used, so that a [[01-atomic/computer-science/Destructor\|Destructor]] and a [[Assignment Operator\|Assignment Operator]] should be written (See [[Rule Of Three\|Rule Of Three]])