# K20_Lab6 – Portfolio CV cá nhân

- **Sinh viên:** Trần Phúc An
- **Mã sinh viên:** 2071020001
- **Lớp:** Công nghệ Thông tin 20-02
- **Tên sản phẩm:** Portfolio 

## Sản phẩm này là gì?

Đây là website CV cá nhân của mình, được xây dựng để giới thiệu bản thân, kỹ năng, các dự án học tập và thông tin liên hệ. Dự án giúp mình thực hành HTML, CSS và cách tổ chức một website tĩnh trong quá trình học ngành Công nghệ Thông tin.

## Demo

[Mở website portfolio](http://phucantran616-droid.github.io/k20-02-Tranphucan-./)

## Tính năng

- **Giới thiệu:** hiển thị thông tin cá nhân, ảnh đại diện minh họa và định hướng học tập.
- **Kỹ năng:** liệt kê kiến thức C++ cơ bản, HTML5, CSS3 và các công cụ đang học sử dụng.
- **Dự án:** giới thiệu ba sản phẩm học tập: chương trình C++ cơ bản, portfolio CV cá nhân và website thực hành HTML & CSS.
- **Học tập:** trình bày học phần và sản phẩm tương ứng bằng bảng.
- **Liên hệ:** hiển thị email, địa chỉ GitHub và form nhập lời nhắn.
- **Điều hướng:** menu chuyển tới từng phần của trang; nút **Xem dự án** dẫn tới phần dự án.
- **Giao diện:** có CSS điều chỉnh bố cục theo độ rộng màn hình, hiệu ứng khi rê chuột và viền đánh dấu khi dùng bàn phím.

Form liên hệ sử dụng kiểm tra dữ liệu HTML5 của trình duyệt:

- Họ và tên: bắt buộc, ít nhất 2 ký tự.
- Email: bắt buộc, đúng định dạng email.
- Lời nhắn: bắt buộc, từ 10 đến 500 ký tự.

Khi dữ liệu hợp lệ, form chuyển tới `ket-qua.html` bằng phương thức GET. Đây là form thực hành, chưa gửi email thật và không lưu lời nhắn vào cơ sở dữ liệu; dữ liệu nhập xuất hiện trên URL trang kết quả.

## Công nghệ sử dụng

- **HTML5:** cấu trúc nội dung, bảng và form liên hệ.
- **CSS3:** định dạng giao diện với Flexbox, Grid và media queries.
- **SVG:** ảnh đại diện và ảnh minh họa dự án.
- **Google Fonts:** tải phông chữ Inter; có phông chữ hệ thống dự phòng.

Dự án không sử dụng JavaScript, framework hay backend. Không cần cài thư viện hoặc chạy lệnh build để mở website.

## Cách mở và sử dụng

1. Tải mã nguồn về máy và giải nén nếu cần.
2. Mở thư mục chứa `index.html`, `ket-qua.html` và thư mục `css/`.
3. Mở `index.html` bằng trình duyệt. Nếu dùng Visual Studio Code và đã cài tiện ích Live Server, có thể chọn **Open with Live Server**.
4. Bấm các mục trên menu để xem **Giới thiệu**, **Kỹ năng**, **Dự án**, **Học tập** và **Liên hệ**.
5. Tại phần **Liên hệ**, nhập thông tin mẫu hợp lệ rồi bấm **Gửi lời nhắn** để xem trang kết quả. Bấm **Quay lại liên hệ** để trở về form.

Giữ nguyên vị trí các thư mục để trình duyệt tìm được CSS và ảnh. Cần kết nối Internet để tải phông chữ Google Fonts và mở các liên kết bên ngoài.

## Cấu trúc thư mục

```text
portfolio/
├── index.html          # Trang portfolio chính
├── ket-qua.html        # Trang kết quả của form thực hành
├── css/
│   ├── style.css       # Định dạng giao diện và responsive
│   └── assets/         # Ảnh SVG được index.html sử dụng
│       ├── avatar.svg
│       ├── du-an-1.svg
│       ├── du-an-2.svg
│       └── du-an-3.svg
├── assets/             # Các tệp SVG khác hiện có trong dự án
├── docs/               # Thư mục hiện có một tệp ảnh JPG
├── AI_log.md           # Nhật ký sử dụng AI và kiểm chứng
├── CHANGELOG.md         # Tệp nhật ký thay đổi, hiện chưa có nội dung
└── README.md           # Giới thiệu và hướng dẫn sử dụng
```

## Đã kiểm tra

Các mục dưới đây được kiểm tra bằng cách đọc mã nguồn và đối chiếu tệp trên máy:

- Hai trang `index.html`, `ket-qua.html` và tệp `css/style.css` tồn tại.
- Các đường dẫn ảnh, CSS và trang nhận form trong hai trang HTML có tệp tương ứng.
- Các liên kết điều hướng nội bộ trỏ tới ID có trong `index.html`.
- Form có các thuộc tính `required`, `minlength`, `maxlength` và `type="email"` phù hợp với yêu cầu nhập liệu nêu trên.
- CSS có quy tắc điều chỉnh giao diện tại độ rộng 768px và 480px.

Chi tiết lần kiểm tra và sửa lỗi trước đó được ghi trong [nhật ký AI](AI_log.md). Các kiểm tra mã nguồn không thay thế việc thử giao diện và thao tác thực tế trên trình duyệt.

## Hạn chế / Chưa kiểm tra

- Ba địa chỉ GitHub ở phần dự án vẫn là văn bản chờ cập nhật, chưa phải liên kết có thể bấm.
- Form chưa có chức năng gửi email hoặc lưu lời nhắn; trang kết quả chỉ hiển thị thông báo thực hành.
- Chưa xác minh bản demo online có khớp với mã nguồn hiện tại hay không.
- Chưa kiểm chứng giao diện trên các trình duyệt và thiết bị thực tế, bao gồm điện thoại iPhone và Android.
- Chưa thử trực tiếp các trường hợp gửi form hợp lệ, bỏ trống, sai định dạng hoặc sai độ dài trên trình duyệt.
- Chưa có bộ kiểm thử tự động hoặc tệp tổng hợp minh chứng `docs/evidence-index.md`.

## Khai báo AI

Dự án có sử dụng **Codex (ChatGPT)** để hỗ trợ kiểm tra đường dẫn tài nguyên, phát hiện và sửa lỗi HTML, đồng thời biên soạn README dựa trên mã nguồn hiện có.
