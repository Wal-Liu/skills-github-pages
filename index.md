---
title: Welcome to my blog
---

---

---
---
Em chào thầy, em có ghi chú lại những kiến thức bằng phần mềm obsidian, 1 phần mềm viết bằng markdown nên có thể sẽ khó nhìn nếu mở bằng editor bình thường, bên cạnh đó có 1 số hình chụp lại công thức của các phương pháp hồi quy. em mong thầy thông cảm ạ 
___

# Một số khái niệm cơ bản
1. tool thu thập dữ liệu trên cơ sở dữ liệu theo thời gian thực: Azure Stream Analytics 
2. khi dữ liệu bị thiếu ta có thể nội suy để điền vào chỗ trống, nếu như ngày tháng thì sẽ rất đơn giản nhưng với dữ liệu không thể nội suy như dữ liệu bán hàng, dữ liệu phát tờ rơi sẽ dùng chiến lược khác( điền số trung bình) nếu điền vào số 0 sẽ ảnh hưởng rất lớn khi thống kê dữ liệu 

# Các câu hỏi có thể đặt ra khi phân tích dữ liệu:
1. Câu hỏi mô tả: Tôi đã bán được bao nhiêu đồ uống, doanh thu bao nhiêu
2. Mối tương quan: yếu tố nhiệt độ có ảnh hướng đến doanh thu hay không
3. Câu hỏi so sánh: so sánh giữa các mặt hàng
4. Câu hỏi về tính dự đoán: dùng các phép liên kết và so sánh từ đó dự đoán về số lượng bán ra, doanh thu hoặc số lượng tờ rơi

# Khái niệm cơ bản về biểu đồ
1. biểu đồ Gee Whiz về bản chất là biểu đồ box and whisker chart (Biểu đồ hộp và dải dữ liệu trung bình) 
2. PivotTable và PivotChart là cái tool để cắt lát dữ liệu ra, xào nấu như kiểu muốn cột nào hàng nào, nhìn rõ hơn là doanh số theo ngày hay doanh dố theo nhiệt độ 

# Các loại biến số
## 1. Biến liên tục 
vd: nhiệt độ
## 2. Biến rời rạc
vd: số tờ rơi 
Biến số rời rạc là biến số thường hay đếm thay vì tính toán 
## 3. Biến phân loại 
vd location ở đâu park beach .....
thì mình sẽ đánh nhãn ví dụ 1 là biển 2 là công viên 3 là trường học

# Xu Hướng tập trung
## 1. Trung bình x 
trung bình trong toán bình thường
## 2. Trung vị
là số chính giữa nhất Md = n+1 /2
ví dụ MD là 5 thì 5 không phải là giá trị trung vị mà giá trị thứ 5 trong bộ dữ liệu đã được sắp xếp theo thứ tự và giá trị thứ 5 là giá trị trung vị
## 3. Yếu vị M0
số xuất hiện nhiều nhất, số phổ biến nhất
để xét 1 bộ dữ liệu được phân phối chuẩn thì thường nhìn vào 3 giá trị trên để đánh giá, nếu nó hút cao lên ở giữa và phân phối đều ở 2 bên là khá đẹp 
nếu 3 số tụ lại 1 chỗ thì phân phối chuẩn
nếu có số lệch thì là lệch phải / lệch trái

# Phương sai
## Range 
max - min phạm vi giá trị phân tán từ đâu tới đâu
## Variance (Phương sai)
## Standard Deviation ( độ lệch chuẩn)
là căn bậc 2 của phương sai
trong 1 phân phối chuẩn 68,2% độ lệch chuaản là +-1
95,4% là +-2 gần như 99,7 +-3 
để hiểu dữ liệu phân bố như thế nào quanh số trung bình 
## Sai số chuẩn
ước lượng được số giá trị trung bình được tính ra gần số trung bình đến mức nào 

# Thống kê mô tả trong excel 
## yếu vị
nếu giá trị không khả dụng là do không có giả trị phổ biển hơn 
## kurtosis ( độ nhọn)
ước tính về tính chuẩn của dữ liệu 
giá trị càng gần 0 thì càng phân phối chuẩn
## Skewness (độ lệch)
biểu bị phần đuôi của phân phối 
nếu dương lệch phải âm lệch trái
Nếu cả 2 chỉ số đều nằm trong khoảng +- 2 thì dữ liệu phân phối bình thường 

# Thống kê kết hợp 
## hệ số tương quan (correlation )
luôn trong khoảng -1 -> +1 giá trị càng gần 1 thì các biến số càng liên quan với nhau 
nếu hệ số tương quan dướng thì đồng biến 
nếu hệ số tương quan âm thì nghịch biến
 xét mối tương quan giữa 3 biến: giá cả, nhiệt độ, số lượng tờ rơi 
 nếu tăng giá => số lượng bán ra giảm
 nhiệt độ thay đổi => số lượng không thay đổi nhiều 
 tờ rơi nhiều hơn => số lượng bán ra tăng
 ### tương quan giả
 2 biến có thể tương quan với nhau vd: số lượng tờ rơi tăng thì nhiệt độ tăng
 nhưng nguyên nhân là nhân số thứ 3 làm cho 2 biến trên vô tình tương quan với nhau 
 => khi có hệ số tương quan lớn, không có nghĩa 2 biến đó tồn tạiquan hệ nguyên nhân kết quả 
# Kiểm định giả thuyết
## Giả thuyết được hình thành nên từ gì
có 2 loại giả thuyết trong thống kê:
1. giả thuyết không (đó chỉ là ngẫu nhiên, không có ý nghĩa) 
2. giả thuyết thay thế 
giả thuyết thay thế đưa ra ý tưởng, có thể đưa ra 3 lạo giả thuyết thay thế: lớn hơn, nhỏ hơn hoặc không biết khác nhau như thế nào, chỉ biết là có khác nhau 
chỉ số sai p thường p= 0.05 => 5% 
đây là lỉ lệ phần trăm sai sót vd có 5% sai sót do ngẫu nhiên 

# Phép thống kê thông dụng để so sánh các bộ dữ liệu khác nhau 
có 4 loại 
## 1. Kiểm định T tests trung bình 1 mẫu (kiểm định Z Test)
ví dụ: có dữ liệu bán hành trong 5 năm 
trung bình trong tháng 7 5 năm qua là 120 
lấy (giá trị trung bình của mẫu hiện tại - số có từ các mẫu trước) / sai số chuẩn 
Bậc tự do: số để xác định trị số đó có quan trọng về mặt thống kê hay không 
![[Pasted image 20250222071926.png]]

Về cơ bản phép toán Z test mà T test là như nhau 
z test giả định rằng bạn đã sẵ 1 số thông tin tổng thể (thứ là T có thể k có )
## 2. Kiểm định T test trung bình 2 mẫu 
![[Pasted image 20250222081117.png]]

t Critical one-tail: giá trị tới hạn là 1.67 
t Critical two-tail: giá trị tới hạn phải lớn hơn 1.67 

## 3. Kiểm định T Test cặp đôi
![[Pasted image 20250222082522.png]]

# Phân tích phương sai (Analysis of variance - ANOVA)
vấn đề: bán nước ở biển và công viên vậy có sai phân ở địa điểm hay không 
Phương pháp anova cho phép thực hiện nhiều kiểm định T-tests cùng 1 lúc từ đó nắm được điều gì đang diễn ra trong tổng thể
Phương pháp Anova phân chia sai số và phương sai theo cách để mình hiểu điều gì có ý nghĩa thống kê 

# hồi quy 
## Ý tưởng:
mình có 1 số biến hoặc đặc tính mà muốn biết
vd tờ rơi giá cả, nhiệt độ
giờ mình phải tạo cái hàm có 3 biến là 3 cái trên để tính ra được kết quả 
F(tờ rơi, nhiệt độ giá cả) = số lượng bán được 
=> hồi quy cho biết hàm của x sẽ phù hợp nhất với biểu diễn dữ liệu nào 
## hồi quy tuyến tính 
 hệ số chặn (i) là một hằng số để dự đoán kết quả nhận được
 note: trong excel phải chọn chính xác vùng chứ k có chọn nguyên cột được
Residuals ( phần dư)
Standardized residuals (phần dư chuẩn hoá)
Residual Plot (đồ thị phần dư)
Line fit plot (đồ thị đường thẳng)