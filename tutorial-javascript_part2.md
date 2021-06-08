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

        ví dụ: 
```
    var name = "JavaScript" console.log("Xin chào" + " " + name);

    Hoặc nối chuỗi với số:

    console.log("Xin chào" + " " + 2016);
```

####    Toán tử gán giá trị: 
        Toán tử = được sử dụng để gán giá trị cho biến:

        ví dụ:
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


