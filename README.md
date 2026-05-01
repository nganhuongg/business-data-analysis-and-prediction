# Business Data Analysis and Prediction

## Mô tả

Project này dùng để phân tích dữ liệu kinh doanh và xây dựng mô hình dự báo `Revenue` và `COGS` theo ngày. Mã nguồn chính nằm trong notebook, gồm một notebook baseline do ban tổ chức cung cấp và một notebook pipeline hoàn chỉnh cho quá trình huấn luyện, đánh giá và xuất submission.

## Cấu trúc thư mục

```text
business-data-analysis-and-prediction/
├── assets/
├── data/
├── docs/latex/
├── eda/
├── requirements/
├── result/
├── src/
├── requirements.txt
└── README.md
```

## Ý nghĩa từng thư mục

- `data/`: chứa dữ liệu gốc do ban tổ chức cung cấp.
- `docs/latex/`: chứa các thành phần của file report, bao gồm code latex, ảnh các biểu đồ và đầu ra file pdf.
- `eda/`: chứa notebook trực quan hóa dữ liệu, bao gồm biểu đồ và phần mô tả/nhận xét dữ liệu.
- `requirements/`: chứa đề thi và tài liệu gốc từ ban tổ chức.
- `src/`: chứa mã nguồn notebook chính của project.
- `assets/`: chứa các ảnh được sinh ra từ quá trình huấn luyện và đánh giá mô hình, ví dụ biểu đồ feature importance, CV performance, forecast plot.
- `result/`: chứa các file đầu ra cuối cùng như `submission.csv` và model artifact `.pkl`.

## Nội dung trong `src/`

- `baseline.ipynb`: notebook baseline do ban tổ chức cung cấp, dùng làm mốc so sánh ban đầu.
- `model_pipeline.ipynb`: pipeline chính cho toàn bộ quá trình đọc dữ liệu, tạo feature, huấn luyện model, đánh giá, trực quan hóa kết quả và xuất file nộp bài.

## Dependencies

Các thư viện Python cần thiết được khai báo trong `requirements.txt`.

## Hướng dẫn chạy lại EDA

1. Kích hoạt môi trường ảo:

```powershell
.\.venv\Scripts\Activate.ps1
```

2. Cài thư viện nếu chưa có:

```powershell
pip install -r requirements.txt
```

3. Mở Jupyter Notebook:

```powershell
jupyter notebook
```

4. Mở file `eda/final_eda_report.ipynb`.

5. Chạy lần lượt toàn bộ các cell để dựng lại phần trực quan hóa và mô tả dữ liệu.

## Hướng dẫn chạy lại model

1. Kích hoạt môi trường ảo:

```powershell
.\.venv\Scripts\Activate.ps1
```

2. Cài thư viện nếu chưa có:

```powershell
pip install -r requirements.txt
```

3. Mở Jupyter Notebook:

```powershell
jupyter notebook
```

4. Mở file `src/model_pipeline.ipynb`.

5. Chạy toàn bộ notebook từ trên xuống dưới để:

- đọc dữ liệu từ `data/`
- tạo feature và train model
- sinh biểu đồ vào `assets/`
- sinh `submission.csv` và `models_ensemble.pkl` vào `result/`

## Hướng dẫn chạy baseline

1. Mở file `src/baseline.ipynb`.

2. Chạy toàn bộ notebook để tái tạo kết quả baseline từ dữ liệu trong `data/`.

## Ghi chú

- Ảnh output của pipeline được lưu ra thư mục `assets/`.
- Kết quả submission và model được lưu ra thư mục `result/`.
- Notebook được chỉnh để ưu tiên làm việc theo cấu trúc thư mục của project hiện tại, không phụ thuộc vào đường dẫn máy cục bộ cũ.
