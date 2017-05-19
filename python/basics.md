* to excute a .py file, just add
```
#!/usr/bin/env python
```
at the head of that .py file.
* a python inner function to see the type of a variable
```
type()
```
* tuple is unchangable, while list is changable
```
tuple_example=(1,2,3,4,5)
list_example=[1,2,3,4,[5,6,7]]
```
* use list_example[down_index:up_index: increment]
to get part of the list in an easier way. Remember the value of up_index is excluded.
```
print list_example[2:5]
```
it will print out '3, 4,5'
```
print list_example[3:0:-1]
```
it will print out '4,3,2'
