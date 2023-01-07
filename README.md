# Android_Interview
안드로이드 면접 대비

안드로이드 개발직 기술면접대비를 위한 나만의 공부 기록소

# Android
<details>
<summary>안드로이드 4대 컴포넌트</summary>
<br>
안드로이드 4대 컴포넌트란??<br>
<br>
컴포넌트란 구성요소를 의미한다.<br>
다시 말해서 안드로이드 4대 컴포넌트란 안드로이드 앱을 구성하는데 필요한 4개의 요소를 의미한다. 안드로이드 4대 컴포넌트에는 액티비티(Activity), 서비스(Service), 방송 수신자(Broadcast Receiver), 콘텐트 제공자(Content Provider)가 있다.<br>

 - 각 컴포넌트는 독립적으로 존재한다.
 - 각 컴포넌트들은 고유의 기능을 수행한다.
 - 각 컴포넌트들은 인텐트를 통해 서로 상호작용한다.

## 1. 액티비티(Activity)
**사용자와 상호작용**을 담당하는 인터페이스입니다.<br>
액티비티는 **생명주기(Life Cycle)** 관련 메서드들을 재정의하여 원하는 기능들을 구현할 수 있습니다.<br>

 - 액티비티는 사용자가 Application과 상호작용하며 실제로 사용자에게 보이는 화면을 의미합니다.
 - 액티비티는 인텐트(Intent)를 통해 다른 Application의 액티비티를 호출할 수 있습니다.
 - 2개이상의 액티비티를 동시에 Display 할 수 없습니다.
 - 1개 이상의 View(텍스트,버튼,이미지) 또는 ViewGroup(레이아웃)을 포합합니다.
 - 반드시 Application에는 하나 이상의 액티비티가 있어야 합니다.
 - 액티비티 내에 프래그먼트(Fragment)를 추가하여 화면을 분할시킬 수 있습니다.

## 2. 서비스(Service)
서비스는 액티비티와 반대로 사용자와 직접적으로 상호작용하는 요소는 아니다.<br>
다만, **백그라운드(BackGround)에서 어떠한 작업**을 처리하기 위해서 주로 사용한다.<br>

 - Application이 종료되어도 BackGround에서 동작하는 컴포넌트이다.
 - 음악 앱을 예시로 들 경우 앱을 종료 해도, 음악은 계속 재생되며, 타이머의 앱의 경우도 타이머 앱을 종료할 경우 타이머는 계속 흘러간다. 즉, 애플리케이션이 종료되어도 이미 시작된 서비스는 백그라운드에서 계속 동작한다.
 - 네트워크(Network)와 연동이 가능하다.
 - 액티비티와 서비스는 Ui스레드라고 불리는 동일한 애플리케이션 스레드로 실행됩니다.
 

## 3. 방송 수신자(Broadcast Receiver)
방송수신자는 안드로이드 OS로부터 발생하는 **각종이벤트와 정보를 받아 핸들링**하는 컴포넌트이다.<br>
안드로이드 디바이스의 특수한 상황에 대응하기 위해서 사용된다. 여기서 말하는 특수한 상황이란,<br>
시스템 부팅시 앱 초기화, 네트워크 끊김같은 특수한 상황에대한 처리 그리고 배터리 부족 알림, 문자수신같은 정보를 받아서 하는 처리이다.

 - 거의 대부분 Ui를 가지지 않는다. 수신기를 통해 디바이스 상황을 감시하다가 이벤트가 발생하면 해당 이벤트에 맞게 정의한 작업들을 수행하는 역할을 한다.
 - 특정한 상황을 제외하고는 브로드캐스트는 시스템에서 시작된다.

## 4. 콘텐트 제공자(Content Provider)
콘텐트 제공자는 **데이터를 관리하고 다른 Application의 데이터를 제공하는데 사용**되는 컴포넌트이다.<br>
특정한 Application이 사용하고 있는 DB를 공유하기 위해 사용하며 애플리케이션 간의 데이터 공유를 위해 표준화된 인터페이스를 제공합니다.
 - SQLite DB/ Web/ 파일 입출력 등을 통해서 데이터를 관리합니다.
 - 외부 어플리케이션이 현재 실행중인 Application 내에 있는 데이터베이스에 함부로 접근하지 못하게 할 수 있으면서 나 자신이 공개하고 공유하고 싶은 데이터만 공유할 수 있도록 도와줍니다.
 - 작은 데이터들은 인텐트(intent)로 Application끼리 데이터를 서로 공유가 가능하지만 콘테트 프로바이더는 음악 또는 사진 파일 등과 같이 용량이 큰 데이터들을 공유하는데 적합합니다.
 - 프로바이더는 데이터의 Read, Write에 대한 퍼미션이 있어야 Application에 접근이 가능합니다.
 - 데이터베이스에서 흔히 사용되는 CRUD 원칙을 준수한다.

</details>

<details>

<summary> MVC,MVP,MVVM,MVI </summary>

[MVC](https://superohinsung.tistory.com/64)

[MVP](https://superohinsung.tistory.com/65)

[MVVM](https://superohinsung.tistory.com/66)

[MVI]()

</details>

# Kotlin
<details>

<summary>data class, enum class, sealed class </summary>

[data class란](https://superohinsung.tistory.com/58)

[enum class란](https://superohinsung.tistory.com/59)

[sealed class란](https://superohinsung.tistory.com/61)

</details>

<details>

<summary>스코프함수 run, with, apply, let</summary>

[스코프 함수 정리](https://superohinsung.tistory.com/63)

</details>


# OS
<details>
<summary>프로세스와 스레드의 차이</summary>

## 프로세스
프로그램을 실행하는 순간 해당 파일은 컴퓨터 메모리에 올라가게 되고, 이 상태를 동적(動的)인 상태라고 하며 이 상태의 프로그램을 프로세스라고 한다.

## 스레드
과거에는 프로그램을 실행시킬 때 실행시작부터 실행 끝까지 하나의 프로세스만으로 운영을 하였다. 하지만 시간이 흐를수록 더욱 복잡해지는 프로그램으로 인해 하나의 프로세스만으론 운영이 벅차게 되었다. 그래서 한 프로그램을 처리하기위해 여러개의 프로세스를 만들게 되었다. 하지만 프로세스마다 자신에게 할당된 메모리 내의 정보에만 접근할 수 있도록 제약을 두고있고, 이를 이를 벗어나는 정보에 접근하려면 오류가 발생한다.
이에 탄생한 개념이 스레드이다.
스레드는 프로세스의 코드에 정의된 절차에 따라 실행되는 특정한 수행 경로다.
스레드는 위에서 언급한 프로세스 특성의 한계를 해결하기위해 만들어진 개념이기에 다른 스레드와 메모리를 공유하며 작동한다.

## 차이점
프로세스와 스레드는 개념의 범위부터 다르다. 스레드는 프로세스 안에 포함되어 있기 때문이다. <br><br>

운영체제가 프로세스에게 Code/Data/Stack/Heap 메모리 영역을 할당해 주고 최소 작업 단위로 삼는 반면, 스레드는 프로세스 내에서 Stack 메모리 영역을 제외한 다른 메모리 영역을 같은 프로세스 내 다른 스레드와 공유한다.<br><br>

프로세스는 다른 프로세스와 정보를 공유하려면 IPC를 사용하는 등의 번거로운 과정을 거쳐야 하지만, 스레드는 기본 구조 자체가 메모리를 공유하는 구조이기 때문에 다른 스레드와 정보 공유가 쉽다. 때문에 멀티태스킹보다 멀티스레드가 자원을 아낄 수 있게 된다. 다만 스레드의 스케줄링은 운영체제가 처리하지 않기 때문에 프로그래머가 직접 동기화 문제에 대응할 수 있어야 한다.

</details>

<details>

<summary>Dead Lock</summary>

[교착상태](https://superohinsung.tistory.com/73)

</details>

# NETWORK

<details>

<summary>REST API 란?</summary>

REST란? <br>
Representational State Transfer의 약자로 자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미한다. 즉, 자원의 표현에 의한 상태 전달이다.<br>
HTTP URI 를 통해 자원(Resource)을 명시하고, HTTP Method(POST, GET, PUT DELETE) 를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미하고 기본적으로 웹의 기존 기술과 HTTP 프로토콜을 그대로 활용하기 때문에 웹의 장점을 최대한 활용할 수 있는 아키텍쳐 스타일이며, 네트워크 상에서 Client 와 Server 사이의 통신 방식 중 하나이다.

CRUD Operation
 - Create : 생성(POST)
 - Read : 조회(GET)
 - Udate : 수정(PUT)
 - Delete : 삭제(DELETE)
 - HEAD : header 정보 조회(HEAD)

<br>
API란<br>
데이터와 기능의 집합을 제공하여 컴퓨터 프로그램간 상호작용을 촉진하며, 서로 정보를 교환가능 하도록 하는 것이다.
<br>
즉 REST API란, REST를 기반으로 서비스 API를 구현한 것이다.<br><br>
REST API에는 설계기본규칙이 존재한다.<br><br>
 1. 슬랙시 구분자는 계층관계를 나타내는데 사용한다.<br>
 2. URI 마지막 문자로 슬래시를 포함하지 않는다.<br>
 3. 하이픈은 URI의 가독성을 높이는데 사용한다.<br>
 4. 밑줄은 사용하지 않는다.<br>
 5. URI경로에는 소문자가 적합하지 않다.<br>
 6. 파일 확장자는 URI에 포함하지 않는다.<br>

</details>