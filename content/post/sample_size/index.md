---
authors:
- admin
categories:
date: "2022-03-04"
draft: false
featured: false
image:
  caption: ''
  focal_point: ""
  placement: 2
  preview_only: false
lastmod: "2022-03-04"
projects: []
subtitle: 
summary: Bài viết này sẽ tóm tắt những nguyên tắc và khái niệm chung trong việc tính toán cỡ mẫu cho một nghiên cứu. (I will summarize the key points of calculating sample size for a study in this post).
tags:
- Sample size
title: Ước lượng cỡ mẫu (Sample size calculation)
---

## 1.  Tầm quan trọng của việc tính cỡ mẫu

Nghiên cứu khoa học là một quá trình thiết kế, thu thập, phân tích và diễn giải kết quả nhằm trả lời cho một hoặc nhiều câu hỏi hoặc chứng minh giả thuyết nhất định. Sẽ là lý tưởng nếu nghiên cứu có thể thu thập thông tin trên toàn bộ đối tượng đích, tuy nhiên trên thực tế rất khó hoặc không thể làm được điều này vì nhiều lý do như tính khả thi, nguồn lực và cả vấn đề đạo đức. Do đó một công trình nghiên cứu thường sẽ tiến hành trên một nhóm nhỏ hơn, gọi là mẫu. Từ số liệu thu thập được trên mẫu đó, nhà nghiên cứu sẽ tiến hành phân tích và suy diễn kết quả ra dân số đích. Cũng chính vì vậy mà chúng ta phải ước lượng cỡ mẫu cho nghiên cứu


Việc ước lượng cỡ mẫu cho nghiên cứu là một việc quan trọng. Số lượng mẫu ảnh hưởng tới sai số ngẫu nhiên của nghiên cứu. Nếu một nghiên cứu thu thập số liệu trên một mẫu không đủ lớn thì độ chính xác của các phép tính toán sẽ giảm, từ đó ảnh hưởng tới việc suy diễn kết quả, thậm chí không thể đưa ra được kết luận. Ngược lại, một nghiên cứu tiến hành trên một số lượng mẫu quá lớn so với cần thiết thì mặc dù mang lại tính chính xác trong tính toán nhưng lại hoang phí về nguồn lực. Bên cạnh đó, số lượng người tham gia nghiên cứu cũng nhiều hơn so với cần thiết. Điều này đặc biệt thấy rõ trong nghiên cứu can thiệp, việc tiến hành trên mẫu lớn hơn cần thiết dẫn tới nhiều đối tượng nghiên cứu phải phơi nhiễm với nguy cơ liên quan tới can thiệp, điều này rõ ràng cũng vi phạm vấn đề đạo đức.


Bài viết này nhằm mục đích giải thích các yếu tố liên quan tới việc tính cỡ mẫu, quy trình và lựa chọn các thông số phù hợp thông qua một số công thức tính cỡ mẫu cụ thể. Việc hiểu được nguyên tắc rất quan trọng, vì khi đó chúng ta có thể lựa chọn một cách linh hoạt công thức tính cỡ mẫu phù hợp cho nghiên cứu. Hơn nữa, trong một số trường hợp, thường là một vấn đề quá phức tạp hoặc một thiết kế nghiên cứu mới, không có công thức sẵn có, nhà nghiên cứu phải tiến hành ước lượng cỡ mẫu dựa vào mô phỏng, khi đó bắt buộc nhà nghiên cứu phải nắm được các khái niệm liên quan tới cỡ mẫu.


## 2.  Các yếu tố liên quan tới tính cỡ mẫu

### Xác suất sai lầm loại 1, xác suất sai lầm loại 2 và lực thống kê

Để hiểu về các khái niệm xác suất sai lầm loại 1, xác suất sai lầm loại 2 và lực thống kê, trước tiên cần phải hiểu khái niệm kiểm định giả thuyết thống kê (Null Hypothesis Significance Testing – NHST) . Trong quy trình kiểm định giải thuyết thống kê, bước đầu tiên là cần đặt ra một giải thuyết vô hiệu (null hypothesis - H0), giả thuyết H0 là một giả thuyết “âm tính”, giả định các nhóm là không có khác biệt, không có mối liên quan. Ví dụ khi so sánh sự khác biệt về hiệu quả trong điều trị của phác đồ mới và phác đồ cũ, giả thuyết H0 được đặt ra là hiệu quả của phác đồ mới và phác đồ cũ là tương đương nhau, hay không khác biệt. Sau đó đặt ra một giả thuyết thay thế (alternative hypothesis – HA), giả thuyết HA là một giả thuyết “dương tính” rằng có sự khác biệt, có mối liên quan. Trong ví dụ trên, HA được đặt ra là hiệu quả trong điều trị của phác đồ mới và phác đồ cũ là khác nhau.


Sau khi đặt ra các các giả thuyết H0 và HA, tình huống sẽ trở thành việc chứng minh H0 hay HA đúng. Theo lý thuyết của kiểm định giả thuyết thống kê, chúng ta rất khó hoặc không thể trực tiếp chứng minh một giả thuyết là đúng mà chỉ có thể chứng minh nó sai (bác bỏ), theo đó nếu có đủ bằng chứng cho thấy H0 sai thì chúng ta bác bỏ giả thuyết H0 và chấp nhập HA, ngược lại nếu không đủ bằng chứng để bác bỏ H0 thì chúng ta chấp nhận rằng H0 đúng. Việc quyết định bác bỏ hay chấp nhận H0 thường được thực hiện thông qua chỉ số P (P-value), chỉ số P là một xác suất có điều kiện mang ý nghĩa là xác suất quan sát được giá trị thống kê và những trường hợp hiếm hơn (hướng về giả thuyết thay thế) nếu giả thuyết H0 đúng. Theo đó nếu chỉ số P nhỏ hơn mức ý nghĩa (α) thì chúng ta có thể kết luận có bằng chứng bác bỏ H0 và chấp nhận HA, ngược lại khi P lớn hơn α, chúng ta kết luận không đủ bằng chứng bác bỏ H0.


Thống kê là khoa học dựa vào nguyên lý xác suất, các kết luận đều được diễn giải trong một số giả định hoặc sai số quy ước (chấp nhận được). Khi kết luận chấp nhận hay bác bỏ H0, chúng ta đều có thể gặp phải những sai số tiềm tàng, và sai số này được chấp nhận trong một khoảng quy ước. 

* Sai lầm thứ nhất mà nhà nghiên cứu có thể gặp phải là quyết định bác bỏ H0 nhưng trên thực tế H0 là đúng. Sai lầm này gọi là sai lầm loại 1 (type 1 error). Sai lầm loại 1 còn có thể hiểu là *“dương tính giả”*. 
* Sai lầm thứ 2 có thể gặp phải đó là khi giả thuyết H0 sai nhưng chúng ta lại chấp nhận là đúng. Sai lầm này được gọi là sai lầm loại 2 (type 2 error) hay β. Sai lầm loại 2 còn có thể hiểu là *“âm tính giả”*
* Khi biết được sai lầm loại 2, chúng ta có thể xác định lực thống kê (power) bằng cách lấy 1 trừ xác suất sai lầm loại 2, hay power = 1 – β. Lực thống kê chính là xác suất bác bỏ giả thuyết H0 (chấp nhận HA) khi giả thuyết H0 sai, hay có thể hiểu lực thống kê chính là xác suất dương tính thật.

**Bảng 1: Sai lầm loại 1 và loại 2 và lực thống kê**

![](table1.jpg)

Có thể thấy rằng mỗi lần kết luận thống kê đều không chính xác 100% mà đều có thể mắc sai lầm tiềm tàng. Nếu kết luận có mối liên quan, sự khác biệt, nhà nghiên cứu có thể mắc sai lầm loại 1, nếu kết luận không có mối liên quan, không có sự khác biệt thì có thể mắc sai lầm loại 2. Việc lựa chọn xác suất sai lầm loại 1 và 2 tùy vào lĩnh vực nghiên cứu, tình huống nghiên cứu cụ thể. Thông thường xác suất sai lầm loại 1 được mặc định chấp nhận ở mức 5%, nhưng trong một số tình huống cụ thể mức này có thể đặt ở 10% hoặc 1%, chú ý là khi lựa chọn 10% hay 1%, nhà nghiên cứu phải có bằng chứng chứng minh cho sự lựa chọn của mình. Xác suất sai lầm loại 1 ở 5% có nghĩa là nếu thực sự không có sự khác biệt (ví dụ hiệu quả giữa 2 loại thuốc) thì trong 100 nghiên cứu giống nhau, có 5% (5 lần) nghiên cứu kết luận có sự khác biệt giữa 2 loại thuốc. Xác suất sai lầm loại 2 thường được đặt ở mức 20%, tuy nhiên trong tình huống cụ thể, nhà nghiên cứu có thể thiết lập ở mức khác nhưng không nên đặt β nhỏ hơn α vì khi đó vai trò của H0 và HA bị thay đổi. Xác suất sai lầm loại 2 ở 20% có nghĩa là nếu thực sự có sự khác biệt (ví dụ về hiệu quả giữa 2 loại thuốc) thì trong 100 nghiên cứu giống nhau, có 20% (20 lần) nghiên cứu kết luận không có sự khác biệt về hiệu quả giữa hai loại thuốc. Như đã đề cập ở trên, việc lựa chọn α hay β không phải luôn cố định là 5% và 20% tương ứng. Ví dụ trong trường hợp nhà nghiên cứu muốn chứng minh hiệu quả của một thuốc mới và thận trọng hơn khi kết luận sự khác biệt của loại thuốc mới này so với loại thuốc cũ, thì nhà nghiên cứu có thể lựa chọn xác suất sai lầm loại 1 nhỏ hơn (ví dụ α = 1%), khi đó với kết luận thuốc mới có hiệu quả khác biệt với thuốc cũ thì xác suất mà thuốc mới không khác biệt với thuốc cũ chỉ là 1%.

Một yếu tố rất quan trọng trong kết luận thống kê và cũng được nhiều nhà nghiên cứu quan tâm là lực thống kê. Như đã đề cập, lực thống kê là xác suất kết luận có sự khác biệt khi thực sự có sự khác biệt, hay lực thống kê biểu hiện cho khả năng phát hiện hiệu ứng khi nó thực sự tồn tại. Như vậy, nhà nghiên cứu đều mong muốn có được lực thống kê cao. Một nghiên cứu sẽ được đánh giá không cao nếu không đạt được lực thống kê cần thiết, thậm chí là không thể đưa ra kết luận nếu không đủ lực thống kê. Theo nguyên lý của [kiểm định giả thuyết thống kê (Hypothesis testing) của Neyman và Pearson](https://www.frontiersin.org/articles/10.3389/fpsyg.2015.00223/full), có 3 trường hợp kết luận thống kê:

* Nếu giá trị thống kê (z, t, χ2, F…) nằm trong vùng bác bỏ H0, chúng ta bác bỏ H0 và chấp nhận HA
* Nếu giá trị thống kê (z, t, χ2, F…) nằm trong vùng chấp nhận H0, và có đủ lực thống kê, chúng ta chấp nhận H0
* Nếu giá trị thống kê (z, t, χ2, F…) nằm trong vùng chấp nhận H0, và không có đủ lực thống kê, chúng ta không thể kết luận được gì. Vì khi đó chúng ta không thể quyết định là sự không khác biệt đó là do thực sự không có khác biệt hay do phép tính toán không đủ khả năng để phát hiện khác biệt

Như vậy lực thống kê đóng vai trò rất lớn cho tính giá trị của một kết luận thống kê. Trong thực hành, lực thống kê thường được quy ước là không nhỏ hơn 80%. Do đó, trong quá trình tính cỡ mẫu, nhà nghiên cứu cần phải tính toán cỡ mẫu để đáp ứng được điều này.


### Cỡ tác động (effect size)


Trong kiểm phương pháp kiểm định giả tuyết thống kê, giá trị P thường được sử dụng để kết luận sự khác biệt giữa các nhóm có ý nghĩa về mặt thống kê hay không. Việc kết luận dựa vào giá trị P mang ý nghĩa nhị phân – có/không có ý nghĩa thống kê, giá trị P không nói lên được mức độ của sự khác biệt. Trong thực hành, bên cạnh việc kết luận có hay không khác biệt, chúng ta cần biết mức độ khác biệt là bao nhiêu, và cỡ tác động (effect size) là thể hiện mức độ khác biệt đó. Cỡ tác động là một thuật ngữ chung để chỉ các chỉ số khác nhau nhằm đo lường mức độ khác biệt giữa các nhóm, ví dụ khi so sánh huyết áp tâm thu giữa 2 nhóm dân số thì cỡ tác động chính là sự chênh lệch huyết áp tâm thu trung bình giữa 2 nhóm đo bằng đơn vị mmHg, hoặc khi thể hiện sự liên quan giữa cân nặng và chiều cao thì hệ số tương quan cũng là cỡ tác động. Đối với những nghiên cứu dịch tễ học có biến đo lường kết quả là biến nhị giá thì các chỉ số như tỉ số nguy cơ RR, tỉ số số chênh OR hay tỉ lệ hiện hành PR cũng đo lường mức độ sự khác biệt và được hiểu là cỡ tác động.


Cỡ tác động ảnh hưởng trực tiếp đến cỡ mẫu của một nghiên cứu, và thường là một thành phần trong công thức tính cỡ mẫu, cỡ tác động càng lớn (sự khác biệt giữa các nhóm càng lớn) thì cần ít mẫu hơn để phát hiện sự khác biệt này. Ngược lại nếu cỡ tác động nhỏ, chúng ta cần một cỡ mẫu lớn hơn. Một nhược điểm của cỡ tác động là khó so sánh kết quả nếu đơn vị đo lường khác nhau, ví dụ chúng ta sẽ khó so sánh sự khác biệt giữa chiều cao so với sự khác biệt về cân nặng. Một nhược điểm khác của cỡ tác động là không nói lên được mức độ giao động. Ví dụ sự khác biệt về chiều cao giữa 2 nhóm dân số của nghiên cứu thứ nhất (trung bình ± độ lệch chuẩn) là 3 ± 1 cm sẽ rất khác so với nghiên cứu thứ 2 là 3 ± 5 cm, mặc dù sự khác biệt trung bình giữa 2 nhóm dân số của 2 nghiên cứu đêu là 3 cm. Do đó để có thể so sánh được các cỡ tác động với đơn vị đo lường khác nhau và tính toán đến sự giao động về kết quả, cỡ tác động chuẩn hóa (standardized effect size) được tính đến. [Công thức tính cỡ tác động chuẩn hóa theo Cohen](https://www2.psych.ubc.ca/~schaller/528Readings/Cohen1992.pdf) như sau:


<img src="http://latex.codecogs.com/svg.latex?effect&space;size&space;=&space;\frac{mean_1_&space;-&space;mean_2_}{SD}" title="http://latex.codecogs.com/svg.latex?effect size = \frac{mean_1_ - mean_2_}{SD}" />


Từ công thức trên, có thể thấy cỡ tác động chuẩn hóa không phụ thuộc vào đơn vị của đo lường của biến số. Đơn vị của cỡ tác động chuẩn hóa là độ lệch chuẩn, ví dụ d = 1 có nghĩa là sự khác biệt trung bình giữa 2 nhóm là 1 độ độ lệch chuẩn. Tác giả Cohen chia cỡ tác động chuẩn hóa thành các ngưỡng [0.2 là *“thấp”*, 0.5 là *“trung bình”*, và > 0.8 là *“cao”*](https://www2.psych.ubc.ca/~schaller/528Readings/Cohen1992.pdf).


Cỡ tác động thường được tham khảo từ những nghiên cứu tương tự đã được làm trước đó. Tuy nhiên, khi thực hiện một nghiên cứu mới và không có thông tin tham khảo được từ nghiên cứu trước thì nhà nghiên cứu cũng có thể dựa vào kinh nghiệm lâm sàng, để lựa chọn ngưỡng thấp, trung bình hay cao vì cỡ tác động phản ảnh sự khác biệt quan sát được trên thực tế.


### Hệ số thiết kế (design effect)

Như đã đề cập ở phần trên, việc tính cỡ mẫu phải phù hợp với thiết kế nghiên cứu. Các công thức tính cỡ mẫu thường được áp dụng với giả định đối tượng nghiên cứu được chọn một cách ngẫu nhiên. Trong các nghiên cứu lấy mẫu cụm, thường có thêm tác động của yếu tố cụm, ảnh hưởng tới tính ngẫu nhiên của các đối tượng nghiên cứu. Ví dụ nghiên cứu chọn đơn vị cụm là lớp học hoặc xã, huyện thì những học sinh trong cùng một lớp hoặc những người dân trong cùng một xã, một huyện thường có những đặc điểm giống nhau và khác so với học sinh lớp khác hoặc cư dân trong xã, huyện khác. Hay nói cách khác, những đối tượng nghiên cứu trong phương pháp chọn mẫu cụm là không ngẫu nhiên hoàn toàn. Nếu khi gộp dữ liệu lại và coi như việc chọn mẫu là ngẫu nhiên thì kết quả ước lượng không còn phù hợp. Để giải quyết vấn đề này, đối với các nghiên cứu chọn mẫu cụm, công thức tính cỡ mẫu cần phải được nhân với hệ số thiết kế (design effect). Việc nhân cỡ mẫu với hệ số thiết kế sẽ làm cho cỡ mẫu tăng lên để bù trừ cho ảnh hưởng của việc chọn mẫu cụm.

Tuy nhiên làm sao để tính được hệ số thiết kế phù hợp. Tương tự như ước lượng cỡ mẫu, việc tính toán hệ số thiết kế cũng phụ thuộc vào từng nghiên cứu, không có con số cố định cho tất cả các nghiên cứu. Trước tiên cần hiểu tác động của việc chọn mẫu cụm là như thế nào. Có thể hiểu đơn giản như sau, ví dụ đơn vị cụm được chọn là lớp học, giả định ngẫu nhiên cho rằng các học sinh trong lớp này là hoàn toàn độc lập với nhau hay hoàn toàn không bị ảnh hưởng bởi yếu tố lớp học. Tuy nhiên, trên thực tế những học sinh học chung một lớp thường sẽ bị ảnh hưởng bởi một số yếu tố như nội quy lớp học, giáo viên chủ nhiệm, học lực chung… dẫn tới những học sinh này sẽ có một số đặc điểm “đặc trưng” cho lớp đó so với các học sinh ở lớp khác. Một cách phổ quát hơn, những đối tượng nghiên cứu trong một cụm sẽ có sự tương đồng nhất định so với đối tượng nghiên cứu ở cụm khác. Một chỉ số đo lường mức độ tương đồng của các cá thể trong một cụm là chỉ số tương quan trong nhóm – ICC (Intra-class Correlation Coefficient). Khi đó hệ số thiết kế sẽ được tính bằng công thức:


<img src="http://latex.codecogs.com/svg.latex?DE&space;=&space;1&space;&plus;&space;ICC(k&space;-&space;1)" title="http://latex.codecogs.com/svg.latex?DE = 1 + ICC(k - 1)" />


Trong đó, k là số lượng đối tượng nghiên cứu được chọn trong mỗi cụm.

Có thể thấy rằng, hệ số thiết kế phụ thuộc vào 2 yếu tố: i) mức độ tương quan của các cá thể trong một cụm, được đo lường bằng hệ số ICC và ii) số lượng cá thể được chọn trong mỗi cụm - k. Hệ số ICC có giá trị từ 0 đến 1, với 0 có nghĩa là các cá thể trong cùng một cụm không có tương đồng gì với nhau, hay độc lập hoàn toàn, trường hợp này hệ số thiết kế sẽ bằng 1 và công thức tính cỡ mẫu không có gì thay đổi so với việc chọn mẫu ngẫu nhiên đơn hay ngẫu nhiên hệ thống. Với hệ số ICC bằng 1 có nghĩa là các cá nhân trong cùng 1 cụm là hoàn toàn tương đồng, hoàn toàn giống nhau khi đó hệ số thiết kế chính bằng số lượng cá thể được chọn trong mỗi cụm. Hệ số ICC có thể tính được trực tiếp từ các nghiên cứu trước thông qua phân tích phương sai (phương sai giữa các nhóm và phương sai trong nhóm), bằng công thức:

<img src="http://latex.codecogs.com/svg.latex?ICC&space;=&space;\frac{\sigma_{between}}{\sigma_{within}&space;&plus;&space;\sigma_{between}}" title="http://latex.codecogs.com/svg.latex?ICC = \frac{\sigma_{between}}{\sigma_{within} + \sigma_{between}}" />

 Tuy nhiên, trong thực tế thường không đủ thông tin để tính trực tiếp ICC từ công thức trên, để dễ dàng tính toán hệ số thiết kế, hệ số ICC được phân chia thành các mức độ: tương quan rất thấp (0 < ICC ≤ 0.01), tương quan trung bình (0.01 < ICC ≤ 0.03), tương quan mạnh (0.03 < ICC ≤ 0.05) và tương quan rất mạnh (ICC > 0.05). Việc lựa chọn ICC như thế nào cho phù hợp phải phụ thuộc vào từng nghiên cứu và kinh nghiệm của nhà nghiên cứu. Ví dụ một nghiên cứu sử dụng phương pháp chọn mẫu cụm, và 35 người được chọn từ mỗi cụm (k = 35), với giả định rằng các cá nhân trong mỗi cụm có tương quan với nhau ở mức cao, nhà nghiên cứu lựa chọn ICC bằng 0.05, hệ số thiết kế sẽ bằng 1 + 0.05(35 – 1) = 2.7. Như vậy cỡ mẫu ban đầu phải nhân thêm cho 2.7 lần để phù hợp với việc chọn mẫu cụm đối với nghiên cứu này.

 Một điều chú ý khác, dựa vào công thức tính hệ số thiết kế, nếu muốn cỡ mẫu nhỏ hơn (DE nhỏ hơn) thì cần giảm số lượng cá thể cần lấy trong mỗi cụm, dẫn tới việc cần phải chọn nhiều cụm hơn. Ngược lại, nếu chọn nhiều cá thể trong mỗi cụm thì số lượng cụm cần lấy sẽ giảm nhưng cỡ mẫu tổng cộng sẽ tăng lên


 ### Tỉ số mẫu giữa các nhóm

Trong các nghiên cứu so sánh giữa các nhóm, thường các nhóm sẽ có cỡ mẫu giống nhau. Tuy nhiên, tùy vào hoàn cảnh nghiên cứu mà nhà nghiên cứu có thể thay đổi tỉ số mẫu giữa các nhóm. Ví dụ nghiên cứu thử nghiệm lâm sàng so sánh hiệu quả của một loại thuốc mới so với giả dược thì không nhất thiết phải chọn tỉ số mẫu là 1:1 mà có thể lựa chọn tỉ lệ một ca sử dụng thuốc và nhiều ca đối chứng bằng giả dược. Việc tăng tỉ số mẫu giữa các nhóm làm tăng cỡ mẫu chung. Công thức hiệu chỉnh tỉ số mẫu giữa các nhóm 

<img src="http://latex.codecogs.com/svg.latex?N_{HC}&space;=&space;\frac{N(1&plus;k)}{4k}" title="http://latex.codecogs.com/svg.latex?N_{HC} = \frac{N(1+k)}{4k}" />

Trong đó k là tỉ số giữa 2 nhóm. Ví dụ một nghiên cứu bệnh chứng tính ra được cỡ mẫu ban đầu là 400 (200 ở mỗi nhóm, bệnh và chứng). Tuy nhiên vì khó khăn trong việc tìm người trong nhóm bệnh, nhà nghiên cứu quyết định tăng tỉ lệ giữa các nhóm thành 1 ở nhóm bệnh và 2 ở nhóm chứng. Như vậy cỡ mẫu sau khi hiệu chỉnh là 400x9/8 = 450, trong đó 150 ở nhóm bệnh và 300 ở nhóm chứng.

Dựa vào công thức trên, ta có thể thấy rằng lựa chọn tỉ số cỡ mẫu ở nhóm chứng cũng không nên cao quá 4 lần so với nhóm can thiệp/bệnh, vì khi đó độ chính xác không tăng lên mà sẽ tiêu tốn nguồn lực nghiên cứu



### Hiệu chỉnh đối với quần thể hữu hạn (Finite population correction)


Các công thức tính cỡ mẫu đều mặc định quá trình lấy mẫu là một quá trình có hoàn trả và kích cỡ dân số đích đủ lớn để coi là lấy mẫu có hoàn trả. Trong trường hợp kích cỡ dân số đích nhỏ, chúng ta có thể hiệu chỉnh cho phù hợp. Việc hiệu chỉnh này giúp cho giảm sự hao phí nguồn lực do phải chọn cỡ mẫu lớn hơn cần thiết mà vẫn giữ được tính đại diện của mẫu. Công thức hiệu chỉnh theo kích cỡ dân số đích:

<img src="http://latex.codecogs.com/svg.latex?N_{HC}&space;=&space;\frac{N&space;*&space;N_{population}}{N&space;&plus;&space;N_{population}}" title="http://latex.codecogs.com/svg.latex?N_{HC} = \frac{N * N_{population}}{N + N_{population}}" />


### Hiệu chỉnh tỷ lệ không trả lời, bỏ cuộc

Ước lượng cỡ mẫu từ các công thức tính cỡ mẫu sẽ cho chúng ta cỡ mẫu cần có (cuối cùng) trong nghiên cứu. Tuy nhiên, việc tính cỡ mẫu cần phải dự trù cho khả năng đối tượng nghiên cứu từ chối tham gia, hoặc bỏ ngang trong quá trình nghiên cứu để đảm bảo có được cỡ mẫu cuối cùng cần thiết. Tùy vào tình huống cụ thể mà có thể lựa chọn tỉ lệ mất mẫu cho phù hợp. Thông tin này thường được tham khảo từ những nghiên cứu trước đó trên đối tượng nghiên cứu tương tự. Số lượng cỡ mẫu bao sau khi dự trù mất mẫu được tính bằng công thức

<img src="http://latex.codecogs.com/svg.latex?N_{HC}&space;=&space;\frac{N}{1-P_{nonresponse}}" title="http://latex.codecogs.com/svg.latex?N_{HC} = \frac{N}{1-P_{nonresponse}}" />


Ví dụ nghiên cứu tính ra cần cỡ mẫu bằng 500, với dự trù mất mẫu khoảng 10% thì số đối tượng nghiên cứu cần tiếp cận là 500/0.9 = 556 mẫu. Chú ý là dự trù mất mẫu là lấy số lượng mẫu ban đầu chia cho 1 – tỉ lệ mất mẫu, không phải lấy số mẫu ban đầu cộng thêm 10%, vì khi lấy thêm 10% tức là 50 mẫu, tổng cộng là 550 mẫu, nếu thực sự tỉ lệ mất mẫu là 10% thì cỡ mẫu thu được cuối cùng sau nghiên cứu là 550 – 550x0.1 = 495 mẫu. Khi đó số lượng mẫu thu được cuối cùng ít hơn 5 mẫu so với cần thiết. 

Tỉ lệ mất mẫu cũng cần được suy xét cẩn thận vì nếu chọn tỉ lệ mất mẫu quá thấp sẽ không thu được số lượng mẫu cần thiết cho nghiên cứu. Ngược lại, nếu chọn tỉ lệ mất mẫu quá cao sẽ làm hao phí nguồn lực nghiên cứu do phải tuyển chọn nhiều đối tượng nghiên cứu hơn mức cần thiết.


## Tài liệu tham khảo

* Perezgonzalez JD. Fisher, Neyman-Pearson or NHST? A tutorial for teaching data testing. Front Psychol. 2015;6:223. 

* Jacob Cohen. A Power Primer. Psychological Bulletin [PsycARTICLES]. 1992;112:155



