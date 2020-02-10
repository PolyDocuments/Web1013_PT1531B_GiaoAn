# Buổi 3

## Nội dung bài học
- Box Model
- Layout
- Iframe

## 1. Box model
- 1 website thông thường sẽ có các thành phần:
    - header
    - sidebar
    - contents
    - foooter
- Các phần của layout thường sẽ được chia thành các khối chữ nhật (box).
- Các thẻ html đều là dạng khối chữ nhật (box).
- Khối chữ nhật - box model có các thuộc tính:
    - content: phần nội dung bên trong.
    - height/width: chiều cao/chiều rộng, đây là 2 thuộc tính duy nhất quyết định kích thước của box.
    - padding: khoảng đệm xung quanh, nói cách khác là khoảng cách từ content tới viền bo.
    - border: viền bo xung quanh.
    - margin: khoảng cách từ phần tử html đang xét tới các phần tử xung quanh.
    - backgroung-color/background
- Ví dụ:
    - [Img](https://s3-ap-southeast-1.amazonaws.com/kipalog.com/k68zn5q971_image.png)
    - Bật Inspect(F12) & check 1 phần tử html bất kỳ.

- Kích thước của box được quyết định bởi cặp thuộc tính width-height.
- content > background > background-color (demo)
    - Tận dụng điều này để tạo ra 2 ảnh lồng nhau.
- Từ border trở vào trong: background của box, từ border trở ra ngoài: background của trang web.

- Lưu ý:
    - Các thuộc tính border, margin & padding có thể được định nghĩa cùng lúc nhiều phía (top, right, bottom, left) hoặc 1 phía riêng lẻ.
    - border-width
    - border-style
    - border-color
    - border-radius

## 2. Layout
- Layout: bố cục của 1 trang web.
- Template: mẫu layout được dựng sẵn, được dùng chung cho trang web.
- Thông thường 1 template sẽ cố định về header, sidebar, footer. Chỉ có phần content là thay đổi giữa các trang.
- HTML5 hỗ trợ các cặp thẻ dùng để thiết kế layout:
    - `<header>`: header
    - `<nav>`: menu
    - `<article>`: content
    - `<aside>`: sidebar
    - `<footer>`: chân trang
    - `<section>`: phân ra từng vùng (box) riêng biệt.
- Về bản chất, các cặp thẻ này tương tự thẻ `<div>`.
- Để sắp xếp bố cục cho trang web, ta sử dụng các thuộc tính CSS:
    - `float: left/right;`
- Khi áp dụng thuộc tính `float` cho 1 box, các box kế tiếp cũng sẽ được áp dụng rule css `float` theo box trước đó.
- Với các box không mong muốn áp dụng `float` của box trước đó, hoặc loại bỏ rule `float`, ta sử dụng rule `clear`.
- Demo.

## 3. `iframe`
- `iframe` là 1 cửa sổ con (mini-window) sử dụng để nhúng 1 trang khác vào trang hiện tại.
- `iframe` có 1 số thuộc tính quan trọng:
    - `@src`
    - `@name`
    - Ngoài ra, `iframe` cũng có 1 số thuộc tính khác như `width`, `height`.

- Demo
    - Ví dụ trong slide.
    - Nhúng video youtube
