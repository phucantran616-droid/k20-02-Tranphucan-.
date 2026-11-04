# AI LOG – BUỔI 7, TIẾT 3

> Ghi lại việc kiểm tra và sửa portfolio ngày 04/11/2026. Kết quả trên máy và kết quả trên website được ghi riêng theo những gì đã kiểm chứng.

## Thông tin sinh viên

- Họ và tên: Trần Phúc An
- Mã sinh viên – Lớp: 2071020001 – Công nghệ Thông tin 20-02
- Ngày thực hiện: 04/11/2026
- Link repository: [K20_Lab6](https://github.com/phucantran616-droid/K20_Lab6), lấy từ cấu hình Git `remote.origin.url` của dự án.
- URL website ghi trong bản nháp: [Portfolio cá nhân](https://phucantran616-droid.github.io/K20_porfolio_CNTT20-02/). Chưa xác minh đây là địa chỉ triển khai hiện tại của repository K20_Lab6.
- [x] Website của tôi
- [ ] Repo luyện của giảng viên

## 1. Nhận định của tôi trước khi hỏi AI

- Trang/thao tác cần kiểm tra: trang portfolio `index.html`, đường dẫn CSS, ảnh đại diện và phần dự án.
- Mong muốn: các tài nguyên tải đúng và mã HTML không có lỗi. Trước khi hỏi AI, tôi chưa cung cấp ảnh chụp giao diện hoặc lỗi cụ thể trong cuộc trao đổi này.
- Dữ kiện ban đầu: bản nháp có đường dẫn `css/style.css` và URL website. Thông tin Status 304 nằm trong prompt mẫu, chưa có log Network hoặc ảnh chụp để xác nhận đó là kết quả thực tế.
- Tôi nghi nguyên nhân là: bản nháp ghi nghi vấn CSS chưa tải. Tôi chưa có đủ dữ kiện để kết luận nguyên nhân.
- Cơ sở của nhận định: đây mới là giả thuyết trong bản nháp. Tôi nhờ AI kiểm tra mã nguồn và cấu trúc tệp để tìm lỗi cụ thể.

## 2. Tôi hỏi AI và nhận được gợi ý

- [x] Công cụ AI: Codex (ChatGPT)
- [ ] Phản hồi mẫu của giảng viên
- Câu hỏi/prompt tôi đã gửi:

  > bạn kiểm tra xem tôi có lỗi gì không

  Sau khi nhận kết quả kiểm tra, tôi yêu cầu:

  > hãy sửa lại giúp tôi

- Gợi ý chính của AI:
  - Ảnh đại diện trỏ tới `css/assets/791975572_1060704449904978_7434436045093909714_n.jpg`, nhưng tệp này không có trong dự án. Có thể thêm ảnh đúng tên hoặc dùng ảnh minh họa `css/assets/avatar.svg` đang có sẵn.
  - Phần dự án có thẻ `<github class="com">` không hợp lệ và không đóng. Cần xóa thẻ này; nếu muốn tạo liên kết thì dùng thẻ `<a href="...">` với địa chỉ chính xác.
  - CSS, ba ảnh dự án và trang `ket-qua.html` đều tồn tại trên máy. Chưa có căn cứ từ việc kiểm tra tệp để kết luận đường dẫn CSS sai.
  - Ba địa chỉ GitHub trong phần dự án đang là văn bản trong thẻ `<span>`, có ghi chú cần cập nhật. Form liên hệ là form thực hành, chưa gửi email thật như thông báo trên trang.

## 3. Quyết định của tôi

- [x] Chấp nhận gợi ý
- [ ] Chỉnh sửa gợi ý rồi áp dụng
- [ ] Bác bỏ gợi ý

- Tôi quyết định làm gì: nhờ AI sửa hai lỗi đã xác định. Dùng `css/assets/avatar.svg` làm ảnh đại diện minh họa và xóa thẻ `<github class="com">` bị sai.
- Lý do: ảnh JPG được tham chiếu không tồn tại, trong khi ảnh SVG có sẵn; thẻ `<github>` không tạo được liên kết và làm mã HTML không hợp lệ.
- Phần cần bổ sung sau: địa chỉ GitHub chính xác cho từng dự án. Chưa biến các địa chỉ đang chờ cập nhật thành liên kết.

## 4. Thực hiện và kiểm chứng

- Tệp/vị trí đã sửa: `index.html`, dòng 49 ở phần ảnh đại diện và khu vực dòng 84–87 ở dự án đầu tiên.
- Nội dung thay đổi: đổi thuộc tính `src` của ảnh đại diện sang `css/assets/avatar.svg`; xóa dòng `<github class="com">` và giữ nội dung trong thẻ `<span>`.
- Commit của bản sửa: chưa tạo commit cho hai thay đổi này.
- Bản sửa đã deploy: [ ] Có  [x] Chưa  [ ] Không phát sinh bản sửa

| Nội dung kiểm tra | Trước xử lý | Sau xử lý/thử lại |
| --- | --- | --- |
| Tệp ảnh đại diện trên máy | `Test-Path` trả về `False` với đường dẫn ảnh JPG cũ. | Đường dẫn mới trỏ tới tệp `css/assets/avatar.svg` có thật; đọc được XML của SVG. |
| Thẻ HTML ở dự án đầu tiên | Có `<github class="com">` không hợp lệ và không đóng. | Đã xóa thẻ sai; tìm lại không còn thẻ `<github>` trong hai trang HTML. |
| Các tệp ảnh, CSS và trang nhận form | CSS, ba ảnh dự án và `ket-qua.html` tồn tại; ảnh đại diện bị thiếu. | Kiểm tra 7 tham chiếu tệp trong hai trang HTML: tất cả đều có tệp tương ứng. |
| Request URL và Status của tài nguyên trên website | Chưa kiểm tra bằng Network của trình duyệt; số 304 trong bản nháp chưa được xác thực. | Chưa kiểm tra được. Công cụ truy cập web không mở được URL website, nên chưa có mã HTTP của CSS hoặc ảnh để ghi nhận. |
| Giao diện/chức năng trên URL website | Chưa kiểm tra trực tiếp. | Chưa kiểm tra trực tiếp; chưa xác nhận hiển thị ảnh, bố cục hoặc thao tác gửi form trên bản online. |
| Phần thay đổi trong Git | Có hai lỗi nêu trên trong mã nguồn trước khi sửa. | `git diff -- index.html` thể hiện bản sửa; `git diff --check` không báo lỗi khoảng trắng. |

- Cách thử lại: AI đọc lại hai trang HTML bằng UTF-8, kiểm tra sự tồn tại của các tệp được tham chiếu, đọc ảnh SVG, tìm thẻ `<github>` và xem phần thay đổi bằng Git. Tôi chưa chạy kiểm thử giao diện bằng trình duyệt.
- Căn cứ để đối chiếu: [index.html](index.html), [ảnh đại diện](css/assets/avatar.svg), [CSS](css/style.css), [trang kết quả](ket-qua.html) và lệnh `git diff -- index.html`.
- Giới hạn kiểm chứng: dự án chưa có bộ kiểm thử tự động. Kiểm tra tệp cục bộ không chứng minh website đã triển khai đúng hoặc giao diện đã hoạt động đầy đủ.

## 5. Kết luận

- [ ] Đã xử lý được
- [x] Xử lý được một phần
- [ ] Chưa xử lý được

- Kết quả: đã sửa và kiểm tra lại hai lỗi trong mã nguồn trên máy. Chưa triển khai bản sửa và chưa kiểm chứng giao diện, chức năng trên website.
- Điều tôi rút ra: cần đối chiếu đường dẫn trong HTML với tệp thực tế trước khi sửa. Không dùng thông tin trong prompt mẫu làm bằng chứng kiểm tra.
- Việc cần làm tiếp: mở trang bằng trình duyệt để xem ảnh, bố cục trên điện thoại và máy tính; thử form hợp lệ/không hợp lệ; cung cấp liên kết GitHub đúng; commit và triển khai bản sửa. Sau đó kiểm tra Request URL và Status của CSS, ảnh trên website rồi bổ sung kết quả vào log.

---

*Tệp là minh chứng MC2 để nhận định mức đạt của tiết học; không tính điểm MC2 riêng. Nếu có tình huống khác, sao chép mục 1–5 để ghi thêm.*
