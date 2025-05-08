# PyEXE Converter

## Giới thiệu

PyEXE Converter là công cụ đồ họa giúp chuyển đổi file Python (.py) thành file thực thi độc lập (.exe) mà không cần cài đặt Python. Công cụ được thiết kế với giao diện thân thiện và trực quan, giúp người dùng dễ dàng sử dụng mà không cần kiến thức chuyên sâu về PyInstaller.

## Tính năng chính

- **Chuyển đổi nhanh chóng**: Tạo file .exe từ file Python chỉ với vài cú nhấp chuột
- **Phát hiện thư viện tự động**: Quét và phân tích mã nguồn để xác định các thư viện cần thiết
- **Cài đặt thư viện thiếu**: Tự động phát hiện và cài đặt các thư viện còn thiếu
- **Tùy chọn nâng cao**: Nhiều tùy chọn như onefile/onedir, console/no-console, thêm dữ liệu...
- **Tùy biến icon**: Tùy chỉnh icon cho file .exe của bạn
- **Gợi ý tối ưu**: Đưa ra các gợi ý để giảm kích thước file .exe
- **Tích hợp UPX**: Hỗ trợ nén với UPX để giảm kích thước file đầu ra
- **Giao diện hiện đại**: Giao diện người dùng thân thiện, trực quan với chủ đề tối

## Hướng dẫn sử dụng

### Cài đặt

1. Không cần cài đặt, chỉ cần tải về và chạy file py2exe.py
2. Nếu chưa có PyInstaller, chương trình sẽ tự động cài đặt cho bạn
3. Yêu cầu: Python 3.6 trở lên và PyQt5

### Sử dụng cơ bản

1. **Mở file Python**: Nhấn nút "Mở" để chọn file Python cần chuyển đổi, hoặc kéo và thả file vào ứng dụng
2. **Cấu hình cơ bản**:
   - Chọn "Tạo file duy nhất" nếu muốn tạo một file .exe độc lập
   - Bỏ chọn "Hiển thị console" nếu không muốn hiển thị cửa sổ command line
   - Chọn icon cho file .exe (tùy chọn)
3. **Chuyển đổi**: Nhấn nút "Chuyển đổi" để bắt đầu quá trình
4. **Kết quả**: Sau khi hoàn tất, bạn có thể mở thư mục chứa file .exe đã tạo

### Tính năng nâng cao

#### Thư viện và phụ thuộc

- **Phát hiện thư viện tự động**: Chương trình tự động quét mã nguồn để phát hiện các thư viện được sử dụng
- **Cài đặt thư viện thiếu**: Nếu phát hiện thư viện chưa được cài đặt, chương trình sẽ hỏi bạn có muốn cài đặt tự động không
- **Thư viện ẩn**: Tab "Nâng cao" cho phép bạn thêm các thư viện ẩn không được phát hiện tự động

#### Tùy chọn nâng cao

- **Thêm dữ liệu**: Bạn có thể thêm các thư mục dữ liệu bổ sung vào file .exe
- **Loại trừ thư viện**: Loại bỏ các thư viện không cần thiết để giảm kích thước
- **Runtime hooks**: Thêm các file hook tùy chỉnh
- **Tối ưu kích thước**: Sử dụng UPX và Strip Binary để giảm kích thước file đầu ra
- **Chế độ debug**: Kích hoạt để nhận thông tin debug chi tiết

## Xử lý sự cố

### Các vấn đề thường gặp

1. **Thư viện thiếu**: Nếu báo lỗi về module not found, hãy:
   - Kiểm tra tab thư viện đã phát hiện
   - Sử dụng tùy chọn "Thư viện ẩn" trong tab Nâng cao để thêm thư viện còn thiếu
   - Cài đặt thủ công thư viện bằng pip

2. **Lỗi Tkinter**: Nếu ứng dụng của bạn không sử dụng Tkinter nhưng gặp lỗi liên quan:
   - Thêm "_tkinter" vào danh sách "Loại trừ thư viện" trong tab Nâng cao

3. **Kích thước file lớn**: Để giảm kích thước file .exe:
   - Bật tùy chọn "Nén với UPX" và "Strip Binary"
   - Loại trừ các thư viện lớn không cần thiết như matplotlib, scipy
   - Chỉ nhập các module thực sự cần thiết

4. **Lỗi khi chạy file .exe**: Nếu file .exe không chạy được:
   - Kiểm tra danh sách thư viện đã phát hiện
   - Thử bật chế độ console để xem lỗi chi tiết
   - Thêm các thư viện thiếu vào "Thư viện ẩn"

## Yêu cầu hệ thống

- Windows 7/8/10/11
- Python 3.6 trở lên
- PyQt5
- Kết nối internet (để cài đặt PyInstaller và các thư viện thiếu)

## Về tác giả

Được phát triển bởi **Factory Automation**

## Giấy phép

Phần mềm này được phân phối theo giấy phép MIT. Xem file LICENSE để biết thêm chi tiết.

```
MIT License

Copyright (c) 2023 Factory Automation

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
