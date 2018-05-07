# Bài tập Trainee Colombo 2018
## OOP
Thực hiện bởi [Nguyễn Phi Huy](https://github.com/huynhan147)

## Sự khác nhau giữa Trait, Interface, Abstract
* Interface : 
  - interface là một lớp rỗng(Không phải là một lớp đối tượng thuần túy). chỉ chứa khai báo về tên phương thức , không có khai báo về thuộc tính hay thứ gì khác
  - Khai báo Interface dùng từ khóa interface để thay thế cho từ khóa class
  - Nếu một lớp khác implement một interface thì nó phải khai báo và định nghĩa tất cả các phương thức trong interface.
  - Có tính kế thừa : Một interface A có thể kế thừa một interface B. Lúc này lớp nào implement interface A thì phải định nghĩa lại tất cả các phương thức mà cả hai interface A và B đã khai báo
* Abstract : 
  - Là một lớp và chứa các phương thức abstract
  - Lớp abstract sẽ định nghĩa các phương thức mà từ đó các lớp con sẽ kế thừa nó và OVERWITE lại
  - Tất cả các phương thức của lớp abstract đều phải được khai báo là abstract và phải ở mức protected và public không được ở mức private
  - Lớp Abstract có thể có thuộc tính nhưng thuộc tính không được khai báo là abstract và không thể khởi tạo một đối tượng của lớp abstract
  - Lớp Abstract cũng có tính kế thừa. abstract A kế thừa abstract B thì một lớp nào đó kế thừa B phải viết lại toàn bộ các phương thức của  abstract A và B
  - Một class chỉ có thể kế thừa một lớp abstract
* Trait : 
  - Traits hiểu đơn giản là một nhóm các methods mà bạn muốn include nó trong một class khác
  -  Một Trait giống với abstract class không thể khởi tạo trên chính nó(Không hoàn toàn giống nhau).
  - Traits có chức năng gom lại các phương thức và thuộc tính mà chúng ta muốn sử dụng lại nhiều lần.
  - Các phương thức trong Traits có thể bị override lại trong class sử dụng nó.
  - Để khai báo , sử dụng cú pháp trait thay cho class
## Sự khác biệt giữa public, private và protected
  - Private : Ta không thể truy xuất tới thành phần private ở lớp con hoặc ở bên ngoài lớp
  - Protected : Chỉ cho phép truy xuất nội bộ trong lớp đó và lớp kế thừa, riêng ở bên ngoài lớp sẽ không truy xuất được, mức protected thường được sử dụng cho những phương thức và thuộc tính có khả năng bị lớp con định nghĩa lại
  - Public : Có thể truy cập tới các phương thức và thuộc tính ở bất cứ đâu, dù trong nội bộ của lớp hay ở lớp con hay cả bên ngoài lớp đều được
## Từ khóa Final : 
  - Để chống kế thừa : Muốn tước quyền kế thừa cho một class, đặt từ kháo Final trước class đó 
  - Chống Override : Khi muốn một phương thức không được Override từ các phương thức của class khác. Đặt từ khóa final trước tên phương thức đó
