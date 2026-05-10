## PHẦN A — KIỂM TRA ĐỌC HIỂU
### Câu A1: 3 Cách nhúng CSS
1. inline.
- Ví dụ: 
<h1 style="color: cyan; font-size: 32px;">Title</h1>
- Ưu điểm:  
+ Hữu dụng để sửa nhanh. 
+ Số requests HTTP ít hơn.
- Nhược điểm:
+ Inline CSS phải được áp dụng cho mỗi element.
-> Dùng khi muốn kiểm tra nhanh hoặc xem trước thay đổi.

2. internal.
- Ví dụ:
<head>
    <style>
        h1 { color: magenta; font-size: 32px; }
    </style>
</head>
- Ưu điểm: 
+  Chỉ một trang ảnh hưởng bởi stylesheet Classes và IDs có thể được dùng bởi internal stylesheet. 
+ Không cần phải tải nhiều files. 
+ HTML và CSS có thể là một file.
- Nhược điểm:
+ Tăng thời gian load. 
+ Nó ảnh hưởng tới một trang – không hữu dụng nếu bạn sử dụng cùng một CSS cho nhiều trang.
-> Dùng khi muốn áp dụng một phong cách độc nhất cho một trang HTML đơn lẻ.

3. external.
- Ví dụ:
<!-- html: -->
<head>
    <link rel="stylesheet" href="css/styles.css">
</head>
<!-- css -->
h1 { color: blue; font-size: 32px; }
- Ưu điểm: 
+  Kích thước trang HTML nhỏ hơn cấu trúc gọn hơn. 
+ Tốc độ load trang nhanh hơn. 
+ Một file .css có thể được dùng cho nhiều.
- Nhược điểm:
+ Cho tới khi external CSS được load lên, trang của bạn sẽ không được tải hoàn toàn.
-> Dùng cho hầu hết các dự án, từ nhỏ đến lớn.

### Câu A2:
1. h1                           → Chọn: 
2. .price                       → Chọn: 
3. #app header                  → Chọn: 
4. nav a:first-child             → Chọn:
5. .product.featured h2         → Chọn: 
6. article > p                  → Chọn: 
7. a[href="/"]                  → Chọn: 
8. .top-bar.dark h1              → Chọn: 

### Câu A3: 
/* Trường hợp 1: content-box (mặc định) */
.box-1 {
    width: 400px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
→ Chiều rộng hiển thị = ???
→ Không gian chiếm trên trang = ???

/* Trường hợp 2: border-box */
.box-2 {
    box-sizing: border-box;
    width: 400px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
→ Chiều rộng hiển thị = ???
→ Kích thước content thực tế = ???
→ Không gian chiếm trên trang = ???

/* Trường hợp 3: Margin collapse */
.box-a { margin-bottom: 25px; }
.box-b { margin-top: 40px; }
→ Khoảng cách giữa box-a và box-b = ???
→ Giải thích tại sao KHÔNG PHẢI 65px