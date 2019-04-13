---
layout: post
title: Lập trình hướng đối tượng từ cơ bản đến nâng cao (Phần 1)
image: ![alt](https://imgur.com/4PQRXFF.jpg)
---

Trước khi xem nội dung, nhằm giản lược bài viết, các bạn nên tự mình ôn lại các khái niệm căn bản về OOP, mình sẽ không nhắc lại từ đầu. Nếu bạn nào quên thì có thể tham khảo trên [Wiki](https://vi.wikipedia.org/wiki/L%E1%BA%ADp_tr%C3%ACnh_h%C6%B0%E1%BB%9Bng_%C4%91%E1%BB%91i_t%C6%B0%E1%BB%A3ng) nhé.

Lập trình hướng đối tượng là gì, có ăn được không?
> Mục tiêu chính của OOP chính là “tóm gọn” các thủ tục lại, người ta hay gọi là “đóng gói” đấy. Có nghĩa là, 1 công việc thì có rất nhiều việc cần làm, để làm ra 1 game thì bạn phải chia studio của bạn ra làm nhiều vị trí, ví dụ như 1 bên thì vẽ chi tiết, 1 bên thì tính toán vật lý và các véc tơ, 1 bên thì sáng tạo kịch bản, rồi còn có hẳn 1 bên chuyên làm giám sát tất cả các bên rồi đưa ra đánh giá,… Đấy, chung quy lại, vẫn là thực hiện các thủ tục, nhưng chỉ là bạn chia nó ra cho từng người và chuyên môn hóa nó thôi. OOP cũng vậy, bạn tạo ra một đối tượng, thì mục đích duy nhất của bạn là để đối tượng đấy của bạn giải quyết 1 công việc nào đó nào cho bạn.

Từ những yếu tố trên có thể thấy tầm quan trọng của chúng đối với lập trình viên nói chung và sinh viên nói riêng, một môn học cơ bản đầy quan trọng mà hầu hết chúng ta phải đi qua. Nắm được OOP, chúng ta nắm được phương pháp tư duy thiết kế cách viết chương trình, hay nói ngắn gọn là cách tổ chức và bố trí source code. Ngoài ra đây cũng là 1 phần kiến thức để qua vòng gửi xe của các buổi phỏng vấn đấy nhé. 


## Concepts cơ bản của **lập trình hướng đối tượng**
 
 
### Như ta đã biết, đối tượng có 4 tính chất đặc trưng là:
- Abstraction — Trừu tượng: Tập trung vào cốt lõi của đối tượng, bỏ qua những thứ không liên quan và không quan trọng.
- Encapsulation — Đóng gói: Tính chất không cho phép người dùng hay đối tượng khác thay đổi dữ liệu thành viên của đối tượng nội tại. Chỉ có các hàm thành viên của đối tượng đó mới có quyền thay đổi trạng thái nội tại của nó mà thôi.
- Inheritance — Kế thừa: Kế thừa, tái sử dụng phương thức, thuộc tính của lớp cơ sở. Và lớp kế thừa được gọi là lớp con, nó sẽ thừa hưởng những gì lớp cha có và cho phép.
- Polymorphism — Đa hình: Tính đa hình cho phép các chức năng (method) khác nhau được thực thi khác nhau trên các đối tượng khác nhau.

 
Thật sự thì mình cũng chả thể nhớ chi tiết nội dung từng cái này. Tuy nhiên, đừng lo lắng, nếu thực hành đủ nhiều, ta sẽ cảm nhận được chúng một cách dễ dàng.
 
 
### Đi cụ thể vào một Class

- Về cơ bản, có thể xem một **Class** như là một **Struct** mở rộng với việc sở hữu thêm các tính chất *hướng đối tượng*

- Theo form chuẩn, code của **Class** được chia thành 2 phần :
  - Phần khai báo: trong tập tin *.h*
  - Phần định nghĩa: trong file *.cpp*

- Có 2 cách đơn giản để sử dụng một **Class** :
  - Tạo một đối tượng trực tiếp. Truy cập các phương thức lớp, thuộc tính bằng cách sử dụng dấu chấm
  ```
  myClass objA;
  objA.sayHello();
  ```
   
  - Tạo một đối tượng thông qua con trỏ để sử dụng các phương thức, tính chất ta truy cập qua dấu **->**
  ```
  myClass *objB = new myClass; // or myClass *objB = new myClass();
  (*objB).sayHello(); // or objB->sayHello(); 
  ```
  (có nhiều điều để nói về phần khởi tạo này, tuy nhiên, mình sẽ để dành ở phần nâng cao!)
