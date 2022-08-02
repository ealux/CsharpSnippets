# C# code snippets

Some helpfull snippets in everyday development for **methods**, **properties** and **tasks**.

## Methods

#### non-static

1. `method1null.snippet` - method with 1 argument and null-checking

```csharp
public void MyMethod(object arg)
{
    if (arg == null)
    {
        throw new ArgumentNullException(nameof(arg));
    }
    // Your code here
    throw new NotImplementedException();
}
```

2. `method2null.snippet` - method with 2 argument and null-checking

```csharp
public void MyMethod(object arg1, object arg2)
{
    if (arg1 == null)
    {
        throw new ArgumentNullException(nameof(arg1));
    }
    if (arg2 == null)
    {
        throw new ArgumentNullException(nameof(arg2));
    }
    // Your code here
    throw new NotImplementedException();
}
```

3. `method3null.snippet` - method with 3 argument and null-checking

```csharp
public void MyMethod(object arg, object arg2, object arg3)
{
    if (arg == null)
    {
        throw new ArgumentNullException(nameof(arg));
    }
    if (arg2 == null)
    {
        throw new ArgumentNullException(nameof(arg2));
    }
    if (arg3 == null)
    {
        throw new ArgumentNullException(nameof(arg3));
    }
    // Your code here
    throw new NotImplementedException();
}
```

#### static

1. `smethod1null.snippet` - static method with 1 argument and null-checking

```csharp
public static void MyMethod(object arg)
{
    if (arg == null)
    {
        throw new ArgumentNullException(nameof(arg));
    }
    // Your code here
    throw new NotImplementedException();
}
```

2. `smethod2null.snippet` - static method with 2 argument and null-checking

```csharp
public static void MyMethod(object arg1, object arg2)
{
    if (arg1 == null)
    {
        throw new ArgumentNullException(nameof(arg1));
    }
    if (arg2 == null)
    {
        throw new ArgumentNullException(nameof(arg2));
    }
    // Your code here
    throw new NotImplementedException();
}
```

3. `smethod3null.snippet` - static method with 3 argument and null-checking

```csharp
public static void MyMethod(object arg, object arg2, object arg3)
{
    if (arg == null)
    {
        throw new ArgumentNullException(nameof(arg));
    }
    if (arg2 == null)
    {
        throw new ArgumentNullException(nameof(arg2));
    }
    if (arg3 == null)
    {
        throw new ArgumentNullException(nameof(arg3));
    }
    // Your code here
    throw new NotImplementedException();
}
```

## Properties

#### Double

1. `propd.snippet` - auto-property of `double` type

```csharp
public double MyProperty { get; set; }
```

2. `propdfull.snippet` - property of `double` type with private field

```csharp
private double myVar;

public double MyProperty
{
    get { return myVar; }
    set { myVar = value; }
}
```

#### Bool

1. `propb.snippet` - auto-property of `bool` type

```csharp
public bool MyProperty { get; set; }
```

2. `propbfull.snippet` - property of `bool` type with private field

```csharp
private bool myVar;

public bool MyProperty
{
    get { return myVar; }
    set { myVar = value; }
}
```

#### Nullable-type property

`propnull.snippet` - auto-property of `Nullable-type` (default `double`) type

```csharp
public double? MyProperty { get; set; }
```

`propfullnull.snippet` - property of `Nullable-type` (default `double`) type with private field

```csharp
private double? myVar;

public double? MyProperty
{
    get { return myVar; }
    set { myVar = value; }
}
```

## Tasks

`taskrun.snippet` - **Task.Run** construction

```csharp
Task.Run(() =>
{
    // Your code here
});
```

`taskrunasync.snippet` - **Task.Run** construction with `async` internal method

```csharp
Task.Run(async () =>
{
    await // Your code here
});
```

`ataskrun.snippet` - **await Task.Run** construction
 
```csharp
await Task.Run(() =>
{
    // Your code here
});
```