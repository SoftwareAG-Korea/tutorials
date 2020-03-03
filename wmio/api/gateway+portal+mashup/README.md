  ## 'webMethods.io Integration과 API 살펴보기' 튜토리얼 - Part 2  
  
  2019년 12월 webMethods User Group Meetup 행사의 'webMethods.io Integration과 API 살펴보기' Part 2로 webMethods.io API에 대한 튜토리얼입니다.  
  Part 1과 이어지는 튜토리얼이므로 Part 1을 먼저 확인하시고 Part 2를 진행하시기 바랍니다.  
  ['webMethods.io Integration과 API 살펴보기' Part 1](https://github.com/SoftwareAG-Korea/tutorials/blob/master/wmio/integration/salesforce+messanger+sms/README.md)을 참고 하세요.  
  
  Part 1과 Part 2에 대한 전체적인 개요 설명부터 시작하시려면 [Dec-2019 유저 그룹 행사 페이지](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/wmio+integration+api/)를 참고하세요.  
  
  > Author: [Software AG, Korea](https://www.softwareag.com/kr/) [이범](https://github.com/billybeom)  
  > Last Modified: 10-JAN-2020  
  
  
  ### Part 2의 사전 준비 사항  
  * (필수) [webMethods.io API - Free Trial 신청](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/wmio+integration+api/Prerequisite/README.preq1.md)  
  * (옵션) [네이버 파파고 번역 API 사용 신청](https://github.com/SoftwareAG-Korea/tutorials/blob/master/UserGroup/Dec-2019/wmio+integration+api/Prerequisite/README.preq5.md)  

  
  ### Part 2. webMethods.io API 튜토리얼  
  
  webMethods.io Integration에서 만든 Slack과 SMS workflow을 webMethods.io API에서 API로 만들어 봅니다.  
  Part 2 튜토리얼에서 살펴보는 'workflow을 API로 만드는 과정'이 매우 쉽게 바뀔 예정입니다. 2020년 Spring Release에서는 webMethods.io Integration에서 생성한 workflow를 버튼 몇번 클릭으로만으로 webMethods.io API Gateway에 API을 쉽게 배포할 수 있도록 변경 예정입니다.  
  
  ### Part 2.1 webMethods.io API로 이동 및 API 생성  
  webMethods.io에서 API 생성을 위해서 webMethods.io API Gateway로 이동합니다.   
  ![](./images/part.2-1.webMethods.io.api.gw.01.png)  
  APIs 메뉴를 선택한 후 'Create API' 버튼을 클릭하여 API 생성을 시작합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.02.png)  
  OpenAPI 3.0, Swagger 2.0, RAML 등의 API 명세서(Specification)의 파일이나 URL을 통해서 APIs을 쉽게 생성할 수 있습니다.  
  본 Part 2 튜토리얼은 webMethods.is Integration에서 생성한 workflow에 Webhook으로 생성된 URL을 매뉴얼하게 API를 생성하는 과정으로 진행되기 때문에 3번째 scratch 방식을 선택합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.03.png)  
  
  아래의 URL은 webMethods.io Integration에서 생성했단 Slack과 SMS 메시지를 보내는 workflow의 Webhook URL과 파라미터입니다.  
  API로 등록할 Native 서비스(Slack과 SMS workflow)의 Server URL과 HTTP Resource를 확인합니다. Slack/SMS을 보내는 Workflow에 대한 API를 각각 만들지 않고 TutorialMessage 라는 API 서비스로 만들어서 2개의 Native 서비스를 가지고 있도록 API를 아래처럼 구성합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.04.png)  
  Slack과 SMS workflow에 대한 API에 대한 기본 정보인 Tags, Description 등을 입력합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.05.png)  
  자신의 테넌트 이름으로 생성된 webMethods.io Integration의 Server URL을 입력하여 추가합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.06.png)  
  ![](./images/part.2-1.webMethods.io.api.gw.07.png)  
  'Add resources'을 클릭하여 TutorialMessage에서 제공할 HTTP Resource들을 추가합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.08.png)  
  아래 2개의 그림은 Slack 메시지를 보내는 Slack workflow에 대한 Native 서비스의 URI(HTTP Resource)를 추가하는 과정입니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.09.png)  
  ![](./images/part.2-1.webMethods.io.api.gw.10.png)  
  아래 2개의 그림은 SMS 메시지를 보내는 SMS workflow에 대한 Native 서비스의 URI(HTTP Resource)를 추가하는 과정입니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.11.png)  
  API에 대한 필수 정보 설정이 끝났으니 저장합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.12.png)  
  (옵션) 다음은 필수 과정이 아니지만 Schema validation과 Sample을 입력하는 과정입니다. 이와 같은 정보를 설정하면 API 명세서(Specification)에 보다 많은 정보가 담기게 되어 API 개발자들이 보다 API를 쉽게 연동하는데 도움을 수 있습니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.13.png)  
  ![](./images/part.2-1.webMethods.io.api.gw.14.png)  
    
  API에 등록될 HTTP Resource들에 대한 스키마 등록 단계입니다. 스키마를 등록해두면 API Gateway가 API 호출 요청이 받았을 때 Schema validation하는 기능을 이용할 수 있습니다.  
  아래 과정은 Slack에 대한 스키마를 등록하는 과정입니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.15.png)  
  JSON 샘플을 입력하면 JSON Schema를 생성해주는 서비스를 이용하여 Slack에 대한 Schema를 생성합니다. 필요에 따라서 자동 생성된 Schema를 수정해서 사용합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.16.png)  
  Slack에 대한 JSON Schema를 설정합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.17.png)  
  아래 과정은 SMS에 대한 스키마를 등록하는 과정입니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.18.png)  
  위에서 Slack에 대한 스키마를 자동 생성한 것과 같이 SMS에 대한 Schema를 생성합니다. 필요에 따라서 자동 생성된 Schema를 수정해서 사용합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.19.png)  
  SMS에 대한 JSON Schema를 설정합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.20.png)  
  아래 과정은 샘플을 입력하는 과정입니다. Slack과 SMS에 대한 JSON Schema를 생성할 사용했던 샘플 JSON으로 설정합니다.  
  ![](./images/part.2-1.webMethods.io.api.gw.21.png)  
  ![](./images/part.2-1.webMethods.io.api.gw.22.png)  
  ![](./images/part.2-1.webMethods.io.api.gw.23.png)  
  
  
  ### Part 2.2 가독성 높은 HTTP Resource 추가  
  webMethods.io Integration의 Webhook URL은 unique한 URI로 생성되어 가독성이 떨어지기 때문에 /slacke/message 와 /sms/message HTTP Resource를 추가하여 원래의 Webhook URL의 HTTP Resource로 request path를 매핑해 보도록 하겠습니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.01.png)  
  우선 TutorialMessage API에 /slack/message HTTP Resource와 /sms/message HTTP Resource를 추가합니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.02.png)  
  ![](./images/part.2-2.webMethods.io.api.gw.03.png)  
  ![](./images/part.2-2.webMethods.io.api.gw.04.png)  
  /slack/message HTTP Resource와 /sms/message HTTP Resource에 대한 JSON Schema 추가 작업 부분은 직접 해보시기 바랍니다.  
  Part 2.1에서 JSON Schema를 Components 메뉴에서 추가했기 때문에 기존에 설정했던 JSON Schema를 재활용하여 선택할 수 있습니다(part.2-1.webMethods.io.api.gw.20.png 그림 참고).  
  ![](./images/part.2-2.webMethods.io.api.gw.05.png)  
  이제 request path 매핑을 위해서 'Policies' 메뉴로 이동합니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.06.png)  
  가운데 그림에서 파란색 선은 요청 받아서 처리하는 단계이고 녹색 선은 Native 서비스의 응답을 받아서 API를 호출한 클라이언트에서 응답을 처리하는 단계입니다. 실제 Native 서비스가 호출되기 전에 /slack/message와 /sms/message의 URI를 본래의 Native 서비스인 webMethods.io Integration에서 생성한 workflow의 Webhook URI로 변경하기 위해서 'Request Processing' 단계의 'Request Transformation'를 추가하여 아래와 같이 request mapping을 설정합니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.07.png)  
  ![](./images/part.2-2.webMethods.io.api.gw.08.png)  
  '{request.path}' 변수의 값이 slack 이라는 값이 있으면 '{request.path}'의 값을 slack workflow의 본래의 URI로 변경하도록 설정합니다.   
  ![](./images/part.2-2.webMethods.io.api.gw.09.png)  
  본 튜토리얼에서는 Webhook에 인증 부분을 설정하지 않았기 떄문에 아래의 녹색 글자 설명 부분은 인증에 대한 추가 설명이오니 참고하시고 한번 해보고 싶은 분들은 Part 1에서 Workflow의 Webhook 설정에서 authentication 설정을 하고 아래 녹색 글자 설명대로 따라하시면 됩니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.10.png)  
  sms workflow에 대한 request mapping 단계를 slack request 매핑한 것처럼 'Request Processing' 단계의 'Request Transformation'를 하나 더 추가하여 '{request.path}' 변수의 값이 sms 이라는 값이 있으면 '{request.path}'의 값을 sms workflow의 본래의 URI로 변경하도록 설정합니다.
  ![](./images/part.2-2.webMethods.io.api.gw.11.png)  
  가독성이 높은 HTTP Resource에 대한 URI에 대한 매핑이 완료 되었으니 해당 API를 활성화합니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.12.png)  
  POSTMAN에서 방금 만든 API들에 대해서 테스트하기 위해서 위의 단계에서 OpenAPI 3.0 API 명세서(Specification)을 다운로드 받아서 POSTMAN에서 IMPORT합니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.13.png)  
  POSTMAN에서 지금까지 추가한 HTTP Resource들에 대해서 테스트를 수행합니다. 본 튜토리얼에서는 slack workflow의 Native 서비스를 위한 API 2개를 호출 테스트를 진행하여 잘 동작하는 것을 확인합니다. sms workflow에 대한 부분도 테스트를 해보시기 바랍니다.  
  ![](./images/part.2-2.webMethods.io.api.gw.14.png)  
  ![](./images/part.2-2.webMethods.io.api.gw.15.png)  
  
  
  ### Part 2.3 패키지와 플랜 작성  
  지금까지 생성한 API는 보안 부분을 고려되지 않았습니다. API 서비스들은 인가된 사용자(어플리케이션)에게 다양한 API 정책을 차별화하여 제공하는 것이 일반적입니다. 예를 들어서, 무료 사용자는 1시간에 5회까지 API를 사용할 수 있도록 하고 기본 유료 사용자는 1시간에 10회까지만 VIP 유료 사용자는 1시간에 60회까지 사용할 수 있도록 할 수 있습니다. 이를 위해서는 API를 패키징하고 서비스 플랜을 설정해야 합니다.  
  API 패키징(Packaging)은 여러 API를 묶어서 하나의 API 상품으로 만드는 작업이고 플랜(Plan)은 상품화한 API를 서비스할 정책 수립하고 구성하는 단계입니다. Plan에서 API 과금, API 제한에 대한 설정을 할 수 있습니다. API에 대한 제한은 Rate Limit(순간 폭주 제한)와 Quota(전체 호출 회수 제한)로 설정 가능합니다.  
  그럼 Package와 Plan을 만들어보는 튜토리얼을 시작해보도록 하겠습니다.  
  우선 Package에 매핑될 ForFree와 ForInternal 2개 Plan을 만들도록 하겠습니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.01.png)  
  ForInternal Plan에 대한 기본 정보를 설정합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.02.png)  
  Pricing을 비용, Terms, License 문구 등을 아래와 같이 설정합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.03.png)  
  QoS(Quality of Service)로 API 호출 제한을 위해서 Rate limits와 Quota Rule을 아래와 같이 추가합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.04.png)  
  Rate limits를 1분에 20회까지 호출할 수 있도록 설정합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.05.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.06.png)  
  Quota는 1시간 동안 최대 100회까지 호출할 수 있도록 설정합니다. Quota가 70% 혹은 80% 정도 찼으면 담당자에게 이메일로 알려줄 수 있도록 설정하려면 아래의 그림에서 녹색으로 표시한 부분을 활성화하여 설정합니다.  
  방금 ForInternal 플랜을 설정한 것처럼 ForFree 플랜을 직접 설정해보시기 바랍니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.07.png)  
  Plan 설정이 완료되었으니 이제 만든 API들에 대해서 Packaging해보도록 하겠습니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.08.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.09.png)  
  패키징에 대한 Name, Version, Description과 같은 기본 정보를 입력합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.10.png)  
  패키징할 때 어떤 Plan을 매핑할 지 선택합니다. 위의 단계에서 생성한 Plan들 중에서 사용할 Plan만 선택합니다. 본 튜토리얼에서는 2개의 Plan을 모두 선택하겠습니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.11.png)  
  패키징할 API들을 선택합니다. 여러개의 API들을 선택할 수 있지만 본 튜토리얼에서는 우리가 튜토리얼에서 생성한 TutorialMessage API 한개만 선택하는 것으로 진행하겠습니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.12.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.13.png)  
  이렇게 패키징을 하고 나면 QoS로 설정된 Plan 부분이 자동으로 API Throttling 정책이 추가됩니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.14.png)  
  
  아래의 설정은 webMethods.io의 API Gateway에서 사용할 API Portal의 연결 설정하는 화면입니다. API Gateway에서 API를 만들어서 외부로 노출시키기 위해서는 API Portal에 생성한 API가 배포되어야 하기 떄문입니다. 본 작업은 초기에 한번만 설정하면 됩니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.15.png)  
  생성한 API, Package들을 아래와 같이 API Portal로 배포합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.16.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.17.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.18.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.19.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.20.png)  
  API Portal로 잘 배포되었는지 API Portal로 이동하여 확인합니다.  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.21.png)  
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.22.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.23.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.24.png)
  ![](./images/part.2-3.webMethods.io.api.gw.create.plan.package.25.png)
  
  
  ### Part 2.4 API 포탈의 개발자 피드백 확인  
  자연스러운 튜토리얼 진행 흐름은 TutorialMessage API 버전 1.0을 사용하기 위해서 사용하고자 하는 플랜에 가입(Subscription)하고 API Client 개발을 위해서 API Portal에서 선호하는 언어(java,c,c#,node.js 등)의 클라이언트 SDK를 다운로드 받아서 API Client 샘플 코드로 연계해 봐야 합니다.  
  본 튜토리얼에서는 TutorialMessage API 버전 1.0을 어느 정도 기간동안 충분히 API를 연동하다가 불편한 점을 API Portal에 새로운 HTTP Resource를 추가 지원해달라고 하는 의견을 게시하는 것으로 가정하겠습니다.
  ![](./images/part.2-4.webMethods.io.api.feedback.01.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.02.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.03.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.04.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.05.png)
  ![](./images/part.2-4.webMethods.io.api.feedback.06.png)
  
  
  ### Part 2.5 Mashup을 이용한 신규 HTTP Resource 생성  
  API Portal의 개선 요청 게시글의 "좋아요" 건수가 높은 것을 확인하고 개선 요청 내용을 API에 반영해주기로 합니다.  
  API의 Natvie 서비스를 추가 개발하는 것이 아니라 API Gateway 단에서 기존의 API Resource들을 가지고 API를 Mashup하여 새로운 HTTP Resource을 쉽게 빠르게 추가해 보도록 하겠습니다.  
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
  
  
  ### [API 해커톤 및 베타 프로그램](https://engage.softwareag.cloud/)  
  살아있는 API 서비스를 하기 위해서는 API 개발자들과 지속적으로 소통할 수 있는 채널이 필요합니다.  
  API Portal의 커뮤너티 등을 이용하여 소통도 당연히 해야 하겠지만 API 개발자들의 보다 적극적인 참여 유도 및 동기 부여를 위해서 해커톤 및 베타 프로그램 행사가 필요하기도 합니다.  
  API Engagement platform 서비스는 webMethods.io와는 별도로 제공하는 클라우드 서비스로 필요한 기간 동안만 API 해커톤/베타 프로그램을 빠르고 쉽게 연결하여 운영할 수 있습니다.  
  API Engagement platform 서비스를 통해서 API Consumer와 API Provider들은 보다 긴밀히 소통할 수 있습니다.  
  API Engagement platform 서비스 URL: https://engage.softwareag.cloud  
  
  
