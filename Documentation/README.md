# Trò chơi Kéo Búa Bao bằng AI (Computer Vision)

Dự án này là một ứng dụng nhận diện cử chỉ chỉ tay để chơi trò "Kéo Búa Bao" giữa 2 người chơi thông qua Webcam. Sử dụng công nghệ nhận diện tọa độ bàn tay (Hand Landmarks) của thư viện Mediapipe và phân loại cử chỉ bằng mô hình Neural Network (Keras/Tensorflow).

## Tính năng chính
- Nhận diện bàn tay theo thời gian thực (Real-time hand tracking).
- Trích xuất đặc trưng tọa độ các khớp tay để phân loại cử chỉ: Kéo, Búa, Bao.
- Chơi 2 người cùng lúc qua một Webcam. Tự động tính toán người thắng, người thua.
- Xử lý chuẩn hóa khoảng cách tay để nhận diện một cách chính xác kể cả khi tay ở xa hoặc gần Camera.

## Cấu trúc thư mục
- `test_kbb.py`: File chính chạy ứng dụng Game Kéo Búa Bao.
- `train_kbb.py`: Mã nguồn dùng để huấn luyện mô hình học sâu.
- `toa_do_kbb.py`: Script dùng để thu thập dữ liệu bàn tay và lưu vào CSV.
- `toa_do_kbb.csv`: Tập dữ liệu (Dataset) điểm tọa độ tay dùng để huấn luyện.
- `model_kbb.h5`: Mô hình AI đã được huấn luyện sẵn.
- `requirements.txt`: Danh sách phiên bản các thư viện cần thiết.

## Cài đặt thư viện
Bạn cần cài đặt Python. Để cài đặt các thư viện đúng phiên bản dự án, hãy mở Terminal/Command Prompt trong thư mục dự án và chạy:
```bash
pip install -r requirements.txt
```

*(Lưu ý: Bạn nên sử dụng môi trường ảo Virtual Environment `venv` để tránh xung đột với các project khác).*

## Cách sử dụng
1. Mở terminal và chạy lệnh:
```bash
python test_kbb.py
```
2. Cửa sổ Webcam sẽ hiện lên. Game hỗ trợ nhận diện tối đa 2 bàn tay.
3. Hai người chơi đưa tay ra trước Camera và thực hiện cử chỉ Kéo, Búa, hoặc Bao.
4. Giữ nguyên tay trong khoảng vài khung hình (20 frames) để phần mềm "chốt" kết quả của bạn.
5. Xem kết quả thắng thua in ra trong màn hình Terminal (Console).
6. Nhấn phím `l` để tắt Camera và thoát.

## Công nghệ sử dụng
- Python
- OpenCV (Xử lý hình ảnh)
- MediaPipe (Nhận diện bàn tay)
- Keras & TensorFlow (Mô hình Deep Learning AI)
- NumPy (Xử lý ma trận dữ liệu)

## link dataset1 CNN:
https://drive.google.com/drive/folders/1QEhVClWhdt3OJFzNhGeUFdH-luTx6AWx?usp=drive_link

## link dataset2 CNN:
https://drive.google.com/drive/folders/1Ebz6WvNQ4hdYe0v0Wcc_6kLd_IY9Enep?usp=drive_link
