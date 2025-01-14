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
- Khi pointer tăng hoặc giảm là tăng một lượng bằng kiểu dữ liệu mà nó trỏ vào
  ![image](https://github.com/user-attachments/assets/ddcb51aa-50b6-4802-a49c-6d1f228b093a)
  Là 4bytes nếu là kiểu int hoặc kiểu float
  ![image](https://github.com/user-attachments/assets/29436f3b-a9d2-4b1a-bec0-c891205057b7)
  ![image](https://github.com/user-attachments/assets/99519f4f-7de3-4924-b33f-b24e89b0329c)
### PASSING POINTER TO FUNCTION
```cpp
  void swap(int *a,int *b)
{
  int temp=0;
  tmp = (*a);
 (*a)=(*b);
 *b=tmp;
}
void main()
{
  int a=30;
  int b=60;
printf("%d %d ",a,b);
swap(&a,&b);
printf("%d %d ",a,b);
}
```
![image](https://github.com/user-attachments/assets/20092f79-4b89-4745-b879-c5158015410b)
### POINTER TO POINTER
Con trỏ cấp 2 sẽ lưu địa chỉ của con trỏ cấp 1. Và nó sẽ có quyền chỉnh sửa giá trị mà con trỏ cấp 1 đang chỉ vào.
```cpp
#include <stdio.h>

int main() {
  
      // A variable
    int var = 10;
  
    // Pointer to int
    int *ptr1 = &var;
  
    // Pointer to pointer (double pointer)
    int **ptr2 = &ptr1;  

    printf("var: %d\n", var);          
    printf("*ptr1: %d\n", *ptr1);
    printf("**ptr2: %d", **ptr2);

    return 0;
}
```
![image](https://github.com/user-attachments/assets/a3a5bb60-4320-4243-9f87-d4c0abedb777)
### Chain of Pointer
![image](https://github.com/user-attachments/assets/824c3198-c6e7-41c9-bc44-f59964d80c4a)
## FUNCTION POINTER
Function pointer is a type of pointer that stores the address of a function
- Có nhiều ứng dụng hữu ích như callback function
  ![image](https://github.com/user-attachments/assets/d65d6f03-52c8-4fac-910b-e1376fad3fd5)
Cứ nghĩa đơn giản con trỏ thì lưu địa chỉ của một biến khác. Function ở đây chỉ là một khối các lệnh cùng thực hiện một chức năng nhất định nên nó cũng phải có khu vực địa chỉ mà địa chỉ đầu tiên của Function sẽ được lưu trong con trỏ.
```cpp
int *fptr(int,int);
fptr=&function;
```
## Ứng dụng
```cpp
#include <stdio.h>

int add(int a,int b)
{
    return a+b;
}
int subtract(int a,int b)
{
    return a-b;
}
void calc(int a,int b, int (*fptr)(int,int))
{
    printf("Reuslt: %d\n",fptr(a,b));
}

int main() {
   int a=100;
   int b=90;
   calc(a,b,add);
   calc(a,b,subtract);
    return 0;
}
```
- Viết 2 hàm add và substract
- Một hàm calc truyền vào 2 tham số và một con trỏ hàm với 2 tham số truyền vào là kiểu int
- Ta chỉ cần truyền vào tên hàm thì fptr sẽ trỏ đến tên hàm đó. Tên hàm cũng chính là địa chỉ đầu tiên của hàm đó.




