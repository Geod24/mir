# Mir Random

Advanced random number generators.

## Links

 - [API Documentation](http://docs.random.dlang.io)
 - [GitHub](https://github.com/libmir/mir-random)
 - [Mir Algorithm Documentation](http://docs.algorithm.dlang.io)

## {SourceCode}

```d
/+dub.sdl:
dependency "mir-random" version="~>2.2"
+/
import std.range, std.stdio;

import mir.random: randIndex;
import mir.random.algorithm: randomSlice;
import mir.random.variable: NormalVariable;

void main()
{
    auto sample = NormalVariable!double(0, 1)
        .randomSlice(10)
        .array;

    // prints random element from the sample
    sample[$.randIndex].writeln;
}
```
