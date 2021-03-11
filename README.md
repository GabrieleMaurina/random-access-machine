# random-access-machine
Random Access Machine implemented in python.

RAM is an abstract machine that is turing complete and can compute any partial recursive function. Find out more here https://en.wikipedia.org/wiki/Random-access_machine

Its more advanced brother is called While Machine and you can find its implementation here https://github.com/GabrieleMaurina/while-machine

### Install

Run inside terminal:

```python -m pip install random-access-machine```

### Usage

To execute a ram source file:

```python -m ram <ram source file> <integer input>```

To import it in your script:

```python
from ram import RAM

data = 4
program = 'inc 0'

ram = RAM()
result = ram.compute(program, data)

print(result) # 1
```

### How it works

A ram machine has infinite registers numbered from 0, 1, 2..., the input is loaded on register 1 before the execution starts, the output is taken from register 0 when the execution ends.

### Instructions:

 A ram machine supports only 3 basic instructions:

Increment register k by 1:

```inc k```

Decrement register k by 1:

```dec k```

Jump to instruction i if register k is zero:

```jz k i```

### Example

An example program that will double whatever input you give to the machine:

```
jz 1 6
inc 0
inc 0
dec 1
jz 2 1
dec 1
```

### Compile While

It is possible to compile a While program into a Ram program using the method compile_ram of the class WhileMachine. You can find an implementation of the while machine here https://github.com/GabrieleMaurina/while-machine
