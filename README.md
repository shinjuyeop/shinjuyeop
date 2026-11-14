# 신주엽 | Juyeop Shin

**Embedded Systems · Vehicle Software**\
건국대학교 전기전자공학부

차량 제어 소프트웨어와 임베디드 시스템을 개발합니다.
MCU 펌웨어와 통신, 시험 환경을 연결하고, 임베디드 환경에서 AI 모델의 실행과 성능을 분석합니다.

## Projects

### Control · 차량 제어 시스템

Team K.A.I.의 ROS 2·STM32·FreeRTOS 기반 차량 제어 시스템입니다.
구동·제동·조향을 통합하고, 물리 E-stop 경로와 통신 단절 처리를 구성했습니다.
실차 통합·주행 검증을 완료하고 대회에서 운용했습니다.
실제 제어 보드를 사용하는 HIL 환경과 주행 기록 기반 분석·튜닝 도구를 개발했습니다.

[Repository][control] · [Architecture][control-architecture] · [Safety][control-safety]

### StrataDrive · 차량 소프트웨어 아키텍처

Central–Zone–Leaf ECU 구조에서 구성요소별 책임과 통신·실행 경계를 설계하는 C++ 기반 프로젝트입니다.
SOME/IP 기반 분산 통신과 CARLA 기반 차량 제어를 각각의 Host SIL 구성에서 검증하고, 입력 유효성 검사와 고장 대응을 시험합니다.
현재 영상 인지와 주행·보호 기능의 연결을 확장하고 있습니다.

[Repository][stratadrive] · [Architecture][stratadrive-architecture]

### FastReflex · 위험 감지 모델 연구와 임베디드 배포

MuJoCo에서 IMU 기반 보행 위험 감지와 발바닥 압력 기반 지형 분류 모델을 연구했습니다.
동결한 기준 모델을 INT8·Vela 경로로 변환해 PSoC Edge E84의 Ethos-U55에서 실행하고,
C 전처리와 보드 출력을 Host 기준값과 비교하는 프로토타입을 구현했습니다.

[Research][fastreflex-research] · [E84 Deployment][fastreflex-deployment] · [Pipeline][fastreflex-pipeline]

### edge-asr · ARM64 음성인식 최적화

Qwen3-ASR-0.6B를 Raspberry Pi 5의 ARM64 CPU에서 실행하며 한국어 정확도·처리 완료율과 지연·연산 비용을 함께 분석합니다.
WAV 연속 입력과 USB 마이크로 부분·확정 자막을 확인하고, VAD·재전사 주기·KV 캐시 재사용을 비교하며 최적화하고 있습니다.

[Repository][edge-asr] · [최적화 과정][edge-asr-history]

## Experience

- **(주)딥이티 · 기술개발 인턴** — 2026.06–현재\
  온디바이스 AI 모델 연구와 임베디드 배포 검증, Infineon Startup Challenge 2026 프로젝트 참여
- **Team K.A.I. · 하드웨어 팀장** — 2026\
  분산 차량 제어 구조 설계, 펌웨어·Host 통합과 실차 시험
- **Team K.A.I. · 제어 파트장** — 2025\
  ROS 2·Arduino Mega·CAN 기반 1/2 규모 자율주행차 제어 개발

## Awards

| 연도 | 대회 | 수상 |
|---|---|---|
| 2026 | 대학생AI·S/W 모빌리티 경진대회 · 자작자율차 | 자율주행구현 부문 대상 · 창작기술부문 특별상 |
| 2025 | 대학생 창작 모빌리티 경진대회 · 자작자율차 | 자율주행구현 부문 특별상 · 창작기술부문 우수상 |
| 2025 | 제17회 창의설계경진대회 · 건국대학교 | 장려상 |

## Technical Focus

- **Embedded** · C/C++, STM32, FreeRTOS, CAN, UART, SPI, I2C, PWM
- **Vehicle Software** · ROS 2, micro-ROS, SocketCAN, SOME/IP, HIL/SIL
- **Edge AI** · Python, PyTorch, TensorFlow Lite, INT8, Vela, ARM64

## Other Projects

- [ohnochoo][ohnochoo] · 친구들과 음악 추천·투표·평점을 공유하는 웹앱
- [whomadethis][whomadethis] · 방문한 음식점의 지도·후기·사진을 공유하는 웹앱

<!--
2026-11-14: 대표 프로젝트 중심으로 프로필 구성 정리.
기술 소개는 각 공개 저장소의 README와 연결한 설계·실험 문서를 기준으로 작성했다.
경력·수상과 대회 적용 시스템의 실차 검증·운용 이력은 본인 확인을 반영했다.
Control은 Team K.A.I. 공동 작업 이력을 보존한 개인 공개 사본이다.
-->

[control]: https://github.com/shinjuyeop/Control
[control-architecture]: https://github.com/shinjuyeop/Control/blob/main/docs/ARCHITECTURE.md
[control-safety]: https://github.com/shinjuyeop/Control/blob/main/docs/SAFETY.md
[stratadrive]: https://github.com/shinjuyeop/StrataDrive
[stratadrive-architecture]: https://github.com/shinjuyeop/StrataDrive/blob/main/docs/architecture/README.md
[fastreflex-research]: https://github.com/shinjuyeop/Infineon_FastReflex
[fastreflex-deployment]: https://github.com/shinjuyeop/Infineon_FastReflex_E84
[fastreflex-pipeline]: https://github.com/shinjuyeop/Infineon_FastReflex_E84/blob/main/docs/deployment_pipeline.md
[edge-asr]: https://github.com/shinjuyeop/edge-asr
[edge-asr-history]: https://github.com/shinjuyeop/edge-asr/blob/main/docs/research/optimization_history.md
[ohnochoo]: https://github.com/shinjuyeop/ohnochoo
[whomadethis]: https://github.com/shinjuyeop/whomadethis
