---
layout: post
title: SOLID Design Principles
comments: true
lang: en
thumbnail: hackergotchi_big.png
tags: [oop, design pattern]
---

SOLID: single responsibility (SOR), open-close (OCR), Liskov substitution (LSP), interface segregation (ISP), dependency injection (DI)

(open-close + encapsulation of varies, etc)  => next: Liskov Substitution
DIP
simplistic form: James Shore: Dependency Injection Demystified http://www.jamesshore.com/Blog/Dependency-Injection-Demystified.html
inject an instance variable to an object => so methods (dependency) is injected
so you have a framework to control
constructor injection, method injection, property injection
IOC vs. DI
http://stackoverflow.com/questions/6550700/inversion-of-control-vs-dependency-injection
Dependency Injection (DI) vs. Inversion of Control (IOC) - CodeProject http://www.codeproject.com/Articles/592372/Dependency-Injection-DI-vs-Inversion-of-Control-IO
IOC ( Inversion of Control) explained... - DotNetInterviewQuestions | Facebook https://www.facebook.com/photo.php?v=690253231015623&set=vb.341019362605680&type=2&theater
Pros and Cons of DI
one principle: only when you try to extend the subsystem,
otherwise reduce coupling/add encapsulation b/c of need to know container’s implementation details
decoupling and high cohesion: minor: less coupling == easier unit test
design patterns - What are the benefits of using Dependency Injection and IoC Containers? - Programmers Stack Exchange http://programmers.stackexchange.com/questions/19203/what-are-the-benefits-of-using-dependency-injection-and-ioc-containers
=> SOR
=> OCP
inversion of control - Utility of IoC and Dependency Injection - Stack Overflow http://stackoverflow.com/questions/2394752/utility-of-ioc-and-dependency-injection
dependency==dependency between abstraction and concrete
dependency injection: inject dependency (concrete) to an abstraction, so abstraction CONTROL the dependency :- decoupling
(done) ISP:
Learning The S.O.L.I.D Programming Principles: Interface segregation principle [Part - V] - CodeProjecthttp://www.codeproject.com/Articles/830355/Learning-The-S-O-L-I-D-Programming-Principles-Inte
what is the issue
Clients should not be forced to depend upon interfaces that they don’t use
how to achieve: interface combine methods for different types of objects => segregate them
Example:  the inventory status of a product as well as manipulate inventory levels => two interfaces if one clients use only one
design - Is Interface segregation principle only a substitue for Single responsibility principle? - Stack Overflow http://stackoverflow.com/questions/8099010/is-interface-segregation-principle-only-a-substitue-for-single-responsibility-pr
SRR vs. ISR: SRR: public interface and internal discrepancy, ISR further divide public interface
SRR: domain/model: ok. but some clients may only need part: ISR client originated
LSP
A Good Example of Liskov Substitution Principle | Claudio Lassala's Blog http://lassala.net/2010/11/04/a-good-example-of-liskov-substitution-principle/
http://stackoverflow.com/questions/56860/what-is-the-liskov-substitution-principle
example: Rectangle versus Square
why it’s matters: usually sub-class add constraints, so public interface can’t enforce => why inheritance evil:
typical look: if (someObject is SomeType)
solution: ISR
PENDING: OCP, SRR
