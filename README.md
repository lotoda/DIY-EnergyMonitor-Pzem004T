# DIY EnergyMonitor with Pzem004T

** Hướng dẫn tự làm đồng hồ đo điện với cảm biến Pzem004T kết nối và giám sát dựa trên nền tảng IoT LOTODA.
** Giám sát các thông số sử dụng điện trong ngôi nhà của bạn hoặc cơ sở sản xuất quy mô nhỏ.
** Các thông số giám sát như sau:
-	Điện áp (V) - Voltage
-	Dòng điện (A) - Current
-	Công suất tiêu thụ (W) - Power
-	Chỉ số tiêu thụ điện (KWh) - Energy
-	Tần số (Hz) - Frequency
-	Hệ số CosPi (PF) = PF

### Giao diện Web trên ESP8266 có thể truy cập bằng IP hoặc địa chỉ: lotodaXXXX.local/
<img src="https://github.com/lotoda/DIY-EnergyMonitor-Pzem004T/blob/master/1.WebUI_monitoring.PNG">

### Giao diện trên LOTODA Mobile App như sau:
<img src="https://github.com/lotoda/DIY-EnergyMonitor-Pzem004T/blob/master/3.Monitoring_on_MobileApp.jpg" width="200" height="400">

# Sơ đồ đấu nối
 | ESP8266 | PZEM | Nút reset |
 |-----------|-----------|-----------|
 | GPIO 5 | TX |  |
 | GPIO 4 | RX |  |
 | GPIO 0 |  | X |
 | GND | GND | GND |
 | VCC | VCC |  |
 
# Hướng dẫn cài đặt và cấu hình

### Bước 1: Upload firmware cho ESP8266
1. Upload firmware file
<img src="https://github.com/lotoda/DIY-EnergyMonitor-Pzem004T/blob/master/Upload_firmware_01of02.PNG">
2. Upload SPIFFS file
<img src="https://github.com/lotoda/DIY-EnergyMonitor-Pzem004T/blob/master/Upload_spiffs_02of02.PNG">

### Bước 2: Khởi động và kết nối wifi
-	Khi bắt đầu cấp nguồn sau 15~30 giây nếu chưa có kết nối wifi được thiết lập. Thiết bị tự động phát wifi “lotodaXXXX” trong đó XXXX là ID của thiết bị bạn.
-	Người dùng sử dụng máy tính hoặc điện thoại di động thực hiện kết nối đến Wifi của thiết bị mà không cần mật khẩu.
-	Sau khi kết nối thành công, truy cập đến địa chỉ: “http://192.168.4.1” để vào trang web của thiết bị.
-	Tại mục “WiFi Network”, Sau đó chọn wifi cần kết nối. Nhập mật khẩu wifi cần kết nối và ấn “Save”.
-	Thiết bị sẽ tự kết nối tới wifi được cài đặt.
-	Sau khi thiết bị đã kết nối thành công. Xem địa chỉ IP của thiết bị trong mục "WiFi Network”. Sau đó tắt AP mode của thiết bị và khởi động lại thiết bị. Sau đó truy cập theo địa chỉ thiết bị “http://<địa_chỉ_IP>” hoặc “http://lotodaXXXX/” (chỉ hổ trợ trên iOS).
 
### Bước 3: Thiết lập kết nối đến MQTT của IoT LOTODA
<img src="https://github.com/lotoda/DIY-EnergyMonitor-Pzem004T/blob/master/2.WebUI_MQTT_config.PNG">

### Bước 4: Thiết lập cấu hình cho ứng dụng LOTODA Mobile App
-	Bạn xem chi tiết các video hướng dẫn để đăng ký (và nhận User ID key & Pass ID key) và sử dụng IoT LOTODA tại website: http://lotoda.vn

# Done, Chúc bạn thành công! Thank you!
