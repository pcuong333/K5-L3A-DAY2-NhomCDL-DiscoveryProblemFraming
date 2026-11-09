# Báo cáo cá nhân — 2A202603687_BuiAnhDung

**Chủ đề của nhóm:** Làm sạch và chuẩn hóa dữ liệu dạng bảng (CSV) trước khi huấn luyện mô hình, trong bối cảnh sinh viên làm bài lab và dự án AI/ML (nằm trong lĩnh vực học tập, nghiên cứu và làm dự án AI/ML của sinh viên).

## 1. Thông tin học viên

- Họ tên: Bùi Anh Dũng
- MSSV: 2A202603687
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm CDL
- Link repo nhóm: https://github.com/pcuong333/K5_L3A-DAY2-NhomCDL-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi chạy nhiều thí nghiệm với các siêu tham số khác nhau, tôi muốn ghi lại cấu hình và kết quả mỗi lần chạy, để sau này biết lần nào cho kết quả tốt và tái hiện được | Sinh viên làm ML, cả nhóm dự án | Ước lượng: khoảng 10–15 lần chạy/dự án; 3–5 phút ghi chép/lần; vài lần không nhớ cấu hình cũ. Cần xác nhận bằng cách đếm lại |
| 2 | Lặp lại | Khi bắt đầu một bài lab hoặc dự án mới, tôi muốn cài môi trường và thư viện (Python, CUDA, package) chạy được ngay, để không mất cả buổi sửa lỗi cài đặt | Sinh viên, cả nhóm | Ước lượng: 1–3 giờ/lần cài môi trường mới; hay gặp lỗi version CUDA/package. Cần xác nhận số lần gặp |
| 3 | Lặp lại | Khi phải thử nhiều cách diễn đạt yêu cầu cho một mô hình để có kết quả tốt, tôi muốn so sánh nhanh các cách trên cùng bộ ví dụ, để chọn cách tốt nhất thay vì thử tay từng cái | Sinh viên làm ứng dụng LLM | Ước lượng: thử 5–10 phiên bản prompt/bài; 2–3 phút/lần thử tay. Cần xác nhận |
| 4 | Tốn thời gian | Khi làm bài toán mới, tôi muốn tìm được dataset phù hợp (đúng nhiệm vụ, đủ lớn, có giấy phép), để bắt đầu huấn luyện sớm | Sinh viên, nhóm dự án | Ước lượng: 1–3 giờ tìm dataset cho bài mới; phải bỏ 2–3 dataset vì sai nhiệm vụ hoặc thiếu giấy phép. Cần xác nhận |
| 5 | Tốn thời gian | Khi dữ liệu thô có nhiều lỗi (thiếu giá trị, nhãn sai, định dạng khác nhau), tôi muốn làm sạch và chuẩn hóa nhanh, để mô hình học trên dữ liệu đáng tin | Sinh viên làm ML | Ước lượng: làm sạch dữ liệu chiếm khoảng 30–50% thời gian dự án. Cần xác nhận bằng cách bấm giờ một lần |
| 6 | Tốn thời gian | Khi dữ liệu cần gán nhãn bằng tay (ảnh, văn bản), tôi muốn gán nhanh và nhất quán, để có đủ dữ liệu huấn luyện đúng hạn | Sinh viên làm ML, nhóm dự án | Ước lượng: vài trăm mẫu, 5–10 giây/mẫu, tổng 1–3 giờ. Cần xác nhận số mẫu thực tế |
| 7 | Cần đọc, tổng hợp nhiều thông tin | Khi chọn mô hình hoặc thư viện cho dự án, tôi muốn so sánh các lựa chọn (hiệu năng, giá, dễ dùng) từ nhiều nguồn, để quyết định có căn cứ | Sinh viên, nhóm dự án | Ước lượng: đọc 3–5 nguồn, mất 1–2 giờ để so sánh. Cần xác nhận |
| 8 | Cần đọc, tổng hợp nhiều thông tin | Khi có kết quả đánh giá của mô hình (log, metric, ví dụ sai), tôi muốn biết mô hình hay sai ở loại mẫu nào, để cải thiện đúng chỗ | Sinh viên làm ML | Ước lượng: 20–30 phút đọc log và xem ví dụ sai/lần đánh giá. Cần xác nhận |
| 9 | Pain từ người khác | Khi mỗi bạn trong nhóm chia train/test hoặc tiền xử lý dữ liệu khác nhau, tôi muốn kết quả của mọi người so sánh được, để chọn mô hình công bằng | Cả nhóm dự án | Ước lượng: 1–2 lần/dự án nhóm kết quả không so sánh được; mất 30–60 phút làm lại. Cần xác nhận |
| 10 | Pain từ người khác | Khi cả nhóm dùng chung một khóa truy cập dịch vụ có giới hạn lượt dùng, tôi muốn một người dùng không làm hết hạn mức của mọi người, để ai cũng chạy được thí nghiệm | Cả nhóm, người dùng chung API | Ước lượng: 1–2 lần/dự án hết hạn mức; chờ vài giờ để xin key mới. Cần xác nhận |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Làm sạch và chuẩn hóa dữ liệu thô trước khi huấn luyện (dòng 5) | Quy trình rõ, lặp lại ở mọi dự án ML, chiếm phần lớn thời gian, so sánh được No AI / Rule / Workflow | Con số 30–50% thời gian mới là ước lượng, chưa bấm giờ thật; mỗi dataset lỗi một kiểu nên khó tổng quát |
| 2 | Ghi lại cấu hình và kết quả các lần chạy thí nghiệm (dòng 1) | Lặp lại đều, đo được (phút/lần, số lần mất cấu hình), nhiều bạn cùng gặp | Công cụ có sẵn (MLflow, Weights & Biases) có thể đã đủ, nên có thể không cần AI |
| 3 | Tìm xem mô hình hay sai ở loại mẫu nào (dòng 8) | Pain thật, bước đọc log và ví dụ sai tốn thời gian, hợp với AI hỗ trợ tóm tắt | Chất lượng phân tích khó đo; AI có thể kết luận sai hoặc bỏ sót mẫu lỗi |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi dữ liệu thô có nhiều lỗi (thiếu giá trị, nhãn sai, định dạng khác nhau), tôi muốn làm sạch và chuẩn hóa nhanh, để mô hình học trên dữ liệu đáng tin |
| Actor | Sinh viên làm bài lab hoặc dự án ML với dữ liệu dạng bảng (file CSV) |
| Thời điểm / bối cảnh | Đầu mỗi dự án ML, sau khi tải dataset và trước khi huấn luyện |
| Quy trình hiện tại (3–7 bước) | 1. Tải và đọc thử dữ liệu · 2. Kiểm tra thiếu giá trị, trùng lặp, nhãn lạ · 3. Viết code xử lý từng loại lỗi · 4. Chạy lại và kiểm tra kết quả · 5. Chuẩn hóa định dạng, chia train/test · 6. Lưu bản dữ liệu sạch |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2–3, kiểm tra và viết code xử lý lỗi từng loại: ước lượng 60–90 phút/dataset, phải lặp lại khi phát hiện thêm lỗi |
| Impact (nếu không giải thì sao) | Ước lượng 30–50% thời gian dự án; dữ liệu bẩn làm kết quả mô hình sai và phải huấn luyện lại. Cần xác nhận bằng bấm giờ |
| Success metric (baseline → target) | Tổng thời gian làm sạch từ khoảng 3 giờ (ước lượng) xuống dưới 1 giờ/dataset, đo bằng bấm giờ 2–3 dataset; số lỗi sót sau khi làm sạch không tăng |
| Phương án không dùng AI | Checklist kiểm tra dữ liệu cố định + script làm sạch dùng lại được (pandas, great_expectations) |
| Giả thuyết về AI (nếu có) | AI đọc mẫu dữ liệu và đề xuất danh sách lỗi cùng đoạn code xử lý nháp; sinh viên chạy và kiểm tra từng bước trước khi dùng. Boundary: AI không tự xóa dữ liệu; sinh viên xem số dòng trước/sau mỗi bước và chia train/test trước khi chuẩn hóa |
| Cảm nhận nhanh | Workflow (Rule cho lỗi phổ biến, AI chỉ gợi ý cho lỗi lạ); ước lượng ban đầu, cần kiểm chứng |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ước lượng 3 giờ/dataset
[1 Tải/đọc thử: 15'] → [2 Kiểm tra lỗi: 40'] → [3 Viết code xử lý: 60'] ← BOTTLENECK
→ [4 Chạy lại, kiểm tra: 30'] → [5 Chuẩn hóa, chia train/test: 20'] → [6 Lưu: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi chạy nhiều thí nghiệm với các siêu tham số khác nhau, tôi muốn ghi lại cấu hình và kết quả mỗi lần chạy, để sau này biết lần nào cho kết quả tốt và tái hiện được |
| Actor | Sinh viên làm ML, thành viên nhóm dự án |
| Thời điểm / bối cảnh | Trong lúc huấn luyện và thử nghiệm, nhiều lần mỗi buổi làm việc |
| Quy trình hiện tại (3–7 bước) | 1. Đặt siêu tham số · 2. Chạy huấn luyện · 3. Chép kết quả vào ghi chú hoặc bảng · 4. So sánh với các lần trước · 5. Chọn cấu hình tốt nhất · 6. Lưu lại để báo cáo |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–4, chép kết quả và so sánh bằng tay: ước lượng 3–5 phút/lần chạy; hay quên lưu cấu hình |
| Impact (nếu không giải thì sao) | Ước lượng 10–15 lần chạy/dự án, thỉnh thoảng không tái hiện được kết quả tốt và phải chạy lại. Cần xác nhận |
| Success metric (baseline → target) | Thời gian ghi chép từ 3–5 phút/lần xuống dưới 1 phút; số lần phải chạy lại vì mất cấu hình giảm so với baseline đếm trong 2–4 tuần đầu |
| Phương án không dùng AI | Bảng Google Sheets cố định cột, hoặc công cụ có sẵn (MLflow, Weights & Biases) |
| Giả thuyết về AI (nếu có) | Chưa rõ AI cần ở đâu. Có thể AI chỉ tóm tắt khác biệt giữa hai lần chạy. Giả thuyết yếu: nếu công cụ có sẵn (MLflow, Weights & Biases) đã đủ thì kết luận là không cần AI |
| Cảm nhận nhanh | Rule hoặc No AI (ước lượng ban đầu, cần kiểm chứng) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ước lượng 3–5 phút/lần chạy
[1 Đặt tham số] → [2 Chạy huấn luyện] → [3 Chép kết quả: 3'] ← BOTTLENECK
→ [4 So sánh lần trước] → [5 Chọn cấu hình] → [6 Lưu để báo cáo]
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi có kết quả đánh giá của mô hình (log, metric, ví dụ sai), tôi muốn biết mô hình hay sai ở loại mẫu nào, để cải thiện đúng chỗ |
| Actor | Sinh viên làm bài lab hoặc dự án ML |
| Thời điểm / bối cảnh | Sau khi huấn luyện xong, trước khi quyết định cải thiện mô hình |
| Quy trình hiện tại (3–7 bước) | 1. Chạy đánh giá trên tập kiểm tra · 2. Đọc metric tổng · 3. Lọc các mẫu dự đoán sai · 4. Đọc từng ví dụ sai, gom thành nhóm lỗi · 5. Đoán nguyên nhân · 6. Quyết định chỉnh dữ liệu hoặc mô hình |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4, đọc và gom nhóm các ví dụ sai: ước lượng 20–30 phút/lần đánh giá |
| Impact (nếu không giải thì sao) | Ước lượng mỗi lần đánh giá cần 20–30 phút đọc ví dụ sai; nếu không phân tích lỗi thì chỉnh sai hướng, mất thêm vài lần huấn luyện. Cần xác nhận |
| Success metric (baseline → target) | Thời gian phân tích từ 20–30 phút xuống khoảng 10 phút; số nhóm lỗi chính tìm được không ít hơn bản làm tay |
| Phương án không dùng AI | Bảng confusion matrix, lọc theo nhãn, xem ngẫu nhiên 20 mẫu sai theo từng lớp |
| Giả thuyết về AI (nếu có) | AI đọc danh sách mẫu sai và đề xuất các nhóm lỗi; sinh viên kiểm tra lại với mẫu thật trước khi dùng |
| Cảm nhận nhanh | Workflow (ước lượng ban đầu, cần kiểm chứng) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ước lượng 30–40 phút/lần đánh giá
[1 Chạy đánh giá: 5'] → [2 Đọc metric: 5'] → [3 Lọc mẫu sai: 5']
→ [4 Đọc, gom nhóm lỗi: 20'] ← BOTTLENECK → [5 Đoán nguyên nhân: 5'] → [6 Quyết định]
```

### Card muốn pitch nhất

- Card số: #1 (làm sạch và chuẩn hóa dữ liệu bảng)
- Vì sao: Quy trình rõ, lặp lại ở mọi dự án ML, bottleneck xác định được và so sánh được No AI / Rule / Workflow
- Câu hỏi muốn nhóm phản biện: Checklist + script làm sạch dùng lại được đã đủ chưa, hay AI gợi ý lỗi lạ thật sự đáng công?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Card #1: "Làm sạch dữ liệu" quá rộng (bảng, ảnh, văn bản có loại lỗi khác nhau), khó thiết kế một quy trình chung | Đồng ý | Thu hẹp Actor của Card #1 về sinh viên làm việc với dữ liệu dạng bảng (file CSV) |
| Card #1: Mã xử lý do AI sinh ra có thể xóa nhầm dữ liệu hợp lệ hoặc chuẩn hóa trước khi chia train/test (rò rỉ dữ liệu), làm kết quả mô hình đẹp giả | Đồng ý | Thêm boundary vào mục giả thuyết AI của Card #1: AI không tự xóa dữ liệu; sinh viên kiểm số dòng trước/sau và chia train/test trước khi chuẩn hóa |
| Card #2: Công cụ có sẵn (MLflow, Weights & Biases) có thể đã giải được vấn đề; card chưa nói vì sao sinh viên không dùng chúng | Không đồng ý | Card #2 chưa khẳng định cần AI, đang để cảm nhận nhanh là Rule hoặc No AI và đã nêu MLflow/W&B ở mục phương án không dùng AI. Vì vậy chưa cần giải thích thêm lý do không dùng; chỉ bổ sung ở giả thuyết AI rằng nếu công cụ có sẵn đã đủ thì kết luận là không cần AI |
| Card #2: Metric "số lần không tái hiện được về 0" quá tuyệt đối và khó chứng minh trong 4 tuần | Đồng ý | Đổi metric của Card #2 thành "số lần phải chạy lại vì mất cấu hình giảm so với baseline đếm trong 2–4 tuần đầu" |


## 4. Tôi đã tham gia phần nào (CP3 → CP7)

> Phần nhóm (CP3) ghi chi tiết ở [group_report.md](../team/group_report.md); ở đây chỉ báo cáo phần của tôi.

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 Problem Card (làm sạch dữ liệu, ghi cấu hình thí nghiệm, phân tích ví dụ sai) | Ghi ở group_report mục 2.1, hàng 7–9; Card #1 vào shortlist |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: "AI tóm tắt sai công thức thì ai phát hiện?" (hỏi bài đọc paper của Anh) | Ghi ở group_report mục 2.1, hàng 1 |
| Nhận phản biện | Câu hỏi tôi nhận được: "AI xóa nhầm dòng hợp lệ hoặc rò rỉ train/test thì sao?"; "MLflow hoặc W&B đã giải rồi, vì sao còn cần?" | Tôi đã sửa gì: thu hẹp Actor về dữ liệu CSV, thêm boundary AI không tự xóa dữ liệu (xem mục 3, bảng AI phản biện) |
| Gom cluster / cây OST | Đề xuất cluster A/B/C và danh sách ý bị gạch vì là solution đội lốt opportunity | group_report mục 2.2, 2.3 |
| Chọn candidate problem | Chấm điểm shortlist và đề xuất chọn #7 (làm sạch dữ liệu) | group_report mục 2.4; #7 là candidate được chọn |
| Kiểm chứng / research | Phỏng vấn 1 tech lead (AI Engineer intern) và hỏi một số bạn để chấm Assumption Map; tìm công cụ có sẵn (ydata-profiling, Great Expectations, OpenRefine) và hai khảo sát ngành (Anaconda 2020, CrowdFlower 2016) | group_report mục 3: đổi giả định Impact thành khoảng 26–40%, thêm metric "phát hiện sớm", kết luận công cụ có sẵn chưa phủ lỗi lạ nên giữ hướng Workflow |
| Quy trình nhóm | Vẽ quy trình hiện tại 6 bước (~170', bottleneck bước 2–3), quy trình tương lai 8 bước (~51') có Rule, AI, con người, boundary và phương án quay về; bảng before/after | group_report mục 4: nhóm thấy rõ AI chỉ chen vào bước 3 và 5, người duyệt ở bước 4 và 7 |
| Problem Statement | Viết v0, nhờ AI chỉ lỗ hổng rồi chọn sửa 3 điểm (cách đo baseline/target, metric chất lượng, boundary có ngưỡng); viết v1 kèm bảng thay đổi so với v0 và 3 tiêu chí đánh giá (phát hiện đủ lỗi, tối ưu thời gian, con người kiểm soát) | group_report mục 5 và 7 |
| Mức can thiệp AI | Đặt bài vào ô độ mơ hồ cao × độ phức tạp thấp, so sánh 4 mức, chọn Workflow, điền AI Canvas và 2 câu hỏi PAIR | group_report mục 6: chốt Workflow, AI chỉ ở bước 3 và 5 |
| Quyết định | Chấm 4 rủi ro và đề xuất Go (pilot nhỏ) với ngưỡng dừng đo được | group_report mục 8; các ngưỡng 90', 20%, 5% là giá trị ban đầu, cần điều chỉnh sau khi có số đo thật |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | Nhờ AI phản biện 2 card đầu | Chỉ ra Actor "làm sạch dữ liệu" quá rộng, rủi ro AI xóa nhầm/rò rỉ dữ liệu, metric tuyệt đối | Với Card #2, AI nói thiếu lý do không dùng MLflow/W&B; tôi không đồng ý vì card chưa khẳng định cần AI | Thu hẹp Actor, thêm boundary, đổi metric; giữ nguyên Card #2 và bổ sung điều kiện "công cụ có sẵn đủ thì không cần AI" |
| CP4 Research | Tìm công cụ có sẵn và khảo sát ngành về thời gian làm sạch dữ liệu | Tìm nhanh nguồn, và chỉ ra tín hiệu phản bác (Anaconda cho riêng làm sạch ~26%, thấp hơn 30–40% nhóm giả định) | Con số CrowdFlower được diễn đạt không thống nhất giữa các bài ("60% thời gian" hay "60% người trả lời chọn tốn thời gian nhất"); các nguồn đều là thứ cấp; link ydata là trang của bản cũ | Ghi cả hai cách diễn đạt, đánh dấu nguồn thứ cấp, thêm bằng chứng từ phỏng vấn tech lead, tự kiểm lại link |
| CP5 Quy trình | Dựng khung quy trình từ danh sách các giai đoạn xử lý dữ liệu | Có sẵn khung 7 giai đoạn và mức chậm từng giai đoạn để tham chiếu | Lần đầu viết theo quy trình toàn ngành (có huấn luyện, gán nhãn) nên rộng hơn phạm vi bài | Yêu cầu viết lại theo hướng before/after cho một lần làm sạch một dataset (6 bước) và tự viết quy tắc quy trình tương lai |
| CP5–6 Problem Statement | Nhờ AI chỉ lỗ hổng của v0 (không để AI viết lại) | Chỉ ra baseline và target chưa có cơ sở đo, metric chất lượng không có baseline, boundary thiếu ngưỡng và người kiểm | Ngưỡng 5% và 20% AI đề xuất chưa có cơ sở; nhiều lỗ hổng cùng lúc, không phân biệt mức ưu tiên | Chọn sửa 3 lỗ hổng quan trọng nhất trước, các điểm còn lại để CP6; ghi các ngưỡng là "giá trị ban đầu" |
| CP6 Mức can thiệp / quyết định | Hỏi cách làm ma trận, so sánh 4 mức và AI Canvas | Giải thích hai trục của ma trận và gợi ý nội dung từng ô để tôi đối chiếu với quy trình 4.2 | Lúc đầu AI trộn lẫn độ mơ hồ (về đầu ra) với việc đầu vào đa dạng; một lần AI chèn nhầm và làm lặp một số mục của báo cáo nhóm | Đối chiếu lại định nghĩa trong tài liệu, chọn ô độ mơ hồ cao × độ phức tạp thấp; tự chọn tên tiêu chí 3 (con người kiểm soát) và kiểm lại cấu trúc file sau khi AI sửa |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Nghe Anh và Cường, tôi thấy nhóm có hai hướng khác nhau: Anh nghiêng về đọc tài liệu và chạy thí nghiệm trên GPU, Cường nghiêng về tái lập thí nghiệm và phối hợp trong nhóm. Tôi học được rằng nhiều pain nghe có vẻ khác nhau nhưng cùng một kiểu "việc lặp lại tốn thời gian", và không phải pain nào cũng cần AI vì có cái đã có công cụ sẵn như nvidia-smi, MLflow hay git. Khi gom cluster, card của tôi và của Cường nằm gần nhau ở nhóm ghi lại và tái lập thí nghiệm.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có. Khi lập cây OST, nhiều ý đầu tiên là giải pháp, như "dùng LLM tóm tắt paper", "dashboard theo dõi GPU", "agent tự giải merge conflict". Nhóm nhận ra khi cố viết chúng thành nhu cầu của người dùng mà không được nhắc tên công cụ. Chúng tôi gạch bỏ và viết lại thành pain. Với bài của tôi cũng vậy: lúc đầu tôi nghĩ ngay đến "AI làm sạch dữ liệu", đến khi research mới thấy công cụ có sẵn đã phủ phần phát hiện lỗi phổ biến, nên chỗ cần AI thu hẹp lại ở lỗi lạ và code xử lý nháp.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có. Ở mục 6.1 tôi từng viết độ phức tạp là "trung bình" vì có 6 bước, và coi việc đầu vào không rõ là độ mơ hồ. Sau khi đối chiếu định nghĩa trong tài liệu (độ mơ hồ nói về đầu ra có đáp án đúng rõ hay không, độ phức tạp tính cả số nguồn dữ liệu), tôi đổi thành độ mơ hồ cao và độ phức tạp thấp vì chỉ có một file CSV. Trước đó, khi bị phản biện Actor "làm sạch dữ liệu" quá rộng, tôi cũng thu hẹp về dữ liệu dạng bảng.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Có hai điều làm tôi chú ý. Một là khảo sát Anaconda 2020 cho riêng làm sạch dữ liệu khoảng 26%, thấp hơn mức 30–40% mà tech lead nói và nhóm giả định, nên tôi đổi Impact thành một khoảng có nguồn. Hai là tech lead nói lỗi bị sót vì có quá nhiều trường hợp và chỉ lộ khi chạy kiểm thử rồi đọc log. Tức nỗi đau không chỉ là chậm mà còn là phát hiện muộn, nên nhóm thêm metric "phát hiện sớm" bên cạnh thời gian xử lý.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là viết Success Metric có đủ baseline, target và cách đo, vì baseline khoảng 170 phút chỉ là ước lượng của một người. Tôi phải nghĩ cách đo thật: làm tay và bấm giờ, cài sẵn lỗi đã biết để đếm tỉ lệ lỗi tìm ra. Phần Boundary cũng khó, vì phải cân giữa việc AI không được làm gì và lúc nào người phải dừng lại kiểm tra; ngưỡng 5% tôi đặt còn là giá trị ban đầu, chưa có cơ sở.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Tôi sẽ bấm giờ làm sạch thật 2–3 dataset ngay từ đầu để có baseline thay vì ước lượng, và phỏng vấn thêm sinh viên thật vì mới hỏi được một tech lead. Tôi cũng sẽ phản biện mạnh hơn ở việc công cụ có sẵn đã đủ chưa, nhất là với candidate #4 và #8 của nhóm đang gần trùng nhau, để nhóm chọn dựa trên bằng chứng sớm hơn.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Sinh viên làm ML mất nhiều thời gian làm sạch dữ liệu CSV, nhất là bước kiểm tra lỗi và viết code xử lý. Quy trình hiện tại có 6 bước, khoảng 170 phút, bottleneck ở bước 2–3 (khoảng 100 phút). Metric là giảm từ khoảng 170 phút xuống dưới 60 phút mỗi dataset, tỉ lệ lỗi tìm ra không thấp hơn làm tay, đo bằng bấm giờ và lỗi cài sẵn. Boundary: AI không tự xóa, sửa hay chạy code, luôn giữ bản gốc, người duyệt ở bước 4 và 7 và dừng lại khi một bước đổi hơn 5%. Mức can thiệp là Workflow: Rule quét lỗi phổ biến, AI chỉ gợi ý lỗi lạ và soạn nháp code, vì công cụ có sẵn chưa phủ lỗi lạ còn Agent thì thừa. Quyết định là Go với pilot nhỏ; nếu sau 2 tuần thời gian vẫn trên 90 phút hoặc sót lỗi nhiều hơn làm tay thì quay về Rule và checklist.

---

## 7. Tài liệu tham khảo

- Anaconda, State of Data Science 2020, qua HPCwire: https://www.hpcwire.com/bigdatawire/2020/07/06/data-prep-still-dominates-data-scientists-time-survey-finds/
- CrowdFlower Data Science Report 2016, qua ADTmag: https://adtmag.com/articles/2016/03/25/data-science-report.aspx
- ydata-profiling: https://docs.profiling.ydata.ai/4.5/getting-started/quickstart/
- Great Expectations (GX Core): https://docs.greatexpectations.io/docs/core/introduction/gx_overview
- OpenRefine: https://openrefine.org
- Báo cáo nhóm: ../team/group_report.md
