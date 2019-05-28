## [안내] 카카오 i 오픈빌더(챗봇 빌더 플랫폼) 문의하기

카카오 i 오픈빌더(https://i.kakao.com)에 대한 문의는 kakao i developers DevTak(https://i.kakao.com/forum)에서 받고 있습니다. 
카카오 i 오픈빌더를 통한 챗봇 제작 관련 문의는 kakao i developers DevTak에 해주시면 감사하겠습니다. 

## [공지] API형 스마트채팅 신규 등록 중단 및 카카오 i 오픈빌더 오픈 안내 

안녕하세요. 플러스친구팀입니다. <br/>
18년 12월 3일(월), 스마트채팅 기능의 변경사항이 있어 관련 내용 안내드립니다. <br/>

#### 1. 기존 'FAQ형'의 이름이 '채팅방 메뉴'로 변경되었습니다. 
- 스마트채팅 하위 메뉴에 있는 '채팅방 메뉴' 페이지에서 기존에 등록한 FAQ형 스마트채팅 정보를 관리할 수 있습니다. 

#### 2. API형 스마트채팅 신규 등록이 중단되었습니다.
- 18년 12월 3일(월), 플러스친구 챗봇을 제작할 수 있는 플랫폼인 카카오 i 오픈빌더의 OBT가 시작됨에 따라 기존 API형 스마트채팅의 신규 등록이 중단되었습니다. 기존에 사용 중이던 API형 스마트채팅의 설정 및 수정은 가능하오나 19년 12월에는 API형 스마트채팅이 완전히 종료될 예정입니다. 카카오 i 오픈빌더에서 플러스친구와 챗봇을 연동할 경우, 기존에 등록된 API형 스마트채팅의 앱정보가 삭제되며 API형 스마트채팅 사용이 불가능하오니 참고 부탁드립니다. 
- API형 스마트채팅 신규 등록 중단 공지: https://center-pf.kakao.com/notices/233

#### 카카오톡 플러스친구 챗봇을 제작할 수 있는 플랫폼인 카카오 i 오픈빌더의 OBT가 시작되었습니다. 
- 스마트채팅 하위 메뉴인 '챗봇' 페이지 접속 시 카카오 i 오픈빌더 플랫폼(https://i.kakao.com)으로 접근할 수 있으며 대화형 인터페이스의 챗봇을 제작할 수 있습니다. 카카오 i 오픈빌더에서 챗봇과 플러스친구를 연동할 경우 '채팅방 메뉴'와 'API형 스마트채팅'은 사용할 수 없습니다. 
- API형 스마트채팅에 비해 다양한 형태의 Rich Type 말풍선, 바로연결 버튼, 봇제너릭 메뉴, 각종 플러그인 기능 등 챗봇 설계를 위한 다양한 기능들이 지원됩니다. 

## 카카오톡 플러스친구 API v. 2.0 개요
이 문서는 플러스친구를 통하여 자동응답 기능을 이용하고자 할 때 사용되는 API에 대해 기술합니다.
 
## 1. 이용에 대한 참고사항

 1. 서버간 통신은 보안을 위하여 HTTPS를 쓰도록 권장합니다.<br/>
 1. HTTPS를 통하여 API를 이용하는 파트너사 서버는 유효한 공인인증서를 사용해야 합니다.<br/>
 1. user\_key는 외부에 노출되지 않도록 주의해 주시기 바랍니다.<br/>
 1. 플러스친구 API 운영에 대한 정책 및 가이드라인은 [플러스친구 이용약관](https://center-pf.kakao.com/terms)의 API 플랫폼 운영정책을 참고해 주시기 바랍니다.<br/>

## 2. 개인정보 수집 및 이용에 대한 주의사항

 1. API 이용에 대한 주의사항은 [서비스 이용약관](https://center-pf.kakao.com/terms) '제 26 조 API 플랫폼 서비스'를 따르며, 이를 준수하지 않을 경우 API 서비스 제공을 중단할 수 있습니다. 
 2. 회원이 API 플랫폼 서비스를 이용하는 과정에서 이용자의 개인정보 수집이 필요한 경우, 이용자로부터 개인정보 수집 및 이용에 대한 명시적인 동의를 받아야 합니다.
 3. 카카오는 '[개인정보 취급위탁 동의](https://center-pf.kakao.com/entrustment)'에 따라 안전하게 개인정보 처리 업무를 진행합니다.
 
## 3. 이용 시작하기
#### 3.1. 플러스친구 앱 생성
플러스친구에서 자동응답 기능을 사용하기 위해서는 먼저 운영툴을 통해 key 발급을 위한 앱을 등록해야 합니다. 

1. [플러스친구 운영툴](https://center-pf.kakao.com)의 좌측 '스마트채팅' 메뉴에서 'API형'을 선택합니다.
2. 앱 정보와 모니터링 메시지를 수신할 전화번호를 입력하고, 개인정보 수집 및 이용에 동의한 뒤 정보를 저장하여 앱을 생성합니다.

#### 3.2. 자동응답 서비스 시작
자동응답 서비스가 개발 완료되어 서비스 가능한 상태가 되면, 다음 단계에 따라 서비스를 시작할 수 있습니다.

 1. API TEST : 등록한 앱 url 우측의 API TEST 버튼을 클릭하여 서비스 시작 가능여부를 체크합니다. 필수 API인 Home Keyboard API가 정상적인 응답을 받지 못하는 경우 서비스 시작이 불가합니다. 
 2. 서비스 시작 : API 테스트를 통과한 경우, 서비스 시작 버튼을 클릭하면 자동응답 서비스가 시작됩니다.
 
 - 기존에 (구) 플러스친구 API를 통해 사용중이던 봇이 있는 경우, 신규 API를 통해 자동응답 서비스를 시작하게 되면 (구)API를 이용한 봇은 자동으로 종료되며 다시 (구) 봇의 형태로 이용할 수 없습니다.
 - (구) 플러스친구에서 제공하던 테스트 플친은 더이상 제공되지 않습니다. 실서비스 적용 전 테스트를 원하시는 경우 테스트 전용으로 사용하실 별도의 플러스친구 계정을 생성하여 테스트를 진행해 주시기 바랍니다.
 - 신규 API 자동응답은 키워드형 자동응답과 동시에 사용할 수 없습니다. 다만 API 자동응답의 서비스 중지 후 키워드형 자동응답을 사용하는 것은 가능합니다. 

#### 3.3. 자동응답 서비스 중지

 - 직접 중지 : 더 이상 자동응답 서비스를 이용하지 않으시려면, 운영툴의 자동응답 > 자동응답 API 메뉴에서 '서비스 중지'를 통해 자동응답 기능을 중지할 수 있습니다.
 - 오류 횟수 초과에 따른 중지 : 자동응답 서비스에서 오류가 발생하는 경우, 카카오는 앱 정보에 등록된 전화번호를 통해 모니터링 메시지를 발송합니다. 만일 오류 횟수가 일 1000건을 초과하게 되면 카카오는 자동으로 해당 앱의 서비스를 중지합니다. 오류 횟수 초과로 인해 중지된 앱은 운영툴에서 오류 수정 후 직접 다시 서비스를 시작할 수 있습니다.
 - 관리자의 차단에 따른 중지 : 파트너사에서 플러스친구 API의 운영정책에 반하는 내용을 API를 통해 서비스하는 것이 확인된 경우, 카카오의 관리자는 해당 앱의 서비스를 중지할 수 있습니다. 관리자에 의해 차단된 앱은 직접 서비스를 다시 시작할 수 없으므로, 앱의 차단 사유를 확인하신 뒤 문제가 되는 내용을 수정하여 플러스친구 고객센터(1544-4293)를 통해 차단 해제를 요청해 주시기 바랍니다. 
 

#### 3.4. 클라이언트 테스트
자동응답 기능의 서비스가 시작되면 카카오톡 채팅방에서 직접 자동응답 기능을 실행할 수 있습니다.
신규 자동응답 API를 통한 자동응답 기능은 카카오톡 앱 안드로이드/iOS 5.4.0 버전부터 지원됩니다.

 - 수정된 내용의 반영은 최대 1분까지 소요될 수 있으며, 채팅방을 나갔다 들어오는 시점을 기준으로 정보를 새로고침합니다.
 - 1depth 이상의 자동응답을 구현하는 경우, 카카오톡에서는 자동응답 대화의 맥락을 유지하기 위해 이전 자동응답의 정보를 메시지 수신으로부터 10분간 보관합니다. 메시지를 받은 후 10분이 경과되면 자동으로 기존의 대화 맥락은 expire되며 Home keyboard 를 호출합니다.
 - 클라이언트를 통해 노출되는 안내문구 ('원하는 버튼을 선택하세요')는 고정 문구로, 커스터마이즈할 수 없습니다.
 - 실서비스 적용 전 테스트를 원하시는 경우 별도의 플러스친구를 생성하여 테스트를 진행해보실 수 있습니다. 
 
## 4. 용어 설명

#### 4.1. 수신 API
- 카카오톡 이용자가 플러스친구에게 보낸 메시지를 전달 받은 후 응답을 할 수 있는 API 입니다.
- http(s) restful api를 통하여 카카오 API 서버 -> 파트너 서버를 호출합니다.

#### 4.2. app\_key
- 플러스친구에서 자동응답을 위한 앱 등록시 프로필별로 발급되는 고유 키 값입니다.
- 자동응답 기능만 이용하시는 경우 사용되지 않으며, 일부 app_secret을 통한 별도 인증이 필요한 일부 프로필에만 사용됩니다.


#### 4.3. app\_secret
- 인증을 위해 app\_key와 조합하여 사용되는 키 값입니다.
- 자동응답 기능만 이용하시는 경우 사용되지 않으며, 일부 app_secret을 통한 별도 인증이 필요한 일부 프로필에만 사용됩니다.

#### 4.4. user\_key
- 특정 카카오톡 이용자를 구분하기 위한 key 입니다. 카카오에서는 이용자의 개인정보를 외부에 제공하지 않으므로, 외부 파트너사에서 카카오톡 이용자를 구분하기 위해서는 카카오로부터 API를 통해 user\_key를 response로 받아야 합니다.
- user\_key는 특정 카카오톡 이용자에 대해 프로필별로 각기 다르게 발급됩니다. 따라서 user\_key는 해당 프로필에 대해서만 유효합니다.
- 카카오톡 이용자가 프로필을 차단했다가 다시 추가한 경우에는 user\_key가 갱신되지 않으며, 이용자가 카카오톡 탈퇴 후 재가입한 경우 갱신됩니다.
<br/>


## 5. API specifications

- 카카오 플러스친구 API 서버에서 개발사 서버를 호출하는 API에 대한 명세서입니다.
- 개발사는 아래 스펙에 맞춰서 http(s) 서버를 구축하셔야 합니다.
- 응답 지연시간 : 최대 5초안에 응답이 오지 않는 경우 응답없음 메시지가 사용자에게 발송됩니다.
- QoS : 만약 응답 실패가 10회 이상 발생하게 되면 자동적으로 해당 모듈은 지정된 장애 메시지를 리턴하게 됩니다. 더불어 앱 등록시 지정된 관리자에게 카카오톡으로 장애 메시지가 발송됩니다.
- [플러스친구 운영도구](https://center-pf.kakao.com)를 통해 설정한 개발사 서버 URL을 호출하게 됩니다.
- 개발사 서버가 방화벽으로 보호되고 있는경우 [Server information](https://github.com/plusfriend/auto_reply#7-server-information) 문서를 참고해주세요.


#### 5.1. Home Keyboard API
- 이용자가 최초로 채팅방에 들어올 때 기본으로 키보드 영역에 표시될 자동응답 명령어의 목록을 호출하는 API입니다.
- 챗팅방을 지우고 다시 재 진입시에도 호출됩니다. 다만 카카오 서버에서도 1분동안 캐쉬가 저장되기 때문에 유저가 채팅방을 지우고 들어오는 행동을 반복하더라도 개발사 서버를 1분에 한번씩 호출하게 됩니다. 즉, 개발사 서버에서 정보가 변경되어도 최대 1분뒤에 유저들에게 반영이 됩니다.
- 유저가 자동응답으로 메시지를 주고 받았을 경우는 마지막 메시지에 담겨있던 자동응답 명령어 목록이 표시됩니다. 다만 메시지에 저장된 자동응답 명령어는 10분간 유효합니다. 10분이 지난 다음에는 다시 keyboard api를 호출하여 자동응답 목록을 초기화하게 됩니다.


##### Specification
- **Method** : GET
- **URL** : http(s)://:your\_server\_url/keyboard
- **Content-Type** : application/json; charset=utf-8
- **예제**
```
curl -XGET 'https://:your_server_url/keyboard'
```
- **Response**

| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| keyboard | [Keyboard](https://github.com/plusfriend/auto_reply#6-object) | Required | 키보드 영역에 표현될 버튼에 대한 정보. 생략시 ```text``` 타입이 선택된다.|
- **예제**
```
{
    "type" : "buttons",
    "buttons" : ["선택 1", "선택 2", "선택 3"]
}
```

#### 5.2. 메시지 수신 및 자동응답 API
- 사용자가 선택한 명령어를 파트너사 서버로 전달하는 API입니다.
- 자동응답 명령어에 대한 답변은 응답 메시지(Message)와 응답 메시지에 따른 키보드 영역의 답변 방식(Keyboard)의 조합으로 이루어집니다. 답변 방식은 주관식(text)과 객관식(buttons) 중 선택할 수 있습니다.
- 자동응답을 통해 친구에게 미디어 타입(사진/동영상/오디오)을 받고자 하는 경우 주관식 키보드(text)를 선택하세요. 메시지를 통해 <‘+’버튼을 눌러 미디어를 전송하세요>와 같이 안내하는 것이 필요 할 수 있습니다.
- 유저가 보낸 미디어 타입의 카카오 서버에서의 보존기간은 아래와 같습니다.
  - 음성파일 : 20일
  - 이미지파일 : 20일
  - 비디오 : 20일
- 미디어 파일의 보존기간은 서버의 상황에 의하여 변동 될 수 있습니다.

##### Specification
- **Method** : POST
- **URL** : http(s)://:your\_server\_url/message
- **Content-Type** : application/json; charset=utf-8
- **Parameters**

| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| user\_key | String | Required | 메시지를 발송한 유저 식별 키 |
| type | String | Required | text, photo |
| content | String | Required | 자동응답 명령어의 메시지 텍스트 혹은 미디어 파일 uri |
- **예제**
```
curl -XPOST 'https://:your_server_url/message' -d '{
  "user_key": "encryptedUserKey",
  "type": "text",
  "content": "차량번호등록"
}'
```
```
curl -XPOST 'https://your_server_url/message' -d '{
  "user_key": "encryptedUserKey",
  "type": "photo",
  "content": "http://photo_url/number.jpg"
}'
```
- **Response**

| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| message | [Message](https://github.com/plusfriend/auto_reply/blob/master/README.md#62-message) | Required | 자동응답 명령어에 대한 응답 메시지의 내용. 6.2에서 상세 기술 |
| keyboard | [Keyboard](https://github.com/plusfriend/auto_reply#6-object) | Optional | 키보드 영역에 표현될 명령어 버튼에 대한 정보. 생략시 text 타입(주관식 답변 키보드)이 선택된다. 6.1에서 상세 기술|
- **예제**
```
{
    "message":{
        "text" : "귀하의 차량이 성공적으로 등록되었습니다. 축하합니다!"
    }
}
```
```
{
  "message": {
    "text": "귀하의 차량이 성공적으로 등록되었습니다. 축하합니다!",
    "photo": {
      "url": "https://photo.src",
      "width": 640,
      "height": 480
    },
    "message_button": {
      "label": "주유 쿠폰받기",
      "url": "https://coupon/url"
    }
  },
  "keyboard": {
    "type": "buttons",
    "buttons": [
      "처음으로",
      "다시 등록하기",
      "취소하기"
    ]
  }
}
```

#### 5.3. 친구 추가/차단 알림 API
- 특정 카카오톡 이용자가 플러스친구를 친구로 추가하거나 차단하는 경우 해당 정보를 파트너사 서버로 전달하는 API입니다.

##### Specification
- **Method** : POST / DELETE
- **URL** : http(s)://:your\_server\_url/friend
- **Content-Type** : application/json; charset=utf-8
- **Parameters**

| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| user\_key | String | Required | 유저 식별키 |
- **Response**

| http status code | code | message | comment |
| ---------------- | ---- | ------- | ------- |
| 200 | 0 | SUCCESS | 정상 응답 |
- **예제**
 - *친구 추가*
```
curl -XPOST 'https://:your_server_url/friend' -d '{"user_key" : "HASHED_USER_KEY" }'
```
 - *친구 삭제*
```
curl -XDELETE 'https://:your_server_url/friend/:user_key'
```

#### 5.4. 채팅방 나가기
- 사용자가 채팅방 나가기를 해서 채팅방을 목록에서 삭제했을 경우 해당 정보를 파트너사 서버로 전달하는 API입니다.

##### Specification
- **Method** : DELETE
- **URL** : http(s)://:your\_server\_url/chat\_room/:user\_key
- **Content-Type** : application/json; charset=utf-8
- **Response**

| http status code | code | message | comment |
| ---------------- | ---- | ------- | ------- |
| 200 | 0 | SUCCESS | 정상 응답 |
- **예제**
```
curl -XDELETE 'https://:your_server_url/chat_room/HASHED_USER_KEY'
```

## 6. Object

##### 6.1. Keyboard

 - 응답 메시지에 따라 사용자의 키보드 영역에 표현될 메시지 입력방식에 대한 정보입니다.
 - 별도로 설정하지 않는 경우 text 타입이 기본으로 설정됩니다.
 
| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| type | String | Required | buttons: 객관식 응답의 목록을 구성할 수 있음 <br/>text: 주관식 응답을 입력받을 수 있음 |
| buttons | Array[String] | Optional | 객관식 응답 내용의 목록 <br/>(최대 100개)|

 - 직접 입력
```
{
  "type": "text"
}
```
 - 버튼 입력
   
```
{
  "type": "buttons",
  "buttons": [
    "선택 1",
    "선택 2",
    "선택 3"
  ]
}
```


##### 6.2. Message

 - 카카오톡 이용자가 명령어를 선택 혹은 입력했을 때 이용자에게 전송하는 응답 메시지입니다.
 - String, photo, MessageButton의 조합으로 이루어집니다.
 - 3가지 타입 중 1개 이상이 반드시 들어가야 하며, 최대 3가지 타입 모두 포함될 수 있습니다.

| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| text | String |  Optional | 사용자에게 발송될 메시지 텍스트(최대 1000자) |
| photo | [Photo](https://github.com/plusfriend/auto_reply/blob/master/README.md#63-photo) | Optional | 말풍선에 들어갈 이미지 정보. 1장 제한, JPEG/PNG 포맷. 6.3에서 상세 기술 |
| message_button| [MessageButton](https://github.com/plusfriend/auto_reply/blob/master/README.md#621-messagebutton) | Optional | 말풍선에 붙는 링크버튼 정보. 6.2.1에서 상세 기술 |
 
```
{
  "text": "안녕하세요.",
  "photo": {
    "url": "https://hello.photo.src",
    "width": 640,
    "height": 480
  },
  "message_button": {
    "label": "반갑습니다.",
    "url": "http://hello.world.com/example"
  }
}
```
###### 6.2.1. MessageButton

 - 응답 메시지의 말풍선 하단에 보여지는 링크버튼 정보입니다.

| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| label | String | Required | 링크버튼의 타이틀 |
| url | String | Required | 링크버튼의 연결 링크 주소 |

```
{
  "label": "쿠폰확인하기",
  "url": "http://coupon.coupon.com/~~"
}
```

##### 6.3. Photo

 - 이미지 정보
 
| 필드명 | 타입 | 필수여부 | 설명 |
| ---- | ---- | -------- | ----------- |
| url | String | Required | 이미지 url |
| width | Int | Required | 이미지 width  |
| height | Int | Required | 이미지 height |

> 이미지 권장 사이즈 : 720 x 630px  
지원 파일형식 및 권장 용량 : jpg, png /500KB

```
{
  "url": "https://photo.src",
  "width": 640,
  "height": 480
}
```

## 7. Server information

| host | port | comment |
| ---- | ---- | ---- |
| https://ybot.kakao.com | 443 | https api server |

### 7.1. Proxy Server information
카카오에서 파트너사 서버를 호출하는 경우 아래 3대의 proxy서버를 통하게 됩니다. 파트너사 방화벽 설정을 하게 될 경우 아래 3개의 IP에 대한 ACL을 허용해주시기 바랍니다.

| IP |
| ---- |
| 110.76.143.234 |
| 110.76.143.235 |
| 110.76.143.236 |

## 8. Response Code
##### Success Response

| http status code | code | message | comment |
| ---------------- | ---- | ------- | ------- |
| 200 | 0 | SUCCESS | 정상 응답 |

##### Error Response

| http status code | code |  comment |
| ---------------- | ---- |  ------- |
| 400 | 100 | bad request |
| 400 | 201 | wrong api key |
| 400 | 202 | wrong bot url |
| 503 | 203 | wrong message format |
| 408 | 204 | request timeout |
| 408 | 204 | wrong keyboard initialization |
| 400 | 301 | profile not found |
| 400 | 302 | user not found |
| 400 | 303 | not user friend |
| 400 | 400 | unsupported media type |



## 9. 질의응답
상단의 issue를 통해 자유롭게 질의응답을 나누실 수 있습니다.
- https://github.com/plusfriend/auto_reply/issues

그외 문의사항은 카카오 고객센터로 주시기 바랍니다.
- http://cs.kakao.com/requests?service=102
