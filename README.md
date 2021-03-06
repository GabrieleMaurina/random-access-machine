# random-access-machine
Random Access Machine implemented in python.

### Install

Run inside terminal:

python -m pip install random-access-machine

### Usage

To execute a ram source file:

python -m ram \<ram source file\> \<integer input\>

To import it in your script:

from ram import RAM

data = 4
program = 'inc 0'

ram = RAM()
result = ram.compute(program, data)

print(result)

### Instructions:

Increment register k by 1:

inc k

Decrement register k by 1:

dec k

Jump to instruction i if register k is zero:

jz k i

### Example

An example program to will double whatever input you give to the machine:

jz 1 6
inc 0
inc 0
dec 1
jz 2 1
dec 1

