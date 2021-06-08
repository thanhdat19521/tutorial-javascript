## Javascript cho người mưới bắt đầu – tutorial javascript cho frontend (phần 2)

### Toán tử
JavaScript hỗ trợ rất nhiều các phép toán khác nhau như phép toán số học (cộng, trừ, nhân, chia, tìm phần dư..) hay các phép toán dùng để đếm số ký tự trong một chuỗi, nối chuỗi... Tương ứng với mỗi phép toán là toán tử dùng để thực hiện các phép toán này.

####    Toán tử số học:
JavaScript hỗ trợ các toán tử cơ bản trong số học như:

            •	Toán tử +: Thực hiện phép cộng
            •	Toán tử -: Thực hiện phép trừ
            •	Toán tử *: Thực hiện phép nhân
            •	Toán tử \: Thực hiện phép chia
            •	Toán tử %: Thực hiện phép tính phần dư

####    Toán tử chuỗi: 
Toán tử + ngoài việc được sử dụng để thực hiện phép cộng thì nó còn được sử dụng để nối các chuỗi
(bao gồm một hoặc nhiều ký tự) lại với nhau:

vi dụ:
```
        var name = "JavaScript" console.log("Xin chào" + " " + name);
```
Hoặc nối chuỗi với số:
```
        console.log("Xin chào" + " " + 2016);
```

####    Toán tử gán giá trị: 
Toán tử = được sử dụng để gán giá trị cho biến:

vi dụ:
```
        var year = 2016;
```

####    Toán tử logic: 
            •	Toán tử  == : So sánh ngang bằng giá trị.
            •	Toán tử  === : So sánh ngang bằng giá trị và kiểu dữ liệu.
            •	Toán tử  != : So sánh khác giá trị.
            •	Toán tử  >= : So sánh lớn hơn hoặc bằng.
            •	Toán tử  <= : So sánh nhỏ hơn hoặc bằng.
            •	Toán tử  AND  hay ( & ): Thực hiện logic kết hợp các biểu thức.
            •	Toán tử  OR  hay ( || ): Thực hiện logic hoặc.
            •	Toán tử  NOT  hay ( ! ): Thực hiện logic phủ định biểu thức.

vi dụ:
```
        var a = 5; 
        var b = "5"; 
        console.log(a == b); // true 
        console.log(a === b); // false
```

### Cấu trúc điều kiện:
Cấu trúc điều khiển được sử dụng để kiểm soát luồng thực thi của các đoạn mã có trong chương trình.

####    Câu lệnh if: 
Câu lệnh if được sử dụng khi việc thực thi của một đoạn mã lệnh phụ thuộc vào tính đúng của của một biểu thức điều kiện cho trước.

ví dụ:
```
        var greet; hour = 7;
        if (hour < 12 && hour > 0) { 
            greet = "Good morning"; 
        }
```

        - Ở ví dụ trên khi biểu thức điều kiện là:

        hour < 12 && hour > 0

        - trả về giá trị là true thì đoạn mã bên trong sẽ được thực thi để gán giá trị cho biến greet.

        greet = "Good morning";

#### Câu lệnh else:
Câu lệnh else được sử dụng kết hợp với if để thực thi đoạn mã lệnh khi biểu thức điều kiện trả về giá trị là false.

ví dụ:
```
        var greet; hour = 13; 
        if (hour < 12 && hour > 0) { 
            greet = "Good morning"; 
        } else { 
            greet = "Hello"; 
        }
```

####  Câu lệnh else if: 
Câu lệnh elseif được sử dụng kết hợp với câu lệnh if để gán thêm điều kiện cho cấu trúc điều khiển.

ví dụ:
```
        var greet; hour = 21; 
        if (hour < 12 && hour > 0) { 
            greet = "Good morning"; 
        } else if (hour >= 12 && hour < 18) { 
            greet = "Good afternoon"; 
        } elseif (hour >= 18 && hour < 21) { 
            greet = "Good evening"; 
        } else { 
            greet = "Good night"; 
        }
```



