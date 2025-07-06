# btl_Nhung
# PROJECT SAMPLE

Trò chơi Space Invaders là trò chời dạng shoot-em-up, trong đó người chơi điều khiển nhân vật di chuyển để tránh hoả lực của kẻ thù và tiêu diệt các mục tiêu.  
Trò chơi sẽ được xây dựng trên kit STM32F429I-DISC1 kết hợp với thư viện đồ hoạ TouchGFX. Bộ 32F429IDISCOVERY tận dụng khả năng của các vi điều khiển hiệu suất cao STM32F429, cho phép người dùng dễ dàng phát triển các ứng dụng phong phú với giao diện người dùng đồ họa tiên tiến.


## GIỚI THIỆU

__Đề bài__: _SpaceInvaders._

__Sản phẩm:__
1. Tính năng
2. Tính năng
3. Tính năng
- Ảnh chụp minh họa:\
  ![Ảnh minh họa](https://soict.hust.edu.vn/wp-content/uploads/logo-soict-hust-1-1024x416.png)

## TÁC GIẢ

- Tên nhóm:.6h50
- Thành viên trong nhóm
  |STT|Họ tên|MSSV|Công việc|
  |--:|--|--|--|
  |1|Nguyễn Huy Hoàng|20215581|hiện thị oled, hiệu ứng, và xử lý ngắt|
  |1|Nguyễn Duy Khương|20215602|hiện thị oled, hiệu ứng, và xử lý ngắt|
  |1|Vũ Đức Lương|20215614|hiện thị oled, hiệu ứng, và xử lý ngắt|


## MÔI TRƯỜNG HOẠT ĐỘNG

- Liệt kê module CPU/dev kit.
STM32F429I-DISC1.
- Liệt kê các kit, module được sử dụng:
STM32F429I-DISCO: Dev kit chính với LCD tích hợp
LCD ILI9341 / RGB565: Màn hình TFT LCD dùng giao tiếp RGB (có thể là màn tích hợp trên F429I-DISCO)
Joystick:	Điều khiển nhân vật, sử dụng qua ADC chân PA0/PA1
TouchGFX: Giao diện đồ họa
SDRAM ngoài: Giao tiếp qua FMC (do cấu hình có dùng FMC)
I2C3: Có thể dùng cho cảm biến hoặc Audio codec
DMA2D, LTDC: Xử lý đồ họa và truyền dữ liệu đến LCD

## SO ĐỒ SCHEMATIC

_Cho biết cách nối dây, kết nối giữa các linh kiện_ 
Ví dụ có thể liệt kê dạng bảng
|STM32F429|Module ngoại vi|
|--|--|
|PA0|VRX của Joystick|
|PA1|VRY củaJoystick|
|Nguồn 5V|chân dương còi TMB12A05|
|PB0|chân âm còi TMB12A05|




### TÍCH HỢP HỆ THỐNG

- Mô tả các thành phần phần cứng và vai trò của chúng: máy chủ, máy trạm, thiết bị IoT, MQTT Server, module cảm biến IoT...
  Hệ thống gồm 4 thành phần chính:
-	Kit STM32F429I-DISC1
-	Mini USB-cable 
- Joystick
-	Dây nối

- Mô tả các thành phần phần mềm và vai trò của chúng, vị trí nằm trên phần cứng nào: Front-end, Back-end, Worker, Middleware...
  Kiến trúc phần mềm gồm có 5 thành phần chính:
-	GameScreenView: Tiếp nhận dữ liệu từ người dung và hiển thị hình ảnh lên màn hình
-	inputTask: Nhận dữ liệu từ người dụng và gửi vào inputQueue để chờ xử lý
-	gameTask: Cập nhật thông tin các đối tượng xử lý logic trò chơi
-	inputQueue: Chứa dữ liệu được người dung gửi tới trò chơi thông qua các nút bấm
-	gameInstance: Đối tượng trò chơi của chương trình, chứa thông tin về trò chơi


### ĐẶC TẢ HÀM

- Giải thích một số hàm quan trọng: ý nghĩa của hàm, tham số vào, ra

  ```C
     /**
      *  Hàm tính ...
      *  @param  x  Tham số
      *  @param  y  Tham số
      */
     void abc(int x, int y = 2);
  ```
  
### KẾT QUẢ

- Các ảnh chụp với caption giải thích.
- Hoặc video sản phẩm
