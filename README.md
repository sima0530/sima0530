# 안녕하세요, 임베디드 시스템 엔지니어입니다

**센서에서 클라우드까지 한 사람이 잇는 일**을 20년 해왔습니다.
회로를 그리고, PCB를 뜨고, 펌웨어를 올리고, 앱과 서버를 붙이고,
인증을 받고, 현장에 설치하고, 고장 나면 다시 갑니다.

지금은 **의료가스 공급·감시·경보 시스템**을 만듭니다.
병원 수술실과 중환자실에서 산소·아산화질소·진공 배관의 압력을 재고,
이상이 생기면 표시반이 울리고 담당자 휴대폰으로 알림이 갑니다.
사람이 다치는 영역이라 「대충 동작하는 것」과 「믿을 수 있는 것」 사이의 거리가 멉니다.

---

## 무엇을 다루나

| 층 | 내용 |
|---|---|
| **아날로그·센서** | 압력·로드셀·온도, 4–20mA 루프, ADC 다점 보정, 노이즈·EMI |
| **펌웨어** | AVR(ATmega) · STM8 · STM32(F1/F4) · ESP8266/ESP32, 협력형 스케줄러·이벤트 OS |
| **통신** | RS485(Modbus·자체 프로토콜) · UART · I2C · SPI · BLE · Wi-Fi |
| **하드웨어** | 회로 설계, PCB 아트웍(Altium·OrCAD), 전원·보호 회로, 양산 이관 |
| **앱·클라우드** | Flutter, Firebase(Firestore · FCM · Functions), Python 도구 |
| **품질·인증** | 의료기기 GMP, 전자파 적합성, 해외 전파 인증 |
| **현장** | 병원·특수차량 설치, 시운전, AS, 고객 대응 |

## 이 일을 하며 배운 것

**설계는 현장에서 완성됩니다.** 책상에서 맞던 회로가 병원 지하 기계실에서는
접지 하나로 틀어집니다. 설치와 AS를 직접 다니며 얻은 것이
결국 다음 회로의 여유 설계와 진단 기능으로 돌아왔습니다.

**기록하지 않은 것은 없어집니다.** 몇 년 뒤 같은 보드를 다시 열었을 때
남아 있는 것은 기억이 아니라 그때 적어 둔 리비전 노트와 핀맵뿐이었습니다.
그래서 지금은 **회로·펌웨어·현장 기록을 함께 남기는 구조**를 따로 만들어 운영합니다.

---

## 대표 작업

**의료가스 알람 시스템** · ATmega128 + W5300 + STM32 표시반
병원 전관의 가스 압력을 RS485로 모아 TFT 표시반에 띄우고, Wi-Fi 모듈을 거쳐
Flutter 앱으로 보냅니다. 마스터·에어리어 다단 구성, 센서별 다점 보정 테이블,
현장별 펌웨어 변형 관리까지 포함합니다.

**가스 모니터** · ESP32-S2 + Firestore
센싱 노드에서 클라우드까지 직접 올리는 구조. ADC 보정과 통신 안정성,
그리고 **클라우드 과금**을 함께 설계해야 하는 일이었습니다.

**스마트 네일아트 로봇** · 5축 모터 제어 + BLE + 앱 (국책과제)
회로·펌웨어·모터 제어·통신·앱·PM·외주·양산을 한 번에 겪은 프로젝트입니다.

**어린이 전동차 제어기** · STM32F103
주행·조향·제동 모터를 타이머 하나의 네 채널로 몰고, 핸들과 조향모터의
포텐셔미터 두 개를 맞추는 폐루프. 보호자 리모컨이 오면 조향 권한이 넘어갑니다.

**음압 구급차 환경 제어** · 특수차량
차량 실내를 음압으로 유지하고 감시하는 시스템입니다.

---

## 경력

| 기간 | 분야 |
|---|---|
| 2016 ~ | 의료가스 알람·IoT·특수차량, 개발 PM |
| 2016 | RF · 해외 전파 인증 |
| 2015 ~ 2016 | 어린이 전동차 STM32 제어기 |
| 2013 ~ 2015 | 네일아트 로봇(국책), 미용·의료기기 6종, PM·GMP |
| 2012 ~ 2013 | 모바일 Wi-Fi 디버깅 |
| 2011 ~ 2012 | 자동차 가속·제동 페달 |
| 2011 | FPCB |
| 2008 ~ 2010 | 초음파·갈바닉·레이저·수분측정기 |
| 2007 | 산업교육 강사 |
| 2005 ~ 2007 | 정전용량 터치스위치 |

프리랜서로 BMS PCB 설계, 수처리 LCD 컨트롤러, 진단키트 컨트롤러,
전기·전자 인증 컨설팅을 했고, 2021~2022년에는 Python 교육 캠프 강사로 참여했습니다.

---

<details>
<summary><b>English summary</b></summary>

<br>

**Embedded systems engineer — 20 years, from sensor to cloud.**

I design the circuit, lay out the PCB, write the firmware, connect the app and
the backend, get it certified, install it on site, and go back when it breaks.

Currently I build **medical gas supply, monitoring and alarm systems** — measuring
oxygen, nitrous oxide and vacuum line pressure in operating rooms and ICUs, driving
alarm panels, and pushing notifications to the staff's phones. In a field where
people can get hurt, there is a long distance between "it works" and "it can be trusted."

| Layer | |
|---|---|
| **Analog / sensing** | Pressure, load cell, temperature · 4–20mA loops · multi-point ADC calibration · noise & EMI |
| **Firmware** | AVR (ATmega) · STM8 · STM32 (F1/F4) · ESP8266/ESP32 · cooperative schedulers, event-driven OS |
| **Comms** | RS485 (Modbus and in-house protocols) · UART · I2C · SPI · BLE · Wi-Fi |
| **Hardware** | Schematic design, PCB layout (Altium, OrCAD), power & protection, transfer to production |
| **App / cloud** | Flutter · Firebase (Firestore, FCM, Functions) · Python tooling |
| **Quality** | Medical device GMP · EMC · overseas radio certification |
| **Field** | Installation and service in hospitals and special-purpose vehicles |

**Two things this work taught me.** First, a design is finished on site, not on the
desk — a circuit that measured fine on the bench drifts on a single ground in a
hospital basement. Doing the installs and the service calls myself is what fed the
margins and the self-diagnostics into the next revision. Second, what is not written
down disappears: opening the same board years later, what survived was never memory
but the revision notes and the pin map I had bothered to write.

</details>

---

> 여기 있는 저장소는 **대부분 비공개**입니다. 고객사 제품의 회로·펌웨어라
> 공개할 수 없는 것이 많습니다. 공개 가능한 정리물은 준비되는 대로 올리겠습니다.
