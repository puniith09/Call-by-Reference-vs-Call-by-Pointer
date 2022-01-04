# Call-by-Reference-vs-Call-by-Pointer
## Call By Reference - 
If the value's address is passed to the function, real and formal arguments share the same address space. As a consequence, every value change within the function is reflected both within and outside the function. Actual and formal arguments will be created in the same memory location.
```
void swap(int &x, int &y)
{
   int temp;
   temp = x; /* save the value at address x */
   x = y;    /* put y into x */
   y = temp; /* put x into y */

   return;
}

swap(a, b);
```
## Call By Pointer -
The pointer technique of passing arguments to a function transfers the address of an argument into the formal parameter. Within the function, the address is used to obtain the actual parameter used in the call. Changes to the parameter have an effect on the provided argument.
```
void swap(int *x, int *y)
{
   int temp;
   temp = *x; /* save the value at address x */
   *x = *y; /* put y into x */
   *y = temp; /* put x into y */

   return;
}

  swap(&a, &b);
```


#### The fundamental difference between utilising references and pointers is that that there are no null references. And, pointers may be empty or may lead to incorrect location in memory. References always refer to "something," but pointers can point to anything.
