# Domain-Driven Design Template
A Domain-Driven Design template project with Gradle &amp; Spring Boot for IntelliJ IDEA. Inspired by 'Domain-Driven Design: Tackling Complexity in the Heart of Software, by Eric J. Evans'.

# Layered Architecture 
The concept of layers in software design is a metaphor that is widely accepted in the industry. They allow different
parts of the system to operate in isolation, conforming to the separation of concerns, while only depending on
themselves and the layers beneath them.

> In an object-orientated program, UI, database, and other support code often gets written directly into the business
objects. Additional business logic is embedded in the behaviour of UI widgets and database scripts. This happens
because it is the easiest way to make things work, in the short run.

So although its easy to 'hack' your new features into the codebase to speed up the implementation delivery, 
forethought into the design of the application, the domain, and its elements will ultimately eliminate future code
debt and make the software easier to maintain, extend and understand. 

## Presentation Layer
> Responsible for showing information to the user and interpreting the user's commands. The external actor might sometimes be another computer system rather than a human user.

## Application Layer
> Defines the jobs the software is supposed to do and directs the expressive domain objects to work out problems. The tasks this layer is responsible for are meaningful to the business or necessary for interaction with the applications layers of other systems. This layer is kept thin. It does not contain business rules or knowledge, but only coordinates tasks and delegates work to collaborations of domain objects in the next layer down. It does not have state reflecting the business situation, but it can have state that reflects the progress of a task for the user or the program.

## Domain Layer
> Responsible for representing concepts of the business, information about the business situation, and business rules. State that reflects the business situation is controlled and used here, even though the technical details of storing it are delegated to the infrastructure. *This layer is the heart of business software*.

## Infrastructure
> Provides generic technical capabilities that support the higher layers; message sending for the application, persistence for the domain, drawing widgets for the UI, and so on. The infrastructure layer may also support the pattern of interactions between the four layers through an architectural framework.

# Separation of Concerns
> Separating the domain layer from the infrastructure and user interface layers allows a much cleaner design of each layer. Isolated layers are much less expensive to maintain, because they tend to evolve at different rates and respond to different needs. The separation also helps with development in a distributed system, to allow different layers to be placed flexibly in different servers or clients, in order to minimise communication overhead and improve performance. (Fowler, 1996)

*All quotes above, unless otherwise cited, are from 'Domain-Driven Design: Tackling Complexity in the Heart of Software, Eric J. Evans.*

*For a repository containing domain-driven design elements as marker interfaces. See my [domain-library](https://www.github.com/TomPlum/domain-library.git).*
