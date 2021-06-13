## Javascript cho người mới bắt đầu – tutorial javascript cho frontend (phần 2)



### [Toán tử](#1)
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
Câu lệnh **if** được sử dụng khi việc thực thi của một đoạn mã lệnh phụ thuộc vào tính đúng của của một biểu thức điều kiện cho trước.

ví dụ:
```
var bank_balance = 302.13;
var amount = 99.99;
if (amount < bank_balance) {
   console.log( "I want to buy this phone!" );
}

```

- Lệnh **if** cần một diễn đạt trong dấu ngoặc đơn **()** được thể hiện như **true** hoặc **false**.
- trong ví vụ chúng ta có biểu thức **amount < bank_balance**, nó sẽ xác định **true** hoặc **false** tuỳ thuộc vào gía trị của biến **bank_balance**.

---
#### Câu lệnh else: Cung cấp môt sự thay thế điều kiện nếu điều kiện của if không thoả mãn
Câu lệnh **else** được sử dụng kết hợp với **if** để thực thi đoạn mã lệnh khi biểu thức điều kiện trả về giá trị là false.

ví dụ:
```
const ACCESSORY_PRICE = 9.99;
var bank_balance = 302.13;
var amount = 99.99;
amount = amount * 2;

// chúng ta có đủ khả năng mua thêm không?
if ( amount < bank_balance ) {
    console.log( "I'll take the accessory!" );
    amount = amount + ACCESSORY_PRICE;
}
// nếu không thì:
else {
    console.log( "No, thanks." );
}

```
- Tại đây, nếu **amount < bank_balance** là **true**, chúng ta sẽ in ra *"I'll take the accessory!"* và thêm *9.99* vào biến *amount*.
- Ngược lại mệnh đề **else** nói ra chúng ta sẽ trả lời lịch sự *"No,thanks."* và *amount* không thay đổi.
---

####  Câu lệnh else if: Cung cấp điều kiện như câu lệnh if
Câu lệnh **else if** được sử dụng kết hợp với câu lệnh **if** để gán thêm điều kiện cho cấu trúc điều khiển.

ví dụ:
```
var greet; hour = 21; 

// Đây có phải là buổi sáng?
if (hour < 12 && hour > 0) { 
        greet = "Good morning"; 
}
// Đây có phải là buổi chiều?
else if (hour >= 12 && hour < 18) { 
        greet = "Good afternoon"; 
} 
// Đây có phải là buổi tối?
else if (hour >= 18 && hour < 21) { 
        greet = "Good evening"; 
} 
// Đã đến giờ đi ngủ?
else { 
        greet = "Good night"; 
}
```
- Tại đây, nếu **hour < 12 && hour > 0** là **true**, chúng ta sẽ in ra *"Good morning"*.
- Tại đây, nếu **hour >= 12 && hour < 18** là **true**, chúng ta sẽ in ra *"Good afternoon"*.
- Tại đây, nếu **hour >= 18 && hour < 21** là **true**, chúng ta sẽ in ra *"Good evening"*.
- Ngược lại mệnh đề **else** nói ra chúng ta sẽ trả lời lịch sự *"Good night"*.

---

### Vòng lặp:
Ta muốn làm một việc gì đó lặp đi lặp lại cho đến một thời điểm nhất định thì dùng lại. Vòng lặp cũng vậy, nó sẽ lặp đi lặp lại 1 công việc khi điều kiện trả về *true*, cho đến khi điều kiện trả về *false* thì vònglawpj sẽ kết thúc.
- Một vòng lăp bao gồm điều kiện kiểm tra cũng như một *block* (thường la {...}). Mỗi lần *block* vòng lặp được thực hiện, nó được gọi là *sự lặp lại*.

Ví dụ: vòng **while** và **do..while** minh họa khái niệm lặp lại một *block* câu lệnh cho đến khi điều kiện không còn được đánh giá là *true*:
```
while (numOfCustomers > 0) {
console.log( "How may I help you?" );
    // giúp đỡ khách hàng...
    numOfCustomers = numOfCustomers - 1;
}

// So với:

do {
    console.log( "How may I help you?" );
    // giúp đỡ khách hàng...
    numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);

```

- Sự khác biệt thực tế duy nhất giữa các vòng lặp này là liệu điều kiện được kiểm tra trước lần lặp đầu tiên **(while)** hay sau lần lặp đầu tiên **(do..while)**.
- Ở một trong hai dạng, nếu điều kiện kiểm tra là **false**, lần lặp kế tiếp sẽ không chạy. Có nghĩa là điều kiện khởi tạo là **false**, vòng lặp **while** sẽ không bao giờ chạy, nhưng một vòng lặp **do..while** sẽ chạy lần đầu.
- Điều kiện được kiểm tra cho mỗi lần lặp, giống như nó có lệnh **if** bên trong vòng lặp.


**Gợi ý**: *Chúng ta có thể sử dụng lệnh **break** của JS để ngừng một vòng lặp. Đồng thời, chúng ta có thể thấy rằng thật dễ dàng một cách kinh khủng để tạo ra một vòng lặp chạy liên tục mà không có cơ chế **break**.*

**Ví dụ:**

```
var i = 0;

// vòng lặp `while..true` sẽ chạy mãi mãi
while (true) {
    // dừng vòng lặp?
    if ((i <= 9) === false) {
    break;
}
    console.log( i );
    i = i + 1;
}
// 0 1 2 3 4 5 6 7 8 9
```

Trong khi **while** hay **(do..while)** có thể hoàn thành nhiệm vụ thủ công, có một dạng cú pháp khác được gọi là vòng lặp **for** cho dành mục đích đó.

```
for (var i = 0; i <= 9; i = i + 1) {
    console.log( i );
}
// 0 1 2 3 4 5 6 7 8 9
```

- Như bạn thấy, trong cả hai trường hợp điều kiện **i <= 9** là *true* trong 10 lần lặp đầu tiên của một dạng vòng lặp **(các giá trị i từ 0 đến 9)** trở thành *false* khi *i* đạt giá trị 10.
- Vòng lặp for có ba mệnh đề: mệnh đề khởi tạo **(var i=0)**, mệnh đề kiểm tra điều kiện **(i <= 9)**, và mệnh đề cập nhật **(i = i + 1)**. Vì vậy nếu bạn định đếm với vòng lặp lặp đi lặp lại, **for** là hỉnh thức gọn gàng và dễ hiểu hơn để hiểu và viết.


## Cảm ơn bạn đã theo dõi, Xin chào và hẹn gặp lại các bạn ở phần [tiếp theo](https://github.com/thanhdat19521/tutorial-javascript/blob/main/tutorial-javascript_part2.md).




