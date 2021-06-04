### Javascript cho người mưới bắt đầu – tutorial javascript cho frontend (phần 1)

- Javascript là ngôn ngữ lập trình phổ biến nhất trên thế giới trong suốt 20 năm qua. Nó cũng là một trong 3 ngôn ngữ trính của website:
- HTML: Giúp ta thêm nội dung cho website.
- CSS: Định dạng thiết kế, bố cục, phong cách, căn lề,... của website.
- Javascript: Cải thiện cách hoạt động của website.
- Javascript có thể học nhanh và dễ dàng áp dụng cho nhiều mục đích khác nhau, từ việc cải thiện tính năng của website cho đến chạy game và tạo phần mềm trên website.
- Mục tiêu của tutorial này chính là giúp bạn “vượt qua” giai đoạn bắt đầu học javascript.
- Sau khi đọc hết tutorial này bạn (có thể) sẽ nắm được cơ bản về: 

  - Javascript là gì? Tại sao nó lại được dùng nhiều như vậy?
  - Nhúng javascript vào website của bạn
  - biến trong javascript
  - Toán tử trong javascript
  - Câu lệnh rẽ nhánh, câu lệnh điều kiện
  - Hàm và tạo hàm trong javascript
  - Biến toàn cục và biến cục bộ trong javascript
  - Sử dụng firebug để kiểm tra lỗi javascript
  - Vòng lắp trong javascript
  - Events trong javascript
  - DOM trong javascript
  - Data Types
  - Object
  - ...

- Những chủ đề này sẽ là cơ sở cho các bạn có thể tiếp tục với những kiến thức cao hơn ,...

### Javascript là gì?

- JavaScript là ngôn ngữ lập trình thường được dùng chung với HTML để tạo ra các tương tác động cho trang web.
- Trong khi HTML được sử dụng để tạo nội dung và CSS được dùng để trang trí website thì JavaScript được sử dụng để tạo ra các tương tác cho website.
- Ban đầu ngôn ngữ JavaScript được viết ra với mục đích dùng để phục vụ việc tạo các tương tác cho website. Tuy nhiên tới thời điểm hiện tại thì JavaScript đã được phổ biến rộng rãi trong việc tạo các ứng dụng phức tạp như game hay các ứng dụng chạy trên máy chủ.

### Tại sao nó lại được dùng nhiều như vậy?

- Giảm gánh nặng cho server: Ví dụ bạn có thể xác nhận đầu vào (input) người sử dụng trước khi gửi trang tới Sever, từ đó giúp trang tải nhanh hơn do không cần request ngay từ đầu.
- Phản hồi ngay lập tức cho user: Giả sử có quên nhập một thông tin nào đó trên form đăng ký popup, khách hàng cũng không cần cả website load lại từ đầu để điền thêm nếu form popup này được lập trình bởi JavaScript.
- Tăng tương tác với user:  JavaScript cho phép khách hàng có thể tương tác ngay với website bằng cách click chuột hay thông qua bàn phím( đổi màu text hay hình động...)
- Website sinh động hơn với kho giao diện phong phú: Nếu chỉ sử dụng HTML, bạn chỉ có thể tạo ra các giao diện tĩnh, không có DnD (Drag và Drop), Slider hay một Rich Interface (giao diện giày tính năng).

<div style="page-break-after: always"></div>

### Nhúng javascript vào website?

-  Có 3 cách nhúng mã javascript vào website. 

  - Nhúng kiểu internal
  - Nhúng kiểu inline
  - Nhúng kiểu external
  ---
- ***Cách 1: Kiểu internal:*** 

Có thể hiểu là chúng ta chèn code javascript vao cùng một cụm nào đó trong file HTML. Thông thường thì chúng ta hay nhóm ns vào cặp thẻ
*\<head>*  và  *\<body>.*


- Nhúng trong thẻ \<head>:

```

<head>

<script language="javascript">

  alert("Chào mừng bạn đến với tutorial javascript");

</script>

</head>

```

- Nhúng trong thẻ \<body>: 

```
<body>

<script language="javascript">

  alert("Chào mừng bạn đến với tutorial javascript");

</script>

</body>
```
---
- ***Cách 2: Kiểu inline***

Nhúng kiểu này ta có thể chèn ngay vị trí bất kỳ nào của một dòng HTML.

```
<button type="button" onclick="document.getElementById('body’).innerHTML =Date()">

    Nhấn vào để xem thời gian

</button>
```
---
- ***Cách 3: Kiểu external***

Nếu cách 1 và 2 chúng ta viết trực tiếp trên file html thì ở cách này chũng ta tách riêng file javascript và gọi nó thông qua thẻ \<script>

>folder
>|
>|___  index.html
>|
>|__  main.js

```
<script src="./main.js"></script>
```

Trên đây là 3 cách nhúng javascript vào website của bạn, tôi khuyến khích bạn nên dùng cách số 3 (external). Cách này giúp chúng qua quản lý mã code javascript tốt hơn và gọn gàng hơn,...

___
### Biến trong javascript

- **Biến**: Lưu trữ dữ liệu để có thể sử dụng lại sau đó là một trong những công việc quan trọng của lập trình. Trong JavaScript bạn có thể thực hiện công việc này nhờ sử dụng biến.

- **Biến là gì**: Trong lập trình biến giống như một hộp chứa được sử dụng để lưu trữ dữ liệu có trong chương trình để sau đó khi cần thiết chúng ta có thể dễ dàng lấy dữ liệu này ra sử dụng. 

**Ví dụ:**

```

var name = prompt(‘lên của bạn là gì?’);

alert(‘Xin chào ’ +  name); 
```
**Giải thích:**

>**var** name = prompt(‘Tên của bạn là gì?’);

Ở ví dụ trên biến name được tạo ra để lưu trữ dữ liệu nhập vào tên người dùng.

>alert(‘Xin chào ’ +  name); 

Sau đó giá trị của biến name được sử dụng để hiển thị hộp thoại có thông báo xin chào.

***Khai báo biến***

Một biến tồn tại sau khi chúng ta thực hiện việc khai báo. Việc khai báo biến được thực hiện sử dụng từ khoá var và đi sau là tên biến.

>Ví dụ:  **var** name;

Sử dụng dấu , để phân biệt giữa các biến khi cần khai báo nhiều biến sử dụng một câu lệnh duy nhất.

>Ví dụ: **var** firstName, lastName, gender, age;

***Tên biến:***

Việc đặt tên biến giống như việc chúng ta dán nhãn cho các hộp để phân biệt các hộp khác nhau. Trong JavaScript, tên biến có thể bao gồm:
  - Chữ cái (in hoa hoặc in thường): a đến z, A đến Z.
  - Chữ số: 0 đến 9.
  - Các ký tự: $ hoặc \_.
  - Tên biến không được bắt đầu bằng chữ số.

***Ví dụ:*** 

**Tên biến hợp lý:**

> ***var*** myName;
>***var*** name1;
>***var*** $name\_2;
>***var*** \_name3;

**Tên biến không hợp lý:**

>***var*** 1name;
>***var*** 123;

***Gán giá trị cho biến:***

_Để gán giá trị cho biến chúng ta sử dụng dấu =._

**Ví dụ:** 
```
var name; 

name = "JavaScript";
```
_Giá trị của biến có thể được thay đổi nhiều lần trong chương trình._

**Ví dụ:** 
```
var name; 

name = "JavaScript"; 

name = "HTML"; 

name = "CSS";
```

***Khởi tạo biến:***

Khởi tạo biến là việc khai báo và gán *giá trị bạn đầu* cho biến trong cùng một câu lệnh.

>**Vi dụ**: **var** name = "JavaScript";

**Còn tiếp . . .**
