# Report 1 Page – FIT4012 Lab 1

## 1. Mục tiêu
- Hiểu cách tính entropy của một chuỗi ký tự và ý nghĩa xác suất xuất hiện ký tự.
- Bổ sung hàm đo độ dư thừa thông tin dựa trên entropy thực tế.
- Cài đặt hàm tìm nghịch đảo modulo dùng thuật toán Euclid mở rộng.
- Kiểm thử và hoàn thiện báo cáo, log, test để nộp bài đúng yêu cầu.

## 2. Cách làm
- Đọc mã mẫu `src/entropy_redundancy.cpp` và hiểu công thức entropy.
- Cài đặt `calculate_redundancy()` bằng `log2(alphabet_size) - H(X)` với `alphabet_size = 256`.
- Cài đặt `mod_inverse()` trong `src/mod_inverse.cpp` bằng `extended_euclid()` và chuẩn hóa kết quả trong phạm vi `[0, m-1]`.
- Chạy thử các test case trong `tests/test_cases.md` và ghi kết quả vào `logs/run_log.md`.

## 3. Kết quả chính
### 3.1 Entropy và redundancy
| Input | Entropy | Redundancy | Nhận xét |
|---|---:|---:|---|
| aaaa | 0 | 8 | Chuỗi đồng nhất nên entropy tối thiểu, redundancy lớn nhất với bảng 256 ký tự. |
| abcd | 2 | 6 | 4 ký tự khác nhau xuất hiện đều, entropy bằng 2 bit, redundancy là 6 bit. |
| hello world | 2.84535 | 5.15465 | Entropy và redundancy được tính với bảng ký tự 256, phù hợp với chuỗi có ký tự lặp. |

### 3.2 Modulo inverse
| a | m | Kết quả mong đợi | Kết quả chương trình |
|---:|---:|---|---|
| 3 | 7 | 5 | 5 |
| 10 | 17 | 12 | 12 |
| 6 | 9 | Không tồn tại | Không tồn tại |

## 4. Kết luận
Qua bài lab, em hiểu rõ hơn về cách entropy đo khoảng thông tin của một chuỗi và redundancy cho biết phần dư thừa so với kích thước bảng chữ cái. Em đã thực hiện được hàm `mod_inverse()` bằng thuật toán Euclid mở rộng và thấy rằng nghịch đảo modulo chỉ tồn tại khi `gcd(a, m) = 1`. Khó khăn lớn nhất là kiểm tra lại giá trị log2 và chuẩn hóa nghịch đảo sao cho luôn dương trong modulo.