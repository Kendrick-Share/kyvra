Dưới đây là phiên bản viết lại từ đầu, coi như bạn chưa biết các thuật ngữ phát triển phần mềm. Tôi sẽ dùng ví dụ xuyên suốt là xây chức năng đặt lệnh mua chứng khoán.

QUY TRÌNH PHÁT TRIỂN PHẦN MỀM DÙNG AI CHO MỘT TEAM LỚN

Giải thích từ cơ bản đến nâng cao cho người mới

⸻

1. Trước tiên, cần hiểu đúng vai trò của AI

AI có thể giúp team:

* Phân tích yêu cầu.
* Phát hiện yêu cầu thiếu hoặc mâu thuẫn.
* Thiết kế hệ thống.
* Vẽ sơ đồ.
* Chia công việc.
* Viết code.
* Viết test.
* Review code.
* Tìm ảnh hưởng khi nghiệp vụ thay đổi.
* Hỗ trợ triển khai và vận hành.

Nhưng AI không tự biết đâu là nghiệp vụ đúng của công ty.

Ví dụ, AI không thể tự quyết định:

Khi người dùng đặt lệnh mua nhưng không đủ tiền, hệ thống nên từ chối ngay hay cho phép vay margin?

Đây là quyết định nghiệp vụ do con người đưa ra.

Vì vậy, nguyên tắc quan trọng nhất là:

Con người quyết định hệ thống phải làm gì. AI giúp biến quyết định đó thành tài liệu, thiết kế, code, test và hệ thống hoàn chỉnh.

AI càng mạnh thì càng nên giao cho nó những việc:

* Mơ hồ.
* Phức tạp.
* Có nhiều phương án.
* Nếu làm sai sẽ ảnh hưởng lớn.

AI phổ thông có thể đảm nhận những việc:

* Đã có yêu cầu rõ.
* Đã biết input và output.
* Đã có test kiểm tra.
* Phạm vi thay đổi nhỏ.

⸻

2. Mô hình tổng thể nên áp dụng

Quy trình phát triển phần mềm có AI nên đi theo chuỗi sau:

flowchart LR
    A["1. Xác định vấn đề<br/>Muốn giải quyết việc gì?"]
    B["2. Làm rõ nghiệp vụ<br/>Hệ thống phải hoạt động thế nào?"]
    C["3. Viết đặc tả rõ ràng<br/>Quy tắc, ví dụ, điều kiện đúng sai"]
    D["4. Thiết kế hệ thống<br/>Chia thành phần và cách chúng giao tiếp"]
    E["5. Thiết kế hợp đồng và test<br/>API, dữ liệu, sự kiện, cách kiểm tra"]
    F["6. Chia nhỏ công việc<br/>Mỗi task đủ rõ để AI có thể làm"]
    G["7. Viết code<br/>AI Agent và Developer thực hiện"]
    H["8. Kiểm tra tự động<br/>Test, bảo mật, tương thích"]
    I["9. Triển khai<br/>Đưa sản phẩm lên môi trường thực tế"]
    J["10. Theo dõi vận hành<br/>Log, metric, cảnh báo, lỗi"]
    K["11. Tiếp nhận thay đổi<br/>Quay lại cập nhật tài liệu và hệ thống"]
    A --> B --> C --> D --> E --> F --> G --> H --> I --> J --> K
    K --> B

Đây không phải quy trình làm một lần rồi kết thúc.

Nó là một vòng lặp:

Hiểu yêu cầu
→ Thiết kế
→ Code
→ Test
→ Triển khai
→ Quan sát thực tế
→ Điều chỉnh yêu cầu
→ Tiếp tục phát triển

⸻

3. Giải thích các vai trò trong team

3.1. Product Owner hoặc người phụ trách sản phẩm

Người này quyết định:

* Sản phẩm giải quyết vấn đề gì.
* Chức năng nào quan trọng.
* Làm trước hay làm sau.
* Khi nào chức năng được coi là đạt yêu cầu.

Ví dụ:

Chức năng đặt lệnh phải cho phép khách hàng mua chứng khoán nếu tài khoản đủ tiền.

⸻

3.2. BA là gì?

BA là viết tắt của Business Analyst, nghĩa là chuyên viên phân tích nghiệp vụ.

BA đứng giữa:

* Người kinh doanh.
* Người dùng.
* Developer.
* Tester.
* Người vận hành hệ thống.

BA có nhiệm vụ biến yêu cầu mơ hồ như:

Làm chức năng đặt lệnh chứng khoán.

thành yêu cầu rõ ràng như:

* Người dùng nào được đặt lệnh?
* Đặt được loại lệnh nào?
* Thị trường đóng cửa thì sao?
* Không đủ tiền thì sao?
* Lệnh gửi trùng hai lần thì sao?
* Lệnh đã khớp có hủy được không?
* Ai được sửa lệnh?
* Cần lưu lịch sử những gì?

⸻

3.3. Developer là gì?

Developer, thường gọi là DEV, là người:

* Thiết kế kỹ thuật.
* Viết code.
* Viết test kỹ thuật.
* Sửa lỗi.
* Bảo trì hệ thống.

Developer không chỉ “gõ code”.

Developer tốt phải hiểu:

* Nghiệp vụ.
* Kiến trúc hệ thống.
* Dữ liệu.
* Bảo mật.
* Hiệu năng.
* Cách hệ thống vận hành ngoài thực tế.

⸻

3.4. QA và Tester là gì?

QA là viết tắt của Quality Assurance, nghĩa là đảm bảo chất lượng.

Tester thường tập trung vào kiểm tra sản phẩm.

QA có phạm vi rộng hơn:

* Thiết kế chiến lược test.
* Phát hiện lỗ hổng trong yêu cầu.
* Kiểm tra trường hợp biên.
* Kiểm tra quy trình phát triển.
* Đảm bảo lỗi không dễ lọt ra production.

Trong thực tế, nhiều công ty dùng hai từ QA và Tester gần giống nhau.

⸻

3.5. Architect và Tech Lead

Architect là người thiết kế kiến trúc tổng thể của hệ thống.

Tech Lead là người dẫn dắt kỹ thuật của một team hoặc một nhóm hệ thống.

Họ quyết định hoặc tham gia quyết định:

* Hệ thống chia thành những phần nào.
* Phần nào lưu dữ liệu gì.
* Các service gọi nhau thế nào.
* Dùng database nào.
* Xử lý khi một service bị lỗi.
* Làm sao bảo mật.
* Làm sao hệ thống chịu tải lớn.

⸻

3.6. DevOps, Platform và SRE

DevOps

DevOps không chỉ là một chức danh.

Đây là cách kết hợp:

* Phát triển phần mềm.
* Triển khai phần mềm.
* Vận hành hệ thống.

Mục tiêu là đưa code từ máy developer lên môi trường thật nhanh và an toàn.

Platform Team

Platform Team xây nền tảng dùng chung cho các team:

* Pipeline build.
* Môi trường chạy.
* Kubernetes.
* Logging.
* Monitoring.
* Quản lý secret.
* Công cụ cho AI Agent.

SRE

SRE là viết tắt của Site Reliability Engineering, nghĩa là kỹ thuật đảm bảo hệ thống hoạt động ổn định.

SRE quan tâm đến:

* Hệ thống có thường xuyên bị lỗi không?
* Có chậm không?
* Có chịu được tải lớn không?
* Khi lỗi thì phục hồi bao lâu?
* Cảnh báo có hoạt động không?

⸻

4. Phương pháp tổng thể nên kết hợp

Không có một phương pháp duy nhất giải quyết tất cả.

Nên kết hợp:

SDD
+ BDD hoặc ATDD
+ Contract-First
+ TDD
+ Continuous Verification
+ DevSecOps
+ SRE

Sau đây là giải thích từng phần.

⸻

5. SDD là gì?

SDD là viết tắt của Spec-Driven Development.

Có thể hiểu đơn giản là:

Phát triển dựa trên một bản đặc tả rõ ràng.

Spec, hay specification, nghĩa là tài liệu mô tả chính xác:

* Hệ thống cần làm gì.
* Không làm gì.
* Quy tắc là gì.
* Input là gì.
* Output là gì.
* Khi nào được coi là đúng.
* Trường hợp lỗi xử lý thế nào.

Ví dụ một spec đơn giản:

Chức năng: Đặt lệnh mua chứng khoán
Input:
- Mã chứng khoán
- Giá
- Khối lượng
- Tài khoản đặt lệnh
Điều kiện:
- Tài khoản đang hoạt động
- Thị trường đang cho phép giao dịch
- Tài khoản đủ tiền
- Giá và khối lượng hợp lệ
Output thành công:
- Tạo lệnh mới
- Giữ lại số tiền cần thiết
- Trả về mã lệnh
Output thất bại:
- Trả về lý do thất bại
- Không giữ tiền
- Không tạo lệnh

SDD rất hợp với AI.

Nếu chỉ bảo AI:

Viết chức năng đặt lệnh.

AI phải tự đoán rất nhiều.

Nếu đưa cho AI một spec rõ, nó sẽ code chính xác hơn rất nhiều.

⸻

6. BDD là gì?

BDD là viết tắt của Behavior-Driven Development.

Có thể hiểu là:

Phát triển dựa trên hành vi mà người dùng hoặc hệ thống mong đợi.

BDD thường mô tả theo ba phần:

Given: trạng thái ban đầu
When: hành động xảy ra
Then: kết quả phải đạt được

Ví dụ:

Scenario: Từ chối lệnh khi không đủ tiền
Given tài khoản có 1.000 USD
When khách hàng đặt lệnh cần 1.200 USD
Then hệ thống phải từ chối lệnh
And hệ thống không được giữ tiền
And lý do trả về là INSUFFICIENT_BUYING_POWER

Ý nghĩa:

* Given: trước khi hành động xảy ra, hệ thống đang ở trạng thái nào.
* When: người dùng làm gì.
* Then: hệ thống phải phản ứng thế nào.

BDD giúp BA, DEV và QA nói cùng một ngôn ngữ.

BA đọc được.

QA dùng để viết test.

DEV dùng để hiểu logic.

AI dùng để sinh code và test.

⸻

7. ATDD là gì?

ATDD là viết tắt của Acceptance Test-Driven Development.

Có thể hiểu là:

Viết điều kiện nghiệm thu trước khi viết code.

Acceptance Test là bài test kiểm tra chức năng có đáp ứng đúng yêu cầu kinh doanh hay không.

Ví dụ:

Khi tài khoản không đủ tiền, lệnh phải bị từ chối và tiền không được giữ.

Đây là acceptance test vì nó kiểm tra một yêu cầu nghiệp vụ hoàn chỉnh.

BDD và ATDD khá gần nhau:

* BDD nhấn mạnh hành vi.
* ATDD nhấn mạnh điều kiện để business chấp nhận sản phẩm.

Trong thực tế có thể dùng chung.

⸻

8. TDD là gì?

TDD là viết tắt của Test-Driven Development.

Có thể hiểu là:

Viết test trước, sau đó mới viết code.

Quy trình TDD:

flowchart LR
    A["1. Viết test<br/>Test đang thất bại"]
    B["2. Viết code tối thiểu<br/>Để test chạy đúng"]
    C["3. Dọn lại code<br/>Không làm thay đổi hành vi"]
    D["4. Tiếp tục test mới"]
    A --> B --> C --> D --> A

Ba bước thường được gọi là:

Red → Green → Refactor

* Red: test đang đỏ, tức là thất bại.
* Green: viết code để test chuyển sang xanh.
* Refactor: dọn lại code cho sạch hơn nhưng không làm thay đổi kết quả.

Ví dụ cần viết hàm tính số tiền cần giữ:

Số tiền cần giữ = Giá × Khối lượng + Phí dự kiến

Có thể viết test trước:

Giá = 10
Khối lượng = 100
Phí = 5
Kết quả phải bằng 1.005

Sau đó mới viết hàm tính toán.

⸻

9. SDD, BDD và TDD khác nhau thế nào?

Có thể hiểu theo ba tầng:

SDD: Xây cái gì?
BDD/ATDD: Hệ thống phải thể hiện hành vi gì?
TDD: Code bên trong phải được viết và kiểm tra thế nào?

Ví dụ:

SDD

Xây chức năng đặt lệnh mua.

BDD

Khi không đủ tiền, hệ thống phải từ chối lệnh.

TDD

Viết test cho hàm kiểm tra sức mua trước khi viết hàm đó.

Vì vậy không nên chọn chỉ một mô hình.

Nên kết hợp chúng.

⸻

10. Contract-First là gì?

Contract nghĩa là hợp đồng giao tiếp giữa hai hệ thống.

Ví dụ Order Service muốn gọi Balance Service để giữ tiền.

Hai bên phải thống nhất:

* Order Service gửi dữ liệu gì?
* Balance Service trả dữ liệu gì?
* Nếu lỗi thì trả mã gì?
* Nếu gọi trùng thì sao?
* Bao lâu không trả lời thì coi là timeout?

Một contract có thể được mô tả như sau:

{
  "accountId": "ACC-001",
  "amount": 1000,
  "currency": "USD",
  "referenceId": "ORDER-001"
}

Kết quả:

{
  "success": true,
  "reservationId": "RSV-001"
}

Contract-First nghĩa là:

Thống nhất hợp đồng giao tiếp trước khi các team bắt đầu code.

Điều này rất quan trọng khi nhiều team làm song song.

⸻

11. API là gì?

API là viết tắt của Application Programming Interface.

Hiểu đơn giản:

API là cánh cửa để một chương trình gọi một chương trình khác.

Ví dụ:

POST /orders

Client gửi yêu cầu đặt lệnh.

Hoặc:

POST /balances/reservations

Order Service yêu cầu Balance Service giữ tiền.

API phải mô tả rõ:

* Đường dẫn gọi.
* Loại yêu cầu.
* Dữ liệu đầu vào.
* Dữ liệu trả về.
* Mã lỗi.
* Quyền truy cập.

⸻

12. OpenAPI là gì?

OpenAPI là một định dạng chuẩn để mô tả API HTTP.

Ví dụ nó mô tả:

* API /orders nhận trường gì.
* Trường nào bắt buộc.
* Kiểu dữ liệu là số hay chuỗi.
* Có thể trả về mã lỗi nào.

Từ OpenAPI, công cụ có thể tự động:

* Sinh tài liệu API.
* Sinh code client.
* Sinh khung code server.
* Sinh test.
* Kiểm tra API có bị thay đổi sai không.

⸻

13. Event là gì?

Event nghĩa là một sự kiện đã xảy ra trong hệ thống.

Ví dụ:

OrderCreated
OrderAccepted
OrderRejected
OrderFilled
OrderCancelled

Khi Order Service phát sự kiện:

OrderAccepted

các hệ thống khác có thể nhận được:

* Reporting Service cập nhật báo cáo.
* Notification Service gửi thông báo.
* Risk Service cập nhật trạng thái.
* Audit Service lưu lịch sử.

Điểm khác giữa API và event:

* API thường là một bên gọi trực tiếp một bên khác.
* Event thường là một bên thông báo rằng một việc đã xảy ra.

⸻

14. AsyncAPI và Protobuf là gì?

AsyncAPI

AsyncAPI là định dạng mô tả các message hoặc event.

Nó tương tự OpenAPI, nhưng dùng cho hệ thống giao tiếp bất đồng bộ như:

* Kafka.
* RabbitMQ.
* Message Queue.

Bất đồng bộ nghĩa là bên gửi không nhất thiết phải chờ bên nhận xử lý xong ngay.

Protobuf

Protobuf là cách mô tả dữ liệu thường dùng với gRPC.

Nó giúp quy định rõ:

* Tên field.
* Kiểu dữ liệu.
* Mã số field.
* Cấu trúc request và response.

⸻

15. Contract Testing là gì?

Contract Testing là kiểm tra xem hai hệ thống có còn tuân thủ hợp đồng đã thống nhất không.

Ví dụ:

Order Service mong Balance Service trả:

{
  "success": true,
  "reservationId": "RSV-001"
}

Nhưng Balance Service sửa thành:

{
  "status": "SUCCESS",
  "id": "RSV-001"
}

Nếu không có contract test, Order Service có thể bị lỗi.

Contract test sẽ phát hiện:

Balance Service đã thay đổi response, không còn tương thích với Order Service.

⸻

16. Quy trình chi tiết từ yêu cầu đến sản phẩm hoàn chỉnh

⸻

Giai đoạn 1: Xác định vấn đề thật sự

Trước khi viết tài liệu hay code, cần trả lời:

* Người dùng đang gặp vấn đề gì?
* Chức năng này giúp ích thế nào?
* Ai sẽ sử dụng?
* Kết quả nào chứng minh chức năng thành công?
* Phạm vi lần đầu là gì?
* Việc nào chưa làm trong giai đoạn này?

Ví dụ yêu cầu mơ hồ:

Làm hệ thống đặt lệnh chứng khoán.

Cần làm rõ thành:

Người dùng:
Khách hàng cá nhân.
Mục tiêu:
Cho phép khách hàng đặt lệnh mua cổ phiếu.
Phạm vi đầu tiên:
- Chỉ lệnh mua.
- Chỉ tài khoản tiền mặt.
- Chỉ một thị trường.
- Chưa hỗ trợ margin.
- Chưa hỗ trợ lệnh điều kiện.
Tiêu chí thành công:
- Lệnh hợp lệ được tiếp nhận.
- Lệnh không hợp lệ bị từ chối đúng lý do.
- Không được giữ tiền sai.
- Không được tạo trùng lệnh.

AI có thể giúp:

* Đặt câu hỏi còn thiếu.
* Phát hiện điểm mâu thuẫn.
* Đưa ra các trường hợp business chưa nghĩ đến.
* Tạo danh sách giả định.

Nhưng người phụ trách sản phẩm phải chốt quyết định.

⸻

Giai đoạn 2: BA làm rõ nghiệp vụ

BA không nên chỉ viết một luồng thành công.

BA cần mô tả các nhóm tình huống:

Luồng thành công

Ví dụ:

Người dùng nhập lệnh
→ Hệ thống kiểm tra
→ Tài khoản đủ tiền
→ Hệ thống giữ tiền
→ Tạo lệnh
→ Gửi lệnh đi

Luồng thay thế

Ví dụ:

Người dùng sửa giá trước khi lệnh được gửi.

Luồng lỗi

Ví dụ:

* Không đủ tiền.
* Mã chứng khoán không tồn tại.
* Thị trường đang đóng.
* Tài khoản bị khóa.
* Balance Service bị timeout.
* Người dùng gửi trùng yêu cầu.

Trường hợp biên

Trường hợp biên, hay edge case, là tình huống nằm sát giới hạn.

Ví dụ:

* Tài khoản có đúng bằng số tiền cần mua.
* Khối lượng bằng khối lượng tối thiểu.
* Giá bằng giá trần.
* Lệnh đến đúng lúc thị trường vừa đóng.
* Hai yêu cầu cùng giữ một khoản tiền.

⸻

17. Decision Table là gì?

Decision Table là bảng quyết định.

Nó giúp mô tả nhiều điều kiện kết hợp với nhau.

Ví dụ:

Tài khoản hoạt động	Thị trường mở	Đủ tiền	Kết quả
Có	Có	Có	Chấp nhận lệnh
Có	Có	Không	Từ chối vì thiếu tiền
Có	Không	Có	Từ chối vì thị trường đóng
Không	Có	Có	Từ chối vì tài khoản bị khóa

AI có thể sinh decision table từ tài liệu BA.

QA có thể dùng bảng này để tạo test case.

DEV có thể dùng để kiểm tra logic có bỏ sót nhánh nào không.

⸻

18. State Machine là gì?

State Machine là mô hình trạng thái.

Nó mô tả một đối tượng có thể ở trạng thái nào và được chuyển sang trạng thái nào.

Ví dụ lệnh chứng khoán:

stateDiagram-v2
    [*] --> Created
    Created --> Validating
    Validating --> Rejected: Dữ liệu không hợp lệ
    Validating --> Accepted: Dữ liệu hợp lệ
    Accepted --> Routed: Đã gửi ra ngoài
    Routed --> PartiallyFilled: Khớp một phần
    Routed --> Filled: Khớp toàn bộ
    Routed --> Cancelled: Đã hủy
    PartiallyFilled --> Filled: Khớp phần còn lại
    PartiallyFilled --> Cancelled: Hủy phần còn lại

Giải thích:

* Created: lệnh vừa được tạo.
* Validating: đang kiểm tra.
* Rejected: bị từ chối.
* Accepted: đã được chấp nhận.
* Routed: đã gửi đến hệ thống giao dịch.
* PartiallyFilled: khớp một phần.
* Filled: khớp toàn bộ.
* Cancelled: đã hủy.

State Machine giúp tránh các hành vi sai như:

Một lệnh đã khớp toàn bộ nhưng vẫn bị chuyển về trạng thái hủy.

⸻

19. Business Rule là gì?

Business Rule là quy tắc nghiệp vụ.

Ví dụ:

BR-ORDER-001:
Chỉ tài khoản ACTIVE mới được phép đặt lệnh.
BR-RISK-007:
Sức mua khả dụng phải lớn hơn hoặc bằng số tiền cần giữ.
BR-ORDER-008:
Một idempotency key chỉ được tạo tối đa một lệnh.

Nên gắn mỗi rule với một mã cố định.

Ví dụ:

BR-RISK-007

Mã này được dùng để liên kết:

* Tài liệu.
* Test.
* Code.
* Task.
* Lỗi production.
* Báo cáo thay đổi.

⸻

20. Invariant là gì?

Invariant là điều kiện bắt buộc phải luôn đúng.

Ví dụ trong hệ thống tiền:

Số dư khả dụng không được âm.
Số tiền giữ không được âm.
Một khoản tiền không được giữ hai lần.
Tổng số dư phải khớp với các thành phần bên trong.

Ví dụ:

Tổng số dư =
Số dư khả dụng
+ Số tiền đang giữ
+ Số tiền đang chờ xử lý

Invariant đặc biệt quan trọng với:

* Tiền.
* Ledger.
* Order.
* Position.
* Tài sản.
* Thanh toán.

AI có thể sinh nhiều test từ invariant, nhưng con người phải xác nhận invariant đúng về nghiệp vụ.

⸻

21. Idempotency là gì?

Idempotency nghĩa là:

Gửi cùng một yêu cầu nhiều lần nhưng hệ thống chỉ thực hiện hành động chính một lần.

Ví dụ người dùng nhấn nút “Đặt lệnh” hai lần vì mạng chậm.

Không có idempotency:

Lần 1 → tạo ORDER-001
Lần 2 → tạo ORDER-002

Kết quả là người dùng vô tình đặt hai lệnh.

Có idempotency:

Lần 1 với key ABC → tạo ORDER-001
Lần 2 với key ABC → trả lại ORDER-001

Không tạo thêm lệnh mới.

⸻

22. Timeout và Retry là gì?

Timeout

Timeout là khoảng thời gian tối đa chờ một hệ thống khác trả lời.

Ví dụ:

Order Service chỉ chờ Balance Service tối đa 3 giây.

Nếu quá 3 giây:

Balance Service timeout

Retry

Retry nghĩa là thử gọi lại.

Ví dụ:

Lần 1 thất bại
→ chờ 200ms
→ thử lần 2
→ vẫn thất bại
→ chờ 500ms
→ thử lần 3

Retry phải đi cùng idempotency.

Nếu không, retry có thể vô tình tạo dữ liệu trùng.

⸻

Giai đoạn 3: Viết đặc tả có cấu trúc

Mỗi chức năng nên có một thư mục riêng.

Ví dụ:

specs/
└── ORD-001-place-order/
    ├── requirements.md
    ├── business-rules.md
    ├── examples.feature
    ├── decision-table.md
    ├── state-machine.md
    ├── non-functional-requirements.md
    ├── assumptions.md
    └── trace.yaml

Giải thích:

* requirements.md: yêu cầu chức năng.
* business-rules.md: quy tắc nghiệp vụ.
* examples.feature: các ví dụ Given/When/Then.
* decision-table.md: bảng quyết định.
* state-machine.md: trạng thái.
* non-functional-requirements.md: yêu cầu về tốc độ, bảo mật, ổn định.
* assumptions.md: những giả định chưa chắc chắn.
* trace.yaml: file liên kết spec với task, code và test.

⸻

23. Functional và Non-functional Requirement

Functional Requirement

Là yêu cầu chức năng.

Ví dụ:

* Người dùng đặt được lệnh.
* Người dùng hủy được lệnh.
* Hệ thống kiểm tra số dư.
* Hệ thống trả mã lỗi.

Non-functional Requirement

Thường viết tắt là NFR.

Đây là yêu cầu về chất lượng hoạt động.

Ví dụ:

* API phải phản hồi dưới 200ms trong 95% request.
* Hệ thống chịu được 5.000 request mỗi giây.
* Không được mất lệnh.
* Dữ liệu phải được mã hóa.
* Khi một node chết, hệ thống vẫn hoạt động.
* Mọi thay đổi số dư phải có lịch sử audit.

Có thể hiểu:

Functional Requirement:
Hệ thống làm được gì?
Non-functional Requirement:
Hệ thống phải làm việc đó nhanh, an toàn và ổn định đến mức nào?

⸻

24. Khi nào một spec được coi là đủ rõ?

Một spec chỉ nên được đưa sang DEV khi:

* Mục tiêu rõ.
* Phạm vi rõ.
* Có business rule.
* Có ví dụ thành công.
* Có ví dụ thất bại.
* Có trường hợp biên.
* Có input và output.
* Có mã lỗi.
* Có các câu hỏi chưa giải quyết được ghi rõ.
* Có người chịu trách nhiệm phê duyệt.
* Có NFR cần thiết.

Không nên dùng những câu như:

Hệ thống phải nhanh.

Nên viết:

95% request đặt lệnh phải phản hồi trong vòng 200ms khi hệ thống xử lý 1.000 request mỗi giây.

⸻

Giai đoạn 4: Thiết kế domain và kiến trúc

⸻

25. Domain là gì?

Domain nghĩa là lĩnh vực nghiệp vụ mà phần mềm đang giải quyết.

Ví dụ trong chứng khoán:

* Quản lý khách hàng.
* Quản lý tài khoản.
* Đặt lệnh.
* Quản lý tiền.
* Quản lý vị thế.
* Quản lý phí.
* Quản lý settlement.
* Báo cáo.
* Quản lý rủi ro.

Mỗi domain có:

* Thuật ngữ riêng.
* Quy tắc riêng.
* Dữ liệu riêng.
* Người phụ trách riêng.

⸻

26. Bounded Context là gì?

Bounded Context có thể hiểu là:

Một vùng nghiệp vụ có ranh giới rõ, bên trong sử dụng cùng một bộ khái niệm và quy tắc.

Ví dụ từ “Account” có thể mang nghĩa khác nhau:

Trong Customer Domain:

Account = tài khoản đăng nhập

Trong Trading Domain:

Account = tài khoản giao dịch

Trong Accounting Domain:

Account = tài khoản kế toán

Nếu không chia ranh giới rõ, các team có thể dùng cùng một từ nhưng hiểu khác nhau.

Bounded Context giúp nói rõ:

Trong khu vực này, từ Account có nghĩa chính xác là gì?

⸻

27. Service là gì?

Service là một chương trình có trách nhiệm tương đối độc lập.

Ví dụ:

* Order Service quản lý lệnh.
* Balance Service quản lý số dư và giữ tiền.
* Risk Service kiểm tra rủi ro.
* Notification Service gửi thông báo.

Một service thường:

* Có code riêng.
* Có dữ liệu riêng hoặc quyền sở hữu dữ liệu rõ.
* Có API hoặc event riêng.
* Có thể được triển khai độc lập.

Nhưng không nên chia quá nhiều service từ đầu.

AI viết code nhanh hơn không có nghĩa là vận hành hàng trăm service sẽ dễ hơn.

Mỗi service phát sinh thêm:

* Triển khai.
* Monitoring.
* Log.
* Cảnh báo.
* Bảo mật.
* Network.
* Timeout.
* Retry.
* Version.
* Quản lý lỗi.

⸻

28. Module, Package, Namespace, Class và Function

Cách hiểu đơn giản:

Hệ thống
└── Service
    └── Module hoặc Package
        └── Class hoặc File
            └── Function hoặc Method

Service

Một chương trình hoặc thành phần có thể chạy độc lập.

Ví dụ:

order-service

Module

Một nhóm code có cùng trách nhiệm.

Ví dụ bên trong Order Service:

validation
risk-checking
order-lifecycle
exchange-routing

Package

Một cách nhóm code.

Trong Java có thể là:

com.company.order.validation

Namespace

Namespace là vùng tên giúp tránh trùng tên.

Ví dụ có hai class cùng tên Account:

Customer.Account
Trading.Account

Hai class đều tên Account nhưng thuộc namespace khác nhau.

Namespace chủ yếu là cơ chế tổ chức tên, không nhất thiết là một module nghiệp vụ độc lập.

Class

Class là khuôn mẫu chứa dữ liệu và hành vi.

Ví dụ:

Order
BalanceReservation
BuyingPowerCalculator

File

File là tệp code vật lý.

Một file có thể chứa:

* Một class.
* Nhiều class.
* Nhiều function.

Tùy ngôn ngữ và quy ước.

Function

Function là một khối code thực hiện một công việc.

Ví dụ:

calculateRequiredAmount()
validateOrder()
reserveBalance()

Method

Method là function thuộc về một class.

Ví dụ:

order.cancel()

cancel() là method của class Order.

⸻

29. Có nên để AI thiết kế đến từng function trước không?

Không nên làm như vậy cho toàn bộ hệ thống.

Nếu thiết kế trước đến từng class, file và function, có thể xảy ra:

* Tài liệu quá lớn.
* Code thay đổi làm tài liệu lỗi thời.
* Mất nhiều thời gian duy trì tài liệu.
* AI phải đọc quá nhiều context.
* Thiết kế trở nên cứng nhắc.
* Team mất khả năng linh hoạt.

Nên đặc tả kỹ ở các ranh giới quan trọng:

* Business rule.
* Module.
* API.
* Event.
* Dữ liệu.
* Input/output.
* Invariant.
* Error handling.
* Security.
* Performance.
* Task.

Chỉ thiết kế tới mức function khi phần đó:

* Có công thức tài chính phức tạp.
* Có xử lý đồng thời.
* Có yêu cầu performance cao.
* Có logic bảo mật.
* Có thuật toán khó.
* Có nguy cơ mất tiền hoặc sai dữ liệu.

⸻

30. Concurrency là gì?

Concurrency nghĩa là nhiều việc xảy ra gần như cùng lúc.

Ví dụ tài khoản có 1.000 USD.

Hai request đặt lệnh đến cùng lúc:

Request A cần 800 USD
Request B cần 800 USD

Nếu cả hai cùng đọc số dư là 1.000 USD trước khi số dư được cập nhật:

A thấy đủ tiền
B cũng thấy đủ tiền

Hệ thống có thể giữ tổng cộng 1.600 USD dù tài khoản chỉ có 1.000 USD.

Đây là lỗi concurrency.

Cần có cơ chế như:

* Lock.
* Transaction.
* Compare-and-set.
* Version checking.
* Serial processing.

AI model mạnh nên phân tích các tình huống này, vì đây là phần dễ gây lỗi nghiêm trọng.

⸻

31. Transaction là gì?

Transaction là một nhóm thao tác phải được xem như một đơn vị hoàn chỉnh.

Ví dụ:

1. Giữ tiền
2. Tạo lệnh

Nếu giữ tiền thành công nhưng tạo lệnh thất bại, hệ thống phải:

* Hoàn lại tiền.
* Hoặc tiếp tục hoàn tất việc tạo lệnh.
* Hoặc đánh dấu để hệ thống xử lý bù.

Không được để tiền bị giữ mãi nhưng không có lệnh.

⸻

32. Consistency là gì?

Consistency nghĩa là tính nhất quán của dữ liệu.

Ví dụ:

* Order Service nói lệnh đã hủy.
* Balance Service vẫn giữ tiền.
* Reporting Service nói lệnh đang hoạt động.

Ba hệ thống đang không nhất quán.

Trong hệ thống phân tán, đôi khi dữ liệu không thể đồng bộ ngay lập tức.

Do đó phải xác định:

* Có cần đồng bộ ngay không?
* Có thể chậm vài giây không?
* Khi lệch dữ liệu thì sửa bằng cách nào?
* Hệ thống nào là nguồn dữ liệu chính?

⸻

33. Kiến trúc hệ thống nên có những sơ đồ gì?

Không cần vẽ mọi thứ.

Nên có các loại sơ đồ sau:

Sơ đồ toàn cảnh

Cho biết:

* Người dùng là ai.
* Hệ thống tương tác với bên nào.
* Hệ thống nằm ở đâu.

Sơ đồ các service

Cho biết:

* Có những service nào.
* Service nào sở hữu dữ liệu nào.
* Service nào gọi service nào.

Sequence Diagram

Mô tả thứ tự gọi trong một flow.

Ví dụ:

sequenceDiagram
    participant U as Người dùng
    participant O as Order Service
    participant R as Risk Service
    participant B as Balance Service
    participant E as Exchange Gateway
    U->>O: Đặt lệnh
    O->>R: Kiểm tra rủi ro
    R-->>O: Hợp lệ
    O->>B: Giữ tiền
    B-->>O: Giữ tiền thành công
    O->>E: Gửi lệnh
    E-->>O: Đã tiếp nhận
    O-->>U: Trả mã lệnh

State Diagram

Mô tả trạng thái của đối tượng.

Data Flow

Mô tả dữ liệu đi qua đâu và được biến đổi thế nào.

⸻

34. ADR là gì?

ADR là viết tắt của Architecture Decision Record.

Có thể hiểu là:

Biên bản ghi lại một quyết định kiến trúc quan trọng.

Ví dụ:

ADR-023: Sử dụng Kafka để phát sự kiện OrderAccepted

ADR nên ghi:

* Vấn đề cần giải quyết.
* Các phương án đã cân nhắc.
* Phương án được chọn.
* Lý do chọn.
* Nhược điểm.
* Rủi ro.
* Hậu quả về sau.

Ví dụ:

Phương án 1: Order Service gọi trực tiếp Reporting Service.
Phương án 2: Order Service phát event qua Kafka.
Chọn phương án 2 vì:
- Order Service không phải chờ Reporting.
- Có thể thêm consumer mới.
- Giảm phụ thuộc trực tiếp.
Nhược điểm:
- Dữ liệu báo cáo có thể chậm vài giây.
- Phải xử lý event trùng.
- Hệ thống phức tạp hơn.

AI có thể viết ADR nháp.

Tech Lead hoặc Architect phải review và phê duyệt.

⸻

Giai đoạn 5: Thiết kế contract và test trước khi code

Ví dụ các service giao tiếp:

flowchart LR
    UI["Ứng dụng người dùng"]
    OMS["Order Service"]
    RISK["Risk Service"]
    BAL["Balance Service"]
    BUS["Kafka/Event Bus"]
    REP["Reporting Service"]
    UI -->|"API đặt lệnh"| OMS
    OMS -->|"API kiểm tra rủi ro"| RISK
    OMS -->|"API giữ tiền"| BAL
    OMS -->|"Phát event OrderAccepted"| BUS
    BUS --> REP

Trước khi code, cần thống nhất:

* Request.
* Response.
* Error code.
* Timeout.
* Retry.
* Idempotency.
* Authentication.
* Authorization.
* Phiên bản.
* Cách nâng cấp contract.
* Xử lý event trùng.
* Xử lý event đến sai thứ tự.

⸻

35. Authentication và Authorization

Authentication

Là xác định:

Người gọi là ai?

Ví dụ:

* Đăng nhập bằng username/password.
* Token.
* Chứng thư.
* API key.

Authorization

Là xác định:

Người đó được phép làm gì?

Ví dụ:

* Khách hàng được đặt lệnh trên tài khoản của mình.
* Advisor được đặt lệnh cho khách hàng được phân công.
* Nhân viên support chỉ được xem, không được sửa.
* Admin được khóa tài khoản.

Có thể nhớ:

Authentication = Bạn là ai?
Authorization = Bạn được làm gì?

⸻

36. Mock, Stub và hệ thống giả lập

Khi Order Service cần gọi Balance Service nhưng Balance Service chưa làm xong, team cần giả lập.

Mock

Mock là đối tượng giả dùng trong test.

Ví dụ:

Khi gọi reserveBalance(1000)
→ giả lập trả về thành công

Mock rất nhanh nhưng có nhược điểm:

Mock có thể không giống hệ thống thật.

Stub

Stub là một hệ thống hoặc thành phần giả đơn giản trả về dữ liệu định trước.

Ví dụ:

POST /reserve
→ luôn trả success

Contract-verified Stub

Đây là stub được kiểm tra theo contract thật.

Nó đáng tin cậy hơn vì response phải phù hợp với OpenAPI hoặc contract.

Ephemeral Dependency

Ephemeral nghĩa là tạm thời.

Ví dụ khi chạy test, hệ thống tự tạo:

* Một PostgreSQL tạm.
* Một Kafka tạm.
* Một Redis tạm.

Test chạy xong thì xóa.

Điều này giúp test gần giống môi trường thật hơn.

Full Environment

Là môi trường có gần như đầy đủ các service.

Nó phù hợp cho:

* End-to-end test.
* Release test.
* Kiểm tra flow tổng thể.

Nhưng nó chậm và khó duy trì hơn.

⸻

Giai đoạn 6: Chia hệ thống thành task cho AI Agent

Task là một đơn vị công việc.

Không nên giao cho AI:

Viết toàn bộ Order Service.

Nên chia nhỏ:

T1: Định nghĩa API đặt lệnh
T2: Xây domain model của Order
T3: Viết logic validation
T4: Viết adapter gọi Balance Service
T5: Viết logic điều phối đặt lệnh
T6: Phát event OrderAccepted
T7: Viết component test
T8: Viết contract test
T9: Viết acceptance test

Quan hệ phụ thuộc:

flowchart TD
    A["T1: Contract API"]
    B["T2: Domain model"]
    C["T3: Validation"]
    D["T4: Balance adapter"]
    E["T5: Order orchestration"]
    F["T6: Publish event"]
    G["T7: Component test"]
    H["T8: Contract test"]
    I["T9: Acceptance test"]
    A --> D
    A --> E
    B --> C
    B --> E
    C --> E
    D --> E
    E --> F
    E --> G
    A --> H
    G --> I
    H --> I

Đây gọi là Task Graph, nghĩa là sơ đồ cho biết task nào phụ thuộc task nào.

⸻

37. Một gói công việc cho AI cần có gì?

Một task dành cho AI Agent nên có:

1. Mục tiêu
2. Phạm vi được phép thay đổi
3. Phần không được làm
4. Tài liệu cần đọc
5. Input
6. Output
7. Business rule
8. Invariant
9. Các trường hợp lỗi
10. Test bắt buộc
11. Command để chạy test
12. Điều kiện hoàn thành

Ví dụ:

# TASK ORD-001-T05
## Mục tiêu
Viết logic điều phối đặt lệnh mua.
## Phạm vi được sửa
- services/order/src/application/place-order/
- services/order/test/component/place-order/
## Không thuộc phạm vi
- Margin
- UI
- Logic gửi lệnh ra sở giao dịch
## Input
PlaceOrderCommand
## Output thành công
AcceptedOrder
## Output thất bại
Lỗi nghiệp vụ có mã rõ ràng
## Quy tắc bắt buộc
- Phải giữ tiền trước khi xác nhận lệnh.
- Idempotency key trùng phải trả lại kết quả cũ.
- Giữ tiền thất bại thì không được tạo lệnh.
## Trường hợp lỗi
- Không đủ tiền.
- Balance Service timeout.
- Request trùng.
- Hai request đồng thời.
## Test bắt buộc
- Unit test.
- Component test.
- Idempotency test.
- Concurrency test.
## Điều kiện hoàn thành
- Tất cả test pass.
- Không làm hỏng contract.
- Không phát sinh lỗi bảo mật nghiêm trọng.
- Tài liệu liên quan được cập nhật.

Nếu nhận được task như vậy, model phổ thông có thể code khá tốt.

⸻

38. AI Agent là gì?

AI Agent là AI không chỉ trả lời câu hỏi mà có thể thực hiện chuỗi hành động như:

* Đọc repository.
* Tìm file liên quan.
* Viết code.
* Tạo file mới.
* Chạy test.
* Đọc lỗi.
* Sửa code.
* Tạo commit hoặc pull request.

Một Agent tốt cần được giới hạn:

* Được sửa file nào.
* Không được sửa file nào.
* Được chạy command nào.
* Có được dùng Internet không.
* Có được truy cập secret không.
* Khi nào phải dừng và hỏi người.

⸻

39. Nên phân chia model mạnh và model phổ thông thế nào?

Không nên chỉ dựa vào giá model.

Nên dựa trên hai yếu tố:

Độ mơ hồ

Công việc có rõ hay không?

Ví dụ mơ hồ:

Thiết kế hệ thống order chịu tải cao.

Ví dụ rõ:

Viết hàm validatePrice theo rule BR-ORDER-012.

Blast Radius

Blast Radius có thể hiểu là:

Nếu làm sai thì phạm vi hậu quả lớn đến đâu?

Ví dụ blast radius thấp:

* Đổi tên biến.
* Sửa format log.
* Viết thêm unit test.

Blast radius cao:

* Sửa logic số dư.
* Sửa ledger.
* Sửa permission.
* Sửa database migration.
* Sửa quy tắc thanh toán.
* Sửa cách tính phí.

Bảng phân chia:

Độ mơ hồ	Hậu quả nếu sai	Cách xử lý
Thấp	Thấp	Model phổ thông làm
Cao	Thấp	Model mạnh lập kế hoạch, model phổ thông code
Thấp	Cao	Có thể dùng model phổ thông code nhưng phải review mạnh
Cao	Cao	Model mạnh và senior engineer cùng thiết kế

⸻

40. Những khu vực luôn phải kiểm soát chặt

* Tiền.
* Ledger.
* Order.
* Position.
* Authentication.
* Authorization.
* Mã hóa.
* Secret.
* Database migration.
* Concurrency.
* Settlement.
* Báo cáo pháp lý.
* Hạ tầng production.

Không nên để Agent tự động merge hoặc deploy các thay đổi này mà không có con người review.

⸻

41. Có thể chia AI thành các vai trò nào?

Requirement Critic Agent

Đọc yêu cầu và tìm:

* Mâu thuẫn.
* Điểm mơ hồ.
* Trường hợp thiếu.
* Giả định chưa được xác nhận.

Architecture Agent

Đề xuất:

* Cách chia service.
* Cách giao tiếp.
* Cách lưu dữ liệu.
* Các phương án và trade-off.

Trade-off nghĩa là sự đánh đổi.

Ví dụ:

Dùng microservice tăng khả năng triển khai độc lập nhưng làm hệ thống vận hành phức tạp hơn.

Implementation Planner

Chia thiết kế thành task nhỏ.

Coding Agent

Viết code theo task.

Test Adversary Agent

Adversary có thể hiểu là người cố tình phá hệ thống.

Agent này tìm:

* Input xấu.
* Trường hợp biên.
* Lỗi đồng thời.
* Lỗi retry.
* Lỗi khi dependency chết.

Security Reviewer

Kiểm tra:

* Lỗ hổng.
* Permission.
* Token.
* Secret.
* SQL injection.
* Lộ dữ liệu.

Contract Compatibility Reviewer

Kiểm tra contract mới có làm hỏng hệ thống cũ không.

Documentation Sync Agent

Kiểm tra code và tài liệu có bị lệch nhau không.

Release Readiness Agent

Kiểm tra bản release đã đủ điều kiện triển khai chưa.

Không nhất thiết phải dùng tám model khác nhau.

Có thể dùng một model nhưng với tám prompt và quyền khác nhau.

⸻

Giai đoạn 7: Viết code và test song song

Developer và AI Agent có thể cùng thực hiện:

1. Đọc spec.
2. Đọc business rule.
3. Đọc contract.
4. Viết test.
5. Viết code.
6. Chạy test.
7. Sửa lỗi.
8. Review.
9. Cập nhật tài liệu.
10. Tạo pull request.

Pull Request, thường viết là PR, là yêu cầu đưa một thay đổi code vào nhánh chính.

PR nên chứa:

* Mô tả thay đổi.
* Spec liên quan.
* Business rule liên quan.
* Test đã chạy.
* Rủi ro.
* Screenshot hoặc log nếu cần.
* Cách rollback.

⸻

42. Các tầng test cần có

flowchart BT
    A["Static Check<br/>Kiểm tra code không cần chạy"]
    B["Unit Test<br/>Test function hoặc class"]
    C["Component Test<br/>Test một service"]
    D["Contract Test<br/>Test giao tiếp giữa service"]
    E["Integration Test<br/>Test với DB, Kafka, Redis thật"]
    F["Acceptance Test<br/>Test nghiệp vụ"]
    G["E2E Test<br/>Test toàn bộ hành trình người dùng"]
    H["Performance và Security Test"]
    I["Production Verification<br/>Kiểm tra sau triển khai"]
    A --> B --> C --> D --> E --> F --> G --> H --> I

⸻

43. Static Check là gì?

Đây là kiểm tra code mà không cần chạy toàn bộ chương trình.

Ví dụ:

* Code có compile không?
* Kiểu dữ liệu có đúng không?
* Có lỗi cú pháp không?
* Có vi phạm coding convention không?
* Có dependency nguy hiểm không?
* Có secret trong code không?

Các loại phổ biến:

* Compile.
* Type check.
* Lint.
* Dependency scan.
* Secret scan.

⸻

44. Unit Test là gì?

Unit test kiểm tra một đơn vị nhỏ.

Ví dụ:

calculateRequiredAmount()
validatePrice()
isAccountActive()

Ưu điểm:

* Chạy nhanh.
* Dễ tìm lỗi.
* Phù hợp chạy liên tục.

Nhược điểm:

* Không chứng minh được các thành phần tích hợp đúng với nhau.

⸻

45. Property-based Test là gì?

Thay vì chỉ test một vài ví dụ, property-based test sinh rất nhiều input khác nhau để kiểm tra một nguyên tắc luôn đúng.

Ví dụ:

Với mọi giá >= 0
Và mọi khối lượng >= 0
Số tiền cần giữ không được âm.

Hệ thống test có thể tự sinh:

* Giá 0.
* Giá rất lớn.
* Khối lượng lẻ.
* Giá có nhiều số thập phân.
* Các giá trị sát giới hạn.

Property-based test đặc biệt phù hợp cho:

* Công thức.
* Tiền.
* Risk.
* Ledger.
* Thuật toán.

⸻

46. Model-based Test là gì?

Model-based test dựa trên một mô hình trạng thái.

Ví dụ model của Order quy định:

Created → Accepted
Accepted → Routed
Routed → Filled

Test sẽ tự sinh nhiều chuỗi hành động và kiểm tra:

* Có chuyển từ Filled về Created không?
* Có cancel sau khi Filled không?
* Có fill một lệnh đã Rejected không?

⸻

47. Component Test là gì?

Component test kiểm tra một service như một khối tương đối hoàn chỉnh.

Ví dụ test Order Service:

Gọi API đặt lệnh
→ Order Service xử lý
→ Gọi stub Balance
→ Ghi database
→ Trả response

Component test rộng hơn unit test nhưng vẫn không chạy toàn bộ hệ thống.

⸻

48. Integration Test là gì?

Integration test kiểm tra nhiều thành phần thật hoạt động cùng nhau.

Ví dụ:

* Service kết nối PostgreSQL thật.
* Service phát event Kafka thật.
* Service lưu Redis thật.
* Service gọi một dependency chạy trong container.

Integration test phát hiện những lỗi mà mock không thấy được:

* Sai câu SQL.
* Sai cấu hình Kafka.
* Sai transaction.
* Sai serialization.
* Sai timezone.
* Sai encoding.

⸻

49. Acceptance Test là gì?

Acceptance test kiểm tra yêu cầu nghiệp vụ hoàn chỉnh.

Ví dụ:

Khi tài khoản không đủ tiền
→ lệnh bị từ chối
→ không tạo bản ghi accepted order
→ không giữ tiền
→ trả đúng mã lỗi

Acceptance test nên gắn với business rule.

Ví dụ:

AT-ORDER-014 kiểm tra BR-RISK-007

⸻

50. E2E Test là gì?

E2E là viết tắt của End-to-End.

Nghĩa là test từ đầu đến cuối.

Ví dụ:

Người dùng đăng nhập
→ mở màn hình đặt lệnh
→ nhập lệnh
→ API Gateway
→ Order Service
→ Risk Service
→ Balance Service
→ Exchange Gateway
→ nhận trạng thái
→ hiển thị lại cho người dùng

E2E có giá trị cao nhưng:

* Chạy chậm.
* Khó setup.
* Dễ thất bại do môi trường.
* Khó tìm chính xác lỗi nằm ở đâu.

Do đó chỉ nên có số lượng E2E vừa phải, tập trung vào flow quan trọng.

⸻

51. Load, Stress, Spike và Soak Test

Load Test

Kiểm tra hệ thống dưới tải dự kiến.

Ví dụ:

Hệ thống có xử lý ổn định 2.000 lệnh mỗi giây không?

Stress Test

Tăng tải cho tới khi hệ thống không chịu được nữa.

Mục tiêu:

* Điểm gãy ở đâu?
* Hệ thống gãy như thế nào?
* Có phục hồi được không?

Spike Test

Tải tăng đột ngột.

Ví dụ:

100 request/giây
→ tăng lên 10.000 request/giây trong 5 giây

Soak Test

Cho hệ thống chạy tải lâu, có thể nhiều giờ hoặc nhiều ngày.

Mục tiêu tìm:

* Memory leak.
* Connection leak.
* Disk tăng dần.
* Queue tích tụ.
* Hiệu năng giảm theo thời gian.

Capacity Test

Tìm công suất tối đa.

Ví dụ:

Một instance Order Service xử lý tối đa bao nhiêu lệnh mỗi giây?

Resilience Test

Kiểm tra khả năng chịu lỗi.

Ví dụ:

* Kill một node.
* Làm database chậm.
* Làm Kafka ngừng hoạt động.
* Cho Balance Service timeout.
* Làm network mất kết nối.

⸻

52. Mutation Testing là gì?

Mutation testing kiểm tra chất lượng của test.

Công cụ sẽ cố tình sửa code thành code sai.

Ví dụ code đúng:

availableBalance >= requiredAmount

Công cụ sửa thành:

availableBalance > requiredAmount

Nếu test vẫn pass, nghĩa là test chưa đủ mạnh.

Nếu test fail, nghĩa là test phát hiện được lỗi.

Mutation testing trả lời:

Bộ test của chúng ta có thực sự bắt được lỗi hay chỉ chạy cho có?

⸻

53. Vì sao không nên để cùng một AI viết code và tự xác nhận?

Giả sử AI hiểu sai rule:

Đủ tiền khi số dư lớn hơn số tiền cần mua.

Trong khi rule đúng là:

Số dư lớn hơn hoặc bằng số tiền cần mua.

Nếu cùng AI:

* Viết code sai.
* Viết test theo cách hiểu sai.
* Review lại cũng theo cách hiểu sai.

Kết quả:

Code pass toàn bộ test nhưng nghiệp vụ vẫn sai.

Cách giảm rủi ro:

* Acceptance test do BA và QA sở hữu.
* Test Agent độc lập với Coding Agent.
* Test Agent đọc spec trước, không đọc code ở vòng đầu.
* Dùng property-based test.
* Dùng mutation test.
* Human review phần nghiệp vụ quan trọng.
* Dùng reference model cho công thức tài chính.

⸻

54. BA, DEV và QA phối hợp thế nào?

sequenceDiagram
    participant BA as BA
    participant RAI as AI phân tích yêu cầu
    participant DEV as Developer
    participant QA as QA
    participant TAI as AI chuyên tìm lỗi
    participant CI as Hệ thống kiểm tra tự động
    BA->>RAI: Yêu cầu và business rule
    RAI-->>BA: Điểm mơ hồ, mâu thuẫn, trường hợp thiếu
    BA->>DEV: Spec đã phê duyệt
    BA->>QA: Rule và ví dụ đã phê duyệt
    QA->>TAI: Sinh test lỗi và trường hợp biên
    DEV->>CI: Code và developer test
    QA->>CI: Acceptance test
    CI-->>DEV: Báo test thất bại
    DEV->>CI: Sửa code
    CI-->>BA: Kết quả nghiệm thu

Phân chia quyền sở hữu:

Loại test	Người chịu trách nhiệm chính
Acceptance test	BA, Product và QA
Test trường hợp lỗi	QA
Unit test	DEV
Component test	DEV
Contract test	Team cung cấp và sử dụng API
Performance test	DEV, QA Performance, SRE
Security test	Security và DEV
Production verification	DEV, Platform, SRE

⸻

55. CI là gì?

CI là viết tắt của Continuous Integration.

Có thể hiểu là:

Mỗi khi code thay đổi, hệ thống tự động kiểm tra thay đổi đó.

Ví dụ khi developer tạo PR, CI tự chạy:

Compile
→ Lint
→ Unit test
→ Component test
→ Contract test
→ Security scan
→ Build image

Nếu một bước thất bại, PR không được merge.

⸻

56. CD là gì?

CD có thể mang hai nghĩa:

Continuous Delivery

Code luôn ở trạng thái sẵn sàng để triển khai, nhưng có thể cần con người bấm xác nhận.

Continuous Deployment

Code tự động được triển khai khi toàn bộ điều kiện đạt.

Với hệ thống tài chính lớn, thường nên thận trọng:

* Môi trường DEV có thể tự động.
* UAT có thể bán tự động.
* Production cần approval theo mức rủi ro.

⸻

57. DevSecOps là gì?

DevSecOps là kết hợp:

Development
+ Security
+ Operations

Ý nghĩa:

Bảo mật không phải việc kiểm tra ở cuối dự án. Nó phải có từ lúc viết yêu cầu, thiết kế, code, test và triển khai.

Ví dụ:

* BA ghi rõ dữ liệu nhạy cảm.
* Architect thiết kế phân quyền.
* DEV không hard-code secret.
* CI quét lỗ hổng.
* Production có audit log.
* Security test chạy tự động.

⸻

58. Nên chạy test vào thời điểm nào?

Khi Developer đang code

Chạy:

* Unit test.
* Một số component test liên quan.
* Static check.

Khi tạo Pull Request

Chạy:

* Compile.
* Lint.
* Unit test.
* Component test.
* Contract test.
* Integration test cần thiết.
* Security scan.

Khi merge vào nhánh chính

Chạy:

* Acceptance test.
* Test tương thích.
* Integration test rộng hơn.
* Build artifact chính thức.

Ban đêm

Chạy:

* Full integration test.
* Mutation test.
* Test dài.
* Scan dependency.

Trước release

Chạy:

* E2E.
* Performance test.
* Migration test.
* Rollback test.
* Security test.
* Resilience test.

Sau release

Chạy:

* Synthetic test.
* Theo dõi metric.
* Kiểm tra SLO.
* So sánh lỗi trước và sau release.

⸻

59. Synthetic Test là gì?

Synthetic test là các request giả được chạy định kỳ trên production.

Ví dụ mỗi phút hệ thống tự:

Đăng nhập bằng tài khoản test
→ gọi API xem số dư
→ tạo một lệnh test trong môi trường cho phép
→ kiểm tra phản hồi

Mục đích là phát hiện sớm:

* API chết.
* Login hỏng.
* Network lỗi.
* Dependency không hoạt động.

⸻

Giai đoạn 8: Quản lý nguồn dữ liệu đúng

⸻

60. Source of Truth là gì?

Source of Truth nghĩa là nơi được coi là thông tin chính thức.

Không nên có một tài liệu duy nhất chứa mọi thứ.

Nên có nguồn chính cho từng loại thông tin.

Nội dung	Nguồn chính
Mục tiêu sản phẩm	Product brief
Nghiệp vụ	Feature spec và business rule
Quyết định kiến trúc	ADR
API	OpenAPI
Event	AsyncAPI hoặc Protobuf
Cấu trúc database	Schema và migration
Cách hệ thống đang chạy	Code
Bằng chứng hệ thống đúng	Test
Thực tế production	Log, metric, trace, SLO

Ví dụ:

* Muốn biết API nhận field nào: đọc OpenAPI.
* Muốn biết vì sao dùng Kafka: đọc ADR.
* Muốn biết nghiệp vụ từ chối lệnh: đọc business rule.
* Muốn biết hệ thống hiện thực tế đang lỗi gì: đọc production metric và log.

⸻

61. Database Migration là gì?

Database migration là file mô tả thay đổi cấu trúc database.

Ví dụ:

Thêm cột idempotency_key vào bảng orders.

Migration có thể gồm:

ALTER TABLE orders
ADD COLUMN idempotency_key VARCHAR(100);

Migration rất rủi ro vì có thể:

* Khóa bảng.
* Làm hệ thống chậm.
* Làm mất dữ liệu.
* Không tương thích với code cũ.
* Khó rollback.

Do đó phải kiểm tra:

* Code cũ có chạy với database mới không?
* Code mới có chạy với database cũ không?
* Migration mất bao lâu?
* Có cần chạy theo từng bước không?
* Có thể khôi phục nếu lỗi không?

⸻

62. Backward Compatibility là gì?

Backward compatibility nghĩa là phiên bản mới vẫn tương thích với phiên bản cũ.

Ví dụ API cũ trả:

{
  "orderId": "ORD-001"
}

Phiên bản mới thêm field:

{
  "orderId": "ORD-001",
  "status": "ACCEPTED"
}

Thường vẫn tương thích vì client cũ có thể bỏ qua field mới.

Nhưng nếu đổi:

{
  "id": "ORD-001"
}

thì client cũ tìm orderId sẽ bị lỗi.

Đây là breaking change.

⸻

63. Breaking Change là gì?

Breaking change là thay đổi làm hệ thống đang dùng bị hỏng.

Ví dụ:

* Xóa field.
* Đổi tên field.
* Đổi kiểu dữ liệu.
* Đổi ý nghĩa field.
* Đổi error code.
* Bắt buộc thêm field mới.
* Đổi event structure không tương thích.

Breaking change thường cần:

* Tạo version mới.
* Cho hai version chạy song song.
* Migration.
* Thông báo consumer.
* Kế hoạch ngừng support version cũ.

⸻

Giai đoạn 9: Khi BA thay đổi logic

Đây là vấn đề rất quan trọng.

Ví dụ rule cũ:

BR-RISK-007 phiên bản 1:
Từ chối lệnh nếu số dư khả dụng nhỏ hơn tiền mua.

Rule mới:

BR-RISK-007 phiên bản 2:
Từ chối lệnh nếu số dư sau khi trừ phí dự kiến nhỏ hơn tiền mua.

Không nên sửa code ngay.

Nên đi theo quy trình:

flowchart TD
    A["1. Business gửi yêu cầu thay đổi"]
    B["2. Cập nhật business rule"]
    C["3. AI tìm vùng bị ảnh hưởng"]
    D["4. Con người review vùng ảnh hưởng"]
    E["5. Cập nhật acceptance test"]
    F["6. Cập nhật domain và contract"]
    G["7. Cập nhật thiết kế và ADR"]
    H["8. Chia task thay đổi"]
    I["9. Sửa code"]
    J["10. Chạy toàn bộ test liên quan"]
    K["11. Release an toàn"]
    L["12. Theo dõi production"]
    A --> B --> C --> D
    D --> E
    D --> F
    D --> G
    E --> H
    F --> H
    G --> H
    H --> I --> J --> K --> L

⸻

64. Impact Analysis là gì?

Impact Analysis nghĩa là phân tích vùng bị ảnh hưởng.

Khi một business rule thay đổi, AI cần tìm:

* Spec nào tham chiếu rule.
* Acceptance test nào kiểm tra rule.
* Service nào dùng rule.
* API nào liên quan.
* Event nào liên quan.
* Database field nào liên quan.
* Report nào dùng dữ liệu này.
* Dashboard nào cần cập nhật.
* Các version nào đang được support.
* Tài liệu nào phải sửa.

AI có thể đề xuất.

Con người phải xác nhận.

AI có thể tìm nhiều file có chữ BR-RISK-007, nhưng không chắc tất cả đều cần sửa.

⸻

65. Traceability là gì?

Traceability nghĩa là khả năng truy vết.

Ví dụ từ một business rule có thể tìm đến:

Business Rule
→ Acceptance Test
→ Technical Design
→ Task
→ Code
→ Unit Test
→ Pull Request
→ Release
→ Production Metric

Sơ đồ:

flowchart LR
    A["Mục tiêu kinh doanh"]
    B["Yêu cầu"]
    C["Business Rule"]
    D["Acceptance Test"]
    E["ADR và Contract"]
    F["Task"]
    G["Code"]
    H["Automated Test"]
    I["Deployment"]
    J["Production Evidence"]
    A --> B --> C --> D
    C --> E
    D --> F
    E --> F
    F --> G
    F --> H
    G --> I
    H --> I
    I --> J

Mỗi phần nên có mã định danh.

Ví dụ:

REQ-ORDER-001
BR-RISK-007
AT-ORDER-014
ADR-023
TASK-ORDER-056

AI sẽ dùng các mã này để tìm tác động thay đổi.

⸻

66. Production Evidence là gì?

Đây là bằng chứng từ hệ thống đang chạy thật.

Ví dụ:

* Tỷ lệ lệnh thành công.
* Tỷ lệ lệnh bị từ chối.
* Thời gian phản hồi.
* Số request lỗi.
* Số lần giữ tiền thất bại.
* Số event bị trùng.
* Số lệnh cần xử lý thủ công.

Test chỉ chứng minh:

Hệ thống đúng trong các tình huống đã được kiểm tra.

Production evidence cho biết:

Hệ thống thực tế có đang hoạt động đúng không?

⸻

67. Log, Metric và Trace

Log

Log là bản ghi chi tiết về việc đã xảy ra.

Ví dụ:

2026-07-25 10:00:01 Order request received
2026-07-25 10:00:01 Risk check passed
2026-07-25 10:00:02 Balance reservation succeeded

Metric

Metric là số liệu được tổng hợp.

Ví dụ:

request_count = 10.000
error_rate = 0,2%
p95_latency = 180ms

Trace

Trace theo dõi một request đi qua nhiều service.

Ví dụ:

Request đặt lệnh
→ API Gateway: 10ms
→ Order Service: 50ms
→ Risk Service: 30ms
→ Balance Service: 80ms
→ Tổng: 170ms

Trace giúp biết request chậm ở đâu.

⸻

68. Observability là gì?

Observability nghĩa là khả năng hiểu trạng thái bên trong hệ thống thông qua dữ liệu mà hệ thống phát ra.

Ba trụ cột phổ biến:

Logs
Metrics
Traces

Observability tốt giúp trả lời:

* Hệ thống đang lỗi ở đâu?
* Request nào bị lỗi?
* Service nào chậm?
* Lỗi bắt đầu từ khi nào?
* Release nào gây lỗi?
* Khách hàng nào bị ảnh hưởng?
* Có vi phạm business invariant không?

⸻

69. SLO là gì?

SLO là viết tắt của Service Level Objective.

Đây là mục tiêu chất lượng dịch vụ.

Ví dụ:

99,95% request đặt lệnh phải thành công trong một tháng.
95% request phải phản hồi dưới 200ms.

SLO giúp team quyết định:

* Hệ thống đang đủ ổn định chưa?
* Có nên tiếp tục thêm feature không?
* Có cần ưu tiên sửa độ ổn định không?

⸻

Giai đoạn 10: Release và triển khai an toàn

⸻

70. Release là gì?

Release là một phiên bản phần mềm được chuẩn bị để đưa ra sử dụng.

Release thường bao gồm:

* Code.
* Cấu hình.
* Database migration.
* Tài liệu.
* Release note.
* Test evidence.
* Kế hoạch triển khai.
* Kế hoạch khôi phục.

⸻

71. Rollback là gì?

Rollback nghĩa là quay lại phiên bản cũ khi phiên bản mới bị lỗi.

Ví dụ:

Version 3.2.0 bị lỗi
→ đưa hệ thống quay về 3.1.5

Không phải thay đổi nào cũng rollback dễ dàng.

Ví dụ database migration đã xóa cột hoặc chuyển đổi dữ liệu có thể không quay lại được.

Trong trường hợp đó cần forward recovery.

Forward recovery nghĩa là:

Không quay lại bản cũ mà tạo bản sửa lỗi mới và triển khai tiếp.

⸻

72. Canary Deployment là gì?

Canary Deployment nghĩa là chỉ triển khai bản mới cho một phần nhỏ hệ thống hoặc người dùng trước.

Ví dụ:

5% request dùng phiên bản mới
95% request vẫn dùng phiên bản cũ

Nếu metric tốt:

5% → 20% → 50% → 100%

Nếu lỗi:

Quay lại 0%

Canary giúp giảm phạm vi ảnh hưởng khi release lỗi.

⸻

73. Feature Flag là gì?

Feature Flag là công tắc bật hoặc tắt một chức năng mà không cần deploy lại code.

Ví dụ:

new_order_validation = false

Code mới đã được triển khai nhưng chức năng chưa hoạt động.

Sau đó bật cho:

* Nhân viên nội bộ.
* 1% khách hàng.
* Một quốc gia.
* Một loại tài khoản.

Nếu lỗi có thể tắt nhanh.

⸻

74. GitOps là gì?

GitOps là cách quản lý cấu hình triển khai thông qua Git.

Ví dụ trong Git có:

production/order-service.yaml

File ghi:

image: order-service:3.2.0
replicas: 10

Muốn nâng phiên bản:

3.1.5 → 3.2.0

Team tạo PR.

Sau khi được phê duyệt, hệ thống tự đồng bộ cấu hình từ Git ra Kubernetes.

Ưu điểm:

* Có lịch sử.
* Có review.
* Biết ai thay đổi.
* Có thể quay lại commit cũ.
* AI có thể kiểm tra thay đổi trước khi triển khai.

⸻

75. Quality Gate là gì?

Quality Gate là cổng kiểm soát chất lượng.

Thay đổi chỉ được đi tiếp nếu đạt các điều kiện.

Gate 1: Spec Ready

* Nghiệp vụ rõ.
* Có business rule.
* Có ví dụ.
* Không còn câu hỏi chặn việc phát triển.

Gate 2: Design Ready

* Ranh giới hệ thống rõ.
* API và event rõ.
* Failure case rõ.
* Có ADR khi cần.
* Có chiến lược test.

Gate 3: Build Ready

* Task đủ nhỏ.
* Input/output rõ.
* AI biết được sửa file nào.
* Có test và command.

Gate 4: Merge Ready

* Test pass.
* Contract không bị phá.
* Security scan pass.
* Human review xong.
* Spec và code được cập nhật cùng nhau.

Gate 5: Release Ready

* Migration được kiểm tra.
* Có rollback hoặc forward recovery.
* Dashboard và alert đã có.
* Có runbook.
* Có release note.

Gate 6: Production Verified

* Error rate không tăng.
* Latency không tăng bất thường.
* Business metric đúng.
* Không vi phạm invariant.
* Không có sự cố nghiêm trọng.

⸻

76. Runbook là gì?

Runbook là tài liệu hướng dẫn xử lý vận hành.

Ví dụ:

Sự cố:
Order Service không gọi được Balance Service.
Cách kiểm tra:
1. Kiểm tra dashboard Balance Service.
2. Kiểm tra error rate.
3. Kiểm tra network.
4. Kiểm tra circuit breaker.
5. Kiểm tra queue tồn đọng.
Cách xử lý:
1. Tắt feature mới.
2. Chuyển traffic về version cũ.
3. Khởi động lại instance lỗi.
4. Liên hệ team Balance.
Cách xác nhận phục hồi:
- Error rate dưới 0,1%.
- Queue không còn tăng.
- Synthetic test thành công.

AI có thể sinh runbook nháp từ kiến trúc và failure mode.

⸻

77. Circuit Breaker là gì?

Circuit Breaker là cơ chế ngắt gọi đến một service đang lỗi.

Ví dụ Balance Service liên tục timeout.

Nếu Order Service cứ gọi tiếp:

* Request tồn đọng.
* Thread bị giữ.
* Hệ thống chậm toàn bộ.
* Lỗi lan sang nhiều service.

Circuit Breaker hoạt động như cầu dao điện:

Balance Service lỗi nhiều
→ tạm ngừng gọi
→ trả lỗi nhanh
→ sau một thời gian thử lại

⸻

78. Cấu trúc repository gợi ý

/
├── AGENTS.md
│
├── docs/
│   ├── product/
│   │   ├── product-brief.md
│   │   ├── glossary.md
│   │   └── success-metrics.md
│   │
│   ├── domain/
│   │   ├── capability-map.md
│   │   ├── context-map.md
│   │   └── business-rules/
│   │
│   ├── architecture/
│   │   ├── system-context.md
│   │   ├── service-diagram.md
│   │   ├── sequences/
│   │   └── adr/
│   │
│   └── operations/
│       ├── slo.md
│       └── runbooks/
│
├── specs/
│   └── features/
│       └── ORD-001-place-order/
│           ├── requirements.md
│           ├── business-rules.md
│           ├── examples.feature
│           ├── design.md
│           ├── tasks.md
│           └── trace.yaml
│
├── contracts/
│   ├── openapi/
│   ├── asyncapi/
│   ├── protobuf/
│   └── database-schemas/
│
├── services/
│   ├── order-service/
│   │   ├── AGENTS.md
│   │   ├── src/
│   │   └── test/
│   │
│   ├── risk-service/
│   └── balance-service/
│
├── quality/
│   ├── test-strategy.md
│   ├── performance-budgets.yaml
│   ├── security-policies.yaml
│   └── traceability-rules.yaml
│
└── deployment/
    ├── infrastructure/
    ├── environments/
    └── gitops/

⸻

79. AGENTS.md là gì?

AGENTS.md là file hướng dẫn AI Agent cách làm việc trong repository.

Nó không nên chứa toàn bộ nghiệp vụ.

Nó nên chứa quy tắc làm việc.

Ví dụ:

# Hướng dẫn cho AI Agent
## Kiến trúc
- Service không được đọc database của service khác.
- Business logic không được phụ thuộc trực tiếp vào database.
- Mọi API public phải có OpenAPI.
## Quy trình bắt buộc
1. Đọc feature spec.
2. Đọc business rule.
3. Đọc ADR và contract liên quan.
4. Viết hoặc cập nhật test.
5. Viết code.
6. Chạy các command kiểm tra.
7. Báo rõ giả định còn tồn tại.
## Không được phép
- Không sửa public API nếu chưa cập nhật OpenAPI.
- Không thêm dependency mới nếu chưa được duyệt.
- Không truy cập production secret.
- Không xóa test để làm pipeline pass.
- Không bỏ qua exception một cách âm thầm.
## Command
- Unit test: ...
- Component test: ...
- Contract test: ...
- Lint: ...

Có thể có:

* AGENTS.md ở gốc repository.
* AGENTS.md riêng trong từng service.
* AGENTS.md riêng cho database hoặc deployment.

File gần code hơn sẽ chứa hướng dẫn cụ thể hơn.

⸻

80. AI Governance là gì?

AI Governance là các quy tắc quản lý việc dùng AI.

Nó trả lời:

* Model nào được sử dụng?
* Dữ liệu nào được gửi cho model?
* AI được phép sửa gì?
* AI có được dùng Internet không?
* AI có được truy cập secret không?
* Ai chịu trách nhiệm với code AI sinh ra?
* Khi nào bắt buộc human review?
* Log hoạt động của AI được lưu ở đâu?
* Chi phí sử dụng AI được kiểm soát thế nào?

⸻

81. Những việc AI có thể tự động hóa mạnh

* Sinh boilerplate.
* Viết CRUD đơn giản.
* Viết unit test.
* Tạo test data.
* Refactor cục bộ.
* Cập nhật tài liệu.
* Tạo client từ OpenAPI.
* Tìm dependency.
* Review coding convention.
* Phân tích lỗi CI.
* Tạo release note.
* Nâng dependency rủi ro thấp.
* Tạo PR.

Boilerplate là code lặp lại, có cấu trúc quen thuộc và ít logic đặc biệt.

CRUD là:

Create
Read
Update
Delete

Tức là tạo, đọc, sửa, xóa dữ liệu.

⸻

82. Những việc bắt buộc con người phê duyệt

* Business rule.
* Kiến trúc.
* Service boundary.
* Logic tiền.
* Ledger.
* Risk.
* Order.
* Position.
* Authentication.
* Authorization.
* Breaking API change.
* Database migration nguy hiểm.
* Production infrastructure.
* SLO.
* Release có rủi ro cao.
* Xóa dữ liệu.
* Thay đổi liên quan pháp lý.

⸻

83. Sandbox là gì?

Sandbox là môi trường cách ly cho AI Agent.

AI có thể:

* Đọc code.
* Sửa code.
* Chạy test.

Nhưng không được:

* Truy cập production database.
* Đọc secret thật.
* Gửi dữ liệu nhạy cảm ra ngoài.
* Chạy command nguy hiểm trên máy thật.
* Deploy production không kiểm soát.

Sandbox giúp giảm hậu quả nếu Agent làm sai.

⸻

84. Những sai lầm cần tránh

Sai lầm 1: Để AI tự hoàn thiện nghiệp vụ

AI có thể đưa ra giả định hợp lý nhưng không chắc đúng với công ty.

AI phải ghi:

Đây là giả định cần xác nhận.

Không được âm thầm biến giả định thành business rule.

Sai lầm 2: Viết tài liệu đến từng function cho toàn hệ thống

Tài liệu sẽ:

* Quá lớn.
* Nhanh lỗi thời.
* Khó duy trì.
* Làm team chậm.

Sai lầm 3: Cùng một AI viết code, test và review

AI có thể lặp lại cùng một hiểu lầm ở cả ba phần.

Sai lầm 4: Chia quá nhiều microservice

Microservice là service nhỏ, triển khai độc lập.

Nhiều microservice có thể dẫn đến:

* Gọi network nhiều.
* Khó debug.
* Khó transaction.
* Khó test.
* Khó deploy.
* Khó vận hành.

Bắt đầu bằng modular monolith thường an toàn hơn.

Sai lầm 5: Chỉ nhìn code coverage

Code coverage cho biết bao nhiêu dòng code đã được chạy qua bởi test.

Coverage cao không chứng minh nghiệp vụ đúng.

Cần xem thêm:

* Business rule coverage.
* Mutation score.
* Defect lọt ra production.
* Test trường hợp lỗi.
* Test concurrency.
* Test invariant.

Sai lầm 6: Cho AI quyền quá lớn

Không nên cho Agent:

* Secret production.
* Quyền sửa toàn bộ repository.
* Quyền tự merge code rủi ro cao.
* Quyền tự deploy production.
* Quyền xóa dữ liệu.

Sai lầm 7: Chạy tất cả test trên mọi thay đổi

Stress test hoặc E2E dài không cần chạy trên từng commit.

Cần chia test theo tầng để pipeline đủ nhanh.

⸻

85. Modular Monolith là gì?

Monolith là ứng dụng được triển khai thành một khối chính.

Modular Monolith là monolith nhưng được chia module rõ ràng bên trong.

Ví dụ:

trading-platform
├── order-module
├── balance-module
├── risk-module
├── account-module
└── reporting-module

Các module:

* Có ranh giới rõ.
* Không truy cập dữ liệu lung tung.
* Giao tiếp qua interface rõ.
* Có thể tách thành service sau này.

Ưu điểm:

* Dễ phát triển ban đầu.
* Dễ test.
* Dễ transaction.
* Dễ vận hành.
* Ít lỗi network.

Nhược điểm:

* Không deploy module hoàn toàn độc lập.
* Nếu thiết kế module không tốt, code dễ dính vào nhau.
* Scale từng phần riêng khó hơn microservice.

Đối với dự án mới, modular monolith thường phù hợp hơn việc tạo hàng chục microservice ngay từ đầu.

⸻

86. Lộ trình áp dụng thực tế cho team

Không nên xây toàn bộ hệ thống AI phức tạp ngay.

Nên đi theo từng giai đoạn.

⸻

Giai đoạn 1: Chuẩn hóa cách làm

Chọn một feature vừa phải.

Xây các mẫu sau:

* Product Brief.
* Feature Spec.
* Business Rule.
* BDD Scenario.
* ADR.
* API Contract.
* Task Packet.
* Test Strategy.
* AGENTS.md.
* Pull Request Template.

Xây CI cơ bản:

* Compile.
* Lint.
* Unit test.
* Component test.
* Security scan.

Mục tiêu giai đoạn này:

Team làm cùng một quy trình và cùng một loại tài liệu.

⸻

Giai đoạn 2: AI hỗ trợ từng bước

Thêm AI vào:

* Review yêu cầu.
* Phát hiện điểm mơ hồ.
* Sinh decision table.
* Sinh Mermaid.
* Đề xuất kiến trúc.
* Chia task.
* Viết code task nhỏ.
* Viết unit test.
* Review code.
* Cập nhật tài liệu.

Mục tiêu:

Tăng tốc nhưng vẫn giữ human approval.

⸻

Giai đoạn 3: Mở rộng nhiều team

Bổ sung:

* Contract registry.
* Ownership rõ cho từng service.
* Traceability.
* Impact analysis.
* Test environment tự động.
* API compatibility check.
* Database migration check.
* Performance budget.
* Security policy.

Contract Registry là nơi tập trung quản lý các API và event contract.

Performance Budget là giới hạn hiệu năng.

Ví dụ:

API đặt lệnh:
- p95 dưới 200ms
- CPU dưới 70%
- Memory dưới 2GB mỗi instance

⸻

Giai đoạn 4: Agent tự động hóa có kiểm soát

Agent có thể:

Nhận task
→ tạo branch
→ đọc spec
→ viết test
→ viết code
→ chạy test
→ sửa lỗi
→ gọi Agent khác review
→ tạo pull request

Nhưng:

* Human vẫn review phần rủi ro.
* Không tự merge logic tiền hoặc bảo mật.
* Không tự deploy production không kiểm soát.

⸻

87. Vai trò của bạn khi là Head của project lớn

Bạn không nên review từng function của hàng chục developer.

Bạn nên xây “hệ thống vận hành team”.

Bạn cần quyết định:

1. Chuẩn tài liệu

Mọi feature phải có gì?

Ví dụ:

* Business rule.
* Acceptance criteria.
* API contract.
* NFR.
* Test plan.
* Owner.

2. Quality Gate

Khi nào được chuyển từ BA sang DEV?

Khi nào được merge?

Khi nào được release?

3. Ownership

Ai chịu trách nhiệm cho:

* Nghiệp vụ.
* Service.
* Database.
* API.
* Event.
* Production.
* Security.
* Test.

4. Risk Classification

Thay đổi nào là:

* Rủi ro thấp.
* Rủi ro trung bình.
* Rủi ro cao.

5. AI Policy

* Việc nào dùng model mạnh?
* Việc nào dùng model phổ thông?
* Khi nào bắt buộc human review?
* Agent có quyền gì?
* Dữ liệu nào không được gửi cho AI?

6. Golden Path

Golden Path là con đường chuẩn được công ty chuẩn bị sẵn để team phát triển nhanh và đúng.

Ví dụ muốn tạo service mới, developer có sẵn template:

* Cấu trúc thư mục.
* Logging.
* Monitoring.
* Security.
* CI/CD.
* Docker.
* Kubernetes.
* Test.
* AGENTS.md.

Developer không phải tự xây lại từ đầu.

7. Metrics

Đo xem AI có thực sự giúp hay không.

Ví dụ:

* Thời gian từ yêu cầu đến production.
* Số lỗi lọt ra production.
* Thời gian review PR.
* Số lần rollback.
* Tỷ lệ test flaky.
* Chi phí AI cho mỗi feature.
* Tỷ lệ code AI sinh phải sửa lại.
* Thời gian xử lý incident.
* Tỷ lệ requirement phải làm lại.

⸻

88. Quy trình hoàn chỉnh đề xuất

flowchart TB
    subgraph HumanIntent["1. Con người quyết định mục tiêu"]
        A["Mục tiêu sản phẩm"]
        B["Yêu cầu nghiệp vụ"]
        C["Business Rule"]
        D["Ví dụ và Acceptance Criteria"]
    end
    subgraph Design["2. AI hỗ trợ, con người phê duyệt thiết kế"]
        E["Domain và ranh giới"]
        F["Kiến trúc"]
        G["API, Event, Data Contract"]
        H["NFR và Security"]
        I["ADR"]
    end
    subgraph Planning["3. Chia nhỏ công việc"]
        J["Task Graph"]
        K["Task Packet"]
        L["Test Strategy"]
    end
    subgraph Execution["4. DEV và AI Agent thực hiện"]
        M["Viết test"]
        N["Viết code"]
        O["AI review độc lập"]
        P["Human review theo rủi ro"]
    end
    subgraph Verification["5. Kiểm chứng tự động"]
        Q["Unit và Property Test"]
        R["Component và Contract Test"]
        S["Integration và Acceptance Test"]
        T["Security và Performance Test"]
    end
    subgraph Delivery["6. Triển khai có kiểm soát"]
        U["CI/CD"]
        V["Feature Flag và Canary"]
        W["Monitoring, Log, Trace, SLO"]
    end
    A --> B --> C --> D
    D --> E --> F --> G
    F --> H
    F --> I
    G --> J
    H --> J
    I --> J
    J --> K
    J --> L
    K --> M
    L --> M
    M --> N --> O --> P
    P --> Q --> R --> S --> T
    T --> U --> V --> W
    W -->|"Phản hồi thực tế"| B

⸻

89. Mô hình ngắn gọn nhất để ghi nhớ

Có thể rút gọn thành sáu bước:

1. Con người làm rõ nghiệp vụ.
2. Model mạnh hỗ trợ thiết kế và tìm rủi ro.
3. Model mạnh chia công việc thành task rõ ràng.
4. Model phổ thông và DEV code theo task.
5. QA, AI và CI kiểm tra độc lập.
6. Triển khai từng bước và quan sát production.

Hoặc chỉ bằng một câu:

Con người quyết định điều gì là đúng; AI mạnh xử lý phần mơ hồ và phức tạp; AI phổ thông thực hiện các task đã được mô tả rõ; test và dữ liệu production chứng minh hệ thống thực sự đúng.

⸻

90. Bộ tài liệu tối thiểu nên xây đầu tiên

Nếu bắt đầu áp dụng ngay, chưa cần làm quá nhiều.

Chỉ cần chuẩn hóa bốn bộ tài liệu đầu tiên:

1. Feature Specification

Mô tả:

* Chức năng.
* Người dùng.
* Business rule.
* Input/output.
* Ví dụ.
* Trường hợp lỗi.
* Acceptance criteria.

2. Technical Design

Mô tả:

* Service hoặc module nào thay đổi.
* Data flow.
* API và event.
* Database.
* Failure handling.
* Security.
* Performance.
* Mermaid diagram.

3. Task Packet

Mô tả:

* AI hoặc DEV cần làm gì.
* Được sửa file nào.
* Không được làm gì.
* Input/output.
* Test bắt buộc.
* Điều kiện hoàn thành.

4. Test Evidence

Mô tả:

* Business rule nào đã được test.
* Test nào đã chạy.
* Kết quả.
* Performance.
* Security.
* Contract compatibility.
* Release verification.

Khi bốn phần này vận hành tốt, mới tiếp tục xây:

* Multi-agent.
* Impact graph.
* Contract registry.
* Automatic documentation sync.
* Automated release governance.

⸻

KẾT LUẬN

Hướng suy nghĩ của bạn là đúng, nhưng cần điều chỉnh thành mô hình thực tế hơn:

Không nên:

AI mạnh thiết kế toàn bộ tới từng function
→ AI yếu code toàn bộ
→ AI tự test và tự xác nhận

Nên:

Con người và AI làm rõ nghiệp vụ
→ Model mạnh đề xuất kiến trúc và phân tích rủi ro
→ Con người phê duyệt
→ Model mạnh chia thành task nhỏ
→ Model phổ thông hoặc AI Agent code
→ QA và Test Agent kiểm tra độc lập
→ CI tự động kiểm chứng
→ Human review theo mức rủi ro
→ Triển khai từng bước
→ Dùng production data để xác nhận

Điểm khó nhất không phải là chọn model nào viết code tốt nhất.

Điểm khó nhất là xây được một quy trình trong đó:

* Yêu cầu không mơ hồ.
* Mọi quyết định quan trọng được ghi lại.
* Mỗi task có phạm vi rõ.
* Mỗi business rule có test.
* Mỗi thay đổi có thể truy vết ảnh hưởng.
* AI bị giới hạn quyền.
* Code không thể merge nếu thiếu bằng chứng chất lượng.
* Production được theo dõi và có khả năng phục hồi.

Khi xây được nền tảng này, AI sẽ trở thành lực lượng nhân rộng năng lực của team.

Nếu nền tảng chưa rõ, AI chỉ giúp team tạo ra code, tài liệu và lỗi nhanh hơn.

Bản này có thể tiếp tục được chuyển thành một quy trình chuẩn áp dụng trong công ty, chia rõ công việc hằng ngày của BA, DEV, QA, Tech Lead và từng AI Agent.