# Buổi 2: CSS

## Nội dung buổi học:
- Giới thiệu Css
- Vị trí đặt Css
- Css Selector
- Nạp chồng Css
- Giới thiệu 1 vài Css rule

## 1. Giới thiệu Css
- Css (Cascading Style Sheet) là ngôn ngữ được dùng để định dạng các thành phần & thực hiện bố cục của 1 trang web:
    - Màu sắc
    - Viền
    - Bo góc
    - Căn lề
    - ...
- Cú pháp: *Css* có cú pháp dạng `key: value`:
```
.color-red {
    color: red;
}
```

## 2. Vị trí đặt Css
### 2.1. Inline
- Css được đặt trong thuộc tính ***style*** của các thẻ *html*.
```
<h1 style="color: red;">This is heading 1</h1>
```
- **Chú ý**:
    - Với cú pháp inline, các rule của Css sẽ được đặt theo dạng `key: value;`. Trong đó `key` chỉ định thuộc tính css, `value` chỉ định giá trị cho thuộc tính đó.
    - Với ví dụ trên, `key` là thuộc tính `color` của thẻ `<h1>`, sẽ chỉ định màu sắc cho text trong thẻ `<h1>`. (Lưu ý thuộc tính `color` sẽ chỉ định màu sắc cho text, không phải bôi màu cho thẻ html)
    - 1 trong những nhược điểm của cách viết này là mỗi thẻ html sẽ phải định nghĩa rule riêng, không tái sử dụng được code cho các thẻ khác.
### 2.2. Embeded
- Css được đặt trong thẻ `<style></style>` của file *.html*.
```
<style>
.color-red {
    color: red;
}
</style>
```
- **Lưu ý**:
    - Với cách viết này ta sẽ định nghĩa ra các class của Css.
        - Cú pháp:`.class-name { key: value; }`
        - Phần đặt liền sau dấu chấm `.` và trước ngoặc nhọn mở `{` là tên của class css.
        - Các rule Css sẽ được đặt trong cặp ngoặc nhọn `{ ... }` với cú pháp dạng: `key: value;`
    - Với việc định nghĩa ra các class css, ta có thể tái sử dụng lại code css cho các thẻ html có định dạng kiểu giống nhau, dựa trên thuộc tính `class` của các thẻ html: `<h1 class="color-red"></h1>`
    - Tuy nhiên, cách viết này chỉ tái sử dụng được code cho các phần tử html bên trong cùng 1 file html. Các file **.html** khác sẽ không tái sử dụng được các class css mà ta vừa khai báo.
### 2.3. External
- Với cách viết này, css thay vì đặt trong thẻ `<style></style>` hay đặt trong thuộc tính `style=""` của thẻ html, ta sẽ viết Css ra 1 file riêng, với tên file có dạng: file_name<b>.css</b> (chú ý định dạng file phải là **.css**).
- Sau đó ta khai báo đường dẫn tới file **.css** để file **.html** có thể load được Css class ta vừa khai báo:
`<link href="/path/to/file_name.css" rel="stylesheet">`
- Với cách viết này ta có thể tái sử dụng được các class Css cho các phần tử html ở nhiều file **.html** khác nhau.

## 3. Selector
- Selector giúp trình duyệt nhận biết rule css sẽ được áp dụng cho phần tử html nào.
- Có 3 kiểu selector:
    - html-tag
    - .class
    - #id
- Với cách viết này, cú pháp cũng tương tự như cách ta định nghĩa class Css, chỉ khác ở điểm các cú pháp Selector sẽ đứng trước ngoặc nhọn mở `{` thay vì `.class-name`

#### 3.1. Selector `html-tag`
- Cú pháp:
```
p {
    color: red;
}
```
- Với ví dụ trên, tất cả các thẻ `<p></p>` sẽ đều được áp dụng rule Css.
- Chú ý trước hay sau kí tự `p` không có các kí tự khác, kể cả dấu `.`

#### 3.2. Selector `.class`
- Cú pháp:
```
.class-name {
    key: value;
}
```

- Cách viết này chính là khai báo 1 class Css. Sau khi khai báo xong các rule Css, ta sẽ khai báo cho các thẻ html (mà ta muốn áp dụng rule này) load class vừa khai báo thông qua thuộc tính `class=""`.
#### 3.3. Selector `#id`
- Cú pháp:
```
#id {
    key: value;
}
```
- Với cách viết này, thay vì đặt `.class-name` trước cặp ngoặc nhọn `{ ... }`, ta khai báo `#id` tương ứng với thuộc tính `id` của thẻ html mong muốn áp dụng rule Css.
- Lưu ý: do thuộc tính id của thẻ html là duy nhất, nên với cách viết này, rule Css sẽ chỉ áp dụng cho 1 thẻ html duy nhất với `id` tương ứng.
## 4. Nạp chồng Css
- Với 3 cách viết *Inline*/*Embeded*/*External*, thứ tự ưu tiên sẽ là: `inline > embeded > external`. Điều này có nghĩa là các rule Css được định nghĩa với kiểu *Inline* sẽ có độ ưu tiên cao nhất trong 3 kiểu, sau đó sẽ là *Embeded*, kiểu *External* sẽ có độ ưu tiên thấp nhất.

- Đối với các selectors, ...

- Khi định nghĩa Css, đôi lúc ta sẽ cần khai báo 1 rule có độ ưu tiên cao nhất, vượt trên các rule khác với cùng thuộc tính Css. Lúc này ta sẽ sử dụng từ khoá (keyword) `!important`. Từ khoá `!important` sẽ được đặt ở sau `value` thể hiện độ ưu tiên cao nhất.
```
color: white !important;
```

- Khi ta định nghĩa nhiều rule Css với cùng 1 selector, rule viết sau sẽ được ưu tiên hơn rule viết trước:
```
h1 {
    color: white; // Độ ưu tiên thấp hơn
}

h1 {
    color: red; // Độ ưu tiên cao hơn
}
```

## 5. Giới thiệu 1 vài Css rule
- font-size
- font-style
- font-weight
- text-align
- line-height
- color
- px
- a
    - a:link
    - a:visited

- Demo
