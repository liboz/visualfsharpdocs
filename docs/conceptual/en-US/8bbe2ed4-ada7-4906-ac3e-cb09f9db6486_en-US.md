# Array.iteri<'T> Function (F#)

Applies the given function to each element of the array. The integer passed to the function indicates the index of element.

**Namespace/Module Path**: Microsoft.FSharp.Collections.Array

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## CAPS_SYNTAX_MD

```
// Signature:
Array.iteri : (int -> 'T -> unit) -> 'T [] -> unit

// Usage:
Array.iteri action array
```

#### CAPS_PARAMETERS_MD
*action*
Type: [int](http://msdn.microsoft.com/en-us/library/025d5455-3622-4ea5-9573-3ecbd4ee1375)**-&gt; 'T -&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)


The function to apply to each index and element.


*array*
Type: **'T**[[]](http://msdn.microsoft.com/en-us/library/def20292-9aae-4596-9275-b94e594f8493)


The input array.




## CAPS_REMARKS_MD
This function is named **IterateIndexed** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following code examples shows the differences between [Array.iter](http://msdn.microsoft.com/en-us/library/94eba0f1-ecd7-459f-b89f-ed2a2923e516), [Array.iter2](http://msdn.microsoft.com/en-us/library/018aa9b9-f186-4142-be8a-a62462794fdc), Array.iteri, and [Array.iteri2](http://msdn.microsoft.com/en-us/library/c041b91f-6080-45b7-867b-2ed983a90405).**
```

    let array1 = [| 1; 2; 3 |]
    let array2 = [| 4; 5; 6 |]
    Array.iter (fun x -> printfn "Array.iter: element is %d" x) array1
    Array.iteri(fun i x -> printfn "Array.iteri: element %d is %d" i x) array1
    Array.iter2 (fun x y -> printfn "Array.iter2: elements are %d %d" x y) array1 array2
    Array.iteri2 (fun i x y ->
                   printfn "Array.iteri2: element %d of array1 is %d element %d of array2 is %d"
                     i x i y)
                array1 array2
```

**Output**
**Array.iter: element is 1**
**Array.iter: element is 2**
**Array.iter: element is 3**
**Array.iteri: element 0 is 1**
**Array.iteri: element 1 is 2**
**Array.iteri: element 2 is 3**
**Array.iter2: elements are 1 4**
**Array.iter2: elements are 2 5**
**Array.iter2: elements are 3 6**
**Array.iteri2: element 0 of array1 is 1 element 0 of array2 is 4**
**Array.iteri2: element 1 of array1 is 2 element 1 of array2 is 5**
**Array.iteri2: element 2 of array1 is 3 element 2 of array2 is 6**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Array Module &#40;F&#35;&#41;](Collections.Array+Module+%28F%23%29.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+%28F%23%29.md)
