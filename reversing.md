[Back](README.md)

## Reversing 75 p - C Skarp Ud

Here we're hinted to use dnSpy to look at a C# binary.

here we can find what values the sliders need
![example](images/reversing/csharpthreeslidervalues.png)

Oneway now to complete the challenge is to just run the program and change the sliders to these values.
But its also possible to just extract the method and run in an online [C# fiddle tool](https://dotnetfiddle.net/)

![example](images/reversing/csharpgetflag.png)

DotnetFiddle:

```c#
using System;
using System.Text;		
public class Program
{
 public static void Main()
 {
  Console.WriteLine(GetFlagString());
 }

  private static string GetFlagString()
  {
    byte b = 125;
    byte[] array = new byte[]
    {
     51,62,78,6,30,34,14,21,28,15,13,
     34,8,25,24,19,34,18,31,27,8,14,22,
     24,15,20,19,26,34,24,15,34,28,17,17,
     24,15,24,25,24,34,8,25,13,28,22,22,24,9,0
    };
    for (int i = 0; i < array.Length; i++)
    {
     array[i] ^= b;
    }
    return Encoding.UTF8.GetString(array);
  }
}
```

Flag: *NC3{c_sharp_uden_obfuskering_er_allerede_udpakket}*

---

[Back](README.md)
