# Báo cáo cá nhân — 2A202603669_PhanVanCuong

# Chủ đề của nhóm: Học tập, nghiên cứu và làm dự án AI/ML của sinh viên (đọc và tổng hợp paper/tài liệu, gỡ lỗi code, làm việc nhóm trên Git, huấn luyện và triển khai mô hình, ôn tập kiến thức AI).

## 1. Thông tin học viên

- **Họ tên:** Phan Văn Cường
- **MSSV:** 2A202603669
- **Email trường:** [Bổ sung nếu cần]
- **Tên nhóm:** Nhóm CDL
- **Link repo nhóm:** https://github.com/pcuong333/K5_L3A-DAY2-NhomCDL-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Các vấn đề dưới đây cùng thuộc bối cảnh học tập, nghiên cứu và phát triển phần mềm/AI, nhưng tập trung vào những nội dung khác với các problem về đọc paper, debug lỗi tensor, theo dõi tài nguyên GPU và xung đột mã nguồn.

### Bảng scan

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi bắt đầu một task mới, tôi muốn xác định được việc nào cần làm trước, để không mất thời gian chuyển qua lại giữa nhiều việc. | Tôi và thành viên cùng nhóm | Mỗi tuần có khoảng 4–5 task cần xử lý; mất 10–15 phút mỗi lần sắp xếp lại danh sách khi có việc phát sinh. Căn cứ: bảng task và lịch cá nhân. |
| 2 | Tốn thời gian | Khi cần chạy lại một thí nghiệm đã thực hiện trước đó, tôi muốn biết chính xác phiên bản code, dữ liệu và tham số đã dùng, để có thể tái lập kết quả. | Tôi và người tiếp tục nghiên cứu | Lần gần nhất mất khoảng 1 giờ để tìm lại tham số và kiểm tra các file cấu hình của một lần chạy cũ. Căn cứ: thư mục thí nghiệm, file cấu hình và lịch sử commit. |
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi bắt đầu sử dụng một thư viện hoặc framework mới, tôi muốn biết các bước cài đặt và ví dụ phù hợp với phiên bản đang dùng, để triển khai nhanh hơn. | Tôi và sinh viên trong nhóm | Khi làm việc với một thư viện mới, phải mở nhiều trang tài liệu và ví dụ; lần gần nhất mất khoảng 1 giờ để xác định cách sử dụng đúng. Căn cứ: ghi chú cá nhân và lịch sử tìm kiếm. |
| 4 | Lặp lại | Khi hoàn thành một thí nghiệm, tôi muốn ghi lại kết quả theo một mẫu thống nhất, để dễ so sánh giữa các lần chạy. | Tôi và các thành viên nghiên cứu | Kết quả thường được lưu ở nhiều file khác nhau; mỗi lần tổng hợp bảng so sánh mất khoảng 20–30 phút. Căn cứ: các file kết quả và bảng theo dõi thí nghiệm. |
| 5 | Tốn thời gian | Khi chuẩn bị báo cáo hoặc thuyết trình về một dự án kỹ thuật, tôi muốn chọn được những kết quả quan trọng, để không phải mất quá nhiều thời gian chỉnh sửa nội dung. | Tôi, thành viên nhóm và người nghe báo cáo | Mỗi lần chuẩn bị báo cáo mất khoảng 2–3 giờ; phần tốn thời gian nhất là chọn số liệu và sắp xếp nội dung. Căn cứ: lịch sử chỉnh sửa slide và file thuyết trình. |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi nhận góp ý từ nhiều người cho một tài liệu hoặc sản phẩm, tôi muốn gom các góp ý theo chủ đề và mức độ ưu tiên, để xử lý đúng những điểm quan trọng trước. | Tôi và người review | Góp ý thường nằm trong nhiều tin nhắn hoặc comment; lần gần nhất mất khoảng 30 phút để tổng hợp và tránh bỏ sót ý kiến. Căn cứ: thread trao đổi và lịch sử chỉnh sửa tài liệu. |
| 7 | Pain từ người khác | Khi bàn giao một module cho thành viên khác, họ muốn có hướng dẫn chạy và kiểm tra rõ ràng, để không phải hỏi lại nhiều lần. | Thành viên nhận bàn giao và người phụ trách module | Sau mỗi lần bàn giao thường phát sinh 2–3 câu hỏi về cách cài đặt hoặc chạy thử. Căn cứ: tin nhắn trao đổi và checklist bàn giao. |
| 8 | Lặp lại | Khi làm việc nhóm qua nhiều kênh trao đổi, tôi muốn các quyết định và việc cần làm được ghi lại ở một nơi, để mọi người không hiểu khác nhau về nhiệm vụ. | Tôi và các thành viên nhóm | Sau các buổi trao đổi thường mất 10–15 phút để xác nhận lại ai làm gì và thời hạn nào. Căn cứ: lịch sử tin nhắn nhóm và danh sách công việc. |

### Nếu có dùng AI để gợi ý thêm

- **Tôi đã tự scan trước khi hỏi AI chưa?:** Có. Tôi đã tự liệt kê các khó khăn thường gặp khi quản lý task, chạy lại thí nghiệm, chuẩn bị báo cáo và phối hợp trong nhóm.
- **Ý AI gợi ý mà tôi giữ lại:** Vấn đề chuẩn hóa việc ghi lại kết quả thí nghiệm và tổng hợp góp ý từ nhiều nguồn. Tôi giữ lại vì cả hai vấn đề đều có quy trình lặp lại và có thể quan sát bằng thời gian xử lý, số lần hỏi lại hoặc số lần bỏ sót.
- **Ý AI gợi ý mà tôi bỏ và vì sao:** Tôi bỏ các ý quá rộng như “xây trợ lý AI cho toàn bộ dự án” và “tự động quản lý mọi công việc”, vì chưa xác định được actor, quy trình cụ thể và metric để kiểm chứng.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Khó tái lập một thí nghiệm cũ vì code, dữ liệu và tham số được lưu chưa thống nhất. | Có quy trình cụ thể, ảnh hưởng trực tiếp đến độ tin cậy của kết quả và đã có baseline khoảng 1 giờ cho một lần tìm lại. | Chưa biết các thành viên khác gặp vấn đề với tần suất giống nhau hay không; chưa xác định cách phân biệt lỗi do cấu hình với lỗi do code. |
| 2 | Khó tổng hợp và ưu tiên góp ý từ nhiều người cho cùng một tài liệu hoặc sản phẩm. | Có nhiều nguồn phản hồi, dễ đo thời gian xử lý và nguy cơ bỏ sót góp ý. | Chưa biết tiêu chí ưu tiên nào được mọi người thống nhất; một số góp ý có thể mâu thuẫn nhau. |
| 3 | Bàn giao module chưa có hướng dẫn chạy và kiểm tra thống nhất. | Pain ảnh hưởng trực tiếp đến người nhận bàn giao, có dấu hiệu qua số câu hỏi phát sinh và phù hợp để thử quy trình đơn giản trước khi dùng AI. | Chưa biết phần lớn câu hỏi xuất phát từ tài liệu thiếu hay do môi trường máy khác nhau. |

### Problem Card #1 — Tái lập thí nghiệm

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần chạy lại một thí nghiệm đã thực hiện trước đó, tôi muốn biết chính xác phiên bản code, dữ liệu và tham số đã dùng, để có thể kiểm tra và tái lập kết quả. |
| Actor | Sinh viên hoặc thành viên nghiên cứu chịu trách nhiệm chạy thí nghiệm. |
| Thời điểm / bối cảnh | Khi cần kiểm tra lại kết quả, so sánh mô hình hoặc bàn giao thí nghiệm cho người khác. |
| Quy trình hiện tại (3–7 bước) | 1. Tìm commit hoặc thư mục code gần đúng. 2. Tìm file dữ liệu đã dùng. 3. Tìm tham số trong notebook, log hoặc tin nhắn. 4. Kiểm tra phiên bản thư viện. 5. Chạy thử lại. 6. So sánh kết quả với lần chạy trước. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Tìm và đối chiếu code, dữ liệu, tham số ở nhiều nơi; mất khoảng 60 phút/lần. |
| Impact (nếu không giải thì sao) | Không tái lập được kết quả, phải chạy thử nhiều lần và khó xác định nguyên nhân khi kết quả khác trước. |
| Success metric (baseline → target) | Thời gian từ lúc bắt đầu tìm kiếm đến khi chạy thành công mô hình từ khoảng 60 phút xuống dưới 20 phút; tái lập đúng cấu hình trong ít nhất 90% lần thử. |
| Phương án không dùng AI | Dùng template bắt buộc cho mỗi thí nghiệm, lưu file cấu hình cùng commit và tạo checklist trước khi chạy. |
| Giả thuyết về AI (nếu có) | AI có thể đọc metadata, log và file cấu hình để tạo bản tóm tắt lần chạy, nhưng người nghiên cứu vẫn phải xác nhận các phiên bản và tham số. |
| Cảm nhận nhanh | Rule trước; chỉ cân nhắc Workflow nếu việc chuẩn hóa metadata chưa đủ. |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 60 phút/lần
[Tìm commit: 15'] → [Tìm dữ liệu: 15'] → [Tìm tham số: 20']
→ [Kiểm tra môi trường: 10'] → [Chạy lại và so sánh]
                         ↑ BOTTLENECK
```

### Problem Card #2 — Tổng hợp và ưu tiên góp ý

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận góp ý từ nhiều người cho một tài liệu hoặc sản phẩm, tôi muốn gom các góp ý theo chủ đề và mức độ ưu tiên, để xử lý đúng những điểm quan trọng trước. |
| Actor | Người phụ trách chỉnh sửa tài liệu hoặc sản phẩm nhóm. |
| Thời điểm / bối cảnh | Sau khi gửi báo cáo, slide, tài liệu kỹ thuật hoặc bản demo để các thành viên review. |
| Quy trình hiện tại (3–7 bước) | 1. Mở các tin nhắn, comment hoặc file review. 2. Đọc từng góp ý. 3. Chép góp ý vào danh sách riêng. 4. Gom các ý trùng nhau. 5. Phân loại theo nội dung và mức độ ưu tiên. 6. Cập nhật tài liệu. 7. Hỏi lại khi góp ý mâu thuẫn. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Đọc và gom góp ý từ nhiều nguồn; mất khoảng 30 phút/lần review. |
| Impact (nếu không giải thì sao) | Có thể bỏ sót góp ý quan trọng, xử lý sai thứ tự hoặc mất thêm thời gian trao đổi lại với người review. |
| Success metric (baseline → target) | Thời gian tổng hợp từ 30 phút xuống dưới 15 phút; 100% góp ý được ghi nhận; giảm số lần hỏi lại về trạng thái xử lý. |
| Phương án không dùng AI | Dùng một biểu mẫu review thống nhất với các trường: nội dung, vị trí, mức độ ưu tiên và trạng thái. |
| Giả thuyết về AI (nếu có) | AI có thể gom các góp ý tương tự và đề xuất nhóm ưu tiên, nhưng người phụ trách phải xác nhận trước khi thay đổi tài liệu. |
| Cảm nhận nhanh | Workflow, sau khi đã thống nhất mẫu input. |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 30 phút/lần
[Mở các nguồn: 5'] → [Đọc comment: 10'] → [Chép ra danh sách: 10']
→ [Gom và ưu tiên: 5'] → [Cập nhật tài liệu]
                                  ↑ BOTTLENECK
```

### Problem Card #3 — Bàn giao module

| Trường | Nội dung |
|---|---|
| Job Story | Khi bàn giao một module cho thành viên khác, tôi muốn có hướng dẫn chạy và kiểm tra rõ ràng, để người nhận có thể tiếp tục công việc mà không phải hỏi lại nhiều lần. |
| Actor | Thành viên phát triển module và người nhận bàn giao. |
| Thời điểm / bối cảnh | Khi hoàn thành một module hoặc khi chuyển người phụ trách trong dự án nhóm. |
| Quy trình hiện tại (3–7 bước) | 1. Gửi link repository hoặc thư mục code. 2. Nhắn các bước cài đặt. 3. Gửi biến môi trường hoặc cấu hình cần thiết. 4. Người nhận thử chạy. 5. Người bàn giao trả lời câu hỏi phát sinh. 6. Sửa hoặc bổ sung hướng dẫn. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Trả lời các câu hỏi lặp lại sau khi người nhận chạy thử; thường phát sinh 2–3 câu hỏi/lần bàn giao. |
| Impact (nếu không giải thì sao) | Người nhận bị chậm bắt đầu công việc, người bàn giao bị gián đoạn và việc phụ thuộc module có thể bị trễ. |
| Success metric (baseline → target) | Giảm số câu hỏi sau bàn giao từ 2–3 câu xuống tối đa 1 câu; người nhận chạy được kiểm tra cơ bản trong 15 phút đầu. |
| Phương án không dùng AI | Dùng README và checklist bàn giao bắt buộc, kèm một lệnh kiểm tra môi trường và ví dụ đầu vào/đầu ra. |
| Giả thuyết về AI (nếu có) | AI có thể dựa trên cấu trúc repository để tạo bản nháp hướng dẫn, nhưng người phụ trách phải kiểm tra nội dung và thông tin nhạy cảm. |
| Cảm nhận nhanh | Rule hoặc No AI trước; chưa cần Agent. |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 30–45 phút cả hai bên
[Gửi code: 5'] → [Gửi hướng dẫn rời rạc: 10'] → [Người nhận chạy thử: 10']
→ [Hỏi đáp và sửa hướng dẫn: 10–20'] ← BOTTLENECK
```

### Card muốn pitch nhất

- **Card số:** 1
- **Vì sao:** Có pain rõ, ảnh hưởng trực tiếp đến khả năng kiểm chứng kết quả và có thể bắt đầu bằng một giải pháp rule đơn giản trước khi cân nhắc AI.
- **Câu hỏi muốn nhóm phản biện:** Việc chuẩn hóa template và metadata có đủ giải quyết vấn đề không, hay vẫn cần một workflow hỗ trợ tổng hợp thông tin từ log và repository?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Card #1 có thể giải quyết phần lớn bằng quy ước lưu code, dữ liệu và tham số; chưa nên chọn AI ngay. | Đồng ý | Thêm phương án rule và đặt Rule là hướng ưu tiên trước Workflow. |
| Metric “tái lập được kết quả” cần định nghĩa rõ thế nào là đạt. | Đồng ý | Bổ sung mục tiêu tái lập đúng cấu hình trong ít nhất 90% lần thử. |
| Card #2 chưa có tiêu chí khách quan để xác định góp ý đã được xử lý đầy đủ. | Đồng ý một phần | Thêm metric 100% góp ý được ghi nhận và trạng thái xử lý được cập nhật. |


## Quá trình tự nhận diện vấn đề của mình
Lúc đầu ngồi nhìn lại đống tài liệu nghiên cứu trên máy tính, mình thực sự thấy nản. Cứ mỗi lần muốn tìm hiểu sâu về một thuật toán hay phương pháp mới cho đề tài, mình lại rơi vào cái vòng luẩn quẩn quen thuộc: lên mạng tải về vài bài báo, mở lèo tèo chục cái tab PDF cùng lúc, mắt thì hoa lên vì công thức toán học rồi lại cặm cụi ghi chú ra Notion.

Cái lúc tốn thời gian nhất không phải là lúc đi tìm tài liệu, mà là đoạn ngồi đối chiếu xem phương pháp của bài này khác bài kia ở điểm nào, rồi cố hiểu cho đúng bản chất công thức để đem ra áp dụng. Đã thế, nhiều khi đọc xong một buổi chiều, tắt máy đi ngủ hôm sau mở lên lại quên béng mất đoạn chi tiết đó nằm ở trang mấy, lại phải mất công mò mẫm tìm lại từ đầu. Tính ra mỗi lần tổng hợp một chủ đề nhỏ thôi mà mất toi cả buổi, vừa oải vừa dễ bị sót ý quan trọng.

Nghĩ đến chuyện làm sao để thoát khỏi cảnh "bơi trong tài liệu" này, mình quyết định đưa nó vào làm đề tài để mổ xẻ xem có tối ưu hóa được khâu nào không, thay vì cứ cắm đầu đọc thủ công mãi vừa mệt vừa kém hiệu quả.