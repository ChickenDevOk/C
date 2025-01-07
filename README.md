# C
C programming
### String trong C là một chuỗi ký tự kết thúc bằng '\0'. Khác với một mảng ký tự
![image](https://github.com/user-attachments/assets/af4f146d-fc3a-42a1-8a0b-fb316e16cd7f)
### Có nhiều cách khởi tạo chuỗi:
```cpp
char str[] = "Hello";
```
Chuỗi ký tự thì không cần gán kích thước trước cho nó.

Nhưng ta cũng có thể gán kích thước trước cũng không sao.
```cpp
char str[15]={'a','b','c','e'};
```
### Đọc chuỗi từ bàn phím
```cpp
char str[50];
scanf("%s",str);
printf("This is string %s",str);
```
Có thể thấy ta chỉ dùng hàm scanf và str không cần dấu "&" là vì tên của mảng cũng chính là địa chỉ cơ sở(địa chỉ của phần tử đầu tiên). Và nó cứ như vậy ghi vào 
tiếp theo từ phần tử này đến phần tử tiếp theo do mảng là một tập hợp các biến có cùng kiểu dữ liệu được sắp xếp liên tiếp nhau.

### Một hạn chế cực lớn của scanf đó là nó chỉ có thể đọc được tới dấu khoảng trắng??? Vì mảng chuỗi kết thúc bằng '\0' mà scanf chỉ đọc được tới đó thì nó ngưng.
### Câu hỏi đặt ra làm cách nào để đọc một chuỗi được phân tách bằng dấu khoảng trắng???
Có nhiều phương pháp để làm điều này những phổ biến nhất:
- Sử dụng hàm **fgets()** để đọc một dòng chuỗi và dùng **gets()** để đọc từng ký tự cho đến khi gặp ký tự xuống dòng hoặc kết thúc tệp **EOF**  .
- Có thể quét các ký tự bên trong hàm scanf().
  
