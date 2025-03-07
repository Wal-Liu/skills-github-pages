
---
# I. Fundamentals of pricing (cơ bản về giá cả)

## 1. AWS pricing model (mô hình định giá của AWS)
Có 3 yếu tố ảnh hưởng đến chi phí sử dụng dịch vụ AWS
### 1.1.Compute (máy)
- Được tính phí theo giờ hoặc giây sử dụng (chỉ áp dụng cho Linux).
- Chi phí thay đổi tùy thuộc vào loại máy chủ (instance) bạn sử dụng.
### 1.2. Storage (Lưu trữ)
- Thường được tính phí theo dung lượng (GB).
### 1.3. Data Transfer (Truyền dữ liệu)
- **Dữ liệu đi ra ngoài AWS** (Outbound) bị tính phí và được tổng hợp từ nhiều dịch vụ khác nhau.
- **Dữ liệu vào AWS** (Inbound) thường miễn phí, nhưng có một số trường hợp ngoại lệ.
- Chi phí truyền dữ liệu thường được tính theo GB.

## 2. How do you pay for AWS?
Có ba mô hình thanh toán chính:
1. **Pay for what you use (Trả tiền cho những gì bạn sử dụng)**
    - Bạn chỉ trả tiền cho tài nguyên mà bạn thực sự dùng, không cần cam kết dài hạn.
    - Cuối mỗi tháng, hóa đơn sẽ phản ánh mức sử dụng thực tế.
2. **Pay less when you reserve (Trả ít hơn khi đặt trước)**
    - Nếu bạn cam kết sử dụng tài nguyên trong một khoảng thời gian dài (ví dụ: 1 hoặc 3 năm), bạn sẽ được giảm giá so với mức giá theo yêu cầu (on-demand).
    - Điều này đặc biệt áp dụng cho **Reserved Instances** trong EC2 hoặc các dịch vụ AWS khác có tùy chọn đặt trước.
3. **Pay less when you use more and as AWS grows (Trả ít hơn khi sử dụng nhiều hơn và khi AWS phát triển)**
    - Khi sử dụng AWS ở quy mô lớn hơn, bạn có thể được giảm giá theo bậc.
    - Ví dụ: khi bạn lưu trữ nhiều dữ liệu hơn trong S3 hoặc truyền nhiều dữ liệu hơn, AWS có thể giảm giá trên mỗi GB sau một ngưỡng nhất định.
    - Khi AWS mở rộng quy mô và tối ưu hóa hạ tầng, AWS thường giảm giá cho khách hàng
    
## 3. Pay for what you use
| On-premises                                                                                                                                                           | AWS                                                                                                                                                                                                                                                                                                                                                                                                              |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| -Cần đầu tư trước một khoản chi phí lớn để mua máy chủ, phần mềm, và xây dựng trung tâm dữ liệu <br> -Chi phí cố định, không linh hoạt, ngay cả khi nhu cầu thay đổi. | -Chỉ trả tiền cho tài nguyên bạn sử dụng, không cần đầu tư ban đầu lớn. <br>-Giảm chi phí biến đổi, không cần lo lắng về việc mua sắm phần cứng, cấp phép phần mềm hoặc thuê trung tâm dữ liệu.<br>-Dịch vụ theo yêu cầu (**on-demand**), không có hợp đồng dài hạn hay yêu cầu giấy phép phức tạp.<br> Linh hoạt điều chỉnh tài nguyên theo nhu cầu thực tế, giúp doanh nghiệp thích ứng nhanh với sự thay đổi. |
 **Ý nghĩa**
- AWS giúp doanh nghiệp **tập trung vào đổi mới** thay vì tốn nhiều thời gian và tiền bạc vào việc vận hành hạ tầng CNTT.
- Phù hợp với những doanh nghiệp có nhu cầu mở rộng hoặc thay đổi tài nguyên linh hoạt mà không muốn bị ràng buộc bởi chi phí cố định cao.

![[Pasted image 20250226082344.png]]

## 4. **Pay less when you reserve** (**Reserved Instances (RIs)**)
### Lợi ích của Reserved Instances (RIs)
- **Tiết kiệm lên đến 75%** so với giá **On-Demand** (trả tiền theo giờ thông thường).
- **Giữ trước dung lượng**: đảm bảo tài nguyên sẵn có, thích hợp cho nhu cầu dài hạn.

### Ba loại Reserved Instances (RIs):
1. **All Upfront Reserved Instance (AURI)** – **Trả trước toàn bộ**    
    - Được **giảm giá nhiều nhất**.
    - Cần thanh toán toàn bộ chi phí trước.
    - Phù hợp nếu bạn có ngân sách lớn và muốn tiết kiệm tối đa.
2. **Partial Upfront Reserved Instance (PURI)** – **Trả trước một phần**
    - Giảm giá ít hơn AURI nhưng vẫn tốt hơn On-Demand.
    - Thanh toán một phần trước, phần còn lại tính theo tháng.
    - Giúp cân đối giữa tiết kiệm chi phí và dòng tiền.
3. **No Upfront Payments Reserved Instance (NURI)** – **Không cần trả trước**
    - **Giảm giá ít nhất** trong ba loại RI.
    - Không cần thanh toán ban đầu, chỉ trả phí hàng tháng thấp hơn On-Demand.
    - Phù hợp nếu bạn muốn tiết kiệm mà không có ngân sách lớn để trả trước.

### Khi nào nên sử dụng Reserved Instances?
- Khi có **nhu cầu sử dụng dài hạn**, ít nhất là **1 hoặc 3 năm**.
- Khi muốn **tiết kiệm chi phí** so với On-Demand.
- Khi doanh nghiệp cần **dự đoán ngân sách ổn định**, tránh biến động giá.

## 5. Pay less by using more
- **Tiết kiệm khi mức sử dụng tăng lên**
    - Khi bạn sử dụng **nhiều hơn**, giá trên mỗi GB dữ liệu sẽ giảm.
- **Mô hình giá theo cấp bậc (Tiered Pricing)**
    
    - Các dịch vụ như **Amazon S3 (Simple Storage Service), Amazon EBS (Elastic Block Store), Amazon EFS (Elastic File System)** có mức giá giảm dần khi sử dụng nhiều hơn.
    - Ví dụ: Nếu bạn lưu trữ 50 TB dữ liệu trên S3, chi phí cho mỗi GB sẽ thấp hơn so với khi bạn chỉ lưu trữ 5 TB.
- **Sử dụng nhiều dịch vụ lưu trữ khác nhau để tối ưu chi phí**
    
    - AWS có nhiều loại dịch vụ lưu trữ với chi phí khác nhau.
    - Ví dụ: **Amazon S3 Glacier** rẻ hơn nhưng truy xuất chậm, phù hợp để lưu trữ dữ liệu lâu dài.
### Lợi ích của việc sử dụng nhiều hơn trên AWS

- **Hưởng lợi từ quy mô lớn**: Khi mức sử dụng tăng, bạn **giảm chi phí trên mỗi đơn vị tài nguyên**.
- **Kiểm soát chi phí tốt hơn**: Nhờ **giảm giá theo khối lượng**, doanh nghiệp có thể tăng quy mô mà không tăng mạnh chi phí.
- **Linh hoạt trong lựa chọn lưu trữ**: Có thể tối ưu hóa chi phí bằng cách **kết hợp nhiều loại dịch vụ lưu trữ** phù hợp với nhu cầu.

## 6. Pay even less as AWS grows
 **Cách AWS giúp giảm chi phí theo thời gian**:
1. **Tập trung vào việc giảm chi phí vận hành**
    - AWS liên tục tối ưu hóa chi phí phần cứng, cải thiện hiệu suất hoạt động và giảm tiêu thụ năng lượng.
    - Điều này giúp AWS giảm chi phí kinh doanh và có thể chuyển những khoản tiết kiệm đó đến khách hàng.
2. **AWS truyền lại lợi ích tiết kiệm cho khách hàng**
    - Khi AWS mở rộng, chi phí trên mỗi đơn vị tài nguyên giảm xuống.
    - AWS đã **giảm giá tới 75 lần kể từ năm 2006 (tính đến tháng 9/2019)**, giúp người dùng hưởng mức giá thấp hơn theo thời gian.
3. **Tài nguyên hiệu suất cao hơn thay thế tài nguyên cũ mà không tăng giá**
    - Khi AWS cải tiến công nghệ, khách hàng có thể sử dụng tài nguyên tốt hơn mà **không cần trả thêm phí**.
### Lợi ích khi AWS tiếp tục phát triển:

- **Giảm giá dịch vụ theo thời gian** → Chi phí thấp hơn cho doanh nghiệp.
- **Cải tiến phần cứng liên tục** → Tận dụng công nghệ mới nhất mà không cần nâng cấp thủ công.
- **Không có chi phí ẩn** → Không cần trả thêm khi AWS cung cấp tài nguyên mạnh hơn.

## 7. Custom pricing
Mỗi khách hàng có mỗi nhu cầu khác nhau. Nếu các mô hình sẵn có không đáp ứng được nhu cầu, mình có thể tuỳ chỉnh các mô hình để phù hợp cho mỗi doanh nghiệp

## 8. AWS free tier
AWS cung cấp **tài khoản miễn phí** trong **1 năm** cho khách hàng mới, giúp bạn trải nghiệm thực tế với nền tảng, sản phẩm và dịch vụ AWS.
![[Pasted image 20250226085247.png]]
### Những dịch vụ miễn phí phổ biến:
- **Amazon EC2 T2 micro**: Máy chủ ảo miễn phí **1 năm**.
- **Amazon S3**: Lưu trữ dữ liệu đám mây miễn phí.
- **Amazon EBS**: Ổ đĩa lưu trữ đám mây miễn phí.
- **Elastic Load Balancing**: Cân bằng tải miễn phí.
- **AWS Data Transfer**: Truyền dữ liệu miễn phí.

 ## 9. Services with no charge
  **Các dịch vụ miễn phí phổ biến**:

- **Amazon VPC** – Tạo mạng ảo riêng trên AWS.  
- **AWS IAM** – Quản lý quyền truy cập người dùng.  
-  **AWS CloudFormation** – Tạo và quản lý hạ tầng AWS tự động.  
- **AWS Auto Scaling** – Tự động mở rộng tài nguyên dựa theo nhu cầu.  
- **AWS Elastic Beanstalk** – Triển khai ứng dụng nhanh chóng.

 **Lợi ích của dịch vụ miễn phí AWS**:
- **Bảo mật & kiểm soát tốt hơn**: IAM giúp phân quyền người dùng chặt chẽ.
- **Tối ưu hóa chi phí**: Auto Scaling tự động điều chỉnh tài nguyên.
- **Triển khai nhanh chóng**: Elastic Beanstalk giúp khởi chạy ứng dụng dễ dàng.
- **Quản lý tập trung**: Consolidated Billing giúp theo dõi chi phí nhiều tài khoản AWS.

---
# II. Total Cost of Ownership
## 1. On-premises vs cloud
| Traditional                                                                                                                                                        | Could                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - Chi phí đầu tư lớn (CapEx) – Mua máy chủ, phần cứng, giấy phép.<br>- Mất nhiều thời gian triển khai và mở rộng.<br>- Yêu cầu đội ngũ vận hành, bảo trì liên tục. | - **Không cần đầu tư ban đầu** – trả tiền theo mức sử dụng.<br>- **Tăng/giảm tài nguyên linh hoạt** theo nhu cầu. <br>- **Triển khai nhanh chóng**, cải thiện thời gian ra thị trường. <br>- **Mô hình tự phục vụ**, giảm tải quản lý hạ tầng |                                                                                                                                                                   |                                                                                                                                                                                                                                               |

![[Pasted image 20250226091540.png]]

## 2. What is Total cost of Ownership (TCO)
TCO là ước tính tài chính giúp xác định chi phí trực tiếp và gián tiếp của một hệ thống
TCO dùng để:
- So sánh chi phí vận hành một toàn bộ môi trường cơ sở hạ tầng hoặc khối lượng công việc cụ thể tại cơ sở so với trên AWS 
- Để lập ngân sách và xây dựng trường hợp kinh doanh cho việc chuyển sang đám mây

## 3. TCO considerations
Chi phí máy chủ cho cả phần cứng và phần mềm, và chi phí cơ sở vật chất để chứa thiết bị.
- Chi phí lưu trữ cho phần cứng, quản trị và cơ sở vật chất.
- Chi phí mạng cho phần cứng, quản trị và cơ sở vật chất.
- Và chi phí lao động CNTT cần thiết để quản lý toàn bộ giải pháp.
![[Pasted image 20250226113508.png]]

| Direct costs | Indirect costs |
| ------------ | -------------- |
| việc vận hành máy chủ như như điện, diện tích sàn, lưu trữ và hoạt động CNTT để quản lý các tài nguyên đó. | khi vận hành máy chủ, như cơ sở hạ tầng mạng và lưu trữ. Đào tạo và chứng nhận AWS  |

## 4. On-premises versus all-in-cloud
![[Pasted image 20250226145557.png]]
We could save up to 96 percent a year by moving your infrastructure to AWS.

## 5. AWS Pricing Calculator
Tác dụng:
- Ước tính chi phí hàng tháng 
- Xác định các cơ hội để giảm chi phí hàng tháng 
- Lập mô hình các giải pháp của bạn trước khi xây dựng chúng
- Khám phá các điểm giá và tính toán đằng sau ước tính của bạn  
- Tìm các loại phiên bản khả dụng và các điều khoản hợp đồng đáp ứng nhu cầu của bạn 
- Đặt tên cho ước tính và tạo và đặt tên cho các nhóm dịch vụ

## 6. Reading an estimate

- The total for your first 12 months – Tổng ước tính cho nhóm hiện tại của bạn và tất cả các dịch vụ và nhóm trong nhóm hiện tại của bạn. Nó kết hợp các ước tính trả trước và hàng tháng.
- Your total upfront – Số tiền bạn ước tính phải trả trước khi thiết lập  AWS stack của mình
- Your total monthly –Số tiền bạn ước tính phải chi tiêu hàng tháng trong khi bạn chạy  AWS stack của mình<br>
![[Pasted image 20250226172706.png]]
Hình trên có ý nghĩa The first 12 month total : $886.92, the total upfront cost: $0, và the total monthly cost: $73.91
## 7. Activity: AWS Pricing Calculator activity
![[Pasted image 20250226173836.png]]
sau khi tự tạo sẽ có bảng như trên.
Thông tin chi tiết
The first 12 month total : $3723,00, the total upfront cost: $0, và the total monthly cost: $310.25

## 8. Lợi ích bổ sung khi sử dụng AWS Cloud

### So sánh lợi ích cứng và lợi ích mềm

| Lợi ích cứng (Hard Benefits) [^1]                     | Lợi ích mềm (Soft Benefits) [^2]                           |
| ----------------------------------------------------- | ---------------------------------------------------------- |
| Giảm chi phí phần cứng, lưu trữ, mạng, bảo mật.       | Tái sử dụng dịch vụ và ứng dụng trên nền tảng AWS.         |
| Giảm chi phí mua sắm phần mềm & phần cứng (CapEx).    | Tăng năng suất phát triển phần mềm.                        |
| Giảm chi phí vận hành, sao lưu và khắc phục thảm họa. | Cải thiện sự hài lòng của khách hàng.                      |
| Giảm nhu cầu về nhân sự vận hành hệ thống.            | Mô hình kinh doanh linh hoạt, dễ thích ứng với cơ hội mới. |
|                                                       | Mở rộng phạm vi hoạt động toàn cầu dễ dàng.                |
[^1]:  Lợi ích cứng là lợi ích có thể dễ dàng đo lường về mặt tài chính
[^2]: Lợi ích mềm mang lại giá trị lâu dài, khó định lượng về tài chính hơn

### Phân tích chi phí sở hữu (TCO) và ROI

- **TCO (Total Cost of Ownership):**  
  So sánh tổng chi phí giữa hạ tầng truyền thống và cloud để đánh giá hiệu quả kinh tế.

- **ROI (Return on Investment):**  
  Xác định giá trị mang lại từ việc tiết kiệm chi phí vận hành và tối ưu tài nguyên.

---

### Tổng kết
AWS không chỉ giúp giảm chi phí mà còn tối ưu vận hành, nâng cao năng suất và khả năng cạnh tranh.

---
## 9. Case study: Tổng Chi Phí Sở Hữu (TCO) - Delaware North
### 1)
**Thông tin chung** 
- **Doanh nghiệp toàn cầu đang phát triển**, sở hữu hơn **200 địa điểm**. 
- **Phục vụ 500 triệu khách hàng** mỗi năm, với **doanh thu hàng năm đạt 3 tỷ USD**. 

**Bối cảnh** 
Delaware North được thành lập vào năm **1915** với tư cách là nhà cung cấp đậu phộng và bỏng ngô. Ngày nay, công ty này là một trong những tập đoàn lớn trong ngành **dịch vụ thực phẩm và khách sạn**. Dù không quá nổi bật trên thị trường, nhưng Delaware North vẫn là **một trong những doanh nghiệp hàng đầu trong ngành**. Mỗi năm, Delaware North phục vụ hơn **500 triệu khách hàng** tại **hơn 200 địa điểm** trên toàn cầu. 
Một số địa điểm tiêu biểu mà công ty hoạt động bao gồm: 
 - **Trung tâm không gian Kennedy** (Florida, Mỹ). 
 - **Sân bay Heathrow** (London, Anh). 
 - **Khu nghỉ dưỡng Kings Canyon** (Úc). 
 - **Sân vận động Lambeau Field của đội Green Bay Packers** (Wisconsin, Mỹ). 
 Với **quy mô hoạt động toàn cầu**, Delaware North đã phát triển thành một tập đoàn trị giá **3 tỷ USD**.

---
### 2)
**Thách thức** 
- **Nhu cầu triển khai nhanh chóng các giải pháp công nghệ mới**. 
- **Liên tục nâng cấp thiết bị cũ**, gây tốn kém tài nguyên.

**Vấn đề của Delaware North** 
Trung tâm dữ liệu (data center) tại chỗ của Delaware North đã trở nên **quá đắt đỏ và kém hiệu quả** để hỗ trợ các hoạt động kinh doanh toàn cầu của công ty. 

Kevin Quinlivan, Giám đốc Thông tin (CIO) của Delaware North, chia sẻ: > "Khi công ty tiếp tục mở rộng, **nhu cầu triển khai nhanh chóng các giải pháp mới** để đáp ứng yêu cầu của khách hàng cũng tăng lên. Điều này, cùng với **việc phải liên tục nâng cấp thiết bị cũ**, khiến chúng tôi phải đầu tư nhiều tài nguyên hơn. Chúng tôi cần tìm một chiến lược tốt hơn." 
Delaware North đã chọn **AWS** làm giải pháp cho bài toán này.

---
### 3)
 **Tiêu chí đánh giá** 
 - **Giải pháp toàn diện** để xử lý tất cả khối lượng công việc. 
 - **Khả năng điều chỉnh quy trình** để nâng cao hiệu quả và giảm chi phí. 
 - **Loại bỏ công việc dư thừa**, như cập nhật phần mềm. 
 - **Đạt được lợi tức đầu tư (ROI) tích cực**. 

 **Quá trình đánh giá** Sau khi **di chuyển thành công khoảng 50 trang web lên AWS vào năm 2013**, Delaware North đã đánh giá chi phí và **Tổng Chi Phí Sở Hữu (TCO)** khi chuyển cơ sở hạ tầng CNTT sang AWS. 
 
 **Ba tiêu chí chính được xem xét:** 
1. **Giải pháp đám mây phải có khả năng xử lý toàn bộ khối lượng công việc của Delaware North**, đồng thời hỗ trợ các chức năng quan trọng. 
2. **Cần linh hoạt để điều chỉnh các quy trình CNTT cốt lõi**, nhằm nâng cao hiệu quả và giảm chi phí. Điều này bao gồm **loại bỏ các công việc dư thừa và tốn thời gian**, như vá lỗi phần mềm hoặc triển khai hệ thống thông qua các phương pháp cũ. 
3. **Yêu cầu tài chính phải chứng minh được lợi tức đầu tư (ROI)** với một phân tích chi phí-lợi ích rõ ràng, để biện minh cho việc rời bỏ trung tâm dữ liệu hiện có.

---
### 4)
**Giải pháp AWS** 
- **Di chuyển toàn bộ trung tâm dữ liệu nội bộ lên AWS**. 
- **Loại bỏ 205 máy chủ**, tương đương **90% cơ sở hạ tầng cũ**. 
- **Di chuyển gần như tất cả các ứng dụng lên AWS**. 
- **Sử dụng gói Amazon EC2 Reserved Instances trong 3 năm**. 

**So sánh chi phí**
- **Tiết kiệm 3,5 triệu USD** trong 5 năm khi chuyển từ trung tâm dữ liệu nội bộ sang AWS. - **Giảm hơn 90% phần cứng máy chủ** bằng cách tận dụng hạ tầng AWS. 
- **Chi trả dựa trên mức sử dụng thực tế**, tránh lãng phí tài nguyên. 

 **Lợi ích mở rộng** 
 - **Tăng khả năng mở rộng tính toán**, hỗ trợ khối lượng công việc lớn hơn. 
 - **Di chuyển hầu hết các ứng dụng doanh nghiệp lên AWS**, bao gồm: 
	 - **Fiorano middleware** 
	 - **Crystal Reports**
	 - **QLIK business intelligence** 
	 - **Citrix virtual desktop** 
	 - **Microsoft System Center Configuration Manager** 
	
**Scott Mercer**, trưởng nhóm kiến trúc dịch vụ CNTT của Delaware North, cho biết: > “Chúng tôi thận trọng để đảm bảo không có độ trễ trong các tác vụ này, nhưng khi đạt đến mức độ tin cậy nhất định, chúng tôi có thể sẽ chuyển toàn bộ lên đám mây.”

---
### 5)
![[Pasted image 20250226194846.png]]
**Kết quả phân tích tài chính trong 5 năm** 
- **Môi trường on-premises**: Chi phí hàng năm **cao hơn đáng kể**, đặc biệt trong năm 2015. 
- **Môi trường AWS** (sử dụng **Amazon EC2 Reserved Instances trong 3 năm + gia hạn thêm 3 năm**) giúp giảm đáng kể chi phí hàng năm. 
- **Tổng mức tiết kiệm**: **3,5 triệu USD trong 5 năm** khi di chuyển sang AWS. 

Việc chuyển đổi sang AWS đã giúp Delaware North tối ưu hóa ngân sách, giảm thiểu chi phí phần cứng và chỉ thanh toán cho tài nguyên thực sự sử dụng.

----
### 6)
![[Pasted image 20250226195217.png]]

**Mục tiêu kinh doanh** 
- Mở rộng quy mô 
- Tăng cường vận hành 24/7 
- Nâng cao hiệu suất hoạt động 
- 
**Kết quả đạt được** 
1. **Tối ưu hóa tài nguyên** 
- Tuân thủ bảo mật mạnh mẽ 
- Cải thiện khả năng phục hồi sau thảm họa 
- Tăng cường khả năng tính toán 
2. **Tăng tốc ra thị trường** 
- Cung cấp doanh nghiệp mới trong 1 ngày
- Chỉ mất vài phút để triển khai dịch vụ 
3. **Hiệu quả hoạt động** 
- Liên tục tối ưu hóa chi phí và giảm thiểu lãng phí 

**Những lợi ích thực tế** 
Sau 6 tháng chuyển đổi lên AWS, Delaware North nhận thấy nhiều lợi ích vượt ngoài việc hợp nhất trung tâm dữ liệu, bao gồm: 
- Tuân thủ bảo mật hiệu quả với chi phí thấp hơn 
- Cải thiện khả năng phục hồi và dự phòng lỗi 
- Triển khai nhanh chóng doanh nghiệp mới trong 1 ngày (thay vì 2-3 tuần) 
- Hợp lý hóa quy trình vận hành bằng cách loại bỏ các tác vụ IT phức tạp và lỗi thời 

**Nhận xét từ chuyên gia** 
Brian Mercer, Kiến trúc sư phần mềm cao cấp tại Delaware North, cho biết: 
*"Với AWS, chúng tôi có thể phản ứng nhanh hơn với nhu cầu kinh doanh, tiết kiệm thời gian và nguồn lực để tạo ra nhiều giá trị hơn cho khách hàng."*

---
---
# III.AWS Organizations

## 1. Introduction to AWS Organizations
AWS Organizations là dịch vụ quản lý tài khoản miễn phí cho phép bạn hợp nhất nhiều tài khoản AWS thành một tổ chức do bạn tạo và quản lý tập trung.
AWS Organizations bao gồm các khả năng quản lý tài khoản và thanh toán hợp nhất giúp bạn đáp ứng tốt hơn các nhu cầu về ngân sách, bảo mật và tuân thủ của doanh nghiệp. 
Các lợi ích chính của AWS Organizations là: 
-  Chính sách truy cập được quản lý tập trung trên nhiều tài khoản AWS. 
- Quyền truy cập được kiểm soát vào các dịch vụ AWS. 
- Tự động tạo và quản lý tài khoản AWS. 
- Hóa đơn hợp nhất trên nhiều tài khoản AWS.
![[Pasted image 20250226200424.png]]

---
## 2. AWS Organizations terminology (thuật ngữ)
![[Pasted image 20250226200744.png]]
Sơ đồ cho thấy một tổ chức cơ bản(root), bao gồm bảy tài khoản được tổ chức thành bốn đơn vị tổ chức (hoặc OU). 
OU là một vùng chứa cho các tài khoản trong một gốc. 
OU cũng có thể chứa các OU khác. 
Cấu trúc này cho phép bạn tạo một hệ thống phân cấp trông giống như một cây trong cấu trúc đồ thị
Các nhánh bao gồm các OU con và chúng di chuyển xuống dưới cho đến khi chúng kết thúc bằng các tài khoản, giống như các lá của cây. 
Khi bạn đính kèm một chính sách vào một trong các nút trong hệ thống phân cấp, chính sách đó sẽ chảy xuống và ảnh hưởng đến tất cả các nhánh và lá. 
Tổ chức ví dụ này có một số chính sách được đính kèm vào một số OU hoặc được đính kèm trực tiếp vào các tài khoản. 
OU chỉ có thể có một đơn vị cha và hiện tại, mỗi tài khoản có thể là thành viên của chính xác một OU. 
Tài khoản là tài khoản AWS chuẩn chứa các tài nguyên AWS của bạn. Bạn có thể đính kèm một chính sách vào một tài khoản để áp dụng các biện pháp kiểm soát chỉ cho một tài khoản đó

----
## 3. Key features and benefits
![[Pasted image 20250226201147.png]]

AWS Organizations cung cấp các tính năng giúp quản lý tài khoản AWS hiệu quả: 
- **Quản lý tài khoản dựa trên chính sách** 
- **Quản lý tài khoản theo nhóm** 
- **Tích hợp API để tự động hóa quản lý tài khoản** 
- **Hợp nhất hóa đơn thanh toán (Consolidated billing)** 

**Lợi Ích Chính** 
- **Chính sách kiểm soát dịch vụ (SCPs):** Quản lý tập trung các dịch vụ AWS trên nhiều tài khoản. - **Nhóm tài khoản:** Dễ dàng áp dụng chính sách cho nhiều tài khoản cùng lúc. 
- **Tự động hóa quản lý tài khoản:** Sử dụng API để tạo và quản lý tài khoản AWS mới nhanh chóng. 
- **Hợp nhất thanh toán:** Quản lý thanh toán tập trung, hưởng lợi từ chiết khấu theo khối lượng sử dụng. Với AWS Organizations, doanh nghiệp có thể tối ưu hóa quản trị, bảo mật và kiểm soát chi phí trên toàn bộ hệ thống AWS của mình.

---
## 4. Security with AWS Organizations
AWS Organizations cung cấp các cơ chế bảo mật mạnh mẽ: 
- **Quản lý quyền truy cập với AWS Identity and Access Management (IAM)** 
- **Chính sách IAM giúp cấp phép hoặc từ chối quyền truy cập AWS cho người dùng, nhóm và vai trò** 
- **Chính sách kiểm soát dịch vụ (SCPs) giúp kiểm soát quyền truy cập AWS ở cấp tài khoản hoặc nhóm tài khoản** 

| Đặc điểm                     | IAM Policies                                                               | Service Control Policies (SCPs)                        |
| ---------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------ |
| **Phạm vi áp dụng**          | Người dùng, nhóm, vai trò trong một tài khoản AWS                          | Toàn bộ tài khoản AWS hoặc nhóm tài khoản (OU)         |
| **Cấp phép / Từ chối**       | Cho phép hoặc từ chối truy cập vào dịch vụ AWS, tài nguyên hoặc API cụ thể | Chỉ có thể từ chối quyền truy cập, không thể cấp quyền |
| **Kiểm soát tài khoản root** | Không thể hạn chế quyền root                                               | Có thể hạn chế quyền root trên tài khoản AWS           |
| **Mục đích sử dụng**         | Kiểm soát chi tiết quyền truy cập của người dùng trong tài khoản           | Thiết lập các quy tắc chung trên nhiều tài khoản       |                             |                                                                            |                                                        |

![[Pasted image 20250226203315.png]]

---
## 5. Cấu hình AWS Organizations
![[Pasted image 20250226203434.png]]
1. **Tạo Organization** 
- Sử dụng tài khoản AWS hiện tại làm tài khoản chính. 
- Mời một tài khoản AWS khác tham gia và tạo một tài khoản thành viên. 
2. **Tạo Organizational Units (OUs)** 
- Thiết lập hai đơn vị tổ chức trong AWS Organizations. 
- Gán các tài khoản thành viên vào các OUs tương ứng. 
3. **Tạo Service Control Policies (SCPs)** 
- Thiết lập các chính sách kiểm soát dịch vụ để áp dụng các hạn chế cho tài khoản thành viên.
- SCPs giúp kiểm soát quyền truy cập của người dùng và vai trò trong tổ chức. 
4. **Kiểm tra các hạn chế** 
- Đăng nhập với vai trò trong từng OU để kiểm tra chính sách SCPs. 
- Sử dụng IAM Policy Simulator để kiểm tra và khắc phục lỗi chính sách IAM hoặc chính sách dựa trên tài nguyên.

---
## 6. Limits of AWS Organizations
![[Pasted image 20250226203658.png]]

---
## 7. Accessing AWS Organizations
![[Pasted image 20250226203800.png]]

---
---
# IV. AWS Billing and Cost Management

## 1. Introducing
AWS Billing and Cost Management là dịch vụ bạn sử dụng để thanh toán hóa đơn AWS, theo dõi mức sử dụng và lập ngân sách cho chi phí của mình. Billing and Cost Management cho phép bạn dự báo và có được ý tưởng tốt hơn về chi phí và mức sử dụng của mình trong tương lai để bạn có thể lập kế hoạch trước.
![[Pasted image 20250226204039.png]]

---
## 2. AWS Billing Dashboard
![[Pasted image 20250226204259.png]]
có 2 biểu đồ chính:
1. Spend Summary: tóm tắt chi tiêu cho bạn biết bạn đã chi bao nhiêu trong tháng trước, chi phí ước tính cho việc sử dụng AWS của bạn trong tháng đến ngày và dự báo về số tiền bạn có thể chi trong tháng này
2. Monthly-to-Date Spend by service: hiển thị các dịch vụ hàng đầu mà bạn sử dụng nhiều nhất và tỷ lệ chi phí được gán cho dịch vụ đó

---
## 3. Tools
![[Pasted image 20250226204620.png]]

---
## 4. Monthly bills
![[Pasted image 20250227065758.png]]
Giao diện của nằm ở tab Bills

---
## 5. Cost Explorer
![[Pasted image 20250227065928.png]]
Giao diện của Cost Explorer ở tab cùng tên. Cho biết thông tin về thành phần cấu thành nên chi phí trong những tháng trước

---
## 6. Forecast and track costs (Dự báo và theo dõi chi phí)
![[Pasted image 20250227070057.png]]
Giao diện nằm ở tab Bugets.
Như tên gọi thì công cụ có phép dự báo chi phí ước tính trong tháng
và theo dõi - thông báo khi vượt quá ngân sách

---
## 7. Cost and usage reporting
![[Pasted image 20250227070253.png]]
Giao diện ở tab Reports.
cung cấp thông tin các dịch vụ đang sử dụng, giải trình chi tiết về mỗi loại dịch vụ

---
---
# V. Technical support

## 1. AWS Support
Cung cấp sự kết hợp độc đáo giữa công cụ và chuyên môn: 
- AWS Support 
- AWS Support Plans 

Hỗ trợ được cung cấp cho: 
- Thử nghiệm với AWS 
- Sử dụng AWS trong môi trường sản xuất 
- Sử dụng AWS cho các tác vụ quan trọng trong doanh nghiệp

 Hướng dẫn chủ động: 
 - Technical Account Manager (TAM) 
 
  Thực hành tốt nhất: 
  - AWS Trusted Advisor 
  
  Hỗ trợ tài khoản: 
  - AWS Support Concierge

---
## 2. Support plans

AWS Support cung cấp bốn gói hỗ trợ: 
- **Basic Support** – Truy cập Trung tâm Tài nguyên, Bảng điều khiển Tình trạng Dịch vụ, FAQ sản phẩm, diễn đàn thảo luận và hỗ trợ kiểm tra tình trạng hệ thống. 
- **Developer Support** – Hỗ trợ cho giai đoạn phát triển sớm trên AWS. 
- **Business Support** – Dành cho khách hàng chạy khối lượng công việc trong môi trường sản xuất. 
- **Enterprise Support** – Dành cho khách hàng vận hành khối lượng công việc quan trọng đối với doanh nghiệp.

| Basic                                                                      | Developer                                                                   | Business                                                                                    | Enterprise                                                                       |
| -------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Truy cập dịch vụ khách hàng, tài liệu, sách trắng và diễn đàn hỗ trợ 24/7. | Cần hướng dẫn và hỗ trợ kỹ thuật.                                           | Chạy một hoặc nhiều ứng dụng trong môi trường sản xuất.                                     | Tập trung vào quản lý chủ động để tăng hiệu suất và tính sẵn sàng                |
| Truy cập sáu kiểm tra cốt lõi của Trusted Advisor.                         | Đang khám phá cách nhanh chóng triển khai AWS.                              | Kích hoạt nhiều dịch vụ hoặc sử dụng các dịch vụ quan trọng rộng rãi.                       | Xây dựng và vận hành khối lượng công việc theo các phương pháp tốt nhất của AWS. |
| Truy cập Bảng điều khiển Sức khỏe Cá nhân (Personal Health Dashboard).     | Sử dụng AWS cho các khối lượng công việc hoặc ứng dụng không phải sản xuất. | Phụ thuộc vào giải pháp doanh nghiệp để đảm bảo tính sẵn sàng, khả năng mở rộng và bảo mật. | Sử dụng chuyên môn của AWS để hỗ trợ triển khai và di chuyển hệ thống            |
|                                                                            |                                                                             |                                                                                             | Sử dụng **Technical Account Manager (TAM)**, người cung cấp chuyên môn kỹ thuật cho toàn bộ các dịch vụ AWS và có hiểu biết chi tiết về trường hợp sử dụng và kiến trúc công nghệ của bạn. TAM là điểm liên hệ chính cho nhu cầu hỗ trợ liên tục.                                                                                 |

---
## 3. Case severity and response times (Mức độ nghiêm trọng của trường hợp và thời gian phản hồi)
![[Pasted image 20250227072920.png]]



![[Pasted image 20250227080013.png]]