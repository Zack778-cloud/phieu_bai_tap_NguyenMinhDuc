PHẦN A — KIỂM TRA ĐỌC HIỂU
Câu A1 (5đ) — HTTP & Browser
1. Khi gõ https://shopee.vn vào trình duyệt và nhấn Enter, theo thứ tự các bước xảy ra:
Bước 1: Browser thực hiện DNS lookup tìm địa chỉ IP của domain.
Bước 2: Gửi HTTP Request đến Server.
Bước 3: Server xử lý Request.
Bước 4: Server trả HTTP Response Codes.
Bước 5: Trình duyệt parse HTML, CSS, JS và render trang web.

2. Trong DevTools của Chrome, tab Network cho thấy thông tin các requests/responses.
Mở trang web sonic.sega.jp (PBT_01/screenshots/a1-2.PNG)
- Status Code của request đầu tiên: khoanh tròn màu đỏ.
- Tổng thời gian load trang: khoanh tròn màu vàng.
- Một request trả về file CSS: gạch chân màu xanh.


Câu A2 (5đ) — Semantic HTML
- Trang web dưới đây bị Google đánh giá SEO thấp do trang web sử dụng thẻ <div> cho tất cả mọi thành phần khiến Google và các công cụ tìm kiếm không thể hiểu được cấu trúc và ý nghĩa của nội dung.

<div class="header"> 
    <div class="logo">ShopTLU</div>
    <div class="menu">
        <div><a href="/">Trang chủ</a></div>
        <div><a href="/products">Sản phẩm</a></div>
    </div>
</div>
<div class="main">
    <div class="product">
        <div class="title">iPhone 16 Pro</div>
        <div class="price">25.990.000đ</div>
        <div class="image"><img src="iphone.jpg"></div>
    </div>
</div>
<div class="footer">© 2026 ShopTLU</div>

- Lỗi 1: dòng 1; 7 - sửa: <header> </header>
- Lỗi 2: dòng 3; 6 - sửa: <nav> </nav>
- Lỗi 3: dòng 8; 14 - sửa: <main> </main>
- Lỗi 4: dòng 15 - sửa: <footer>

Câu A3 (5đ) — Block vs Inline:
- Kết quả hiển thị của đoạn HTML:
Hộp 1
Text A Text B
Hộp 2
Text C Text D
Hộp 3

- Do <div> là Block Element nên mỗi phần tử chiếm cả dòng và tự xuống dòng mới; <span> và <strong> là Inline Element nên mỗi phẩn từ chỉ chiếm nội dung và hiển thị trên một dòng
<div>Hộp 1</div> 
<span>Text A</span>
<span>Text B</span>
<div>Hộp 2</div>
<span>Text C</span>
<strong>Text D</strong>
<div>Hộp 3</div>


Câu A4 (5đ) — Table
- Sự khác nhau giữa <thead>, <tbody>, <tfoot>:
+ <thead> có vai trò làm tiêu đề cột, giúp trình duyệt và trình đọc màn hình xác định tiêu đề bảng để cải thiện khả năng truy cập. 
+ <tbody> là nơi chứa các dữ liệu chính của bảng, giúp tách biệt khỏi tiêu đề và chân trang.
+ <tfoot> là nơi chứa tổng kết hoặc tóm tắt ở cuối bảng.

- Ta không nên dùng table để tạo layout trang web vì:
+ Các trình đọc màn hình đều đọc các trang web theo thứ tự hiển thị trong mã HTML, và bảng rất khó để các trình đọc màn hình phân tích.
+ Bảng rất khó hiểu, phức tạp và khó bảo trì do yêu cầu sử dụng nhiều thuộc tính và bảng lồng khác nhau.
+ Bảng không được linh hoạt, thường tải chậm và có thể làm thay đổi đáng kể giao diện tổng thể. 

