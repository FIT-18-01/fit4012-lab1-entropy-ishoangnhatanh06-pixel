# Report 1 Page – FIT4012 Lab 1

## 1. Mục tiêu
Tóm tắt ngắn gọn mục tiêu của bài lab.

## 2. Cách làm
- Đọc hiểu chương trình entropy mẫu.
- Bổ sung hàm tính redundancy.
- Hoàn thiện hàm mod_inverse().
- Chạy thử trên nhiều test case.

## 3. Kết quả chính
### 3.1 Entropy và redundancy
| Input | Entropy | Redundancy | Nhận xét |
|---|---:|---:|---|
| aaaa | 0 | 8 | Chuỗi toàn lặp nên entropy bằng 0, redundancy lớn nhất với alphabet 256 ký tự. |
| abcd | 2 | 6 | Tất cả ký tự xuất hiện đều, entropy bằng 2 bit và redundancy là 6 bit. |
| hello world | 2.84535 | 5.15465 | Entropy và redundancy tính với alphabet chuẩn 256 ký tự. |

### 3.2 Modulo inverse
| a | m | Kết quả mong đợi | Kết quả chương trình |
|---:|---:|---|---|
| 3 | 7 | 5 | 5 |
| 10 | 17 | 12 | 12 |
| 6 | 9 | Không tồn tại | Không tồn tại |

## 4. Kết luận
Em đã học được cách tính entropy của một chuỗi ký tự và cách tính độ dư thừa thông tin dựa trên entropy thực tế. Việc viết hàm nghịch đảo modulo bằng thuật toán Euclid mở rộng giúp em hiểu rõ hơn mối quan hệ giữa gcd(a,m) và sự tồn tại của nghịch đảo. Khó khăn nhất là kiểm tra lại các giá trị log2 và xử lý giá trị âm trong kết quả nghịch đảo hội modulo.
