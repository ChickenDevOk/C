## C Pointer
Pointer is especial concept in C. Their value content the address of variable. We want to access value of variable by using *
- Dereferencing operation **(*)**: used to declare pointer variable and access the value stored in the address.
- Address operator **&**: used to returns the address of a variable.
![image](https://github.com/user-attachments/assets/4a980294-d870-4894-8e54-5d524693370a)

```cpp
int a =10;//declare and initilize value = 10
int *ptr; //declare pointer to integer data type
ptr = &a;//assign ptr = address of a
printf("%d\n",ptr);//display address of a = value of ptr
printf("%d\n",*ptr);//display value of a
printf("%d",&ptr);// display address of ptr
```
### Types of Pointers in C
Pointer in C have many difference types depending on the data it is pointing to:
1. Interger pointer
2. Array pointer
3. Structure pointer
4. Function pointer
5. NULL pointer
6. Void poitner
7. Wild pointer
8. Constant pointer
9. Pointer to constant
As pointer in C store the memory address, their size is independing of data type they are pointing to. This size of pointers only depends on the system architecture.
- 8 bytes for a 64-bit System
- 4 bytes for a 32-bit System.
### Pointer Arithmetic in C with Example
1. Increase/Decrease of a Pointer
2. Addition of integer to a Pointer
3.  Subtraction of integer to a pointer
4.  Subtracing two pointers of the same type
5.  Comparation of pointers.

