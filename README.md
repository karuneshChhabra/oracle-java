To enable the assertions in command line  --> java -ea <package>.<MainClass>


1 what is object,class , instance and constructor in java ?

Object: An instance of a class, representing a specific entity with state and behavior.
Class: A blueprint for creating objects, defining their attributes and behaviors.
Instance: A specific realization of a class; an object created from a class.
Constructor: A special method used to initialize objects when they are created.




2 impact of jigsaw in java and modularity  
Project Jigsaw, introduced in Java 9, significantly impacted Java's modularity. Here are the key aspects and benefits:

1. Introduction of the Module System
Modular JDK: The JDK itself was broken down into a set of modules, making it possible to use only the parts of the JDK needed for a particular application. This results in smaller and more efficient deployments.
Modular Applications: Developers can create modular applications where modules explicitly declare their dependencies and the modules they expose. This leads to better maintainability and clearer architecture.
2. Strong Encapsulation
Enhanced Encapsulation: Modules provide a stronger form of encapsulation compared to packages. Only the public APIs that a module explicitly exports are accessible to other modules. Internal APIs can be hidden, reducing the risk of unintentional usage.
3. Improved Dependency Management
Explicit Dependencies: Modules must declare their dependencies explicitly using the requires directive. This makes dependencies clear and can help avoid classpath issues that were common in earlier versions of Java.
Transitive Dependencies: The requires transitive directive allows a module to declare that its dependencies are also required by any module that depends on it, simplifying dependency management.
4. Performance and Security
Optimized Performance: The modular structure allows the JVM to perform optimizations more effectively, potentially improving application performance.
Enhanced Security: By restricting access to internal APIs, the module system reduces the attack surface for malicious code, leading to more secure applications.
5. Backward Compatibility
Unnamed Modules: Legacy code that does not use modules can still run on the modular JVM using unnamed modules, ensuring backward compatibility.
6. Tooling and Ecosystem Support
jlink: This tool can create custom runtime images containing only the modules required by an application, further reducing the application footprint.
IDE and Build Tool Support: Popular IDEs and build tools have added support for Java's module system, making it easier for developers to adopt modularity in their projects.
Examples
Module Declaration
A simple module declaration in a module-info.java file:

module com.example.myapp {
    requires com.example.utils;
    exports com.example.myapp.api;
}
Conclusion
Project Jigsaw has made Java more scalable, maintainable, and secure by introducing a powerful module system. It encourages better software design practices and allows developers to create modular applications with clear dependencies and strong encapsulation. The impact of Jigsaw extends beyond just modularity; it has redefined the way Java applications are structured and deployed.





