# Trombone_Slider

<H2>목표</H2>
steam 게임 trombone champ을 위한 컨트롤러 제작.

<H2>사전 조사</H2>
1. trombone champ는 마우스 커서의 y축을 조절하여 플레이함.
2. 외부기기를 통해서 마우스 커서의 y축을 조절할 수 있는 방법을 모색.
3. 마우스는 이전 스캔 위치에서 이동한 방향과 거리를 주기에 부적합.
4. 디지타이저 기기가 마우스 커서의 x,y축을 전송함.


<H2>계획</H2>
1. stm32f411를 사용하는 black pill 보드가 시중에서 구할 수 있는 USB Device 장치 중 제일 적합함.
2. 해당 기기에 기존 ST Micronics사에서 지원해주는 HID 클래스를 올려서 사용.
3. USB의 Device Descriptors, Configuration Descriptors, Interface Descriptors, Endpoinit Descriptors, String Descriptors와 HID Descriptors를 수정하는 것으로 디지타이저로 인식.
4. 전원이 연결되면 비활성 상태를 유지
5. 비활성 상태에서 버튼0을 누르면 활성으로 변경
6. 활성 상태 : 버튼1을 누르면 슬라이더의 값을 마우스의 Y값과 함께 좌버튼 릴리즈를 전송.
7. 활성 상태에서 버튼0을 누르면 비활성으로 변경
8. 비활성 상태 : 모든 값을 릴리즈하고 대기


<H2>참고 자료</H2>
https://github.com/linuxwacom/wacom-hid-descriptors
https://usb.org/document-library/usb-20-specification
https://wiki.osdev.org/Universal_Serial_Bus#USB_Device.28s.29

<H2>재료</H2>
슬라이더 전위계 https://ko.aliexpress.com/item/1005003438143940.html

stm32f411 black pill https://ko.aliexpress.com/item/1005001936761405.html

버튼 https://ko.aliexpress.com/item/1005004886455996.html
