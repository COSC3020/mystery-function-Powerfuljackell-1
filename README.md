[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```
The mystery function recursively finds the largest value in a provided array
//added in response to reviewer feedback
The code recursively calls mystery() on a slice of the inout array (this slice omits the first address of the given array) allowing it to iterate through the array in its entirety until it finds the largest value. Moreover, this is not tail recursive as it reliant on the return of the recursion in order to complete.
