# Best Practices

## Classes
1. Make classes as restricted as possible
2. 2 top level access modifiers
    a. Public
    b. Package Private
3. Prefer final classes unless explicitly required
4. If a package-private top-level class or interface is used by only one class, 
  consider making the top-level class a private static nested class of the sole class that uses it 
