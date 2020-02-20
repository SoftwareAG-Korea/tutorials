# webMethods.io Integration과 API 살펴보기  
  * Part 1: webMethods.io Integration에서 workflow을 만들고 자주 활용될 수 있는 부분을 공통 workflow로 생성  
  * Part 2: Part 1에서 만든 공통 workflow을 webMethods.io API에서 API로 생성    
  
  > Author: [Software AG, Korea](https://www.softwareag.com/kr/) [이범](https://github.com/billybeom)  
  > Last Modified: 10-JAN-2020  
  
  
## 튜토리얼 개요  
  
### [사전 준비 사항](./Prerequisite/)  
  
  1. (필수) [webMethods.io Free Trial 신청](./Prerequisite/README.preq1.md)  
  2. (필수) [Saleforce Developer Free Trial](./Prerequisite/README.preq2.md)  
  3. (필수) [Saleforce에서 ConnectedApp 생성](./Prerequisite/README.preq3.md)  
  4. (옵션) [Postman으로 access token과 refresh token 받기](./Prerequisite/README.preq4.md)  
  5. (옵션) [네이버 파파고 번역 API 사용 신청](./Prerequisite/README.preq5.md)  
  
  
  
### [Part 1. webMethods.io Integration](https://github.com/SoftwareAG-Korea/tutorials/blob/master/wmio/integration/salesforce+messanger+sms/)  
webMethods.io Integration에서 Salesforce connector을 이용하여 생성 Lead로부터 연락처를 입력하고 Slack과 SMS를 보내는 workflow를 만들어 봅니다.  
  
  1. Lead 정보의 연락처를 Salesforce에 Contact에 입력하기
  2. Slack의 영업 채널에 Lead 정보 메시지 보내기
  3. Aligo SMS을 이용하여 고객에게 문자 메시지 보내기
  
  
  
### [Part 2. webMethods.io API](https://github.com/SoftwareAG-Korea/tutorials/blob/master/wmio/api/gateway+portal+mashup/)  
webMethods.io Integration에서 만든 Slack과 SMS workflow을 webMethods.io API에서 API로 만들어 봅니다.  
workflow을 API로 만드는 부분이 매우 쉽게 바뀔 예정입니다. 현재 로드맵 상으로 webMethods.io의 2020년 Spring Release에는 만든 workflow를 쉽게 webMethods.io API로 배포할 수 있습니다.  
  
  1. Slack과 SMS workflow을 API로 만들기
  2. API Portal에서 개선 요청 확인하기
  3. Mashup API 만들기
  
  
  
### [API 해커톤 및 베타 프로그램](https://engage.softwareag.cloud/)  
살아있는 API 서비스를 하기 위해서는 API 개발자들과 지속적으로 소통할 수 있는 채널이 필요합니다.  
API Portal의 커뮤너티 등을 이용하여 소통도 당연히 해야 하겠지만 API 개발자들의 보다 적극적인 참여 유도 및 동기 부여를 위해서 해커톤 및 베타 프로그램 행사가 필요하기도 합니다.  
API Engagement platform 서비스는 webMethods.io와는 별도로 제공하는 클라우드 서비스로 필요한 기간 동안만 API 해커톤/베타 프로그램을 빠르고 쉽게 연결하여 운영할 수 있습니다.  
API Engagement platform 서비스를 통해서 API Consumer와 API Provider들은 보다 긴밀히 소통할 수 있습니다.  
API Engagement platform 서비스 URL: https://engage.softwareag.cloud  
  
  
