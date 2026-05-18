# Shrimp-Feed-Grinder-Motor-Driver-PCB
Board dùng vi điều khiển STM32F0 làm trung tâm điều khiển.

STM32 xử lý các tín hiệu vào/ra, điều khiển PWM, relay, MOSFET công suất và LED 7 đoạn.

Phần driver sử dụng MOSFET công suất IRF540N để điều khiển thắng điện từ DC.

Tín hiệu điều khiển MOSFET được cách ly bằng opto PC817, giúp bảo vệ vi điều khiển khỏi nhiễu và xung áp từ tải công suất.

Mạch có diode và zener bảo vệ MOSFET khi đóng/ngắt cuộn thắng điện từ.

Board điều khiển động cơ 220VAC công suất 0.5HP thông qua relay và mạch công suất.

Khối relay dùng để điều khiển các trạng thái chạy, dừng, thắng và chuyển mạch động cơ.

Mạch khởi động mềm sử dụng nguyên lý TRIAC - DIAC, giúp giảm dòng khởi động ban đầu cho động cơ.

Điều khiển tốc độ hoặc mức công suất bằng tín hiệu PWM từ vi điều khiển.

Hiển thị trạng thái hoạt động bằng LED 7 đoạn 4 digit.

LED 7 đoạn được điều khiển qua IC TM1637, chỉ cần hai chân giao tiếp CLK và DIO.

Khối nguồn tạo các mức điện áp cần thiết như 12V, 3.3V và 55VDC.

Nguồn 3.3V cấp cho STM32 và IC hiển thị.

Nguồn 12V cấp cho relay và mạch điều khiển phụ.

Nguồn 55VDC dùng cho phần thắng điện từ.

Tổng thể board tập trung vào điều khiển phần cứng cho động cơ, gồm điều khiển PWM, thắng điện từ, khởi động mềm và hiển thị trạng thái.