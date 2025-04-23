# 1. Chuẩn bị môi trường

- Máy ảo Ubuntu có cài đặt labtainer

- File imodule của labtainer ptit-audio-steg-code 

# 2. Các bước thực hiện

## 2.1 Khởi động bài lab

Tải bài lab, gõ:

    imodule https://github.com/Quyen-TT/B21DCAT161/raw/main/ptit-audio-steg-code-lsb/imodule.tar

Vào terminal, gõ:

    labtainer -r ptit-audio-steg-code

(Chú ý: sinh viên sử dụng mã sinh viên của mình để nhập thông tin email người thực hiện bài lab khi có yêu cầu, để sử dụng khi chấm điểm)

## 2.2 Thực hiện bài lab

Bài lab gồm 3 file python: 

- convert.py: Đọc file WAV, chuyển dữ liệu âm thanh thành mảng byte và in ra màn hình để phân tích. Dùng để xem sự thay đổi dữ liệu trước và sau khi giấu tin.

- encode.py: Nhận một file WAV và chuỗi ký tự bí mật, giấu chuỗi này vào dữ liệu âm thanh bằng kỹ thuật LSB (Least Significant Bit), tạo ra file WAV mới chứa thông điệp.

- decode.py: Đọc file WAV đã được giấu tin và trích xuất lại thông điệp ẩn trong đó.

### Bước 1: Sử dụng các lệnh ls, cat để xem và phân tích các file python 

    ls -l 
    cat convert.py
    cat encode.py
    cat decode.py 

### Bước 2: Chạy script để xem mảng byte đầu vào

    python3 convert.py

Nhập vào file demo.wav

### Bước 3: Tiến hành giấu tin vào file WAV và xuất ra 1 file mới 

    python3 encode.py

Nhập tên file và thông điệp sinh viên muốn giấu 

Sau khi giấu tin thành công, đoạn mã sẽ tạo ra 1 file wav mới

Sử dụng lệnh ls để kiểm tra xem file đã được tạo hay chưa?

Kiểm tra mảng byte của file vừa tạo để quan sát sự thay đổi sau khi giấu tin 

### Bước 4: Tiến hành tách tin

    python3 decode.py

Nhập vào file wav vừa được tạo để in ra thông điệp đã giấu 

# 3. Kiểm tra kết quả

Sử dụng lệnh: 

    checkwork

# 4. Kết thúc bài lab

    Stoplab

# 5. Khởi động lại bài lab (nếu cần)

    labtainer -r ptit-audio-stego-code
