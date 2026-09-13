Bước 1: Trích xuất Lớp, Thuộc tính và Phương thức
Thành phần	Lớp Customer	Lớp Order
Thuộc tính (Attributes)	customerId, fullName, phoneNumber	orderId, createdDate
Phương thức (Methods)	placeOrder()	calculateTotal()
Bước 2: Access Modifiers và Multiplicity
Access Modifier
Thuộc tính: private → ký hiệu -
Phương thức: public → ký hiệu +

Ví dụ:

- customerId: String
+ placeOrder(): void
Multiplicity

Quan hệ giữa Customer và Order:

Customer 1 ───────── 0..* Order

Ý nghĩa:

Một Customer có thể có 0 hoặc nhiều Order
Mỗi Order thuộc về 1 Customer
Bước 3: Class Diagram hoàn chỉnh

Bạn có thể vẽ trên draw.io như sau:

+----------------------------+
|          Customer          |
+----------------------------+
| - customerId: String       |
| - fullName: String         |
| - phoneNumber: String      |
+----------------------------+
| + placeOrder(): void       |
+----------------------------+
              1
              |
              | Association
              |
            0..*
+----------------------------+
|           Order            |
+----------------------------+
| - orderId: String          |
| - createdDate: Date        |
+----------------------------+
| + calculateTotal(): double |
+----------------------------+
