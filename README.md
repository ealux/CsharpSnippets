# C# code snippets

Some helpfull snippets in everyday development for **collections**, **methods**, **Parallel** class, **properties** and **tasks**.

##### Add to Visual Studio

To add snippets to **Visual Studio** copy files to the origin VS C# snippets directory. For example, in my system this is:  
`D:\Program Files\Microsoft Visual Studio\2022\Community\VC#\Snippets\1049\Visual C#\`

##### Use

Use by writing `name` part without extension from `name.snippet`. For example, for `list.snippet` write `list` and press **[Tab]** key.

## Collections

1. `list.snippet` - Use of `List{T}`. `T` is `int` by default

    ```csharp
    List<int> list = new List<int>();
    ```

2. `dict.snippet` - Use of `Dictionary{TKey, TValue}`. `TKey` is `int`, `TValue` is `string` by default

    ```csharp
    Dictionary<int, string> dict = new Dictionary<int, string>();
    ```

3. `bag.snippet` - Use of `ConcurrentBag{T}`. `T` is `int` by default

    ```csharp
    ConcurrentBag<int> bag = new ConcurrentBag<int>();
    ```

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

## Parallel

1. `forp.snippet` - Parallel.For() default construction

    ```csharp
    Parallel.For(0, length, (i, state) =>
    {
        // Your code here
    });
    ```

2. `foreachp.snippet` - Parallel.ForEach() default construction

    ```csharp
    Parallel.ForEach(collection, (item, state) =>
    {
        // Your code here
    })
    ```

3. `foreachpagg.snippet` - Parallel.ForEach() construction with aggregation

    ```csharp
    int aggregatedValue = 0;

    Parallel.ForEach(collection, () => 0, (item, state, localAgg) =>
        {
            // Your code here
            return localAgg;
        },
        (localAgg) => Interlocked.Add(ref aggregatedValue, localAgg)
    );
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

1. `propnull.snippet` - auto-property of `Nullable-type` (default `double`) type

    ```csharp
    public double? MyProperty { get; set; }
    ```

2. `propfullnull.snippet` - property of `Nullable-type` (default `double`) type with private field

    ```csharp
    private double? myVar;

    public double? MyProperty
    {
        get { return myVar; }
        set { myVar = value; }
    }
    ```

## Tasks

1. `taskrun.snippet` - **Task.Run** construction

    ```csharp
    Task.Run(() =>
    {
        // Your code here
    });
    ```

2. `taskrunasync.snippet` - **Task.Run** construction with `async` internal method

    ```csharp
    Task.Run(async () =>
    {
        await // Your code here
    });
    ```

3. `ataskrun.snippet` - **await Task.Run** construction
 
    ```csharp
    await Task.Run(() =>
    {
        // Your code here
    });
    ```