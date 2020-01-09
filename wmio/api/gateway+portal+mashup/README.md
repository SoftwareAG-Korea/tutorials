  ## webMethods.io Integration과 API 튜토리얼 - Part 2  
  2019년 12월 webMethods User Group Meetup 행사의 webMethods.io Integration과 API 살펴보기 Part 2으로 webMethods.io API에 대한 튜토리얼입니다.  

  ## Part 1. webMethods.io API 튜토리얼  
  
webMethods.io Integration에서 만든 Slack과 SMS workflow을 webMethods.io API에서 API로 만들어 봅니다.
Part 2에서 workflow을 API로 만드는 부분이 매우 쉽게 바뀔 예정입니다. 현재 로드맵 상으로 webMethods.io의 2020년 Spring Release에는 만든 workflow를 쉽게 webMethods.io API로 배포할 수 있습니다.  
  
  ## Part 2.1 webMethods.io API로 이동 및 API 생성  
  ![](./images/part.2-1.webMethods.io.api.gw.01.png)
  ![](./images/part.2-1.webMethods.io.api.gw.02.png)
  ![](./images/part.2-1.webMethods.io.api.gw.03.png)
  ![](./images/part.2-1.webMethods.io.api.gw.04.png)
  ![](./images/part.2-1.webMethods.io.api.gw.05.png)
  ![](./images/part.2-1.webMethods.io.api.gw.06.png)
  ![](./images/part.2-1.webMethods.io.api.gw.07.png)
  ![](./images/part.2-1.webMethods.io.api.gw.08.png)
  ![](./images/part.2-1.webMethods.io.api.gw.09.png)
  ![](./images/part.2-1.webMethods.io.api.gw.10.png)
  ![](./images/part.2-1.webMethods.io.api.gw.11.png)
  ![](./images/part.2-1.webMethods.io.api.gw.12.png)
  ![](./images/part.2-1.webMethods.io.api.gw.13.png)
  ![](./images/part.2-1.webMethods.io.api.gw.14.png)
  ![](./images/part.2-1.webMethods.io.api.gw.15.png)
  ![](./images/part.2-1.webMethods.io.api.gw.16.png)
  ![](./images/part.2-1.webMethods.io.api.gw.17.png)
  ![](./images/part.2-1.webMethods.io.api.gw.18.png)
  ![](./images/part.2-1.webMethods.io.api.gw.19.png)
  ![](./images/part.2-1.webMethods.io.api.gw.20.png)
  ![](./images/part.2-1.webMethods.io.api.gw.21.png)
  ![](./images/part.2-1.webMethods.io.api.gw.22.png)
  ![](./images/part.2-1.webMethods.io.api.gw.23.png)
  
  
  ## Part 2.2 가독성 높은 HTTP Resource 추가  
  webMethods.io Integration의 Webhook URL은 가독성이 떨어지기 때문에 /slacke/message 와 /sms/message 리소스 추가하여 request path를 매핑해 보도록 하겠습니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.01.png)
  ![](./images/part.2-2.webMethods.io.api.gw.02.png)
  ![](./images/part.2-2.webMethods.io.api.gw.03.png)
  ![](./images/part.2-2.webMethods.io.api.gw.04.png)
  ![](./images/part.2-2.webMethods.io.api.gw.05.png)
  ![](./images/part.2-2.webMethods.io.api.gw.06.png)
  ![](./images/part.2-2.webMethods.io.api.gw.07.png)
  ![](./images/part.2-2.webMethods.io.api.gw.08.png)
  ![](./images/part.2-2.webMethods.io.api.gw.09.png)
  ![](./images/part.2-2.webMethods.io.api.gw.10.png)
  ![](./images/part.2-2.webMethods.io.api.gw.11.png)
  ![](./images/part.2-2.webMethods.io.api.gw.12.png)
  ![](./images/part.2-2.webMethods.io.api.gw.13.png)
  ![](./images/part.2-2.webMethods.io.api.gw.14.png)
  ![](./images/part.2-2.webMethods.io.api.gw.15.png)
  
  
  ## Part 2.3 패키지와 플랜 작성  
  지금 만든 API를 배포하여 사용할 수 있지만 보안적인 부분과 API Consumer들에게 API 정책을 차별화하여 제공하기 위해서는 API를 패키징하여 플랜을 같이 제공해야 합니다.  
  Package와 Plan을 작성해보도록 하겠습니다.
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.01.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.02.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.03.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.04.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.05.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.06.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.07.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.08.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.09.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.10.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.11.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.12.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.13.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.14.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.15.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.16.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.17.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.18.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.19.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.20.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.21.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.22.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.23.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.24.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.25.png)
  
  
  ## Part 2.4 API 포탈의 개발자 피드백 확인  
  자연스러운 튜토리얼 진행 흐름은 TutorialMessage API 버전 1.0을 사용하기 위해서 사용하고자 하는 플랜에 가입(Subscription)하고 API Client 개발을 위해서 API Portal에서 선호하는 언어(java,c,c#,node.js 등)의 클라이언트 SDK를 다운로드 받아서 API Client 샘플 코드로 연계해 봐야 합니다.  
  이 부분은 본 튜토리얼에서는 SKIP하고 충분히 사용하다가 API를 사용하다가 불편한 점을 API Portal에 HTTP Resource를 추가 지원해주는 의견을 게시하는 것으로 가정하겠습니다.
  ![](./images/part.2-4.webMethods.io.api.feedback.01.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.02.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.03.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.04.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.05.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.06.png)
  
  
  ## Part 2.5 Mashup을 이용한 신규 HTTP Resource 생성  
  API Portal의 개선 요청 게시글의 "좋아요" 건수 매우 많아서 개선 요청 내용을 API에 반영해주기로 합니다.  
  API Mashup 기능을 사용하여 쉽게 새로운 HTTP Resource을 추가해보도록 하겠습니다.  
  ![](./images/part.2-5.webMethods.io.api.mashup.01.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.02.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.03.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.04.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.05.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.06.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.07.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.08.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.09.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.10.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.11.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.12.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.13.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.14.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.15.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.16.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.17.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.18.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.19.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.20.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.21.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.22.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.23.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.24.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.25.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.26.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.27.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.28.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.29.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.30.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.31.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.32.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.33.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.34.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.35.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.36.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.37.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.38.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.39.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.40.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.41.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.42.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.43.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.44.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.45.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.46.png)
  ![](./images/part.2-5.webMethods.io.api.mashup.47.png)
  
  
  ## [API 해커톤 및 베타 프로그램](https://engage.softwareag.cloud/)  
  살아있는 API 서비스를 하기 위해서는 API 개발자들과 지속적으로 소통할 수 있는 채널이 필요합니다.  
  API Portal의 커뮤너티 등을 이용하여 소통도 당연히 해야 하겠지만 보다 적극적으로 API 개발자들의 참여 유도 및 동기 부여가 필요합니다.  
  API Engagement 서비스을 이용하여 API 해커톤(Hackathons)과 베타 프로그램(BETA Programs) 행사를 만들 수 있습니다. 이를 통해서 API 개발자들과 보다 긴밀히 소통할 수 있습니다.  
  API Engagement 서비스는 Software AG가 webMethods.io와는 별도로 제공하는 클라우드 서비스로 고객이 필요한 기간 동안만 API 해커톤/베타 프로그램 쉽게 수행할 수 있습니다.  
  API Engagement 클라우드 서비스 URL : https://engage.softwareag.cloud  
  
  