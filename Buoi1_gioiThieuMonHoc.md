# Buổi 1: Giới thiệu môn học.

- Nội dung buổi học:
    - Giới thiệu môn học, chương trình học (Syllabus)
    - Giới thiệu trang web, các thành phần trang web.
    - IDE
    - Làm quen với HTML.
## 1. Giới thiệu 
### 1.1. Giới thiệu bản thân
- Tình hình lớp:
    - Đã học/code những ngôn ngữ nào?
    - Đã từng nghe/làm việc với HTML/CSS/JS
### 1.2. Giới thiệu môn học (Syllabus)
## 2. Giới thiệu trang web
- Có rất nhiều loại trang web:
    - Tin tức
    - Phim ảnh
    - Email
    - Học online(E-learning)
    - ...
- Trình bày 1 Website luôn có 2 phần chính:
    - Nội dung
        - Văn bản
        - Hình ảnh
        - Video
        - ...
    - Hình thức
        - Màu sắc
        - Kích cỡ
        - Bố cục
        - ...
- Vậy làm thế nào để tạo ra đc 1 website?
    => Vào 1 website, click chuột phải & chọn View source page (Xem mã nguồn)
- Mở source của 1 website sẽ thấy mã nguồn của trang đó. Trình duyệt sẽ từ mã nguồn đó để build lên 1 trang web.
- Để tạo ra mã nguồn cho 1 trang luôn cần [3 thành phần](https://tutorial.techaltum.com/images/htmlandcss.jpg):
    - HTML
    - CSS
    - Javascript.
- **HTML** sẽ tạo nên bộ khung xương cho 1 trang web, nhưng sẽ chỉ là 1 trang thuần text, không có màu sắc, không quyết định được bố cục, kích cỡ ... giống như 1 bộ xương không có cơ bắp, trang phục.
```
<html>
    <!-- Your code goes here -->
</html>
```

- Để tạo được bố cục cho trang web, thay đổi style, màu sắc ... ta cần sử dụng tới **Css**(Cascading Style Sheets).
```
.color {
    color: #fff;
}
```

- **HTML** kết hợp với **CSS** sẽ tạo ra 1 trang web đẹp mắt, nhưng ko có action, hay nói cách khác là website ko có tương tác. Lúc này ta sẽ cần tới Javascript. Javascript sẽ tạo nên hành động giúp website có thể tương tác mượt mà hơn.
```
$('#button').click(function () {
    // Your code goes here ...
})
```

## 3. IDE
- Các IDE nên được sử dụng trong môn học:
    - Notepad++ (không khuyến khích)
    - Netbean (không khuyến khích)
    - Sublime Text
    - VS Code

- Hướng dẫn cài đặt VS Code.

## 4. Giới thiệu HTML
- **HTML**(Hypertext Markup Language) giúp tạo ra bộ khung cho 1 trang web.
- **KHÔNG** phải là ngôn ngữ lập trình, mà là ngôn ngữ đánh dấu (markup).
- Tạo 1 file text có đuôi *.html* . Đây sẽ là 1 file html.
- HTML là ngôn ngữ đánh dấu (markup language), bao gồm các cặp thẻ:
    - `<html></html>`
    - `<body></body>`
    - `<p></p>`
    - Giải thích: bao gồm 1 thẻ mở & 1 thẻ đóng. Thẻ đóng sẽ có ký tự **/** .
- 2 cặp thẻ quan trọng nhất của **HTML** là:
    - `<head></head>`
    - `<body></body>`
    - Thẻ `<head></head>` sẽ được giới thiệu kỹ hơn trong các bài học sau.
    - Thẻ `<body></body>` sẽ là nơi chứa mã nguồn giúp trình duyệt xây dựng lên 1 trang web.
- Trong file *.html* vừa tạo, đặt 2 cặp thẻ `<head></head>`, `<body></body>`.
```
<html>
    <head></head>
    <body></body>
</html>
```
- Bài 1 sẽ tập trung vào thẻ `<body></body>`.
- Giới thiệu 1 số thẻ html
### 4.1. `<h></h>`
- Thẻ `<h></h>` được sử dụng để hiển thị các heading (tiêu đề).
- Có 6 cấp của thẻ `<h>`: `<h1>` -> `<h6>`
- Trong file html vừa tạo, bên trong phần `<body></body>` đặt 3 cặp thẻ `<h>`:
```
...
<body>
    <h1>Đây là heading 1</h1>
    <h2>Đây là heading 2</h2>
    <h3>Đây là heading 3</h3>
</body>
```

- Mở file html trên trình duyệt & quan sát kết quả.

- Thẻ `<h>` thường được dùng để định dạng tiêu đề.

### 4.2.`<p></p>`
- Thẻ `<p></p>` được sử dụng để hiển thị 1 đoạn văn bản.
- Trong file html, bên trong `<body></body>`, dưới phần heading `<h><h>` ta đặt thẻ `<p></p>`:
```
...
<p>Đây là 1 đoạn văn bản</p>
...
```

### 4.3. `<img>`
- Thẻ `<img>` được sử dụng để hiển thị 1 ảnh.
- Thẻ `<img>` luôn cần 1 thuộc tính đi kèm: **src**: `<img src="..." />`
- **Lưu ý**: đối với thẻ `<img>`, thay vì phải đặt 1 thẻ đóng `</img>`, ta đặt kí tự **"/"** ở cuối thẻ mở.

- Download bất kì 1 bức ảnh về máy, đặt cùng thư mục với file html.
- Trong file html, đặt 1 thẻ `<img>`:
```
...
<img src="img_name.png"/>
...
```

- Mở file html trên trình duyệt & quan sát kết quả.

- Phân biệt cách dùng `<img></img>` & `<img />`

- Set giá trị của thuộc tính **src** bằng 1 đường dẫn ảnh online, quay lại trình duyệt & quan sát kết quả.

### 4.4. `<hr>`
- Trong file html, đăt 1 thẻ `<hr>`, sau đó mở file html trên trình duyệt & quan sát kết quả.

- **Lưu ý**: 1 vài thẻ html không có thẻ đóng. `<hr>` là 1 trong số các thẻ đó. **KHÔNG** tồn tại thẻ `</hr>`.

### 4.5. `<br>`
- Tương tự như thẻ `<hr>`, thẻ `<br>` cũng **KHÔNG** có thẻ đóng.
- Trong file html, đặt đoạn code sau vào & quan sát kết quả trên trình duyệt:
```
<p>This is a paragraph!</p>
<p>This is a <br>paragraph!</p>
```

### 4.6. `<a>`
- Giống như thẻ `<img>`, thẻ `<a>` cũng không cần thẻ đóng `</a>`.
- Thẻ `<a>` được dùng để thể hiện 1 liên kết tới 1 trang khác. Đường dẫn của trang được liên kết sẽ được đặt trong thuộc tính **href** của thẻ `<a>`:
```
<a href="đường_dẫn_tới_trang_liên_kết">
```
### 4.7. Các thẻ định dạng văn bản
#### 4.7.1 Các thẻ định dạng văn bản thường
- Tương tự như *Microsoft Word*, html cũng hỗ trợ các thẻ để định dạng văn bản như chữ đậm, in nghiêng ...
- 1 số thẻ được sử dụng để định dạng văn bản:
    - `<strong>`(`<b>` - in đậm)
    - `<em>`(`<i>` - in nghiêng)
    - `<mark>`(highlight text)

#### 4.7.2 Các thẻ định dạng chỉ số
- 2 cặp thẻ `<sub>` & `<sup>` được sử dụng để định dạng các chỉ số:
- Đặt đoạn code sau vào file html, quay lại trình duyệt & quan sát kết quả:
```
<p>2<sub>1</sub><sup>3</sup></p>
```

## 5. Tổng hợp nội dung buổi học
- Cấu trúc của 1 file html.
- Các cặp thẻ thông dụng:
    - `<h></h>`
    - `<p></p>`
    - `<img />`
    - `<hr>`
    - `<br>`
    - `<a />`
- Các cặp thẻ định dạng:
    - `<strong></strong>`
    - `<em></em>`
    - `<mark></mark>`
    - `<sub></sub>`
    - `<sup></sup>`
