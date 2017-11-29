# learningRepo
##Python til

List comprehensions are actually simple

its a list set to equal the results of a for loop

```
list_ = [[(y + x**2)] for x in range(0, n) for y in range (0,n) if( x = 10)]
```
	      |
This section describes the format of the output in the list, in this case it will be a 

single value if we wanted to use a tuple instead we could set the value to something like 

`[y , x**2]` this would result in the elemtns in the list looking like this [(0,0)(0,0)...]

You can also use a list comprehension to split nested lists, say you have a list like 
[(hi,2),(no,7),(yes,4)] you can use the list comprehension [a for a,b in range(len(list))]
and you will get a list that contains only the first value

You can also use it to filter the list say [b for a,b in range(len(list)) if (a==hi)] 

which will return all of the b valus that corrospond with a being equal to hi

The star opperator is very interesting it allows you to do the following

Krishna 67 68 69
Arjun 70 98 63
Malika 52 56 60
Malika
```
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
```
It creates a dynamic list that will contain all the rest of the items inside the input

().split(), instead of Variadic arguemnts we are looking at a Variadic varible 

A list that will contain as many arguments as it needs to. 


When printing a float using the formatter the precision comes before the float specifier 
    print('{:.2f}'.format(t/len(student_marks[query_name])))
is the correct syntax to print out to 2 decimals

Python allows on the fly modified code using the eval function this lets us do something 

like 

eval("string." + methodFromList + "(" + dynmicArguments + ")"  

This example preforms multiple tests on a single string
```
    s = input()
    for test in ('isalnum','isalpha','isdigit','islower','isupper'):
        print (any(eval("c."+test+"()") for c in s))
```

The any function returns true of any of the functions executed within its context return 

true, for a less complicated example see 
```
str = raw_input()
print any(c.isalnum()  for c in str)
print any(c.isalpha() for c in str)
print any(c.isdigit() for c in str)
print any(c.islower() for c in str)
print any(c.isupper() for c in str)
```