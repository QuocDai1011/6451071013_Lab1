# 6451071013_Lab1 – Khai phá dữ liệu, Báo cáo thực hành buổi 1

Mai Quốc Đại – 64510710513 – CQ.64.CNTT
GVHD: ThS. Nguyễn Thiện Dương

Mỗi câu là một notebook riêng, đặt tên theo mẫu `<MSSV>_LAB1_Bai<X>_Cau<Y>.ipynb`. Mỗi notebook tự chạy được độc lập: phần "Chuẩn bị" thực hiện lại các bước của các câu trước.

## Cấu trúc

| Thư mục                                    | Nội dung                               | Dữ liệu              |
| ------------------------------------------ | -------------------------------------- | -------------------- |
| `Phan1/Bai2_Trang15-17_Titanic`            | Phần 1 – Bài 2 (trang 15–17), câu 1–8  | `titanic.csv`        |
| `Phan1/Bai2_Trang28_BankMarketing`         | Phần 1 – Bài 2 (trang 28), câu 1–8     | `bank-full.csv`      |
| `Phan1/Bai2_Trang30_TbTracking`            | Phần 1 – Bài 2 (trang 30), câu a–d     | `tb_tracking.xlsx`   |
| `Phan2/Bai2_Trang37-38_OnlineRetail_UK`    | Phần 2 – Bài 2 (trang 37–38), câu 1–12 | `Online Retail.xlsx` |
| `Phan2/Bai5a_Trang45_OnlineRetail_Germany` | Phần 2 – Bài 5a (trang 45), câu 1–12   | `Online Retail.xlsx` |
| `Phan2/Bai6_Trang45_Groceries`             | Phần 2 – Bài 6 (trang 45), câu a–c     | `groceries.csv`      |

Dữ liệu nằm trong thư mục `data/`.

## Cài đặt và chạy

```bash
pip install -r requirements.txt
jupyter notebook
```

- Với Online Retail, nên chạy **Câu 1 trước**: câu này đọc file Excel (mất 1–2 phút) và lưu bản cache `data/online_retail.pkl` để các câu sau đọc nhanh.
- Bài 6 (Groceries): với 9.835 giao dịch, min_sup = 0,01% tương đương support count ≥ 1, nên số tập phổ biến bùng nổ và không thuật toán nào chạy hết được. Notebook khảo sát min_sup từ 0,1% xuống 0,05% cho cả hai thuật toán, và chạy thêm FP-Growth ở 0,04%–0,02% (Apriori bị tràn bộ nhớ ở các mức này trên máy 8 GB RAM).
