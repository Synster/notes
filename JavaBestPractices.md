# Best Practices

## Classes
1. Make classes as restricted as possible
2. 2 top level access modifiers
    a. Public
    b. Package Private
3. Prefer final classes unless explicitly required
4. If a package-private top-level class or interface is used by only one class, 
  consider making the top-level class a private static nested class of the sole class that uses it 

### Members
For members (fields, methods, nested classes, and nested interfaces), there are four possible access levels
1. private—The member is accessible only from the top-level class where it is declared.
2. package-private—The member is accessible from any class in the package where it is declared.
3. protected—The member is accessible from subclasses of the class where it is declared and from any class in the package where it is declared.
4. public—The member is accessible from anywhere.
