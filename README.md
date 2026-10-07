# PAP_NER + PhoBERT-v2 + CRF

Bộ notebook và artifact cho bài toán nhận dạng thực thể tiếng Việt (NER) trên **PAP_NER**, sử dụng **PhoBERT-v2 kết hợp CRF**.

## Cấu trúc repository

- `notebooks/PAP_NER_PhoBERT_v2_CRF_1epoch.ipynb` — notebook Kaggle, chạy một epoch để xác minh pipeline.
- `notebooks/PAP_NER_PhoBERT_v2_CRF_20epoch.ipynb` — notebook cấu hình thí nghiệm trên Vast.ai; có profile 20 epoch và các bước kiểm tra, train, đánh giá, đóng gói kết quả.
- `artifacts/PAP_NER_PhoBERT_v2_CRF_20epoch_results.zip` — kết quả chạy, gồm checkpoint tốt nhất, runner, tokenizer, cấu hình, lịch sử train và báo cáo đánh giá. File này được lưu bằng Git LFS.

## Notebook trên Kaggle

[Mở notebook PhoBERT-v2 test 1 epoch trên Kaggle](https://www.kaggle.com/code/dsfsdfdssdfdsf/phobert-v2-test-1-epoch-fs/notebook)

## Kết quả trong artifact

Trên test split được ghi trong artifact, entity strict micro F1 là **0.9804** (precision **0.9888**, recall **0.9721**). Báo cáo đầy đủ nằm trong `test_report.txt` và `test_metrics.json` bên trong file ZIP.

## Lấy artifact

Cần cài Git LFS để tải file ZIP đầy đủ:

```bash
git lfs install
git clone https://github.com/nobody-nothing-nowhere-just-kurumi/papner-phobert-v2-crf.git
cd papner-phobert-v2-crf
git lfs pull
```

Nếu Git LFS chưa được cài, clone vẫn lấy được notebook và README nhưng file ZIP lớn sẽ chỉ là con trỏ LFS.


