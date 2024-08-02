# 배터리 양불판정 및 분류

## 프로젝트 개요
배터리의 외관 사진을 3가지 각도에서 촬영하여 불량 여부를 판별하는 시스템을 개발한다. 촬영된 이미지를 분석하여 정상 제품과 불량 제품을 구분하고, 이를 로봇 팔을 이용하여 자동으로 분류한다. 이를 통해 품질 관리의 효율성을 높이고, 불량 제품의 선별 과정을 자동화하여 생산성을 향상시키는 데 기여한다.

## Architecture
---
![아키텍쳐 그림](https://github.com/I5-BatteryCheck/.github/blob/main/%EC%8B%9C%EB%82%98%EB%A6%AC%EC%98%A4v3-%ED%8E%98%EC%9D%B4%EC%A7%80-3.drawio.png)
---

### 개발기간
- 2024.07.01 ~ 2024.08.20


## 팀원
- 이하빈(팀장): AI
- 강대호: AI
- 김건우: 프론트 엔드
- 박기범: LOW-LEVEL
- 송재훈: 백엔드

## 개발 환경
### Frontend
![react](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![html](https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white) ![css](https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white) ![js](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white) ![figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white) ![bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
### Backend
![spring](	https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white) ![JAVA](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![MYSQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white) 
### AI
![PYTHON](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![FLASK](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white) ![ULA]() ![YOLO]()
### Low-Level
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![ARDUINO](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white) ![RASPBERRY PI](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=for-the-badge&logo=Raspberry%20Pi&logoColor=white) ![ESP32]() ![FLASK](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)


## ER다이어그램
```mermaid
erDiagram
    BATTERY {
        int batteryID PK
        string result
        date testDate
        float batteryTemperature
        float batteryHumidity
        float batteryIlluminance
    }

    PICTURE {
        int pictureID PK
        int batteryID FK
        string pictureName
        int cameraNumber
    }

    DEFECT {
        int defectID PK
        string defectType
        float x_Min
        float x_Max
        float y_Min
        float y_Max
    }

    CONDITION {
        int conditionID PK
        datetime conditionDatetime
        float insideTemperature
        float insideHumidity
        float insideIlluminance
    }

    USER {
        int userID PK
        string userPW
        string userName
    }

    BATTERY ||--|{ PICTURE : has
    PICTURE ||--|{ DEFECT : has

```


## 주요 기능
- 
	- ### 로그인
 - ![로그인화면]()
	- ### 생산 관리 페이지
 - ![생산관리 화면](https://github.com/I5-BatteryCheck/.github/blob/main/profile/%EC%83%9D%EC%82%B0%EA%B4%80%EB%A6%AC.png)
	- ### 배터리 통계 페이지
 - ![배터리 통계 화면](https://github.com/I5-BatteryCheck/.github/blob/main/profile/%ED%86%B5%EA%B3%84.png)
	- ### 과거 조회 페이지
 - ![과거 조회 화면](https://github.com/I5-BatteryCheck/.github/blob/main/profile/%EC%A1%B0%ED%9A%8C.png)
	- ### 생산 환경 모니터링 페이지
 - ![생산 환경 모니터링 화면](https://github.com/I5-BatteryCheck/.github/blob/main/profile/%EC%83%9D%EC%82%B0%ED%99%98%EA%B2%BD.png)

## 세부 내용
