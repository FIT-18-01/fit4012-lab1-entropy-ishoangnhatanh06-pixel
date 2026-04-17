# Run Log – FIT4012 Lab 1

## Entropy / Redundancy
- [x] Đã chạy với input `aaaa` -> Entropy: 0, Redundancy: 8
- [x] Đã chạy với input `abcd` -> Entropy: 2, Redundancy: 6
- [x] Đã chạy với input `hello world` -> Entropy: 2.84535, Redundancy: 5.15465
- [x] Đã chạy với input `a` -> Entropy: 0, Redundancy: 8
- [x] Đã chạy với input `abcdefghijklmnopqrstuvwxyz` -> Entropy: 4.70044, Redundancy: 3.29956

## Modulo inverse
- [x] Đã chạy với `3 7` -> Nghịch đảo: 5
- [x] Đã chạy với `10 17` -> Nghịch đảo: 12
- [x] Đã chạy với `6 9` -> Không tồn tại (gcd=3)

## Điều em học được từ bài lab
Em đã học cách tính entropy và redundancy cho một chuỗi ký tự, và hiểu rõ rằng redundancy bằng log2(kích thước bảng chữ cái) trừ đi entropy thực tế. Em cũng nắm vững cách dùng thuật toán Euclid mở rộng để tìm nghịch đảo modulo và hiểu điều kiện tồn tại là gcd(a, m) = 1.
