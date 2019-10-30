## 1.INTRO 
#### 1.1 Tổng quan về GO ? 
 Có một bài toán đau đầu dành cho các công ty là khi họ đã lên tới tầng scale cho một dự án. Thời gian đầu thì sẽ là optimize code, database, scale phần cứng… nhưng khi tới một lượng user cực lớn thì vấn đề đó sẽ càng ngày càng nan giải. Và giải pháp của một số công ty đó là chọn Go. Nó được thiết kế để có thể scale một hệ thống với số request lớn, có thể lên tới hàng triệu request/s. Thêm một lí do nữa là Go là một ngôn ngữ đơn giản, learning curve thuộc dạng dễ nhất trong các ngôn ngữ, vì thế chi phí để chuyển qua Go thấp. Ngoài ra còn một số tiêu chí: build time nhanh, chuẩn hóa code giữa các thành viên trong team bằng vô số tool xịn…
 Ngày nay khi phần cứng ngày càng phát triển, CPU đa nhân thì các ngôn ngữ theo concurrency model sẽ là xu hướng. Go là một trong số đó. Go không phải là một ngôn ngữ mạnh tuyệt đối. Concurrency Go sẽ không bằng Erlang, Clojure, về mức độ strong typed thì lại càng không thể so sánh với các ngôn ngữ functional như Haskell, Scala, về việc làm prototype nhanh thì không thể bằng Ruby hay Node. Nhưng lí do mọi người thích Go là vì nó support ở mức “vừa đủ xài” hay theo mọi người vẫn hay nói là “simple enough to build the world”.
#### 1.2 Nguyên lý thiết kế GO 
  Golang có cú pháp giống với C/C++, được phát triển tại Google năm 2007. Được sử dụng trong một số hệ thống sản phầm của Google. Nếu ai đã từng học qua C or C++ thì sẽ làm quen rất nhanh với GoLang.
    
    - Nguyên lý thiết kế Golang
     + Thời gian biên dịch nhanh
    
     + Hỗ trợ xử lý đồng thời: gorountines, channels,
    
     + Nhất quán, đơn giản, an toàn
    
     + Hỗ trợ Interface và Type Một số đặc trưng của Golang Method: 
       Golang không có classes, nhưng nó cho phép định nghĩa method dựa trên các kiểu dữ liệu tự đinh nghĩa. Intefaces: định nghĩa tập hợp các phương thức sẽ thực thi.
    
     + Kiểu con trỏ - pointer: lưu địa chỉ bộ nhớ của biến
    
     + Xử lý đồng thời – concurrency: goroutine quàn lý thread trong Go runtime, goroutine giao tiếp với nhau thông qua channel.
     
Example: Hello World
     package main
     
     import "fmt"
     
     func main() {
        fmt.Println("Hello, World!")
     }
##### Tham khảo thêm 
Có thể tham khảo thêm tại: https://golang.org/doc/code.html Hoặc : https://www.tutorialspoint.com/go/go_basic_syntax.htm.

