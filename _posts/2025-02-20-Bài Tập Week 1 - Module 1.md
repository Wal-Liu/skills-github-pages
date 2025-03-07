---
title: "Bài Tập Week 1 - Module 1"
date: 2025-03-07
---

---

 # I. Introduction to cloud computing
## Traditional
1. cơ sở hạ tầng phần cứng
2. hardware solution:
	- cần không gian, nhân viên vận hành, bảo vệ, capital expenditure (vốn ban đầu)
	- chu kỳ mua phần cứng dài
	- khi cần thay đổi phải đầu tư lại nhiều
	- cần phải có chuyên môn để vận hành
## Cloud
1. cơ sở hạ cần như phần mềm
2. Software solutions:
	- linh hoạt (muốn lớn nhỏ, thay đổi nhu cầu dễ hơn)
	- việc thay thế nhanh hơn, dễ hơn, tốn ít chi phí hơn phần cứng
	- loại bỏ các nhiêmj vụ nặng không cần thiết trong vận hành
## Cloud service models
xếp theo more - less việc kiểm soát các tài nguyên IT 
1. IaaS (Infrastructure as a service)
2. PaaS (platform as a service)
3. SaaS (Software as a Service)

## Cloud computing deployment models
1. Cloud
	tất cả sẽ được triển khai trên cloud, tất cả các phần trong phần mềm sẽ được chạy trên cloud
2. Hybrid
	kết nối hạ tầng đang có với cloud, việc khiển khai sẽ nằm trên cả cloud và cái đang có 
3. On-premises(private cloud)

## Similarities between AWS and traditional IT
<img src="Paste%20image/20250225093050.png" alt="Mô tả ảnh" width="600">

<img src="../Paste%20image/20250225093050.png" alt="Hình ảnh minh họa" width="500">



--- 
# II. Advanteges of cloud computing
## 1. Trade capital expense for variable expense (thay thế chi phí vốn ban đầu thành chi phí vận hành)
Thay vì phải đầu tư chi phí cho cả data center lớn thì chỉ việc số tiền nhỏ hơn cho chí trên cloud theo từng tài nguyên mà mình sử dụng.

## 2. Massive economies of scale (lợi thế kinh tế theo quy mô lớn)
Khi các nhà cung cấp cloud (AWS, Azure, Google Cloud…) phục vụ hàng triệu khách hàng trên toàn cầu, họ có thể mua phần cứng, duy trì hạ tầng và tối ưu vận hành với chi phí thấp hơn trên mỗi đơn vị tài nguyên. Điều này giúp họ giảm giá thành và cung cấp dịch vụ rẻ hơn so với việc từng công ty tự xây dựng hệ thống riêng.

## 3. Stop guessing capacity (ngừng đoán dung lượng)
- Khi triển khai hệ thống truyền thống, doanh nghiệp phải dự đoán trước lượng tài nguyên (máy chủ, lưu trữ, băng thông…) cần dùng trong tương lai.
- Nếu **dự đoán quá thấp** → Hệ thống quá tải, hiệu suất kém.
- Nếu **dự đoán quá cao** → Lãng phí tài nguyên, chi phí cao.

## 4. Increase speed and agility (Tăng tốc độ và tính linh hoạt)
- Trong hệ thống truyền thống (on-premises), việc **mua sắm, cài đặt và cấu hình** máy chủ có thể mất **vài tuần hoặc vài tháng**.
- Với **cloud**, bạn có thể triển khai tài nguyên **trong vài phút hoặc vài giây** chỉ với vài cú click hoặc API call.

## 5. Stop spending money on running and maintaining data center
## 6. Go global in minute

----
# III. AWS (Amazon Web Service)

## Web service là gì?
- **Web service** là một phần mềm có thể truy cập qua Internet.
- Sử dụng **định dạng tiêu chuẩn** như **XML hoặc JSON** để trao đổi dữ liệu.
- Hoạt động thông qua **API (Application Programming Interface)** để gửi yêu cầu (request) và nhận phản hồi (response).
## AWS là gì?
- **AWS là nền tảng đám mây an toàn** với nhiều dịch vụ toàn cầu.
- **Cung cấp tài nguyên theo yêu cầu** như tính toán, lưu trữ, mạng, cơ sở dữ liệu...
- **Linh hoạt**, dễ dàng mở rộng hoặc thu hẹp theo nhu cầu.
- **Chỉ trả tiền cho dịch vụ sử dụng**, không phải đầu tư trước.
- **Các dịch vụ AWS hoạt động cùng nhau** như các khối xây dựng (building blocks).
## Các loại dịch vụ AWS
![[Pasted image 20250225100021.png]]

## Việc chọn lựa các dịch vụ
việc chọn lựa phụ thuộc vào doanh nghiệp của bản thân, mục dích là gì, các yêu cầu về công nghệ như thế nào

## Các dịch vụ được đề cập trong khoá học
![[Pasted image 20250225100525.png]]

## Các cách để tương tác với AWS
1. AWS management console 
	- Giao diện đồ họa dễ sử dụng.
	- Thích hợp cho người mới bắt đầu hoặc quản lý thủ công.
2. AWS CLI
	- Truy cập dịch vụ AWS bằng các lệnh hoặc script.
	- Hữu ích cho tự động hóa và quản lý nhanh chóng.
3. Software Development KITs (SDKs)
	- Truy cập dịch vụ AWS trực tiếp từ code (Java, Python, v.v.)
	- Dùng để tích hợp AWS vào ứng dụng.

______
# IV. Moving to the AWS Cloud (Cloud Adoption Framework)
**Các góc nhìn của AWS CAF**
**Cung cấp hướng dẫn & best practices** để tổ chức áp dụng cloud hiệu quả.  
**Hỗ trợ toàn bộ vòng đời CNTT**, từ lập kế hoạch đến vận hành.  
**Gồm 6 góc nhìn (perspectives)**, mỗi góc nhìn tập trung vào một khía cạnh quan trọng.  
**Mỗi góc nhìn bao gồm các năng lực (capabilities)** giúp tổ chức hiểu và triển khai cloud tốt hơn.

## 6 góc nhìn chính
### Kinh doanh
1. business
2. people
3. governance (quản lý)
### Công nghệ
1. Platform
2. Sercurity
3. Operations
## 1. Business
**stakeholders:**
- **Business managers** (Quản lý kinh doanh)
- **Finance managers** (Quản lý tài chính)
- **Budget owners** (Chủ sở hữu ngân sách)
- **Strategy stakeholders** (Những người hoạch định chiến lược)

 **Lợi ích của AWS CAF đối với Business Perspective**  
 **Xây dựng case study mạnh mẽ cho việc áp dụng cloud** 
 **Ưu tiên các sáng kiến chuyển đổi cloud** 
**Đảm bảo chiến lược kinh doanh & chiến lược IT phù hợp với nhau** 
 **Tối ưu hóa chi phí và đo lường lợi ích của cloud** 
 **Tóm lại:** Các bên liên quan trong lĩnh vực kinh doanh có thể sử dụng AWS CAF để đảm bảo rằng chiến lược cloud hỗ trợ mục tiêu của doanh nghiệp một cách hiệu quả và bền vững

## 2. People
AWS CAF cho phép các bên liên quan đến con người (nhân sự, người quản lý, người lao động) đánh giá các cấu trúc tổ chức mới, nhu cầu về kỹ năng và quy trình, từ đó có thể xác định những khoảng trống cần được bao phủ. Với kết quả phân tích này, các quyết định ưu tiên hóa đào tạo, tuyển dụng và thay đổi tổ chức có thể được đưa ra, góp phần vào việc xây dựng một tổ chức agile và hiệu suất cao trong quá trình chuyển đổi sang sử dụng AWS.
- **Resource management**: Quản lý nguồn nhân lực.
- **Incentive management**: Quản lý chế độ khen thưởng và động viên.
- **Career management**: Quản lý lộ trình phát triển nghề nghiệp.
- **Training management**: Quản lý đào tạo và nâng cao kỹ năng.
- **Organizational change management**: Quản lý thay đổi trong tổ chức.
**Stakeholders:**
- **Human resources (HR)**: Nhân sự.
- **Staffing managers**: Quản lý tuyển dụng.
- **People managers**: Quản lý con người và văn hóa doanh nghiệp.

## 3. governance (quản lý)
Góc nhìn Quản trị tập trung vào việc quản lý các danh mục đầu tư, chương trình, dự án và đo lường hiệu suất kinh doanh để đảm bảo rằng IT hỗ trợ hiệu quả cho chiến lược kinh doanh.
- **Portfolio management**: Quản lý danh mục đầu tư IT để đảm bảo hiệu suất và giá trị kinh doanh.
- **Program and project management**: Quản lý chương trình và dự án để đảm bảo thực hiện đúng chiến lược.
- **Business performance measurement**: Đo lường hiệu suất kinh doanh để theo dõi tiến độ và giá trị của IT.
- **License management**: Quản lý giấy phép phần mềm, đảm bảo tuân thủ và tối ưu chi phí.

- Nhấn mạnh **tầm quan trọng của việc căn chỉnh giữa kỹ năng và quy trình IT với chiến lược và mục tiêu kinh doanh**.
- **Mục tiêu**: Giúp tổ chức tối đa hóa giá trị kinh doanh từ các khoản đầu tư IT và **giảm thiểu rủi ro kinh doanh**.
Các đối tượng trên có thể sử dụng **AWS CAF** để tập trung vào việc **cải thiện kỹ năng và quy trình** nhằm đảm bảo chiến lược IT hỗ trợ mục tiêu kinh doanh, từ đó tối đa hóa lợi ích từ các khoản đầu tư IT và giảm thiểu rủi ro.
**Stakeholders:**
- **CIO (Chief Information Officer)**: Giám đốc CNTT.
- **Program managers**: Quản lý chương trình.
- **Enterprise architects**: Kiến trúc sư doanh nghiệp.
- **Business analysts**: Chuyên viên phân tích kinh doanh.
- **Portfolio managers**: Quản lý danh mục đầu tư.
## 4. Platform
Góc nhìn Nền tảng tập trung vào việc **cung cấp, quản lý và kiến trúc hóa các tài nguyên IT**, giúp tổ chức xây dựng một nền tảng hạ tầng mạnh mẽ để hỗ trợ hoạt động kinh doanh.
- **Compute provisioning**: Cung cấp tài nguyên tính toán (máy chủ, containers, serverless, v.v.).
- **Network provisioning**: Cấu hình và quản lý mạng (bao gồm VPC, kết nối hybrid, bảo mật mạng).
- **Storage provisioning**: Cung cấp và quản lý lưu trữ (bao gồm block storage, object storage, file storage).
- **Database provisioning**: Cấu hình và quản lý cơ sở dữ liệu (RDBMS, NoSQL, Data Lake, v.v.).
- **Systems and solution architecture**: Thiết kế kiến trúc hệ thống và giải pháp tổng thể.
- **Application development**: Phát triển ứng dụng trên nền tảng đám mây.
**Stakeholders:**
- **CTO (Chief Technology Officer)**: Giám đốc Công nghệ.
- **IT managers**: Quản lý CNTT.
- **Solutions architects**: Kiến trúc sư giải pháp.

## 5. Sercurity
Góc nhìn An ninh tập trung vào **đảm bảo tổ chức đáp ứng các mục tiêu bảo mật**, bao gồm khả năng giám sát, kiểm tra, kiểm soát và linh hoạt trong việc bảo vệ hệ thống CNTT.
- **Identity and access management**: Quản lý danh tính và quyền truy cập.
- **Detective control**: Kiểm soát phát hiện các mối đe dọa.
- **Infrastructure security**: Bảo mật cơ sở hạ tầng.
- **Data protection**: Bảo vệ dữ liệu.
- **Incident response**: Ứng phó sự cố.
**Stakeholders:**
- **CISO (Chief Information Security Officer)**: Giám đốc an ninh thông tin.
- **IT security managers**: Quản lý an ninh CNTT.
- **IT security analysts**: Chuyên viên phân tích an ninh CNTT.
**Mục đích:**
- Nhấn mạnh rằng **tổ chức cần đảm bảo đáp ứng các mục tiêu bảo mật**.
- Điều này giúp bảo vệ hệ thống và dữ liệu khỏi các rủi ro bảo mật.

## 6. Operations
- Hỗ trợ và điều phối các **hoạt động hàng ngày, hàng quý, hàng năm** của doanh nghiệp.
- Định nghĩa các **quy trình vận hành** để đảm bảo hoạt động ổn định và linh hoạt trên đám mây.
- Xác định các thay đổi quy trình và **các chương trình đào tạo cần thiết** để chuyển đổi thành công.
- **Giám sát dịch vụ (Service Monitoring)**  
- **Giám sát hiệu suất ứng dụng (Application Performance Monitoring)**  
- **Quản lý tài nguyên (Resource Inventory Management)**  
- **Quản lý và triển khai thay đổi (Release Management/Change Management)** 
- **Báo cáo và phân tích dữ liệu (Reporting & Analytics)**  
- **Đảm bảo liên tục kinh doanh/Khôi phục thảm họa (Business Continuity/ Disaster Recovery)**  
- **Danh mục dịch vụ CNTT (IT Service Catalog)**
**Stakeholders**
- IT Operations Managers
- IT Support Managers
**Ý nghĩa của Operations Perspective**
- Giúp các **nhà quản lý vận hành** đảm bảo hoạt động **ổn định, tối ưu, và linh hoạt** trên môi trường cloud.  
- Định nghĩa quy trình vận hành **hiện tại và tương lai** để phù hợp với mô hình điện toán đám mây.  
- Hỗ trợ doanh nghiệp **phát hiện và điều chỉnh** các quy trình cần thay đổi để chuyển đổi lên cloud hiệu quả.
--- 
# V. Tóm tắt
Trong bài đã đề cập đến:
1. Xác định các loại mô hình điện toán đám mây khác nhau
2. Mô tả sáu lợi thế của điện toán đám mây
3. Nhận biết các danh mục dịch vụ AWS chính và các dịch vụ cốt lõi
4. Xem lại  AWS Cloud Adoption Framework (AWS CAF)
## Exam 
Why is AWS more economical than traditional data centers for applications with varying compute workloads? (Tại sao AWS lại tiết kiệm hơn các trung tâm dữ liệu truyền thống đối với các ứng dụng có khối lượng công việc tính toán khác nhau?)
A Amazon Elastic Compute Cloud (Amazon EC2) costs are billed on a monthly basis.
Chi phí Amazon Elastic Compute Cloud (Amazon EC2) được thanh toán hàng tháng.
B Customers retain full administrative access to their Amazon EC2 instances.
Khách hàng vẫn giữ toàn quyền truy cập quản trị vào các phiên bản Amazon EC2 của họ.
C Amazon EC2 instances can be launched on - demand when needed.
Các phiên bản Amazon EC2 có thể được khởi chạy theo yêu cầu khi cần.
D Customers can permanently run enough instances to handle peak workloads.
Khách hàng có thể chạy đủ phiên bản để xử lý khối lượng công việc cao điểm.
**The correct answer is:** C. Amazon EC2 instances can be launched on - demand when needed
