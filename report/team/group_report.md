# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: Nhóm CDL
- Thành viên: xem `TEAM.md` (Lê Hoàng Anh, Phan Văn Cường, Bùi Anh Dũng)
- Candidate problem được chọn (1 câu): Khi dữ liệu dạng bảng (CSV) còn nhiều lỗi, sinh viên muốn làm sạch và chuẩn hóa nhanh trước khi huấn luyện để mô hình học trên dữ liệu đáng tin
- Quyết định cuối: Go (pilot nhỏ), xem mục 8.2

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
| ---: | --- | --- | --- | --- | --- |
| 1 | Lê Hoàng Anh | Khi đọc paper nhiều thuật ngữ và công thức, muốn hiểu ý chính và đối chiếu các phần liên quan để biết áp dụng phương pháp nào | Sinh viên/người làm nghiên cứu | Đọc methodology và đối chiếu giữa tài liệu (hơn 2 giờ/phiên) | Dũng: "AI tóm tắt sai công thức thì ai phát hiện?" |
| 2 | Lê Hoàng Anh | Khi chạy thí nghiệm trên GPU, muốn biết tiến trình đang chạy thế nào và còn chờ bao lâu để sắp xếp bước tiếp | Sinh viên chạy thí nghiệm (Kaggle, máy local) | Kiểm tra thủ công GPU và log (~15 phút/lần, 3–4 lần/tuần) | Cường: "`nvidia-smi` hoặc cảnh báo ngưỡng đã đủ chưa, cần AI làm gì?" |
| 3 | Lê Hoàng Anh | Khi có merge conflict trong repo nhóm, muốn biết đoạn nào xung đột và thống nhất cách giữ code để gộp mà không mất thay đổi | Thành viên nhóm cùng sửa một repo | So sánh diff và trao đổi để chọn phần giữ (~30 phút/lần) | Cường: "Chia nhỏ PR và quy tắc nhánh có giải quyết gốc rễ không?" |
| 4 | Phan Văn Cường | Khi cần chạy lại một thí nghiệm cũ, muốn tái lập được kết quả vì code, dữ liệu và tham số đã được lưu thống nhất | Thành viên nhóm làm thí nghiệm | Tìm lại code, dữ liệu, tham số (~1 giờ/lần tìm lại) | Dũng: "Lỗi tái lập do cấu hình hay do code, phân biệt bằng cách nào?" |
| 5 | Phan Văn Cường | Khi một tài liệu/sản phẩm nhận góp ý từ nhiều người, muốn tổng hợp và ưu tiên góp ý để không bỏ sót | Người viết/chủ tài liệu và người góp ý | Gom và ưu tiên nhiều nguồn góp ý, có góp ý mâu thuẫn | Anh: "Tiêu chí ưu tiên do ai quyết, AI có tự quyết thay không?" |
| 6 | Phan Văn Cường | Khi bàn giao một module, muốn có hướng dẫn chạy và kiểm tra thống nhất để người nhận tự chạy được | Người nhận bàn giao module | Người nhận phát sinh nhiều câu hỏi vì thiếu hướng dẫn | Dũng: "Câu hỏi phát sinh do thiếu tài liệu hay do môi trường máy khác nhau?" |
| 7 | Bùi Anh Dũng | Khi dữ liệu thô có nhiều lỗi, muốn làm sạch và chuẩn hóa nhanh để mô hình học trên dữ liệu đáng tin | Sinh viên làm ML với dữ liệu dạng bảng (CSV) | Kiểm tra và viết code xử lý lỗi từng loại (60–90 phút/dataset, ước lượng) | Anh: "AI xóa nhầm dòng hợp lệ hoặc rò rỉ train/test thì sao?" |
| 8 | Bùi Anh Dũng | Khi chạy nhiều thí nghiệm siêu tham số, muốn ghi lại cấu hình và kết quả để tái hiện và biết lần nào tốt nhất | Sinh viên ML, nhóm dự án | Chép kết quả và so sánh bằng tay (3–5 phút/lần chạy, ước lượng) | Cường: "MLflow hoặc Weights & Biases đã giải rồi, vì sao còn cần?" |
| 9 | Bùi Anh Dũng | Khi có kết quả đánh giá, muốn biết mô hình hay sai ở loại mẫu nào để cải thiện đúng chỗ | Sinh viên ML | Đọc và gom nhóm ví dụ sai (20–30 phút/lần đánh giá, ước lượng) | Anh: "Làm sao đo AI gom nhóm lỗi đúng, có bỏ sót nhóm nào không?" |

*Con số trong bảng lấy từ Problem Card cá nhân (CP2), phần lớn là ước lượng, cần xác nhận bằng bấm giờ. Hàng 4–6 lấy từ bảng top 3 của Cường.*

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
| --- | --- | --- |
| A. Đọc và phân tích thông tin | #1 (đọc paper), #5 (tổng hợp góp ý), #9 (phân tích ví dụ sai) | Phải đọc nhiều nội dung dài rồi tự gom nhóm, đối chiếu bằng tay; chất lượng phụ thuộc người đọc |
| B. Theo dõi trạng thái và ghi lại thí nghiệm | #2 (trạng thái GPU), #4 (tái lập thí nghiệm cũ), #8 (ghi cấu hình và kết quả) | Việc lặp lại nhiều lần mỗi buổi, thông tin nằm rải rác ở terminal, log, ghi chú; công cụ có sẵn có thể đủ |
| C. Chuẩn bị dữ liệu và phối hợp trong nhóm | #3 (merge conflict), #6 (bàn giao module), #7 (làm sạch dữ liệu) | Thiếu quy tắc/checklist chung nên mỗi người xử lý một kiểu, tốn thời gian xử lý lỗi lặp lại |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian sinh viên AI/ML mất cho các bước thủ công lặp lại giữa lúc có dữ liệu/kết quả và lúc ra quyết định, mà không giảm độ tin cậy của kết quả
├── Opportunity A: Sinh viên khó nhanh chóng hiểu và đối chiếu nhiều nội dung dài (paper, ví dụ sai) để rút ra điều cần làm tiếp
├── Opportunity B: Sinh viên khó nắm trạng thái và lịch sử các lần chạy thí nghiệm nên mất thời gian kiểm tra và dễ mất cấu hình
└── Opportunity C: Sinh viên thiếu cách làm chung để xử lý lỗi dữ liệu và xung đột code, nên mỗi người tự xử lý và lặp lại việc
```

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| #7 Làm sạch dữ liệu bảng (Dũng) | 4 | 5 | 3 | 4 | 4 | 5 | 4 | 29 |
| #4 Tái lập thí nghiệm cũ (Cường) | 4 | 4 | 4 | 4 | 4 | 3 | 4 | 27 |
| #9 Phân tích mô hình (Dũng) | 4 | 4 | 3 | 3 | 4 | 4 | 4 | 26 |

*Shortlist 3 candidate có điểm cao nhất sau khi chấm sơ bộ cả 6 candidate (các candidate còn lại: #1 = 25, #6 = 24, #5 = 23). #4 có baseline ~1 giờ/lần tìm lại nên "Pain có bằng chứng" cao hơn #7, nhưng điểm "So sánh được các mức" thấp hơn vì công cụ có sẵn (MLflow, W&B, git + file cấu hình) có thể đã đủ, nghiêng về No AI/Rule. #5 và #6 chưa rõ tiêu chí ưu tiên và nguyên nhân gốc (tài liệu thiếu hay môi trường khác nhau) nên điểm "Quy trình rõ" thấp. Điểm do nhóm tự chấm; "Pain có bằng chứng" của #7 thấp vì phần lớn số liệu còn là ước lượng.*

**Candidate được chọn:** #7 — Làm sạch và chuẩn hóa dữ liệu dạng bảng (CSV) trước khi huấn luyện

**Vì sao chọn:** Quy trình có 6 bước rõ, lặp lại ở mọi dự án ML, bottleneck xác định được (bước kiểm tra lỗi và viết code xử lý), điểm tổng cao nhất (29, hơn #4 hai điểm). So sánh được cả bốn mức No AI (checklist + script pandas), Rule (lỗi phổ biến), Workflow (AI gợi ý lỗi lạ) và Agent. Cả nhóm đều làm ML nên hiểu domain.

**Vì sao loại các candidate còn lại:** #9 pain thật nhưng chất lượng phân tích khó đo, AI có thể bỏ sót nhóm lỗi. #1 thời gian đọc là một trường hợp cá nhân, chưa biết có phổ biến không, và khó kiểm tra bản tóm tắt. #4 pain rõ và có baseline, nhưng công cụ có sẵn (MLflow, W&B) có thể đã đủ nên khó chứng minh cần AI; gần trùng #8, có thể gộp thành hướng dự phòng. #5, #6 chưa rõ tiêu chí ưu tiên và nguyên nhân gốc. #2, #8 rất có thể công cụ có sẵn (`nvidia-smi`, MLflow, W&B) đã đủ, nghiêng về No AI. #3 giải bằng quy tắc nhánh và review chéo, không cần AI.

**Xử lý bất đồng (nếu có):** Lo ngại chính từ phản biện: Actor "làm sạch dữ liệu" quá rộng, nên thu hẹp về dữ liệu dạng bảng (CSV); và AI không được tự xóa dữ liệu. Hai điểm này đã đưa vào candidate và boundary. #4 (Cường) điểm sát #7 (27 so với 29) nên giữ làm hướng dự phòng nếu #7 không đủ bằng chứng.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
| ---: | --- | --- | ---: | ---: | --- |
| 1 | Các nhóm làm về LLM cũng mất khoảng 1–2 giờ để làm sạch dữ liệu | Value | 5 | 4 | Không ưu tiên (đã có bằng chứng khá) |
| 2 | Làm sạch dữ liệu chiếm khoảng 30–40% thời gian của dự án | Value | 4 | 2 | **Có, ưu tiên cao nhất** (quan trọng nhưng ít bằng chứng) |
| 3 | AI hỗ trợ gợi ý đúng chỗ có lỗi và đúng loại lỗi | Feasibility | 5 | 4 | Không ưu tiên (đã có bằng chứng khá), nên thử lại trên dữ liệu thật |
| 4 | Sinh viên đọc danh sách lỗi AI đề xuất và tổng hợp được số lượng lỗi hiện có | Usability | 4 | 4 | Không ưu tiên |

*Điểm "Đã có bằng chứng" lấy từ câu trả lời của các bạn được hỏi.*

Giả định nhóm kiểm chứng trong buổi này: giả định #2 (làm sạch dữ liệu chiếm khoảng 30–40% thời gian dự án), vì quan trọng cao (4) mà bằng chứng thấp (2).

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
| --- | --- |
| Người được hỏi (vai trò, không ghi tên thật) | Tech lead của một dự án, vị trí AI Engineer intern |
| Câu nói đáng nhớ nhất (nguyên văn) | Độ chính xác của câu trả lời từ LLM tăng lên khi dữ liệu được làm sạch kỹ hơn, nên việc làm sạch là bước không thể bỏ qua. |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Làm sạch dữ liệu bị sót lỗi vì có quá nhiều trường hợp. Khi chạy kiểm thử mới phát hiện lỗi, phải đọc log để tìm ra. |
| Hiện đang xử lý bằng cách nào (workaround)? | Xử lý thủ công bằng Excel: xóa dòng trùng, sửa sai định dạng, xử lý giá trị thiếu. |
| Mất bao lâu, bao lần? | Việc làm sạch dữ liệu chiếm khoảng 30–40% thời gian dự án. |
| Insight / opportunity rút ra | Làm sạch dữ liệu ảnh hưởng trực tiếp đến chất lượng đầu ra nên không thể bỏ qua; nỗi đau nằm ở chỗ lỗi bị sót và phát hiện muộn (khi chạy kiểm thử), không chỉ ở tốc độ xử lý |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
| --- | ---: | --- | --- |
| Phỏng vấn tech lead (AI Engineer intern) | 1 | Làm sạch dữ liệu chiếm khoảng 30–40% thời gian dự án; lỗi bị sót vì có quá nhiều trường hợp và chỉ lộ ra khi chạy kiểm thử rồi đọc log; đang xử lý thủ công bằng Excel (xóa dòng trùng, sửa định dạng, xử lý giá trị thiếu) | Không ghi nhận tín hiệu phản bác trong buổi này (mới hỏi 1 người nên chưa đủ để kết luận) |
| [CrowdFlower Data Science Report 2016](https://adtmag.com/articles/2016/03/25/data-science-report.aspx) (nguồn thứ cấp, qua ADTmag) | Khảo sát data scientist (chưa kiểm số mẫu) | Làm sạch và sắp xếp dữ liệu là việc tốn thời gian nhất; các bài đưa tin nêu khoảng 60% | Cách diễn đạt khác nhau giữa các nguồn: có nơi là "60% thời gian", có nơi là "60% người trả lời nói đây là việc tốn thời gian nhất"; [một bài phân tích](https://blog.ldodds.com/2020/01/31/do-data-scientists-spend-80-of-their-time-cleaning-data-turns-out-no/) cho rằng con số 80% bị phóng đại |
| [Anaconda State of Data Science 2020](https://www.hpcwire.com/bigdatawire/2020/07/06/data-prep-still-dominates-data-scientists-time-survey-finds/) (nguồn thứ cấp, qua HPCwire) | Gần 2.400 người trả lời (theo bài đưa tin) | Trung bình 45% thời gian dành cho nạp và làm sạch dữ liệu | Riêng làm sạch chỉ khoảng 26% (nạp dữ liệu 19%), thấp hơn mức 30–40% ta đang giả định ở #2 |

**Nhóm đã sửa problem thế nào sau kiểm chứng:** Sau khi đối chiếu phỏng vấn tech lead với hai khảo sát ngành, nhóm sửa problem ở ba điểm. (1) Đổi giả định #2 từ "30–40%" thành khoảng 26–40% thời gian dự án, vì tech lead nói 30–40% còn Anaconda 2020 cho riêng làm sạch khoảng 26%. (2) Thêm vào bottleneck việc lỗi bị sót và chỉ lộ ra khi chạy kiểm thử, nên bổ sung metric "phát hiện sớm" bên cạnh thời gian xử lý. (3) Giữ phạm vi dữ liệu CSV và hướng Workflow, vì công cụ có sẵn (ydata-profiling, Great Expectations) chỉ phủ bước phát hiện lỗi phổ biến, còn lỗi lạ và code xử lý nháp vẫn là khoảng trống.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
| --- | --- | --- | --- | --- | --- |
| ydata-profiling (trước là pandas-profiling) | [docs.profiling.ydata.ai](https://docs.profiling.ydata.ai/4.5/getting-started/quickstart/) | Bước 2: kiểm tra lỗi (thiếu giá trị, trùng lặp, phân bố) | Tạo báo cáo HTML từ DataFrame bằng vài dòng code, xem được ngay trong Jupyter | Chỉ mô tả và phát hiện, không viết code xử lý; không tự biết giá trị nào là "lỗi" theo ngữ nghĩa bài toán | Bước phát hiện lỗi cơ bản đã có công cụ, có thể dùng như Rule; không cần AI cho phần này |
| Great Expectations (GX Core) | [docs.greatexpectations.io](https://docs.greatexpectations.io/docs/core/introduction/gx_overview) | Bước 2 và 4: viết quy tắc kiểm tra dữ liệu và chạy lại để kiểm kết quả | Quy tắc (Expectation) định nghĩa rõ, chạy lặp lại được, có báo cáo kết quả | Phải tự viết và bảo trì quy tắc, cần thời gian học; không gợi ý quy tắc cho dataset lạ | Hợp cho lỗi đã biết trước (Rule); chỗ trống là gợi ý quy tắc và đoạn code xử lý cho lỗi lạ |
| OpenRefine | [openrefine.org](https://openrefine.org) | Bước 3: xử lý lỗi từng loại (gộp giá trị gần giống, chuẩn hóa định dạng) bằng giao diện | Miễn phí, mã nguồn mở, làm sạch bằng giao diện không cần viết nhiều code | Cần cài Java; thao tác thủ công, khó đưa vào pipeline code Python của dự án | Giúp người mới làm sạch nhanh, nhưng không tích hợp tự nhiên vào quy trình train bằng code |

**Kết luận research:** Các bước phát hiện lỗi và kiểm tra lại đã có công cụ làm được (ydata-profiling, Great Expectations). Khoảng trống còn lại là **đề xuất loại lỗi lạ và đoạn code xử lý nháp** cho từng dataset. Nhóm giữ hướng Workflow: Rule cho lỗi phổ biến, AI chỉ gợi ý cho lỗi lạ, sinh viên duyệt trước khi chạy. *(Link lấy từ tìm kiếm; cần tự mở kiểm lại từng link và nội dung trước khi nộp.)*

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Phạm vi: một lần làm sạch một dataset CSV trước khi huấn luyện (6 bước, theo Problem Card #1). Thời gian là ước lượng, chưa bấm giờ.

```text
[1 Tải, đọc thử: 15'] -> [2 Kiểm tra lỗi: 40'] -> [3 Viết code xử lý: 60'] <- BOTTLENECK
-> [4 Chạy lại, kiểm tra: 30'] -> [5 Chuẩn hóa, chia train/test: 20'] -> [6 Lưu dữ liệu sạch: 5']
                                                                       Tổng: ~170' (~3 giờ)
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
| ---: | --- | --- | --- | --- | --- |
| 1. Tải và đọc thử dữ liệu | Sinh viên | Một dataset CSV, các cột có thể lẫn nhiều định dạng giá trị (ngày, số, chuỗi) | Hiểu sơ bộ cấu trúc cột | ~15', mỗi dataset mới | |
| 2. Kiểm tra lỗi | Sinh viên | Dữ liệu thô | Danh sách lỗi (thiếu giá trị, trùng, nhãn lạ, sai định dạng) | ~40' | Xem từng cột, đoán loại lỗi, dễ sót |
| 3. Viết code xử lý từng loại lỗi | Sinh viên | Danh sách lỗi | Script làm sạch (thường làm thủ công hoặc viết riêng cho từng dataset) | ~60' | **Bottleneck**, lặp lại khi phát hiện thêm lỗi |
| 4. Chạy lại, kiểm tra kết quả | Sinh viên | Script, dữ liệu thô | Dữ liệu sau xử lý, xác nhận lỗi đã hết | ~30' | |
| 5. Chuẩn hóa, chia train/test | Sinh viên | Dữ liệu đã xử lý | Dữ liệu chuẩn hóa, các tập train/test | ~20' | Sai ở đây (rò rỉ dữ liệu) gây hậu quả lớn |
| 6. Lưu dữ liệu sạch | Sinh viên | Dữ liệu chuẩn hóa | File dữ liệu sạch | ~5' | |

*Tham chiếu ngành (nguồn thứ cấp, qua HPCwire): khảo sát Anaconda 2020 cho thấy nạp dữ liệu khoảng 19% và làm sạch khoảng 26% thời gian. Số phút ở bảng trên là ước lượng từ Problem Card #1, cần bấm giờ 2–3 dataset để xác nhận.*

**Bottleneck chính:** Bước 2–3 (kiểm tra lỗi và viết code xử lý), khoảng 100' trong tổng ~170'. Phải xem từng cột, đoán loại lỗi và viết script riêng cho từng dataset.

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
[1 Tải, đọc thử: 10'] -> [2 Quét lỗi tự động: 3'] -> [3 Gợi ý lỗi lạ + báo cáo tổng hợp: 3']
     CON NGƯỜI                 RULE                          AI (chỉ đọc) + RULE
-> [4 Duyệt đề xuất + kiểm mẫu không bị đánh dấu: 10'] <- ĐIỂM KIỂM SOÁT
         CON NGƯỜI (HITL)
-> [5 Soạn nháp code xử lý: 2'] -> [6 Chạy trên bản sao, kiểm lại, so sánh trước/sau: 3']
          AI                                   RULE
-> [7 Xem code + diff, xác nhận, lưu dữ liệu sạch và lưu quy tắc: 15']
         CON NGƯỜI (HITL)
-> [8 Chuẩn hóa, chia train/test bằng script cố định: 5']
         RULE (chặn rò rỉ dữ liệu)
                                                                  Tổng: ~51' (~1 giờ)

BOUNDARY:
- AI không xóa hay sửa dữ liệu gốc; chỉ đánh dấu và soạn nháp code, mọi thay đổi chạy trên bản sao.
- AI không quyết định việc chia train/test; bước 8 do script cố định thực hiện.
- Không đưa dữ liệu nhạy cảm vào AI; chỉ gửi mô tả cột và mẫu đã ẩn danh.
- Mọi thay đổi phải do con người xác nhận ở bước 4 và bước 7.

PHƯƠNG ÁN QUAY VỀ:
- Gợi ý của AI nhiễu hoặc sai nhiều → bỏ bước 3 (phần AI) và 5, dùng kết quả quét ở bước 2 cùng checklist thủ công.
- Nháp code làm sai dữ liệu → bỏ bản sao, giữ dữ liệu gốc, viết lại tay.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
| --- | ---: | ---: | --- |
| Số bước | 6 | 8 | Tăng vì thêm bước duyệt và kiểm tra; mục tiêu là giảm thời gian và rủi ro, không giảm số bước |
| Tổng thời gian | ~170' (~3 giờ, ước lượng) | ~51' (~1 giờ, kỳ vọng) | Target dưới 60' lấy từ Problem Card #1; cần bấm giờ 2–3 dataset để xác nhận cả trước và sau |
| Số bước thủ công | 6/6 | 3/8 | Người chỉ làm bước 1, 4, 7 (đọc thử, duyệt đề xuất, xem diff và xác nhận) |
| Bottleneck chính | Kiểm tra lỗi và viết code xử lý (bước 2–3, ~100') | Duyệt đề xuất và xem diff (bước 4 và 7, ~25') | |
| Rủi ro mới phát sinh | — | AI gợi ý sai hoặc bỏ sót lỗi; người dùng tin AI quá mức và duyệt qua loa; lộ dữ liệu nhạy cảm | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
| --- | --- |
| **Actor** | Sinh viên nghiên cứu và làm dự án AI/ML |
| **Quy trình** | Làm sạch và chuẩn hóa một dataset CSV trước khi huấn luyện (6 bước) |
| **Bottleneck** | Kiểm tra lỗi và viết code xử lý từng loại (bước 2–3, ~100' trong ~170') |
| **Impact** | Tốn khoảng 25–45% thời gian dự án; dữ liệu bẩn làm kết quả sai, phải huấn luyện lại |
| **Success Metric** (baseline → target, cách đo) | **(1) Thời gian:** baseline ~170'/dataset (ước lượng) → target dưới 60'/dataset (giả thuyết, điều chỉnh sau khi có baseline thật). Cách đo: mỗi người trong nhóm làm sạch tay 1 dataset CSV (cùng checklist, cùng bộ dữ liệu thử), bấm giờ từ bước 1 đến bước 6, lấy trung bình thay cho baseline ước lượng. **(2) Chất lượng:** cài sẵn một số lỗi đã biết vào dataset thử (dòng trùng, giá trị thiếu, nhãn lạ, sai định dạng). Baseline = tỉ lệ lỗi tìm ra khi làm tay; target = không thấp hơn baseline. **(3) Phát hiện sớm:** đo thời gian từ lúc có dữ liệu đến lúc phát hiện lỗi, so với việc chỉ phát hiện khi chạy kiểm thử |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | **AI không được:** tự xóa hoặc sửa dữ liệu; ghi đè file gốc (luôn giữ bản gốc); tự chạy code; nhận dữ liệu cá nhân hoặc nhạy cảm; đề xuất chuẩn hóa trước khi chia train/test. **Con người kiểm tra:** sinh viên duyệt từng đề xuất của AI trước khi chạy; so số dòng và số giá trị trước/sau mỗi bước; dừng lại kiểm tra khi một bước làm giảm hơn 5% số dòng hoặc đổi hơn 5% giá trị của một cột (ngưỡng ban đầu, điều chỉnh sau khi thử); dừng khi sinh viên không hiểu lý do AI đề xuất |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- **Baseline và target chưa có cơ sở đo:** Đồng ý. Đã thêm cách đo (mỗi người làm sạch tay 1 dataset thử, bấm giờ, lấy trung bình) và ghi target là giả thuyết cần điều chỉnh.
- **Metric chất lượng không có baseline:** Đồng ý. Đã thêm cách đo bằng lỗi cài sẵn và thêm metric "phát hiện sớm", vì pain thật có thể là phát hiện lỗi muộn.
- **Boundary thiếu ngưỡng và người kiểm:** Đồng ý. Đã thêm các điều AI không được làm, ngưỡng 5% và người kiểm là sinh viên.
- **Impact mâu thuẫn giữa các nguồn, Actor chưa khớp bằng chứng (chỉ có 1 tech lead), có thể trượt sang giải pháp, rò rỉ dữ liệu:** Ghi nhận, chưa xử lý trong v0; sẽ xử lý ở CP6 và khi kiểm chứng thêm với sinh viên.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: độ mơ hồ cao x độ phức tạp thấp
* Vì sao: độ mơ hồ cao vì với lỗi lạ, nhiều cách xử lý vẫn chấp nhận được (điền giá trị thiếu bằng trung bình hay trung vị, bỏ dòng) và cách đúng phụ thuộc bài toán. Độ phức tạp thấp vì quy trình hiện tại (4.1) chỉ có 1 nguồn dữ liệu là một file CSV, 6 bước cố định, không rẽ nhánh dù mỗi bước phụ thuộc bước trước.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
| --- | --- | --- | --- | --- |
| **No AI** (sửa quy trình) | Checklist kiểm tra dữ liệu cố định, script pandas dùng lại cho mọi dataset | Dataset có lỗi quen thuộc, nhóm đã có sẵn script | Với dataset lạ vẫn phải xem từng cột và viết code từ đầu, bottleneck bước 2–3 không đổi  | Không chọn |
| **Rule** | ydata-profiling quét lỗi, Great Expectations viết quy tắc kiểm tra (research 3.3) | Lỗi nằm trong tập đã biết trước (trùng, thiếu, sai kiểu) | Không gợi ý được lỗi lạ và không soạn code xử lý; quy tắc phải tự viết cho từng dataset  | Không chọn |
| **Workflow** | Quy trình 4.2: Rule quét lỗi, AI chỉ gợi ý lỗi lạ và soạn nháp code, người duyệt ở bước 4 và 7 | Các bước cố định, AI chỉ cần ở 1–2 chỗ mơ hồ | AI gợi ý sai hoặc bỏ sót, người dùng tin AI quá mức và duyệt qua loa  | Chọn |
| **Agent** | AI tự đọc dữ liệu, tự chọn cách xử lý và tự chạy | Khi các bước không cố định, cần AI tự quyết bước tiếp theo | Vi phạm boundary (AI không tự sửa hay xóa dữ liệu), khó kiểm, chi phí và rủi ro cao | Không chọn |

**Mức chọn:** Workflow

**Vì sao không chọn mức đơn giản hơn:** No AI và Rule đã phủ bước phát hiện lỗi phổ biến (ydata-profiling, Great Expectations, xem 3.3) nhưng không gợi ý được lỗi lạ và không soạn code xử lý nháp, đúng chỗ tốn khoảng 100' ở bước 2–3. Vì vậy cần AI ở bước 3 và 5 của quy trình tương lai (4.2). Không chọn Agent vì các bước cố định và boundary yêu cầu AI không tự hành động.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
| --- | --- |
| **Prediction** — AI dự đoán / tạo ra gì? | Danh sách cột/dòng nghi có lỗi lạ (ngoài các lỗi phổ biến mà Rule đã quét) kèm loại lỗi và lý do; báo cáo tổng hợp lỗi (bước 3); nháp code xử lý từng loại lỗi (bước 5) |
| **Judgment** — con người cân nhắc, quyết định gì? | Sinh viên duyệt từng đề xuất và kiểm mẫu không bị đánh dấu (bước 4); xem code và diff, quyết định cách xử lý (điền giá trị thiếu bằng trung bình, trung vị hay bỏ dòng) rồi xác nhận (bước 7) |
| **Action** — hành động cuối cùng là gì, ai làm? | Chạy code đã duyệt trên bản sao dữ liệu (Rule, bước 6); sinh viên lưu dữ liệu sạch và bộ quy tắc mới (bước 7); script cố định chuẩn hóa và chia train/test (bước 8) |
| **Outcome** — đo kết quả bằng gì? | Thời gian làm sạch mỗi dataset (baseline ~170' → target dưới 60'); tỉ lệ lỗi tìm ra trên lỗi cài sẵn không thấp hơn làm tay; thời gian từ lúc có dữ liệu đến lúc phát hiện lỗi (xem mục 7) |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Mô tả cột (tên, kiểu, thống kê cơ bản), mẫu dòng đã ẩn danh và kết quả quét của Rule ở bước 2. Có sẵn từ công cụ như ydata-profiling hoặc pandas; không gửi toàn bộ dữ liệu và không gửi dữ liệu nhạy cảm |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Sinh viên đánh dấu đề xuất đúng hoặc sai ở bước 4; kết quả diff ở bước 7; lỗi lộ muộn khi chạy kiểm thử (ghi lại và thêm vào bộ quy tắc đã lưu để lần sau Rule bắt được) |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng: Chọn **được hỗ trợ (augment)**. Bằng chứng gián tiếp: tech lead được hỏi nói lỗi bị sót vì có quá nhiều trường hợp và đang xử lý thủ công, tức người dùng cần công cụ giúp phát hiện và soạn nháp chứ chưa có dấu hiệu muốn giao hẳn việc. Việc này cũng khớp với boundary (AI không tự xóa, sửa hay chạy code). Hạn chế: nhóm chưa hỏi trực tiếp người dùng "muốn được hỗ trợ hay giao hẳn", cần xác nhận khi phỏng vấn thêm sinh viên.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào: **Bỏ sót tệ hơn.** Nếu AI bỏ sót lỗi thì dữ liệu bẩn đi vào huấn luyện, kết quả mô hình sai và chỉ lộ ra muộn khi chạy kiểm thử (đúng nỗi đau tech lead nêu). Báo nhầm chỉ tốn thêm thời gian duyệt, và vì AI không được tự xóa hay sửa dữ liệu nên báo nhầm không làm mất dữ liệu. Thiết kế xử lý: Rule quét lỗi phổ biến ở bước 2 làm lưới an toàn; sinh viên kiểm mẫu không bị đánh dấu ở bước 4 để bắt lỗi bị bỏ sót; bước 6 so sánh trước/sau và bước 7 xem diff để bắt báo nhầm; đo tỉ lệ lỗi tìm ra trên lỗi cài sẵn.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
| --- | --- |
| **Actor** | Sinh viên làm bài lab hoặc dự án ML với dữ liệu dạng bảng (CSV) |
| **Quy trình** | Làm sạch và chuẩn hóa một dataset CSV trước khi huấn luyện (6 bước hiện tại, xem 4.1; quy trình tương lai 8 bước, xem 4.2) |
| **Bottleneck** | Bước 2–3: kiểm tra lỗi và viết code xử lý từng loại lỗi, khoảng 100' trong ~170' (ước lượng). Lỗi hay sót và chỉ lộ ra khi chạy kiểm thử rồi đọc log |
| **Impact** | Làm sạch chiếm khoảng 26–40% thời gian dự án (Anaconda 2020: ~26%; tech lead được hỏi: 30–40%); dữ liệu còn lỗi làm kết quả mô hình sai và phải huấn luyện lại |
| **Success Metric** (baseline → target, cách đo) | **(1) Thời gian:** baseline ~170'/dataset (ước lượng) → target dưới 60'/dataset. Cách đo: mỗi người trong nhóm làm sạch tay 1 dataset CSV (cùng checklist, cùng bộ dữ liệu thử) và bấm giờ từ bước 1 đến bước 6; lấy trung bình để thay baseline ước lượng, rồi điều chỉnh target. **(2) Chất lượng:** cài sẵn một số lỗi đã biết vào dataset thử (dòng trùng, giá trị thiếu, nhãn lạ, sai định dạng). Baseline = tỉ lệ lỗi tìm ra khi làm tay; target = không thấp hơn baseline. **(3) Phát hiện sớm:** đo thời gian từ lúc có dữ liệu đến lúc phát hiện lỗi, so với việc chỉ phát hiện khi chạy kiểm thử |
| **Boundary** | **AI không được:** tự xóa hoặc sửa dữ liệu; ghi đè file gốc (luôn giữ bản gốc); tự chạy code; nhận dữ liệu cá nhân hoặc nhạy cảm; đề xuất chuẩn hóa trước khi chia train/test. **Con người kiểm tra:** sinh viên duyệt từng đề xuất của AI trước khi chạy; so số dòng và số giá trị trước/sau mỗi bước; dừng lại kiểm tra khi một bước làm giảm hơn 5% số dòng hoặc đổi hơn 5% giá trị của một cột (ngưỡng ban đầu, điều chỉnh sau khi thử); dừng khi sinh viên không hiểu lý do AI đề xuất |
| **AI intervention point** | Bước 3 (gợi ý lỗi lạ và báo cáo tổng hợp, AI chỉ đọc) và bước 5 (soạn nháp code xử lý) của quy trình tương lai ở 4.2. Các bước còn lại do Rule hoặc con người làm |
| **Mức chọn** | Workflow |
| **Rủi ro & người kiểm tra** | AI gợi ý sai hoặc bỏ sót lỗi; người dùng tin AI quá mức và duyệt qua loa; nháp code xóa nhầm dòng hợp lệ; lộ dữ liệu nhạy cảm. Người kiểm tra: sinh viên làm bài, ở bước 4 (duyệt đề xuất) và bước 7 (xem code và diff). Rule ở bước 6 so sánh trước/sau và bước 8 chặn rò rỉ dữ liệu |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
| --- | --- | --- | --- |
| Actor | Sinh viên nghiên cứu và làm dự án AI/ML | Sinh viên làm bài lab hoặc dự án ML với dữ liệu dạng bảng (CSV) | Phản biện cho rằng "làm sạch dữ liệu" quá rộng; thu hẹp về một loại dữ liệu |
| Quy trình | Quy trình 6 bước | 6 bước hiện tại và 8 bước tương lai | Đã có quy trình tương lai (4.2) |
| Impact | Khoảng 25–45% thời gian dự án | Khoảng 26–40%, có nguồn (Anaconda 2020 và tech lead) | Hai nguồn lệch nhau; ghi khoảng có nguồn thay vì chọn con số đẹp nhất |
| AI intervention point | Không có trong v0 (v0 chỉ có 6 trường) | Bước 3 và 5 của 4.2 | Cần chỉ rõ AI chen vào đâu |
| Mức chọn | Không có trong v0 (v0 chỉ có 6 trường) | Workflow | Kết quả so sánh 4 mức ở 6.2 |
| Rủi ro & người kiểm tra | Không có trong v0 (v0 chỉ có 6 trường) | Xem hàng trên | Trường mới của v1, quyết định sau khi chọn mức can thiệp ở CP6 |

Phản biện v0 đã xử lý ở v1: Impact mâu thuẫn giữa các nguồn (đã ghi khoảng 26–40% kèm nguồn); Actor quá rộng (đã thu hẹp về CSV; vẫn chỉ có 1 tech lead được hỏi, ghi ở mục 9); trượt sang giải pháp (bottleneck mô tả theo việc phải làm, không nhắc công cụ); rò rỉ dữ liệu (bước 8 do script cố định thực hiện).

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
| ---: | --- | --- | --- |
| 1 | Phát hiện đủ lỗi (không thừa, không thiếu) | Không thiếu: tỉ lệ lỗi tìm ra trên dataset có lỗi cài sẵn không thấp hơn làm tay. Không thừa: dưới 20% đề xuất bị sinh viên loại ở bước 4 vì báo nhầm (ngưỡng ban đầu) | Bỏ sót nhiều lỗi hơn làm tay, hoặc từ 20% đề xuất trở lên là báo nhầm |
| 2 | Tối ưu thời gian | Tổng thời gian làm sạch một dataset dưới 60' (trung bình 2–3 dataset), trong đó thời gian duyệt ở bước 4 và 7 không lâu hơn làm tay | Từ 60' trở lên, hoặc bước duyệt tốn thời gian ngang hay hơn việc tự làm |
| 3 | Con người kiểm soát và quay lại được | Mọi thay đổi chỉ được áp dụng sau khi sinh viên xác nhận ở bước 4 và 7; có so sánh trước/sau (diff); luôn giữ bản dữ liệu gốc để quay về | Có thay đổi được chạy mà chưa qua xác nhận, hoặc không còn bản gốc để khôi phục |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
| --- | --- | --- | --- |
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | Trung bình | Pain được xác nhận bởi tech lead (làm sạch chiếm 30–40% thời gian, lỗi sót phát hiện muộn) và hai khảo sát ngành (Anaconda ~26%, CrowdFlower). Nhưng mới hỏi 1 người không phải sinh viên, chưa có sinh viên nào xác nhận |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | Trung bình | Giả định sinh viên đọc và tổng hợp được danh sách lỗi AI đề xuất có bằng chứng khá (4/5). Rủi ro còn lại là duyệt qua loa; giảm bằng diff trước/sau, kiểm mẫu không bị đánh dấu và đề xuất phải nêu rõ cột, dòng, loại lỗi |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | Trung bình | Công cụ có sẵn (pandas, ydata-profiling, Great Expectations) và dữ liệu CSV sẵn có. Chưa thử AI gợi ý lỗi lạ trên dữ liệu thật nên chưa biết tỉ lệ đúng/sai thực tế |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | Thấp | Chi phí thấp vì dùng công cụ có sẵn và AI chỉ xử lý mô tả cột, mẫu ẩn danh. Sinh viên tự vận hành. Cần lưu ý không gửi dữ liệu nhạy cảm (đã có trong boundary) |

### 8.2. Kết luận

**Quyết định:** Go (pilot nhỏ)

**Lý do:** Pain có bằng chứng từ phỏng vấn và hai khảo sát, bottleneck rõ (bước 2–3, ~100' trong ~170'), và Workflow là mức đơn giản nhất đủ dùng (6.2). Cả bốn rủi ro đều ở mức Thấp hoặc Trung bình, không có rủi ro nào Cao. Chi phí pilot thấp và có đường lui (giữ bản gốc, quay về checklist và Rule). Các điểm còn yếu (mới hỏi 1 người, thời gian là ước lượng, chưa thử AI trên dữ liệu thật) sẽ được kiểm ngay trong pilot.

**Nếu Go — pilot nhỏ nhất:** Chọn 2–3 dataset CSV, cài sẵn các lỗi đã biết (dòng trùng, giá trị thiếu, nhãn lạ, sai định dạng). Mỗi dataset làm hai lần: một lần làm tay, một lần theo quy trình 4.2. Bấm giờ từng lần, đếm lỗi tìm ra và số đề xuất bị loại, kiểm bản gốc còn nguyên. Thực hiện trong khoảng 2 tuần.

**Nếu Not Yet — cần kiểm chứng gì trước:** Phỏng vấn thêm 2–3 sinh viên làm ML để xác nhận pain và mức hỗ trợ họ muốn (augment hay automate); bấm giờ làm tay 2–3 dataset để có baseline thật thay cho ước lượng ~170'.

**Nếu No-Go — nên làm gì thay AI:** Dùng checklist kiểm tra cố định cùng ydata-profiling và Great Expectations (Rule), giữ lại script làm sạch dùng lại cho các dataset sau.

**Ngưỡng dừng** (nếu sau … mà … thì quay về …): Nếu sau 2 tuần và 2–3 dataset mà thời gian trung bình vẫn trên 90' một dataset, hoặc tỉ lệ lỗi tìm ra thấp hơn làm tay, hoặc từ 20% đề xuất trở lên là báo nhầm, thì quay về Rule và checklist (không dùng AI). Các ngưỡng này là giá trị ban đầu, điều chỉnh sau khi có baseline thật.

---

## 9. Hạn chế và hướng tiếp theo

- Mới phỏng vấn 1 tech lead (không phải sinh viên) và dùng hai khảo sát ngành làm nguồn thứ cấp; chưa có tiếng nói của sinh viên, nên cần hỏi thêm 2–3 sinh viên làm ML.
- Các con số thời gian (~170' trước, ~51' sau) vẫn là ước lượng; bước tiếp theo là bấm giờ 2–3 dataset để có baseline thật.
- Chưa thử AI gợi ý lỗi trên dữ liệu thật; cần thử trên một dataset CSV có lỗi cài sẵn để đo tỉ lệ lỗi tìm ra.
- Ngưỡng dừng kiểm tra 5% là giá trị ban đầu, cần điều chỉnh sau khi thử.

## 10. Tài liệu tham khảo

- Anaconda, State of Data Science 2020, qua HPCwire: https://www.hpcwire.com/bigdatawire/2020/07/06/data-prep-still-dominates-data-scientists-time-survey-finds/
- CrowdFlower Data Science Report 2016, qua ADTmag: https://adtmag.com/articles/2016/03/25/data-science-report.aspx
- Phân tích về con số "80% thời gian làm sạch dữ liệu": https://blog.ldodds.com/2020/01/31/do-data-scientists-spend-80-of-their-time-cleaning-data-turns-out-no/
- ydata-profiling: https://docs.profiling.ydata.ai/4.5/getting-started/quickstart/
- Great Expectations (GX Core): https://docs.greatexpectations.io/docs/core/introduction/gx_overview
- OpenRefine: https://openrefine.org
- Tài liệu lab: docs/01-worksheet.md, docs/02-deliverable-example.md, CHECKPOINTS.md
