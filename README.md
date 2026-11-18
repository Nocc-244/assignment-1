# Báo cáo Bài tập 1: Môi trường ảo, Máy ảo, Container & Git

## 1. So sánh Virtual Environment, Container và Virtual Machine

| Đặc điểm | Python Virtual Environment (`venv`) | Docker Container | Virtual Machine (VM) |
| :--- | :--- | :--- | :--- |
| **Cấp độ cô lập** | Môi trường Python & các gói thư viện (`site-packages`). | Tiến trình (Process) & hệ thống file, dùng chung OS Kernel với máy chủ. | Phần cứng (Hardware) thông qua Hypervisor, chạy một OS độc lập hoàn chỉnh. |
| **Kích thước** | Cực nhẹ (~vài chục MB). | Nhẹ (~vài chục đến vài trăm MB). | Nặng (~vài GB đến hàng chục GB). |
| **Tốc độ khởi động** | Tức thì (< 1 giây). | Rất nhanh (vài giây). | Chậm (vài chục giây đến vài phút). |
| **Tính di động** | Phụ thuộc OS và phiên bản Python trên máy. | Cao: Chạy đồng nhất mọi nơi có Docker. | Cao nhất: Chạy độc lập nhiều OS khác nhau. |

## 2. Các công cụ quản lý môi trường Python

* **`venv` / `virtualenv`**: Tạo môi trường ảo cô lập thư viện cho từng dự án Python.
* **`pyenv`**: Cài đặt và chuyển đổi nhiều phiên bản Python khác nhau trên cùng một máy.
* **`conda`**: Quản lý cả Python và các thư viện phi-Python (C/C++, CUDA) cho AI/Data Science.
* **`uv`**: Công cụ thế hệ mới viết bằng Rust, thay thế `pip`, `venv`, `pyenv` với tốc độ nhanh gấp 10-100 lần.

## 3. Cấu trúc Demo thực hành

* `venv-demo/`: Demo tạo môi trường ảo `.venv`, cài đặt `requests` và xuất `requirements.txt`.
* `docker-demo/`: Đóng gói ứng dụng Python (`app.py`) bằng `Dockerfile`.
