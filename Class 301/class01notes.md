# Component Based Architecture

## <ins>What is a Component?</ins>

- A component is a modular, portable, replaceable, and reuseable set of well defined functionality that encapsulates its implementation and exporting it as a higher level interface.

- A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

- A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.

### <p> **A component can have three different views - object oriented view, conventional view, and process related view.**</p>

- Object-oriented view

    A component is viewed as a set of one or more cooperating classes. Each problem domain class (analysis) and infrastructure class (design) are explained to identify all attributes and operations that apply to its implementation. It also involves defining the interfaces that enable classes to communicate and cooperate.

- Conventional view

    It is viewed as a functional element or a module of a program that integrates the processing logic, the internal data structures that are required to implement the processing logic and an interface that enables the component to be invoked and data to be passed to it.

- Process-related view

    In this view, instead of creating each component from scratch, the system is building from existing components maintained in a library. As the software architecture is formulated, components are selected from the library and used to populate the architecture.

    A user interface (UI) component includes grids, buttons referred as controls, and utility components expose a specific subset of functions used in other components.

    Other common types of components are those that are resource intensive, not frequently accessed, and must be activated using the just-in-time (JIT) approach.

    Many components are invisible which are distributed in enterprise business applications and internet web applications such as Enterprise JavaBean (EJB), .NET components, and CORBA components.

&nbsp;

## <ins>***Characteristics of Components***</ins>   <!-- answers the question What are the characteristics of a component>

- Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.

- Replaceable − Components may be freely substituted with other similar components.

- Not context specific − Components are designed to operate in different environments and contexts.

- Extensible − A component can be extended from existing components to provide new behavior.

- Encapsulated − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

- Independent − Components are designed to have minimal dependencies on other components.

&nbsp;

## <ins>**Advantages**</ins>  <!-- Answers the question what are the advantages of using component based architecture?>

- Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

- Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.

- Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

- Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

- Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.

- Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

- System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.

- Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

# <ins>**What is Props and How to use it in React**</ins>

- Q. What is props short for?

- A. Props is short for properties

- Q. How are props used in react

- A. Firstly, define an attribute and its value(data)
Then pass it to child component(s) by using Props
Finally, render the Props Data

- Q. What is the flow of props?

- A. Props have a unidirectional flow. (one way from parent to child.)
