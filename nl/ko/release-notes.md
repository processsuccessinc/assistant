---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# 릴리스 정보

## 서비스 API 버전화
{: shortdesc}

API 요청에는 `version=YYYY-MM-DD` 형식의 날짜를 사용하는 버전 매개변수가 필요합니다. 역호환되지 않는 방법으로 API를 변경할 때마다 API의 새 부 버전을 릴리스합니다.

모든 API 요청과 함께 버전 매개변수를 보내십시오. 서비스는 지정한 날짜의 API 버전 또는 해당 날짜 전 최신 버전을 사용합니다. 현재 날짜로 기본값을 설정하지 마십시오. 대신 앱과 호환 가능한 버전과 일치하는 날짜를 지정하고, 후속 버전에 맞게 앱이 준비될 때까지 변경하지 마십시오.

현재 버전은 `2018-02-16`입니다.

{{site.data.keyword.conversationshort}} 도구의 "연습" 분할창은 최신 API 버전을 사용합니다. 

## 베타 기능

IBM 릴리스 서비스, 기능 및 베타로 분류된 평가용 언어 지원을 제공합니다. 이러한 기능은 불안정하고 자주 변경될 수 있으며 짧은 통보로 중단될 수 있습니다. 베타 기능은 일반적으로 제공되는 기능과 동일한 수준의 성능이나 호환성을 제공하지 않을 수도 있으며 프로덕션 환경에서 사용하기 위한 것이 아닙니다. 베타 기능은 [developerWorks Answers ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/answers/topics/watson-conversation/){: new_window}에서만 지원됩니다. 

## 업데이트된 모델
{: #updated-models}

{{site.data.keyword.conversationshort}} 알고리즘은 피드백, 과학적 개선사항 및 추가 요인에 따라 주기적으로 세분화되고 업데이트되어 지속적으로 성능을 향상시킬 수 있습니다. 모델에 대한 업데이트는 이러한 릴리스 정보에 전달됩니다.

새 모델이 사용 가능하게 되고 60일이 지난 후, 훈련된 기존 모델은 바로 영향을 받지 않지만 만료된 모델은 아직 업데이트되지 않은 경우 최신 모델로 업데이트됩니다.

> **참고:** 이 업데이트 문은 GA(Generally Available) 언어 및 기능에만 적용됩니다.

## 변경사항
{: #change-log}

서비스에 대한 다음 새 기능 및 변경사항이 사용 가능합니다.

### 2018년 2월 16일
{: #16February2018}

- **대화 상자 노드 추적**: "연습" 분할창을 사용하여 대화 상자를 테스트할 경우, 위치 아이콘은 각 응답 다음에 표시됩니다. 사용자는 아이콘을 눌러 서비스가 대화 상자 트리를 통해 응답에 도달하는 경로를 강조표시할 수 있습니다. 세부사항은 [대화 상자 작성](dialog-build.html#test)을 참조하십시오. 

- **새 API 버전**: 현재 API 버전은 `2018-02-16`입니다. 이 버전은 다음 변경사항을 도입합니다.

  - 새 `include_audit` 매개변수는 이제 대부분의 GET 요청에서 지원됩니다. 이것은 응답에 감사 등록 정보(`created` 및 `updated` 시간소인) 포함 여부를 지정하는 선택적 부울 매개 변수입니다. 기본값은 `false`입니다. (`2018-02-16` 이전의 API 버전을 사용 중인 경우, 기본값은 `true`입니다.) 자세한 정보는 [API 참조(![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘"))](https://www.ibm.com/watson/developercloud/conversation/api/v1/){: new_window}를 참조하십시오.

  - 새 버전을 사용하는 API 호출의 응답은 `null`이 아닌 값이 있는 특성을 포함합니다. 

  - `output.nodes_visited` 및 `output.nodes_visited_details` 메시지 응답의 속성에는 이전에 생략된 다음 유형의 노드가 포함됩니다. 

    - Nodes with `type`=`response_condition`
    - Nodes with `type`=`event_handler` and `event_name`=`input`

### 2018년 2월 9일
{: #9February2018}

- **네덜란드 시스템 엔티티(베타)**: 네덜란드어 지원이 향상되어 베타 릴리스에 [시스템 엔티티](system-entities.html)의 가용성이 포함되었습니다. 세부사항은 [지원되는 언어](lang-support.html)를 참조하십시오. 

### 2018년 1월 29일
{: #29January2018}

- {{site.data.keyword.conversationshort}} REST API가 새 요청 매개변수를 지원합니다. 
  - 새 작업공간 데이터를 대체하지 않고 기존 데이터에 추가할지 여부를 나타내는 작업공간을 업데이트할 때 `append` 매개 변수를 사용하십시오. 자세한 정보는 [작업공간 업데이트![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/watson/developercloud/conversation/api/v1/#update_workspace){: new_window}를 참조하십시오. 
  - 메시지 처리 중에 방문한 노드에 대한 추가 진단 정보가 응답에 포함되는지 여부를 나타내는 메시지를 보낼 때 `nodes_visited_details` 매개변수를 사용하십시오. 자세한 정보는, [메시지 보내기![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/watson/developercloud/conversation/api/v1/#send_message){: new_window}을 참조하십시오. 

### 2018년 1월 23일
{: #23January2018}

- **작업공간 목록을 검색할 수 없음**: 도구에서 작업할 때 이와 유사한 오류 메시지가 표시되면, 세션이 만료되었다는 의미일 수 있습니다. **사용자 정보** 아이콘 ![사용자 정보 아이콘 메뉴](images/user-icon.png)에서 **로그아웃**을 선택하여 로그아웃한 후, 다시 로그인하십시오. 

### 2017년 12월 8일
{: #8December2017}

- **인스턴스 간에 데이터 액세스 기록(프리미엄 사용자 전용)**: {{site.data.keyword.conversationshort}} 프리미엄 사용자인 경우, 프리미엄 인스턴스는 다른 프리미엄 인스턴스에서 작업영역의 데이터를 기록할 수 있도록 선택적으로 구성할 수 있습니다. 

- **노드 복사**: 이제 노드 복제 및 해당 하위의 사본을 작성할 수 있습니다. 이 기능을 사용하면 대화 상자의 다른 위치에서 재사용하려는 유용한 논리 노드를 작성하는 경우에 유용합니다. 자세한 정보는 [대화 상자 복사](dialog-build.html#copy-node)를 참조하십시오. 

- **패턴 엔티티의 그룹 캡처**: 엔티티에 대해 정의하는 정규식 패턴의 그룹을 식별할 수 있습니다. 그룹 식별은 나중에 패턴의 하위 섹션을 참조할 수 있기를 원하는 경우에 유용합니다. 예를 들어, 엔티티에 미국 전화 번호를 캡처하는 정규식 패턴이 있을 수 있습니다. 사용자가 번호 패턴의 지역 코드 세그먼트를 그룹으로 식별하면, 해당 그룹을 참조하여 전화 번호의 지역 코드 세그먼트에 액세스할 수 있습니다. 자세한 정보는 [엔티티 정의](entities.html#creating-entities)를 참조하십시오. 

### 2017년 12월 6일
{: #6December2017}

- **{{site.data.keyword.openwhisk}}통합(베타)**: 대화 상자 노드에서 직접 조치를 호출 {{site.data.keyword.openwhisk}}(이전의 IBM OpenWhisk)하십시오. 이 기능을 사용하여, 예를 들어, 대화 상자 노드 내에서 날씨 정보를 검색한 후 대화 상자 응답에서 리턴된 정보에 따라 조건을 지정할 수 있습니다. 현재, 미국 남부에서 호스팅되는 {{site.data.keyword.conversationshort}} 인스턴스에서 조치를 호출하거나 미국 남부에서 호스팅되는 {{site.data.keyword.openwhisk_short}} 인스턴스에서 조치를 호출할 수 있습니다. 자세한 정보는 [대화 상자 노드에서 프로그래밍 방식 호출 작성](dialog-actions.html)을 참조하십시오. 

### 2017년 12월 5일
{: #5December2017}

- **인텐트 및 엔티티에 대해 재설계된 UI**: `인텐트` 및 `엔티티` 탭은 엔티티 및 인텐트를 작성하고 편집할 때 보다 쉽고 효과적인 워크 플로우를 제공하도록 재설계되었습니다. 이러한 탭에 대한 작업과 관련된 자세한 정보는 [인텐트 정의](intents.html#defining-intents) 및 [엔티티 정의](entities.html#defining-entities)를 참조하십시오. 

### 2017년 11월 30일
{: #30November2017}

- **동부 아랍어 숫자 지원**: 이제 동부 아랍어 숫자가 아랍어 시스템 엔티티에서 지원됩니다. 

### 2017년 11월 29일
{: #29November2017}

- **작업공간에서 사용자 입력에 대한 이해 개선**: 이제 인스턴스 내의 다른 작업공간으로 전송된 표현이 있는 작업공간을 향상시킬 수 있습니다. 예를 들어, 여러 버전의 프로덕션 작업공간 및 개발 작업공간이 있는 경우, 동일 표현 데이터를 사용하여 이 공간을 향상시킬 수 있습니다. 자세한 정보는 [작업공간에서 개선](logs.html#deploy_id) 및 [데이터 소스 선택](logs_convo.html#select-source)을 참조하십시오. 

### 2017년 11월 20일
{: #20November2017}

- **GB18030 준수**: GB18030은 중국 시장에서 사용할 확장 코드 페이지를 지정하는 중국 표준입니다. 이 코드 페이지 표준은 중국 국가 정보 기술 표준 기술위원회가 2001년 9월 1일 이후 중국 시장에 출시되는 모든 소프트웨어 애플리케이션에 대해 GB18030을 사용하도록 정했기 때문에 소프트웨어 업계에 중요합니다. {{site.data.keyword.conversationshort}} 서비스는 이 인코딩을 지원하고 GB18030-준수 인증을 받았습니다. 

### 2017년 11월 9일
{: #9November2017}

- **인텐트 예제가 엔티티를 직접 참조할 수 있음**: 인텐트 예제에서 직접 엔티티 참조를 지정할 수 있습니다. 해당 엔티티 참조는 모든 값 또는 동의어와 함께 {{site.data.keyword.conversationshort}} 서비스 분류 기준에서 인텐트를 학습하는 데 사용됩니다. 자세한 정보는 [인텐트](intents.html) 주제의 [*엔티티 예제*](intents.html#entity-as-example)를 참조하십시오. 

  **참고**: 현재 단계에선, 사용자가 정의한 종료 엔티티만 직접 참조할 수 있습니다. 귀하는 [패턴 엔티티](entities.html#pattern-entities) 또는 [시스템 엔티티](system-entities.html)를 직접 참조할 수 없습니다. 

### 2017년 11월 8일
{: #8November2017}

- **{{site.data.keyword.conversationshort}} 커넥터**: 새로운 {{site.data.keyword.conversationshort}} 커넥터 도구를 사용하여 작업공간을 Slack 또는 Facebook Messenger 앱에 연결하여 Slack 또는 Facebook Messenger 사용자와 상호작용할 수 있는 채팅 봇으로 사용할 수 있게 합니다. 이 도구는 {{site.data.keyword.Bluemix_notm}} 미국 남부 지역에서만 사용 가능합니다. 자세한 정보는 [{{site.data.keyword.conversationshort}} 커넥터가 있는 채널에 배치](conversation-connector.html)를 참조하십시오.

### 2017년 11월 3일
{: #3November2017}

- **대화 상자 업데이트**: 다음 업데이트를 통해 대화 상자를 쉽게 작성할 수 있습니다. (세부사항은 [대화 상자 빌드](dialog-build.html) 참조.)

    - 슬롯에 조건을 추가하여 필요한 특정 조건이 충족되는 경우에만 작성할 수 있습니다. 예를 들어, 결혼 여부를 묻는 이전(필수) 슬롯 사용자가 기혼자임을 나타내는 경우에만 필요한 배우자의 이름을 묻는 슬롯을 작성할 수 있습니다. 

    - 이제 노드의 다음 단계로 **사용자 입력 건너뛰기**를 선택할 수 있습니다. 이 옵션을 선택하면, 현재 노드를 처리한 후 서비스가 현재 노드의 첫 번째 하위 노드로 직접 이동합니다. 이 옵션은 기존의 다음 단계로 *점프* 옵션과 유사하지만 더 유연합니다. 점프할 정확한 노드를 지정할 필요가 없습니다. 실행 중에 다음 단계 동작이 정의된 후 추가된 새 노드 또는 하위 노드가 재정렬되었더라도 서비스는 항상 첫 번째 하위 노드가 되는 노드로 이동합니다. 

    - 슬롯에 대한 조건부 응답을 추가할 수 있습니다. 찾음 및 찾을 수 없음 응답의 경우 특정 조건이 충족되는지 여부에 따라 서비스가 응답하는 방식을 사용자 정의할 수 있습니다. 이 기능을 사용하면 사용자가 입력한 값을 슬롯의 컨텍스트 변수에 저장하기 전에 잘못된 해석을 확인하고 오류를 수정할 수 있습니다. 예를 들어, 슬롯이 사용자의 나이를 저장하고 캡처하기 위해 *검사 대상* 필드의 `@sys-number`를 사용하면, *올바른 나이를 제공하십시오.*와 같은 100을 넘는 숫자를 확인하는 조건을 추가할 수 있습니다. 자세한 정보는 [찾음 및 찾을 수 없음 응답에 조건 추가](dialog-slots.html#slot-handler-next-steps)를 참조하십시오. 

    - 노드에 조건부 응답을 추가하는 데 사용하는 인터페이스가 각 조건과 응답을 쉽게 나열할 수 있도록 재설계되었습니다. 노드 레벨 조건부 응답을 추가하려면, **사용자 정의**를 클릭하고 **다중 응답** 옵션을 사용하십시오. 

     **참고**: **다중 응답**은 노드 레벨 응답 전용에 대한 기능을 설정 또는 설정 해제합니다. 이것은 슬롯에 대한 조건부 응답을 정의하는 기능을 제어하지 않습니다. 슬롯 다중 응답 설정은 개별적으로 제어됩니다. 

    - 슬롯을 단순하게 편집하는 페이지를 유지하려면 다음과 같은 메뉴 옵션을 선택하십시오. a.) 처리할 슬롯에 대해 충족되어야 하는 조건을 추가하고 b.) 슬롯 찾음 및 찾을 수 없음 조건에 대한 조건부 응답을 추가하십시오. 이 추가 기능을 추가하기로 선택하지 않으면 슬롯 조건과 다중 응답 필드가 표시되지 않으므로 페이지를 더 쉽게 사용할 수 있습니다. 

### 2017년 10월 25일
{: #25October2017}

- **중국어 업데이트**: 중국어에 대한 언어 지원이 개선되었습니다. 여기에는 문자 레벨 단어 임베딩을 사용하는 인텐트 분류 개선사항 및 시스템 엔티티의 가용성이 포함됩니다. {{site.data.keyword.conversationshort}} 서비스 러닝 모델은 이 개선사항의 일부로 업데이트될 수 있으며, 모델을 재훈련하면 변경사항이 적용됩니다. 자세한 정보는 [업데이트된 모델](release-notes.html#updated-models)을 참조하십시오.
- **스페인어 업데이트** - 매우 큰 데이터 세트에 대해 스페인어 인텐트 분류가 개선되었습니다.

### 2017년 10월 11일
{: #11October2017}

- **한국어 업데이트**: 한국어에 대한 언어 지원이 개선되었습니다. {{site.data.keyword.conversationshort}} 서비스 러닝 모델은 이 개선사항의 일부로 업데이트될 수 있으며, 모델을 재훈련하면 변경사항이 적용됩니다. 자세한 정보는 [업데이트된 모델](release-notes.html#updated-models)을 참조하십시오.

### 2017년 10월 3일
{: #3October2017}

- **패턴 정의 엔티티(베타)**: 이제 정규식을 사용하여 엔티티에 대한 특정 패턴을 정의할 수 있습니다. 이를 통해 정의된 패턴을 따르는 엔티티(예: SKU 또는 부품 번호, 전화 번호 또는 이메일 주소)를 식별할 수 있습니다. 세부사항은 [패턴 정의 엔티티](entities.html#pattern-entities)를 참조하십시오.
    - 단일 엔티티 값에 대한 동의어 또는 패턴을 추가할 수 있으며 둘 다 동시에 추가할 수는 없습니다.
    - 각 엔티티 값에 대해 최대 5개의 패턴이 있을 수 있습니다.
    - 각 패턴(정규식)은 128자로 제한됩니다.
    - CSV 파일을 통한 가져오기 또는 내보내기는 현재 패턴을 지원하지 않습니다.
    - REST API는 패턴에 대한 직접 액세스를 지원하지 않지만 `/values` 엔드포인트를 사용하여 패턴을 검색하거나 수정할 수 있습니다.

- **사전을 기준으로 필터링된 유사 일치(영어만 해당)**: 엔티티에 대한 유사 일치의 개선된 버전이 영어로 사용 가능합니다. 이 개선사항에서는 일부 공통된 올바른 영어 단어를 지정된 엔티티의 유사 일치로 캡처하는 일을 방지합니다. 예를 들어, 유사 일치는 엔티티 값 `like`를 `hike` 또는 `bike`(올바른 영어 단어)와 일치시키지 않지만, 계속해서 `lkie` 또는 `oike`와 같은 예제와 일치시킵니다.

### 2017년 9월 27일
{: #27September2017}

- **조건 빌더 업데이트**: 대화 상자 노드에서 조건을 정의하는 데 도움이 되도록 표시된 제어가 업데이트되었습니다. 개선사항에는 $를 입력하여 컨텍스트 변수 추가를 시작한 후 사용 가능한 컨텍스트 변수 이름을 나열하는 데 대한 지원이 포함됩니다.

### 2017년 8월 31일
{: #31August2017}

- **섹션 롤백 개선**: 평균 대화 시간 메트릭 및 해당 필터가 개선 섹션의 개요 페이지에서 일시적으로 제거되었습니다. 이렇게 하면 특정 메트릭 계산을 통해 평균 대화 시간 메트릭 및 시간에 따른 대화 그래프가 생성되어 부정확한 정보를 표시하는 일을 방지할 수 있습니다. IBM은 도구에서 기능을 제거한 것은 아쉽지만 사용자에게 정확한 정보를 전달하는 일이 중요하다고 생각합니다.
- **대화 상자 노드 이름**: 대화 상자 노드에 이름을 지정할 수 있습니다. 고유할 필요는 없습니다. 그리고 나중에 노드를 내부적으로 참조하는 방법에 영향을 주지 않고 노드 이름을 변경할 수 있습니다. 지정한 이름은 작업공간 JSON 파일에서 노드의 제목 속성으로 저장되고 시스템은 이름 속성에 저장된 고유 ID를 사용하여 노드를 참조합니다.

### 2017년 8월 23일
{: #23August2017}

- **한국어, 일본어 및 이탈리아어 업데이트**: 한국어, 일본어 및 이탈리아어에 대한 언어 지원이 개선되었습니다. {{site.data.keyword.conversationshort}} 서비스 러닝 모델은 이 개선사항의 일부로 업데이트될 수 있으며, 모델을 재훈련하면 변경사항이 적용됩니다. 자세한 정보는 [업데이트된 모델](release-notes.html#updated-models)을 참조하십시오.

### 2017년 8월 10일
{: #10August2017}

- **악센트 정규화**: 대화식 설정에서, 사용자는 {{site.data.keyword.conversationshort}} 서비스와 상호작용하는 동안 악센트를 사용하거나 사용하지 않을 수 있습니다. 이와 같이 악센트 버전의 단어 및 비악센트 버전의 단어가 인텐트 발견 및 엔티티 인식에 대해 동일하게 처리되도록 알고리즘이 업데이트되었습니다.

  하지만 스페인어와 같은 일부 언어의 경우 몇 가지 악센트가 엔티티의 의미를 바꿀 수 있습니다. 따라서 엔티티 발견에 대해 원래 엔티티에 내재적으로 악센트가 있을 수 있지만 서비스는 비악센트 버전의 동일한 엔티티를 일치시킬 수 있습니다. 단, 신뢰도 스코어가 약간 낮아집니다.

  예를 들어, 악센트가 있고 `barrer`(쓸다)라는 동사의 과거 시제에 해당하는 단어 `barrió`에 대해 서비스는 `barrio`(이웃)를 일치시킬 수도 있습니다. 단, 신뢰도가 약간 낮아집니다. 

  시스템은 정확한 일치의 엔티티에 가장 높은 신뢰도 스코어를 제공합니다. 예를 들어, `barrió`가 훈련 세트에 있는 경우 `barrio`는 발견되지 않고, `barrio`가 훈련 세트에 있는 경우에는 `barrió`가 발견되지 않습니다.

  적절한 문자와 악센트를 사용하여 시스템을 훈련시킬 수 있습니다. 예를 들어, `barrió`를 응답으로 예상하는 경우 훈련 세트에 `barrió`를 넣어야 합니다.

  악센트 표시가 아니지만, 동일한 단어에 적용됩니다. 예를 들어, 스페인 문자 `ñ` 대 문자 `n`(예: `uña` 대 `una`)를 사용하는 단어에 동일한 내용이 적용됩니다. 이 경우 문자 `ñ`은 단순히 악센트가 있는 `n`이 아닙니다.

  고객이 적절한 악센트를 사용하지 않거나 단어 철자를 잘못 쓸 것으로 생각되는 경우(예: `ñ` 대신 `n` 입력) 유사 일치를 사용할 수 있습니다. 또는 훈련 예제에 명시적으로 이를 포함할 수 있습니다.

  **참고:** 포르투갈어, 스페인어, 프랑스어 및 체코어에 대해 악센트 정규화가 사용됩니다.

- **작업공간 opt-out 플래그**: {{site.data.keyword.conversationshort}} REST API는 이제 작업공간에 opt-out 플래그를 지원합니다. 이 플래그는 IBM이 일반 서비스 개선을 위해 인텐트 및 엔티티와 같은 작업공간 훈련 데이터를 사용하지 않음을 표시합니다. 자세한 정보는 [API 참조(![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘"))](https://www.ibm.com/watson/developercloud/conversation/api/v1/#data-collection){: new_window}를 참조하십시오.

### 2017년 8월 7일
{: #7August2017}

- **`다음` 및 `마지막` 날짜 해석**: {{site.data.keyword.conversationshort}} 서비스는 `마지막` 및 `다음` 날짜가 참조된 가장 가까운 마지막 요일 또는 다음 요일을 나타내는 것으로 간주되며 이 날짜는 같은 주나 이전 주의 요일일 수 있습니다. 추가 정보는 [시스템 엔티티](system-entities.html#sys-datetime) 주제를 참조하십시오.

### 2017년 8월 3일
{: #3August2017}

- **추가 언어에 대한 유사 일치(베타)**: 엔티티에 대한 유사 일치는 이제 [지원되는 언어](lang-support.html) 주제에 언급된 대로 추가 언어에 대해서도 사용 가능합니다. 
- **부분 일치(베타- 영어만 해당)**: 유사 일치가 이제 자동으로 사용자 정의 엔티티에 있는 하위 문자열 기반 동의어를 제안하며 정확한 엔티티 일치와 비교해 낮은 신뢰도 스코어를 지정합니다. 세부사항은 [유사 일치](entities.html#fuzzy-matching)를 참조하십시오.

### 2017년 7월 28일
{: #28July2017}

- 도구에 대한 양방향 환경 설정을 설정하는 경우 이제 그래픽 사용자 인터페이스 방향을 지정할 수 있습니다.
- 도구의 색상 스킴이 다른 Watson 서비스 및 제품과 일치하도록 업데이트되었습니다.

### 2017년 7월 19일
{: #19July2017}

- {{site.data.keyword.conversationshort}} REST API가 이제 대화 상자 노드에 대한 액세스를 지원합니다. 자세한 정보는 [API 참조(![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘"))](https://www.ibm.com/watson/developercloud/conversation/api/v1/#dialog_nodes){: new_window}를 참조하십시오.

### 2017년 7월 14일
{: #14July2017}

- 대화 상자의 슬롯 기능이 개선되었습니다. 예를 들어, 단일 슬롯에만 적용되는 조건을 정의하는 데 사용할 수 있는 *slot_in_focus* 특성이 추가되었습니다. 세부사항은 [슬롯을 사용하여 정보 수집](/docs/services/conversation/dialog-slots.html)을 참조하십시오.

### 2017년 7월 12일
{: #12July2017}

- **체코어 지원**: 체코어 지원이 소개되었습니다. 추가 세부사항은 [지원되는 언어](lang-support.html)를 참조하십시오. 

### 2017년 7월 11일
{: #11July2017}

- **Slack 테스트**: 새 **Slack 테스트** 도구를 사용하여 테스트 목적으로 작업 공간을 Slack 봇 사용자로 신속하게 배치할 수 있습니다. 이 도구는 {{site.data.keyword.Bluemix_notm}} 미국 남부 지역에서만 사용 가능합니다. 자세한 정보는 [Slack에서 테스트](test-deploy.html)를 참조하십시오.
- **아랍어 업데이트**: 아랍어 지원은 인텐트에 대한 절대 스코어링 및 인텐트를 관련 없음으로 표시하는 기능을 포함하도록 개선되었습니다. 추가 세부사항은 [지원되는 언어](lang-support.html) 주제를 참조하십시오. {{site.data.keyword.conversationshort}} 서비스 러닝 모델은 이 개선사항의 일부로 업데이트될 수 있으며, 모델을 재훈련하면 변경사항이 적용됩니다. 자세한 정보는 [업데이트된 모델](release-notes.html#updated-models)을 참조하십시오.

### 2017년 6월 23일
{: #23June2017}

- **한국어 업데이트**: 한국어 지원이 개선되었습니다. 추가 세부사항은 [지원되는 언어](lang-support.html)를 참조하십시오. {{site.data.keyword.conversationshort}} 서비스 러닝 모델은 이 개선사항의 일부로 업데이트될 수 있으며, 모델을 재훈련하면 변경사항이 적용됩니다. 자세한 정보는 [업데이트된 모델](release-notes.html#updated-models)을 참조하십시오.

### 2017년 6월 22일
{: #22June2017}

- **슬롯 소개**: 이제 슬롯을 추가하여 단일 노드에서 사용자로부터 여러 정보를 쉽게 수집할 수 있습니다. 이전에는 사용자가 정보를 제공할 수 있는 가능한 방법의 조합을 모두 다루는 여러 대화 상자 노드를 작성해야 했습니다. 슬롯을 사용하면 사용자가 제공하는 모든 정보를 저장하고 사용자가 제공하지 않은 필수 세부사항을 입력하라는 프롬프트를 표시하는 단일 노드를 구성할 수 있습니다. 세부사항은 [슬롯을 사용하여 정보 수집](dialog-slots.html)을 참조하십시오.
- **단순화된 대화 상자 트리** - 사용성 향상을 위해 대화 상자 트리가 다시 디자인되었습니다. 트리 보기는 현재 위치를 쉽게 볼 수 있도록 간소화되어 있습니다. 그리고 노드 간 링크가 노드 간 관계를 쉽게 이해할 수 있는 방식으로 표시됩니다.

### 2017년 6월 21일
{: #21June2017}

- **아랍어 지원**: 아랍어 지원이 이제 사용 가능합니다. 세부사항은 [양방향 언어 구성](lang-support.html#configuring-bi-directional)을 참조하십시오.
- **언어 업데이트**: {{site.data.keyword.conversationshort}} 서비스 알고리즘이 전체 언어 지원을 개선하도록 업데이트되었습니다. 세부사항은 [지원되는 언어](lang-support.html) 주제를 참조하십시오.

### 2017년 6월 16일
{: #16June2017}

- **권장사항(베타 - 프리미엄 사용자 전용)**: 개선 패널에는 사용자가 챗봇과 나누는 대화를 분석하고 시스템의 현재 훈련 데이터 및 응답의 확실성을 고려하여 시스템을 개선하는 방법을 권장하는 **권장사항** 페이지도 포함됩니다. 

### 2017년 6월 14일
{: #14June2017}

- **추가 언어에 대한 유사 일치(베타)**: 엔티티에 대한 유사 일치는 [지원되는 언어](lang-support.html) 주제에서 언급된 대로 추가 언어에 대해 사용 가능합니다. 엔티티에 대한 유사 일치를 켜서 엔티티와 유사한 구문으로 사용자 입력 용어를 인식하는 서비스 기능을 개선할 수 있으며, 정확한 일치는 필요하지 않습니다. 기능은 오타 또는 약간의 구문상 차이가 있음에도 적절한 엔티티에 사용자 입력을 맵핑할 수 있습니다. 예를 들어, giraffe를 동물 엔티티의 동의어로 정의하고 사용자 입력에 giraffes 또는 girafe라는 용어가 포함되면, 유사 일치가 용어를 동물 엔티티에 올바르게 맵핑할 수 있습니다. 세부사항은 [유사 일치](entities.html#fuzzy-matching)를 참조하십시오.

### 2017년 6월 13일
{: #13June2017}

- **사용자 대화**: 개선 패널에는 이제 **사용자 대화** 페이지가 포함되며, 이 페이지에는 키워드, 인텐트, 엔티티 또는 일 수를 기준으로 필터링할 수 있는 챗봇과의 사용자 상호작용 목록이 제공됩니다. 개별 대화를 열어 인텐트를 정정하거나 엔티티 값 또는 동의어를 추가할 수 있습니다.
- **정규식 변경**: find, matches, extract, replaceFirst, replaceAll 및 split와 같은 SpEL 함수에서 지원되는 정규식이 변경되었습니다. 정규식 생성자 그룹(look-ahead, look-behind, possessive repetition 및 backreference 생성자 포함)은 더 이상 허용되지 않습니다. 이러한 변경은 원래 정규식 라이브러리에서 보안 노출을 방지하기 위해 필요합니다.

### 2017년 6월 12일
{: #12June2017}

- **라이트** 플랜(이전에는 무료 플랜이라고 함)으로 작성할 수 있는 최대 작업공간 수가 3에서 5로 변경되었습니다.
- 이제 대화 상자 노드에 이름을 지정할 수 있습니다. 이 이름은 고유하지 않아도 됩니다. 그리고 나중에 노드를 내부적으로 참조하는 방법에 영향을 주지 않고 노드 이름을 변경할 수 있습니다. 지정하는 이름을 별명으로 처리하고 시스템은 고유 내부 ID를 사용하여 노드를 참조합니다.
- 작업공간 세부사항을 편집하여 작성한 후에는 더 이상 작업공간 언어를 변경할 수 없습니다. 언어를 변경해야 하는 경우, JSON 파일로 작업공간을 내보내고 언어 특성을 업데이트한 다음 새 작업공간으로 JSON 파일을 가져올 수 있습니다.

### 2017년 6월 6일
{: #6June2017}

- **학습** : 새 *{{site.data.keyword.watson}} {{site.data.keyword.conversationshort}}에 대해 학습* 페이지가 사용 가능하며, 이 페이지에는 시작하기 정보 및 서비스 문서와 기타 유용한 자원에 대한 링크가 제공됩니다. 페이지를 열려면 페이지 헤더에서 ![정보를 가리키는 i](images/info.png) 아이콘을 클릭하십시오.
- **대량 내보내기 및 삭제** : 이제 많은 수의 인텐트나 엔티티를 동시에 CSV 파일에 내보낼 수 있으므로, 내보낸 다음 이러한 인텐트나 엔티티를 가져와 다른 {{site.data.keyword.conversationshort}} 애플리케이션에 재사용할 수 있습니다. 또한 대량 삭제를 위해 여러 엔티티나 인텐트를 동시에 선택할 수 있습니다.
- **한국어 업데이트** : 비공식 언어 지원을 처리하도록 한국어 토큰 생성기가 업데이트되었습니다. IBM은 계속해서 엔티티 인식 및 분류를 개선하고 있습니다.
- **이모티콘 지원** : 인텐트 예제에 또는 엔티티 값으로 추가된 이모티콘이 이제 올바르게 분류/추출됩니다. **참고**: 훈련 데이터에 포함된 이모티콘만 올바르고 일관되게 식별됩니다. 이모티콘 지원은 색상 톤이 다르거나 기타 변형된 유사 이모티콘을 올바르게 분류할 수 없습니다.
- **엔티티 어간 추출(베타 - 영어만 해당)** : 유사 일치 베타 기능은 엔티티를 인식하며 엔티티 값의 어간 양식을 기준으로 일치시킵니다. 예를 들어, 이 기능은 단어들이 공통 어간 양식을 공유할 때 'bananas'를 'banana'와 유사한 것으로, 'run'을 'running'과 유사한 것으로 올바르게 인식합니다. 자세한 정보는 [유사 일치](entities.html#fuzzy-matching)를 참조하십시오.
- **작업공간 가져오기 진행상태** : JSON 파일에서 작업공간을 가져오면 작업공간의 타일이 바로 표시되며 이 타일에 가져오기 진행상태에 대한 정보가 표시됩니다.
- **감소된 훈련 시간** : 이제 여러 모델이 동시에 훈련하여 큰 작업공간에 대한 훈련 시간이 크게 감소됩니다.

### 2017년 5월 26일
{: #26May2017}

- 현재 API 버전은 이제 `2017-05-26`입니다. 이 버전은 다음 변경사항을 도입합니다.
    - ErrorResponse 오브젝트의 스키마가 변경되었습니다. 이 변경사항은 모든 엔드포인트 및 메소드에 적용됩니다. 자세한 정보는 [API 참조(![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘"))](https://www.ibm.com/watson/developercloud/conversation/api/v1/){: new_window}를 참조하십시오.
    - 내보낸 작업공간 JSON에 대화 상자 노드를 표시하는 데 사용되는 내부 스키마가 변경되었습니다. `2017-05-26` API를 사용하여 이전 버전을 통해 내보낸 작업공간을 가져오는 경우, 일부 대화 상자 노드를 올바르게 가져올 수 없습니다. 최상의 결과를 위해서는 내보내기에 사용된 동일한 버전을 사용하여 항상 작업공간을 가져오십시오.

### 2017년 5월 25일
{: #25May2017}

- 이제 "연습" 분할창에서 컨텍스트 변수를 관리할 수 있습니다. **컨텍스트 관리** 링크를 클릭하여 대화 상자를 테스트할 때 컨텍스트 변수의 값을 설정하고 검사할 수 있는 새 분할창을 여십시오. 자세한 정보는 [대화 상자 테스트](dialog-test.html)를 참조하십시오.

### 2017년 5월 16일
{: #16May2017}

- **자동차 대시보드** 샘플 작업공간은 이제 도구를 열 때 사용 가능합니다. 샘플을 고유 작업공간의 시작점으로 사용하려면 작업공간을 편집하십시오. 샘플을 여러 작업공간에 사용하려면 복제하십시오. 샘플 작업공간에는 사용되는 경우를 제외하고 등록 작업공간의 총 수가 포함되지 않습니다.
- 이제 도구를 쉽게 탐색할 수 있습니다. 탐색 메뉴 옵션은 기본 페이지의 맨 위가 아닌 옆에서 사용 가능합니다. 페이지의 맨 위에 현재 위치를 표시하는 사이트 이동 경로 링크가 표시됩니다. 이제 작업공간 페이지에서 서비스 인스턴스 사이를 전환할 수 있습니다. 빠르게 이동하려면 탐색 메뉴에서 **작업공간으로 돌아가기**를 클릭하십시오. 여러 서비스 인스턴스가 있는 경우 현재 인스턴스의 이름이 표시됩니다. 옆에 있는 **변경** 링크를 클릭하여 다른 인스턴스를 선택할 수 있습니다.
- 대화 상자를 작성하면 이제 두 개의 노드가 이 대화 상자에 추가됩니다. 1) 사용자에게 표시할 인사가 포함된 대화 상자 트리의 맨 위에 있는 **Welcome** 노드. 2) 대화 상자의 다른 노드가 인식하지 못하는 사용자 질문을 발견하고 이에 응답하는 트리의 맨 아래에 있는 **Anything else** 노드. 세부사항은 [대화 상자 작성](dialog-create.html)을 참조하십시오.
- "연습" 분할창에서 대화 상자를 테스트하는 경우 이제 위로 키를 눌러 이전 입력을 모두 거쳐 최근 테스트 표현을 찾고 다시 제출할 수 있습니다.
- 5개의 시스템 엔티티(`@sys-date`, `@sys-time`, `@sys-currency`, `@sys-number`, `@sys-percentage`)에 대한 한국어 시험 지원이 이제 사용 가능합니다. 일부 숫자 엔티티에 대한 알려진 문제 및 비공식적 언어 입력에 대한 제한된 지원이 있습니다.
- 개요 페이지는 개선 탭에서 사용 가능합니다. 페이지는 봇과의 상호작용 요약을 제공합니다. 사용자 대화에서 가장 자주 인식된 인텐트 및 엔티티 뿐만 아니라 지정된 시간 동안 트래픽의 양을 볼 수 있습니다. 추가 정보는 [개요 사용 페이지](logs_oview.html)를 참조하십시오.

### 2017년 4월 27일
{: #27April2017}

- 다음 시스템 엔티티는 이제 베타 기능으로 사용 가능합니다(영어만 해당).
    - sys-location: 사용자 표현에서 소도시, 도시 및 국가와 같은 위치에 대한 참조를 인식합니다.
    - sys-person: 사용자 표현에서 사용자의 이름과 성에 대한 참조를 인식합니다.

    자세한 정보는 [시스템 엔티티 참조](system-entities.html)를 참조하십시오.
- 엔티티에 대한 유사 일치는 영어로 사용 가능한 베타 기능입니다. 엔티티에 대한 유사 일치를 켜서 엔티티와 유사한 구문으로 사용자 입력 용어를 인식하는 서비스 기능을 개선할 수 있으며, 정확한 일치는 필요하지 않습니다. 기능은 오타 또는 약간의 구문상 차이가 있음에도 적절한 엔티티에 사용자 입력을 맵핑할 수 있습니다. 예를 들어, **giraffe**를 동물 엔티티의 동의어로 정의하고 사용자 입력에 *giraffes* 또는 *girafe*라는 용어가 포함되면, 유사 일치가 용어를 동물 엔티티에 올바르게 맵핑할 수 있습니다. 세부사항을 보려면 [엔티티 정의](entities.html#fuzzy-matching)를 참조하고 `유사 일치`를 검색하십시오. 

### 2017년 4월 18일
{: #18April2017}

- {{site.data.keyword.conversationshort}} REST API는 이제 다음 자원에 대한 액세스를 지원합니다.
    - 엔티티
    - 엔티티 값
    - 엔티티 값 동의어
    - 로그

    자세한 정보는 [API 참조(![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘"))](https://www.ibm.com/watson/developercloud/conversation/api/v1/){: new_window}를 참조하십시오.
- /messages `POST` 메소드의 동작이 메시지 입력의 일부로 지정된 엔티티와 인텐트의 처리를 변경했습니다.
    - 입력에서 인텐트를 지정하는 경우 서비스가 지정된 인텐트를 사용하지만 자연어 처리를 사용하여 사용자 입력에서 엔티티를 발견합니다.
    - 입력에서 엔티티를 지정하는 경우 서비스가 지정된 엔티티를 사용하지만 자연어 처리를 사용하여 사용자 입력에서 인텐트를 발견합니다.

        인텐트와 엔티티 둘 다 지정하는 메시지 또는 둘 다 지정하지 않은 메시지에 대한 동작은 변경되지 않았습니다.
- 관련 없음으로 사용자 입력을 표시하는 옵션은 이제 지원되는 모든 언어에서 사용 가능합니다. 이는 베타 기능입니다.
- 새 신임 정보 탭에서는 다른 배치 옵션 뿐만 아니라 작업공간에 애플리케이션을 연결하는 데 필요한 모든 정보(예: 서비스 신임 정보 및 작업공간 ID)를 찾을 수 있는 단일 위치를 제공합니다. 작업공간의 신임 정보 탭에 액세스하려면 ![메뉴](images/Menu_16.png) 아이콘을 클릭하고 **신임 정보**를 선택하십시오.

### 2017년 3월 9일
{: #9March2017}

{{site.data.keyword.conversationshort}} REST API는 이제 다음 자원에 대한 액세스를 지원합니다.

- workspaces
- intents
- examples
- counterexamples

자세한 정보는 [API 참조(![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘"))](https://www.ibm.com/watson/developercloud/conversation/api/v1/){: new_window}를 참조하십시오.

### 2017년 3월 7일
{: #7March2017}

- `.` 또는 `..`를 인텐트 이름으로 사용하면 문제점이 발생하며 이러한 사용은 더 이상 지원되지 않습니다.

    이름을 변경하고 인텐트를 파일에 내보내고 파일에서 인텐트의 이름을 바꾸고 작업공간에 업데이트된 파일을 가져오려면 이 이름의 인텐트를 삭제하거나 이름을 바꾸면 안됩니다.

    유료 고객은 데이터베이스 변경 지원을 문의할 수 있습니다.

### 2017년 3월 1일
{: #1March2017}

- 시스템 엔티티는 이제 독일어로 사용 가능합니다.

### 2017년 2월 22일
{: #22February2017}

- 메시지는 이제 2,048자로 제한됩니다.

### 2017년 2월 3일
{: #3February2017}

- 인텐트의 스코어 채점 방법을 변경하고 애플리케이션에 입력을 관련 없음으로 표시하는 기능을 추가했습니다. 세부사항을 보려면 [인텐트 정의](intents.html)를 참조하고 `관련 없음으로 표시`를 검색하십시오. 

- 이 릴리스에서는 작업공간에 관한 주요 변경사항이 소개되었습니다. 변경 사항을 적용하려면 작업공간을 수동으로 업그레이드해야 합니다. 다음 단계를 완료하십시오. 

  1.  [작업공간 복제](configure-workspace.html#exporting-and-copying-workspaces).
  1.  업그레이드 아이콘을 클릭하여 중복 작업공간을 업그레이드하십시오(![업그레이드 아이콘](images/upgrade.png)).
  1.  업그레이드된 작업공간을 테스트하십시오. 
  1.  테스트가 완료되고 작업이 예상대로 진행되는 경우, **2017-02-03** 이상을 사용하는 메시지 API 호출을 변경하여 업그레이드를 애플리케이션에 적용하십시오. 

- **점프** 조치의 처리는 특정 조건에서 발생할 수 있는 루프를 방지하도록 변경되었습니다. 이전에 노드 조건으로 점프했고 이 노드와 해당 피어 노드에 true로 평가된 조건이 없는 경우, 시스템이 루트 레벨 노드로 점프하고 조건이 입력과 일치한 노드를 검색합니다. 어떤 상황에서는 이 처리를 통해 루프가 작성되어 대화 상자가 진행되지 않았습니다.

  새 프로세스에서 대상 노드와 해당 피어가 true로 평가되지 않으면 대화 상자 턴이 종료됩니다. 이전 모델을 재구현하려는 경우, 최종 피어 노드에 `true` 조건을 추가하십시오. 응답에서 대화 상자 트리의 루트 레벨에서 첫 번째 노드의 조건을 대상으로 지정하는 **점프** 조치를 사용하십시오.

### 2017년 1월 11일
{: #11January2017}

- 이 릴리스의 경우 대화 상자에서 노드 제목을 사용자 정의할 수 있습니다.

### 2016년 12월 22일
{: #22December2016}

- 이 릴리스의 대화 상자 노드에 `노드 제목`을 위한 새 섹션이 표시됩니다. `노드 제목`을 사용자 정의하는 기능은 사용할 수 없습니다. 접으면 `노드 제목`에 대화 상자 노드의 `노드 조건`이 표시됩니다. `노드 조건`이 없는 경우 "Untitled Node"가 제목으로 표시됩니다.

### 2016년 12월 19일
{: #19December2016}

여러 변경을 통해 대화 상자 빌더를 보다 쉽고 직관적으로 사용할 수 있습니다.

- 큰 편집 보기를 사용하면 작업 시 노드의 모든 세부사항을 쉽게 볼 수 있습니다.
- 노드에 여러 응답이 포함될 수 있으며 각각은 개별 조건으로 트리거됩니다. 자세한 정보는 [다중 응답](dialog-overview.html#responses)을 참조하십시오.

### 2016년 12월 5일
{: #5December2016}

- 새 언어는 모두 시험 모드에서 지원됩니다(독일어, 중국어 번체자, 중국어 간체자 및 네덜란드어).
- 두 개의 새 시스템 엔티티를 사용할 수 있습니다(@sys-date와 @sys-time). 세부사항은 [시스템 엔티티](system-entities.html)를 참조하십시오.

### 2016년 10월 21일
{: #21October2016}

- {{site.data.keyword.conversationshort}} 서비스는 이제 시스템 엔티티를 제공하며, 이 엔티티는 모든 유스 케이스에서 사용할 수 있는 공통 엔티티입니다. 세부사항을 보려면 [엔티티 정의](entities.html)를 참조하고 `시스템 엔티티 사용`을 검색하십시오. 
- 이제 개선 페이지에서 사용자와의 대화 히스토리를 볼 수 있습니다. 이를 사용하여 봇의 동작을 이해할 수 있습니다. 세부사항은 [이해 향상](logs.html)을 참조하십시오.
- 이제 쉼표로 구분된 값(CSV) 파일에서 엔티티를 가져올 수 있으며, 이는 많은 수의 엔티티가 있을 때 도움이 됩니다. 세부사항을 보려면 [엔티티 정의](entities.html)를 참조하고 `엔티티 가져오기`를 검색하십시오. 

### 2016년 9월 20일
{: #20September2016}

**새 버전**: 2016-09-20

새 버전의 변경사항을 이용하려면 `version` 매개변수 값을 새 날짜로 변경하십시오. 이 버전으로 업데이트할 준비가 되지 않은 경우 버전 날짜를 변경하지 마십시오.

- 버전 **2016-09-20**: `dialog_stack`이 문자열 배열에서 JSON 오브젝트의 배열로 변경되었습니다.

### 2016년 8월 29일
{: #29August2016}

- 하나의 분기에서 다른 분기로 동위 또는 피어인 대화 상자 노드를 이동할 수 있습니다. 세부사항은 [대화 상자 노드 이동](dialog-build.html#move-node)을 참조하십시오. 
- JSON 편집기 창을 펼칠 수 있습니다.
- 봇의 대화에 대한 대화 로그를 확인하여 해당 동작을 이해할 수 있습니다. 인텐트, 엔티티, 날짜 및 시간을 기준으로 필터링할 수 있습니다. 세부사항은 [이해 향상](logs.html)을 참조하십시오.

### 2016년 7월 11일
{: #21July2016}

- 이 GA(General Availability) 릴리스를 사용하면 엔티티 및 대화 상자에 대한 작업을 수행하여 완전하게 작동하는 봇을 작성할 수 있습니다.

### 2016년 5월 18일
{: #18May2016}

- {{site.data.keyword.conversationshort}}의 시험 릴리스는 사용자 인터페이스를 도입하여 작업공간, 인텐트 및 예제에 대한 작업을 수행할 수 있게 합니다.
