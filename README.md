# arduino490

https://youtu.be/wDA_jxWCRw4

(ESPNOW#9) ESPNOW➕LoRa(SX1276)➕IoT<BR>
녹칸다의 ESPNOW시리즈이다!<BR>
이번편은 ESPNOW으로 수집된 정보를 LoRa로 변환해주는 내용을 주제로 해보도록 한다!<BR>
보드 3개 정도로 예시를 구현하면 될 것 같다!<BR>
A보드와 B보드는 ESPNOW로 연결되어 있다!<BR>
B보드와 C보드는 LoRa로 연결되어있다!<BR>
C보드는 인터넷 공유기와 연결되어서 외부로 데이터를 송신한다!(MQTT)<BR>
C보드가 MQTT로 전송하는 데이터를 스마트폰에서 확인한다!<BR>

1.A보드에 센서가 있을때 스마트폰에서 데이터를 확인할 수 있도록 한다!(센서는 녹칸다가 적당히 아무거나 준비함)<BR>
2.A보드에 릴레이가 있을때 스마트폰에서 제어할 수 있도록 한다!<BR>
이런 내용을 주제로 해서 아무거나 만들고 싶은거 만들어본다!<BR>

(실제로한거)

A,B,C보드 3개가 있고 A와 B는 ESPNOW로 연결되고 B와 C는 LoRa로 연결된다!
  
1.A와 B사이의 ESPNOW통신예제를 간단히 구현하라!

![490-1_bb](https://user-images.githubusercontent.com/106683637/171861044-3b13a4d4-881b-4d36-9010-c9e38afd7a0a.jpg)
  
2.B와 C사이의 LoRa통신 예제를 간단히 구현하라!
  
![490-2_bb](https://user-images.githubusercontent.com/106683637/171861042-b53e1144-28de-46e1-ac34-89b4ae3ac946.jpg)

3.A가 보낸 메시지를 B가 ESPNOW로 받은다음 C쪽으로 LoRa통신으로 전송해서 화면에 출력하시오!

![490-3_bb](https://user-images.githubusercontent.com/106683637/171861039-d0dfd01f-92f6-4eff-9f8e-df5be78c1f82.jpg)
  
4.(3)예제에서 C보드가 메시지를 수신했을때 MQTT로 메시지를 전송하도록 하시오!(결과를 스마트폰에서 확인하시오)

5.int형변수2개와float형변수 2개가 있을때 A에서 B로 전송하고 B에서 C로 전송한다음 C가 JSON형태로 스마트폰으로 전송하도록 하시오!

6.스마트폰에서 녹칸다가 전송한 문자열을 MQTT를 이용해서 C로 전송하고 C에서B로 LoRa로 전송하고 B에서 A로 ESPNOW로 전송해서 A의 시리얼모니터화면에 숫자를 출력하시오!

7.A보드에 LED가 4개있을때 C보드에서 전송한 명령에 의해서 개별제어되도록 해보시오!(10=1번LED/OFF, 21=2번LED/ON)

![490-7_bb](https://user-images.githubusercontent.com/106683637/171861038-fff186f5-a4fc-436e-a742-df7f75cc897d.jpg)
  
8.A보드에 온습도센서(DHT-11)을 D3에 연결하고 온도와 습도값을 JSON포멧으로 MQTT로 전송하시오!

![490-8_bb](https://user-images.githubusercontent.com/106683637/171861037-e52ac59a-24e8-4f91-ac6f-3bc2ae01d6d4.jpg)
  
9.(논외) A에서B로 B에서C로 LoRa를 이용해서 전송하시오!
  
![490-9_bb](https://user-images.githubusercontent.com/106683637/171861029-92e870f0-967b-42ae-b146-87f56608f903.jpg)
  
  (Machine translation)

It is Nokanda's ESPNOW series!<BR>
In this episode, the topic of converting information collected with ESPNOW to LoRa is the subject!<BR>
I think it would be enough to implement an example with about 3 boards!<BR>
A board and B board are connected by ESPNOW!<BR>
Board B and C board are connected with LoRa!<BR>
The C board is connected to the Internet router and transmits data to the outside! (MQTT)<BR>
Check the data transmitted by the C board with MQTT on your smartphone!<BR>

1.When there is a sensor on the A board, make it possible to check the data on the smartphone!<BR>
2.When there is a relay on the A board, it can be controlled from the smartphone!<BR>
Let's make something we want to make with this topic!

(actually done)

There are 3 boards A, B, and C, A and B are connected with ESPNOW, and B and C are connected with LoRa!

1.Simple implementation of ESPNOW communication example between A and B!

2.Simple implementation of LoRa communication example between B and C!

3.B receives the message sent by A through ESPNOW, then sends it to C through LoRa communication and prints it on the screen!

4.(3)In the example, when board C receives a message, send the message by MQTT! (Check the result on your smartphone)

5.When there are 2 int type variables and 2 float type variables, send from A to B, then from B to C, and then let C transmit to the smartphone in JSON format!

6.Transmit the string sent by Nokanda from the smartphone to C using MQTT, from C to B to LoRa, and from B to A to ESPNOW, and print the number on A's serial monitor screen!

7.When there are 4 LEDs on board A, try to control them individually by the command sent from board C! (10=No.1 LED/OFF, 21=No.2 LED/ON)

8.Connect the temperature and humidity sensor (DHT-11) to D3 on the A board and send the temperature and humidity values ​​in JSON format to MQTT!

9.(Out of topic) Send from A to B, from B to C using LoRa!
