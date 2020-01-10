  ## 'webMethods.io Integration과 API 살펴보기' 튜토리얼 - Part 1  
  2019년 12월 webMethods User Group Meetup 행사의 'webMethods.io Integration과 API 살펴보기' Part 1으로 webMethods.io Integration에 대한 튜토리얼입니다.  
  Part 1과 Part 2에 대한 전체적인 개요 설명을 [Dec-2019 유저 그룹 행사 페이지](https://github.com/SoftwareAG-Korea/tutorials/tree/master/UserGroup/Dec-2019/wmio+integration+api/)를 참고하세요.  
  
  Part 1과 Part 2에 대한 전체적인 개요 설명부터 시작하시려면 [Dec-2019 유저 그룹 행사 페이지](https://github.com/SoftwareAG-Korea/tutorials/tree/master/UserGroup/Dec-2019/wmio+integration+api/)를 참고하세요.  
  
  > Author: Software AG Korea [이범](https://github.com/billybeom)  
  > Last Modified: 10-JAN-2020  
  > Last Modified: 10-JAN-2020  
  
  
  ### Part 1의 사전 준비 사항    
  * (필수) [webMethods.io Integration - Free Trial 신청](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/Prerequisite/README.preq1.md)  
  * (필수) [Saleforce Developer Free Trial](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/Prerequisite/README.preq2.md)  
  * (필수) [Saleforce에서 ConnectedApp 생성](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/Prerequisite/README.preq3.md)  
  * (옵션) [Postman으로 access token과 refresh token 받기](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/Prerequisite/README.preq4.md)  
  
  ### Part 1. webMethods.io Integration 튜토리얼  
  webMethods.io Integration에서 Salesforce connector을 이용하여 생성되는 Lead로부터 연락처를 입력하고 Slack과 SMS를 보내는 workflow를 만들어 봅니다.  
  
  ### Part 1.1 webMethods.io Integration 로그인 및 프로젝트 생성
  ![](./images/part.1-1.webMethods.io.01.png)
  ![](./images/part.1-1.webMethods.io.02.png)
  ![](./images/part.1-1.webMethods.io.03.png)
  ![](./images/part.1-1.webMethods.io.04.png)
  ![](./images/part.1-1.webMethods.io.05.png)
  ![](./images/part.1-1.webMethods.io.06.png)
  
  
  ### Part 1.2 Workflow 생성  
  ![](./images/part.1-2.webMethods.io.Create.Workflow.01.png)
  ![](./images/part.1-2.webMethods.io.Create.Workflow.02.png)
  ![](./images/part.1-2.webMethods.io.Create.Workflow.03.png)
  
  
  ### Part 1.3 Biz Workflow - 리드 트리거 설정  
  Salesforce에서 사전에 만든 ConnectedApp의 OAuth을 받아서 Salesforce 트리거를 설정합니다.
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.01.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.02.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.03.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.04.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.05.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.06.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.07.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.08.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.09.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.10.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.11.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.12.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.13.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.14.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.15.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.16.png)
  ![](./images/part.1-3.webMethods.io.Workflow.Trigger.Leads.17.png)
  
  
  ### Part 1.4 Biz Workflow - 연락처 입력  
  Salesforce 이외의 다른 CRM SaaS 서비스에 입력할 수도 있습니다. 본 튜토리얼에서는 Lead에 들어온 연락처 정보를 Salesforce의 연락처에 입력하는 시나리오로 진행합니다.
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.01.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.02.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.03.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.04.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.05.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.06.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.07.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.08.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.09.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.10.png)
  ![](./images/part.1-4.webMethods.io.Workflow.Create.Contact.11.png)
  
  
  ### Part 1.5 Biz Workflow - Slack 메신저 보내기  
  사내 메신저가 SaaS/PaaS처럼 API를 제공한다면 node.js로 Custom(사용자 정의) Connector를 만들어서 사용할 수 있습니다. 본 튜토리얼에서는 Slack 메신저로 Salesforce의 Lead 정보를 에 다수의 Slack 사용자가 초대되어 있는 Lead 채널에 Lead 정보를 보내는 시나리오로 진행합니다.  
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.01.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.02.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.03.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.04.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.05.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.06.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.07.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.08.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.09.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.10.png)
  ![](./images/part.1-5.webMethods.io.Workflow.Send.Message.Slack.11.png)
  
  
  ### Part 1.6 Biz Workflow - SMS 문자 보내기  
  Twilio라는 글로벌 SMS SaaS 서비스를 연동하는 경우에는 Twilio Connector를 제공하기 때문에 보다 쉽게 연동할 수 있습니다. 본 튜토리얼에서는 국내 SMS 문자 및 카카오 메시지 서비스를 하는 알리고(Aligo) API를 이용하여 연동하기로 합니다. 알리고(Aligo) 서비스는 유료 서비스이기 때문에 test 파라미터를 설정하여 호출이 잘되는지만 확인하도록 하겠습니다.  
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.01.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.02.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.03.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.04.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.05.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.06.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.07.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.08.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.09.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.10.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.11.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.12.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.13.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.14.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.15.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.16.png)
  ![](./images/part.1-6.webMethods.io.Workflow.Send.Message.SMS.17.png)
  
  
  ### Part 1.7 Reuse 01 Workflow - Slack/SMS 공통 workflow 만들기  
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.01.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.02.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.03.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.04.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.05.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.06.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.07.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.08.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.09.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.10.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.11.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.12.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.13.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.14.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.15.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.16.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.17.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.18.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.19.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.20.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.21.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.22.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.23.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.24.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.25.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.26.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.27.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.28.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.29.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.30.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.31.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.32.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.33.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.34.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.35.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.36.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.37.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.38.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.39.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.40.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.41.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.42.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.43.png)
  ![](./images/part.1-7.webMethods.io.Workflow.Reuse.workflow.44.png)
  
  
  ### Part 1.8 (옵션) 네이버 파파고 번역 서비스 연동하기  
  SMS 문자 보내는 workflow로 연결해야 해야 하지만 알리고(Aligo) 서비스는 유료 서비스이기 떄문에 Slack 메시지를 보내는 Workflow에 파파고 번역 서비스를 API로 연동하는 시나리오로 진행합니다.  
  ![](./images/part.1-8.Optional.Translate.01.png)
  ![](./images/part.1-8.Optional.Translate.02.png)
  ![](./images/part.1-8.Optional.Translate.03.png)
  ![](./images/part.1-8.Optional.Translate.04.png)
  ![](./images/part.1-8.Optional.Translate.05.png)
 
  
  
  ### Part 1.9 (옵션) 공통 workflow 대신에 API 서비스로 변경
  Biz workflow에서 공통 Slack/SMS workflow 호출하는 부분을 Part 2에서 만든 API로 안전하게 연동해보세요.
  
  
