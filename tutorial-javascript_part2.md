## Javascript cho người mới bắt đầu – tutorial javascript cho frontend (phần 2)

### Toán tử
JavaScript hỗ trợ rất nhiều các phép toán khác nhau như phép toán số học (cộng, trừ, nhân, chia, tìm phần dư..) hay các phép toán dùng để đếm số ký tự trong một chuỗi, nối chuỗi... Tương ứng với mỗi phép toán là toán tử dùng để thực hiện các phép toán này.

####    Toán tử số học:
JavaScript hỗ trợ các toán tử cơ bản trong số học như:

  - Toán tử +: Thực hiện phép cộng
  - Toán tử -: Thực hiện phép trừ
  - Toán tử *: Thực hiện phép nhân
  - Toán tử \: Thực hiện phép chia
  - Toán tử %: Thực hiện phép tính phần dư
  ---

####    Toán tử chuỗi: 
Toán tử + ngoài việc được sử dụng để thực hiện phép cộng thì nó còn được sử dụng để nối các chuỗi
(bao gồm một hoặc nhiều ký tự) lại với nhau:

vi dụ:
```
var name = "JavaScript";
console.log("Xin chào" + " " + name);
```
Hoặc nối chuỗi với số:
```
console.log("Xin chào" + " " + 2021);
```
  ---

####    Toán tử gán giá trị: 
Toán tử = được sử dụng để gán giá trị cho biến:

vi dụ:
```
var year = 2021;
```
  ---
####    Toán tử logic: 
  - Toán tử  == : So sánh ngang bằng giá trị.
  - Toán tử  === : So sánh ngang bằng giá trị và kiểu dữ liệu.
  - Toán tử  != : So sánh khác giá trị.
  - Toán tử  >= : So sánh lớn hơn hoặc bằng.
  - Toán tử  <= : So sánh nhỏ hơn hoặc bằng.
  - Toán tử  AND  hay ( & ): Thực hiện logic kết hợp các biểu thức.
  - Toán tử  OR  hay ( || ): Thực hiện logic hoặc.
  - Toán tử  NOT  hay ( ! ): Thực hiện logic phủ định biểu thức.

vi dụ:
```
var a = 5; 
var b = "5"; 

console.log(a == b); // true 
console.log(a === b); // false
```
  ---

### Cấu trúc điều kiện:
Cấu trúc điều khiển được sử dụng để kiểm soát luồng thực thi của các đoạn mã có trong chương trình.
- Có nhiều cách để bạn diễn đạt điều kiện trong chương trình.

####    Câu lệnh if: Nếu điều kiện này đúng thì code nằm trong sẽ được thực thi
Câu lệnh if được sử dụng khi việc thực thi của một đoạn mã lệnh phụ thuộc vào tính đúng của của một biểu thức điều kiện cho trước.

ví dụ:
```
var bank_balance = 302.13;
var amount = 99.99;
if (amount < bank_balance) {
   console.log( "I want to buy this phone!" );
}

```

Lệnh if cần một diễn đạt trong dấu ngoặc đơn () được thể hiện như true hoặc false.
<!-- trong ví vụ chúng ta có biểu thức ==(amount < bank_balance)==, -->
  ---
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

  ---

####  Câu lệnh else if: 
Câu lệnh elseif được sử dụng kết hợp với câu lệnh if để gán thêm điều kiện cho cấu trúc điều khiển.

ví dụ:
```
var greet; hour = 21; 
if (hour < 12 && hour > 0) { 
        greet = "Good morning"; 
} else if (hour >= 12 && hour < 18) { 
        greet = "Good afternoon"; 
} else if (hour >= 18 && hour < 21) { 
        greet = "Good evening"; 
} else { 
        greet = "Good night"; 
}
```
  ---
### Function (Hàm)
Hàm là một đoạn mã lệnh được sử dụng để thực hiện một tác vụ cụ thể và tác vụ này có thể được lặp lại nhiều lần một cách dễ dàng.

#### Định nghĩa hàm: 
Để định nghĩa một hàm chúng ta sử dụng cú pháp như sau:

ví dụ: 

```
        function [tên_hàm] () {
            mã lệnh bên trong hàm 
        }
```

Ví dụ sau khai báo một hàm với tên hàm là greet:

```
        function greet () { 
            console.log("Chào bạn"); 
        }
```
Sau khi khai báo hàm thì để thực thi đoạn mã lệnh bên trong hàm chúng ta cần thực hiện việc gọi hàm.

#### Gọi hàm:
Việc gọi hàm được tiến hành khác đơn giản, trong JavaScript chúng ta cần thêm cặp dấu () sau tên hàm đã được định nghĩa trước đó.

ví dụ:

```
        greet();
```
Bạn có thể gọi hàm nhiều lần trong chương trình:
```
        greet();
        greet();
        greet();
```

####	Tham số: 
Tham số được sử dụng để truyền dữ liệu vào đoạn mã bên trong hàm.

ví dụ:

```
        function greet(name) { 
            console.log("Chào " + name); 
        }
```

Ở ví dụ trên khi định nghĩa hàm greet chúng ta sử dụng tham số name để truyền dữ liệu vào bên trong hàm.
Số lượng đối số là không giới hạn:

```
        function greet(title, name) { 
            console.log("Chào " + title + ". " + name); 
        }
```

#### Đối số:
Đối số là dữ liệu thực tế truyền vào bên trong hàm khi hàm được gọi. Với hàm greet được định nghĩa với một tham số là name như ở ví dụ trước chúng ta có thể truyền đối số khi gọi hàm như sau:

```
        greet("JavaScript");
```

Ở ví dụ trên chuỗi JavaScript được sử dụng là đối số để truyền dữ liệu vào hàm.
Trường hợp hàm greet được định nghĩa với hai tham số là title và name:

```
        greet("Mr.", "JavaScript");
```

####	Đối số mặc định:
Khi định nghĩa hàm bạn có thể gán giá giá trị mặc định cho đối số khi hàm được gọi.

```     
        function greet(name = "JavaScript") { 
            console.log(name); 
        }
```

Ở ví dụ trên chuỗi JavaScript được sử dụng làm đối số mặc định truyền vào cho tham số name khi hàm được gọi. Do đó khi hàm greet được gọi mà không có đối số truyền vào như sau:

```
        greet();
```
Thì giá trị mặc định JavaScript sẽ được sử dụng.

## Cảm ơn bạn đã theo dõi, Xin chào và hẹn gặp lại các bạn ở phần [tiếp theo](https://github.com/thanhdat19521/tutorial-javascript/blob/main/tutorial-javascript_part2.md).




