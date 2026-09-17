Mã học viên theo lớp: 2A202602164    / Họ và tên: Nguyễn Lê Thế AnhAnh
- Ngày / CVAT local: 17/9
- Công cụ đã dùng: Brush / Polygon / Intelligent Scissors

## 1. Bài đã nộp

| Task | File ZIP đúng tên | Hoàn thành mấy ảnh | Điểm tối đa (coach chấm sau) |
| --- | --- | ---: | ---: |
| easy_semantic | easy_semantic.zip | 3 / 3 | 20 |
| medium_instance | medium_instance.zip | 3 / 3 | 32 |
| hard_panoptic | hard_panoptic.zip | 2 / 2 | 30 |
| cp1_holes | cp1_holes.zip | 1 / 1 | 3 |
| cp2_slice | cp2_slice.zip | 1 / 1 | 3 |
| cp5_occlusion | cp5_occlusion.zip | 1 / 1 | 3 |
| cp3_thin | cp3_thin.zip | 1 / 1 | 3 |
| cp4_curb | cp4_curb.zip | 1 / 1 | 3 |
| cp6_coverage | cp6_coverage.zip | 1 / 1 | 3 |
| **Tổng tối đa** | | | **100** |

## 2. Một quyết định trước khi dùng gợi ý

- Ảnh, vị trí và object Medium đầu tiên tự vẽ: Tôi chọn một chiếc xe trong ảnh đầu tiên của medium_instance và tự vẽ bằng Polygon.
- Class và quy tắc tôi dùng để chọn biên: Tôi chọn đúng class của xe và chỉ vẽ theo phần xe nhìn thấy, không vẽ phần bị vật khác che.
- Nếu dùng gợi ý sau đó: Tôi có dùng Intelligent Scissors để hỗ trợ. Tôi kiểm tra lại biên, chỗ nào bị tràn ra nền thì sửa lại bằng tay.

## 3. Một lỗi tôi tìm thấy và sửa

- Task/ảnh/vùng: cp2_slice, vùng hai xe đứng sát nhau.
- Lỗi thuộc loại: gộp-tách.
- Bằng chứng tôi nhìn thấy: Hai xe cùng class đứng gần nhau nhưng vẫn là hai xe riêng.
- Quy tắc và hành động sửa: Tôi tách thành hai object riêng và chỉnh lại biên.
- Sau sửa đã Save và export lại chưa? Có, tôi đã Save và export lại.
- Kết quả tự đánh giá: chưa có.

## 4. Ba ca chưa chắc hoặc đã cân nhắc

| Ảnh/vị trí | Hai cách hiểu có thể | Quy tắc/chứng cứ | Quyết định hoặc câu hỏi cho coach |
| --- | --- | --- | --- |
| cp1_holes, vùng kính xe | Khoét phần kính hoặc giữ trong mask xe | Kính là một phần của xe | Tôi giữ phần kính trong mask xe |
| cp4_curb, ranh đường và vỉa hè | Road hoặc sidewalk | Tôi nhìn theo bó vỉa và chức năng của vùng | Tôi chọn sidewalk cho phần vỉa hè |
| cp5_occlusion, vật bị che | Tách thành hai object hoặc giữ một object | Hai phần nhìn thấy vẫn thuộc cùng một vật | Tôi giữ là một instance |