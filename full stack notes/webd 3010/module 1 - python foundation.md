---
class: webd-3010
module: one
date: january 14, 2023
tags: #python
---

# Module 1 - Python Foundation

### Guiding Questions
- How to develop an environment for execution of python scripts?
- How to create isolate virtual environments to run python?
- What are the basics of python programming language?

### Python Basics

**Python as a Calculator**
- Can do simple math questions, including pascal ()
- / will always return a float; use // to do floor division
- To calculate the remainder, use %
- ** to calculate powers
	- 5 ** 2 is 5 squared (25)
	- 2 ** 7 is 2 to the power of 7 (118)
- = is used to assign a value to a variable, afterwards no result is displayed before the next interactive prompt
- The last printed expression is assigned to the variable _

**Strings**
- \\ can be used to escape quotes
- Strings can be in single or double quotes
- print() works as a function
- \\n to break line
- Strings can be concatenated with + and repeated with *
	- 3 + 'un' + ium will print unununium
- Strings can be indexed (subscripted) with the first character having index 0
	- word = 'Junmyeon'
	- word[0] will print out J
	- word[-1] will print out n
	- word[:2] will print out Ju (character from the beginning to position 2)
	- word[2:5] will print out nmy
- len() returns the length of a string
- Strings are immutable (it is impossible to change their content)

**Lists**
- Python knows a number of compound data types, used to group together other values
- Lists can be written as a list of comma separated values between square brackets
	- squares = [1, 4, 9, 16, 25]
	- squares will print out [1, 4, 9, 16, 25]
- Lists can be indexed and sliced
	- squares[0] will index and return the 0 value item
- Lists support concatenation
- Lists are mutable (it is possible to change their content)
	- cubes[1, 8, 27, 65, 125]
	- cubes[3] = 64 will replace 65 with 64
	- Can also add new items to the end of the list by using append() method
	- cubes.append(216) will add 216 to the end of the list
- Assignment to slices is also possible
	- letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
	- letters[2:5] = ['C', 'D', 'E'] will replace assignments 3, 4, and 5
	- letters[2:5] = [] will remove assignments 3, 4, and 5
	- letters[:] = [] will remove all elements
- It is possible to nest lists
	- a = ['a', 'b', 'c']
	- n = [1, 2, 3]
	- x = [a, n]
	- x will print: ['a', 'b', 'c'], [1, 2, 3]
	- x[0] will print ['a', 'b', 'c']
	- x[0][1] will print b
- len() also applies to lists
	- letters = ['a', 'b', 'c', 'd']
	- >>> len(letters)
	- 4

**Fibonacci Series**
- the sum of two elements defines the nezt
	- a, b = 0, 1
	- >>> while a < 10:
		- print(a)
		- a, b = b, a+b
	- 0
	- 1
	- 1
	- 2
	- 3
	- 5
	- 8
- The first line contains a *multiple assignment*. The variables a and b simultaneously get the new values 0 and 1. On the last line, this is used again, demonstrating that the expressions on the right-hand side are all evaluated first before any of the assignments take place. The right-hand side expressions are evaluated from the left to the right.
- The while loop executes as long as the condition (a < 10) remains true. In Python, any non-zero integer value is true; zero is false. The condition may also be a string or list value. In any sequence, anything with a non-zero length is true, empty sequences are false. The test used in the example is a simple comparison. 
- The body of the loop is indented: indentation is Python's way of grouping statements. At the interactive prompt, you have to type a tab or space for each indented line. In practice, you will prepare more complicated input for Python with a text editor which likely has auto indent. When a compound statement is entered interactively, it must be followed by a blank line to indicate completion (since the parser cannot guess when you have typed the last line). Note that each line within a basic block must be indented by the same amount.
- The print() function writes the value of the arguments it is given. It differs from just writing the expression you want to write in the way it handles multiple arguments, floating point quantities, and strings. Strings are printed without quotes and a space is inserted between items, so you can formate things nicely:
	- >>> i = 256 x 256
	- >>> print('The value of i is', i)
	- The value of i is 65536
- The keyword argument *end* can be used to avoid the newline after the output, or end the output with a different string:
	- >>> a, b = 0, 1
	- >>> while a < 1000:
		- print(a, end=' , ')
		- a, b = b, a+b
	- 0,1,1,2,3,5,8,13,21,34,55,89,144,233,377,610,987,


## More Control Flow Tools

**Else If Statements**
- Example:

> x = int(input("Please enter an integer: "))
Please enter an integer: 42
  if x < 0:
	  x = 0
		print('Negative changed to zero')
elif x == 0:
	print('Zero')
elif x == 1:
	print('Single')
else:
	print('More')
More

- There can be zero or more *elif* parts and the *else* part is optional. The keyword *elif* is short for else if and is useful to avoid excessive indentation. An *if... elif... elif...* sequence is a substitute for the *switch* or *case* statements found in other languages.
- If comparing the same value to several constants, or checking for specific types of attributes, you may also find the *match* statement useful.

**For Statements**
- Rather than always iterating over an arithmetic progression of numbers or giving the user the ability to define both the iteration step and halting condition, Python's *for* statement iterates over the items of any sequence (a list or a string) in the order that they appear in the sequence.

># Measure some strings:
words = ['cat', 'window', 'defenestrate']
  for w in words:
    print(w, len(w))
cat 3
window 6
defenestrate 12`

- Code that modifies a collection while iterating over that same collection can be tricky to get right. Instead, it is usually more straight forward to loop over a copy of the collection or to create a new collection.

># Create a sample collection
>users = {'Hans': 'active', 'Éléonore': 'inactive', '景太郎': 'active'}
># Strategy:  Iterate over a copy
for user, status in users.copy().items():
    if status == 'inactive':
        del users[user]
> # Strategy:  Create a new collection
active_users = {}
for user, status in users.items():
    if status == 'active':
        active_users[user] = status

**The range() Function**
- If you do need to iterate over a sequence of numbers, the built-in function *range()* comes in handy. It generates arithmetic progressions:

> for i in range(5):
    print(i)
0
1
2
3
4

- The given end point is never part of the generated sequence; *range(10)* generates 10 values, the legal indices for items of a sequence of length 10. It is possible to let the range start at another number, or to specify a different increment (even negative; sometimes this is called the 'step'):

> list(range(5, 10))
[5, 6, 7, 8, 9]
list(range(0, 10, 3))
[0, 3, 6, 9]
list(range(-10, -100, -30))
[-10, -40, -70]

- To iterate over the indices of a sequence, you can combine *range()* and *len()* as follows:

> a = ['Mary', 'had', 'a', 'little', 'lamb']
for i in range(len(a)):
    print(i, a[i])
0 Mary
1 had
2 a
3 little
4 lamb

- In most such cases, however, it is convenient to use the *enumerate()* function.
- In many ways, the object returned by *range()* behaves as if it is a list, but in fact it isn't. It is an object which returns the successive items of the desired seqwuence when you iterate over it, but it doesn't really make the list, thus saving space.

> range(10)
> range(0, 10)

- We say such an object is iterable (suitable as a target for functions and constructs that expect something from which they can obtain successive items until the supply  is exhausted). We have seen that the *for* statement is such a construct, while an example of a function that takes an iterable is *sum()*:

> sum(range(4)) # 0 + 1 + 2 + 3
> 6

- Later, we will see more functions that return iterables and take iterables as arguments.

**Break and Continue Statements, and Else Clauses on Loops**
- The *break* statement breaks out of the innermost enclosing *for* or *while* loop.
- Loop statements may have an *else* clause; it is executed when the loop terminates through exhaustion of the iterable (with *for*) or when the condition becomes false (with *while*), but not when the loop is terminated by a *break* statement. This is exemplified by the following loop, which searches for prime numbers:

> for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'equals', x, ' * ', n//x)
            break
    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')
2 is a prime number
3 is a prime number
4 equals 2 * 2
5 is a prime number
6 equals 2 * 3
7 is a prime number
8 equals 2 * 4
9 equals 3 * 3

- When used with a loop, the *else* clause has more in common with the *else* clause of a *try* statement than it does with that of *if* statements. A *try* statement's *else* clause runs when no exception occurs, and a loop's *else* clause runs when no *break* occurs. 
- The *continue* statement, borrowed from C, continus with the next iteration of the loop:

>for num in range(2, 10):
    if num % 2 == 0:
        print("Found an even number", num)
        continue
    print("Found an odd number", num)
Found an even number 2
Found an odd number 3
Found an even number 4
Found an odd number 5
Found an even number 6
Found an odd number 7
Found an even number 8
Found an odd number 9

**Pass Statements**
- The *pass* statement does nothing. It can be used when a statement is required syntactically but the program requires no action.

> while True:
    pass  # Busy-wait for keyboard interrupt (Ctrl+C)

- This is commonly used for creating minimal classes:

> class MyEmptyClass:
    pass

- Another place *pass* can be used is as a place holder for a function or conditional body when you are working on new code, allowing you to keep thinking at a more abstract level. The *pass* is silently ignored.

>def initlog(args):
    pass   # Remember to implement this!

**Match Statements**
- A *match* statement take an expression and compares its value to successive patterns given as one or more case blocks. This is superficially similar to a switch statement, but it's more similar to pattern matching in languages like Rust or Haskell. Only the first pattern that matches gets executed and it can also extract components (sequence elements or object attributes) from the value into variables.
- The simplest form compares a subject value against one or more literals:

>def http_error(status):
    match status:
        case 400:
            return "Bad request"
        case 404:
            return "Not found"
        case 418:
            return "I'm a teapot"
        case _ :
            return "Something's wrong with the internet"

- Note the last block: the "variable name" _ acts as a wildcard and never fails to match. If no case matches, none of the brances is executed. 
- You can combine several literalsd in a single pattern using |

> case 401 | 403 | 404:
    return "Not allowed"

- Patterns can look like unpacking assignments and can be used to bind variables:

> # point is an (x, y) tuple
match point:
    case (0, 0):
        print("Origin")
    case (0, y):
        print(f"Y={y}")
    case (x, 0):
        print(f"X={x}")
    case (x, y):
        print(f"X={x}, Y={y}")
    case _ :
        raise ValueError("Not a point")

- The first pattern has two literals and can be thought of as an extension of the literal pattern shown above. But the next two patterns combine a literal and a variable, and the variable binds a value from the subject (*point*). The fourth pattern captures two values, which makes it conceptually similar to the unpacking assignment *(x, y) = point*
- If you are using classes to structure your data, you can use the class name followed by an argument list resembling a constructor, but with the ability to capture attributes into variables:

> class Point:
    x: int
    y: int
def where_is(point):
    match point:
        case Point(x=0, y=0):
            print("Origin")
        case Point(x=0, y=y):
            print(f"Y={y}")
        case Point(x=x, y=0):
            print(f"X={x}")
        case Point():
            print("Somewhere else")
        case _ :
            print("Not a point")

- You can use positional parameters with some bulitin classes that provide an ordering for their attributes (e.g. data classes). You can also define a specific position for attributes in patterns by setting the __ match _ args __ special attribute in your classes. If it's set to ("x", "y"), the following patterns are all equivalent (and all bind the y attribute to the var variable):

> Point(1, var)
Point(1, y=var)
Point(x=1, y=var)
Point(y=var, x=1)

- A recommended way to read patterns is to look at them as an extended form of what you would pout on the left of an assignment, to understand which variables would be set to what. Only the standalone names (like *var* above) are assigned to by a match statement. Dotted names (like *foo.bar*), attribute names (the *x=* and *y=* above), or class names (recognized by the (...) next to them like *Point* above) are never assigned to.
- Patterns can be arbitrarily nested. For example, if we have a short list of points, we could match it like this:

> match points:
    case []:
        print("No points")
    case [Point(0, 0)]:
        print("The origin")
    case [Point(x, y)]:
        print(f"Single point {x}, {y}")
    case [Point(0, y1), Point(0, y2)]:
        print(f"Two on the Y axis at {y1}, {y2}")
    case _ :
        print("Something else")

- We can add an *if* clause to a pattern, known as a "guard." If the guard is false, *match* goes on to try the next case block. Note that value capture happens before the guard is evaluated:

> match point:
    case Point(x, y) if x == y:
        print(f"Y=X at {x}")
    case Point(x, y):
        print(f"Not on the diagonal")

- Several other key features of this statement:
	- Like unpacking assignments, tuple and list patterns have exactly the same meaning and actually match arbitrary sequences. An important exception is that they don't match iterators or strings.
	- Sequence patterns