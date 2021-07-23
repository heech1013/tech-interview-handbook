# OS

## Table of Contents

- 운영체제
  - 운영체제란?
  - 운영체제의 역할은?
- 프로세스와 스레드
  - 프로세스란?
  - 프로그램이란?
  - 프로세스와 자원의 차이점은?
  - 프로세스와 작업(job)의 차이점은?
  - 메모리는 어떻게 구성되어 있을까?
  - 스레드란?
  - 스레드가 필요한 이유는? (스레드의 장점은?)
  - 프로세스보다 스레드 간 context switching이 더 적은 비용이 드는 이유는?
  - 프로세스와 스레드의 차이점은?
  - 스레드를 지원하는 주체에 따라 나눈다면 어떻게 나뉠까?
  - 사용자 레벨 스레드와 커널 레벨 스레드란?
  - 사용자 레벨 스레드의 장단점?
  - 커널 레벨 스레드의 장단점?
  - 멀티 프로세싱(multi-processing)이란?
  - 멀티 프로그래밍(multi-programming)이란?
  - 멀티 태스킹(multi-tasking)이란?
  - 멀티 프로그래밍과 멀티 태스킹의 차이는?
  - 멀티 스레딩(multi-threading)이란?
  - 멀티 프로그래밍와 멀티 스레드의 차이점?
- 스케줄링
  - Context Switching이란?
  - Context란?
  - Context에는 예를 들어 어떤 정보들이 있을까?
  - PCB(Process Control Block)란?
  - PCB가 생성되는 시점은?
  - PCB가 위치한 곳은?
  - Context Switching이 필요한 이유는? `보충`
  - 프로세스의 상태가 전이되는 과정은? (프로세스 상태 전이도의 흐름은?)
  - 프로세스가 종료되면(terminated) PCB도 함께 제거될까?
  - 스케줄링이 필요한 이유는?
  - 시스템의 성능을 어떤 기준으로 측정할까?
  - (참고) 용어
  - 스케줄링의 주기에 따라 3가지로 나눈다면 어떻게 나뉠까?
  - 장기 스케줄링이란? 예시는?
  - 중기 스케줄링이란? 예시는?
  - 단기 스케줄링이란? 예시는?
  - 선점형 스케줄링과 비선점형 스케줄링의 차이?
  - 선점형 스케줄링의 장단점?
  - 비선점형 스케줄링의 장단점?
  - 자원 관리에 있어서 time sharing과 space sharing의 차이는?
  - FCFS(First Come First Service)란?
  - FCFS의 장단점?
  - FCFS에 적합한 시스템은?
  - 배치 시스템(배치 처리, batch system, batch process)란?
  - Round Robin이란?
  - Round Robin의 장단점?
  - time quantum이 짧을 때와 길 때 성능에 어떤 영향을 미칠까?
  - Round Robin은 어떤 서비스에 적합할까?
  - SPN(Shortest Process Next)이란?
  - SPN의 장단점
  - 시스템 내 프로세스 수를 적게 유지했을 때의 좋은 점은?
  - SRTN(Shortest Remaining Time Next)란?
  - SRTN의 장단점?
  - HRRN(High Response Ratio Next)이란?
  - HRRN의 장단점?
  - MLQ(Multi Level Queue)란?
  - MLQ의 장단점?
  - MFQ(Multi level Feedback Queue)란?
  - feedback에는 어떤 것들이 있을까?
  - MFQ의 장단점?
- 동기화
  - 동기화란?
  - 동기화가 필요한 이유는?
  - Critical section(임계 구역)이란?
  - Race condition(경쟁 상태)이란?
  - Mutual exclusion(상호 배제)이란?
  - Mutual exclusion에 사용되는 기본 연산(primitive)의 조건은?
  - Mutual exclusion을 SW로 구현한 알고리즘에는 어떤 것들이 있나?
  - Dekker's algorithm을 설명해본다면?
  - Dekker's algorithm을 더 자세히 설명해본다면? (간단하게 코드로 표현해본다면?)
  - SW로 구현한 상호 배제 알고리즘의 단점은?
  - HW로 구현한 상호 배제 알고리즘에는 어떤 것들이 있나?
  - TAS(TestAndSet)란?
  - TAS를 이용해 ME가 보장되는 과정을 조금 더 자세히 설명? (코드로 설명?)
  - OS로 구현한 상호 배제 알고리즘에는 어떤 것들이 있나?
  - 스핀락이란?
  - 스핀락의 장단점은?
  - 스핀락은 어떤 특성의 프로세스에서 사용하기 적절할까?
  - 뮤텍스란?
  - 뮤텍스는 어떤 특성의 프로세스에서 사용하기 적절할까?
  - 스핀락과 뮤텍스의 차이점?
  - 세마포어란?
  - 세마포어에 사용되는 연산의 종류와 그 로직은?
  - 스핀락(혹은 뮤텍스)와 세마포어의 차이는?
- 데드락
  - 데드락(dead lock, 교착 상태)이란?
  - 데드락이 발생하기 위한 조건은?
  - 데드락을 처리하는 방법은?
  - 데드락을 예방하는 방법은?
  - 데드락을 예방하는 방법의 단점은?
  - 데드락을 회피하는 방법은?
  - 데드락 회피 알고리즘 중 하나를 설명?
  - 은행원 알고리즘의 안정 상태, 불안정 상태란?
  - 은행원 알고리즘이 수행되기 위해 필요한(유지해야 하는) 정보는?
  - 은행원 알고리즘의 단점은?
  - 데드락을 회복하는 방법은?
  - 언제 데드락 발생을 무시할까?
- 가상 메모리
  - 가상 메모리란? (메모리 가상화란?)
  - 메모리의 가상화가 필요한 이유는?
- 주소 변환(address translation)
  - 주소 변환이란?
  - 주소 변환이 필요한 이유는?
  - 주소 변환을 구현한 기술에는 어떤 것이 있는지?
  - base and bound란?
  - 베이스 레지스터란?
  - 바운드 레지스터(bound register)란?
  - 바운드 레지스터가 타 프로세스 메모리 침범을 막는 방법은?
  - base and bound에서 운영체제의 역할은?
  - base and bound에서 프로세스의 주소 공간을 옮기려면 어떻게 해야 하나?
  - base and bound의 장단점은?
  - base and bound의 내부 단편화 문제란?
- 세그멘테이션(segmentation)
  - 세그멘테이션이란?
  - 세그먼트란?
  - 세그멘테이션에서 가상 주소로부터 물리 주소를 얻는 과정은?
  - 세그먼트의 바운드 레지스터의 역할은?
  - 하드웨어가 가상 주소에서 세그먼트의 종류와 오프셋을 파악하는 방법은?
  - 가상 주소 변환에 있어서 스택과 나머지 종류의 세그먼트 간 차이는?
  - 하드웨어는 세그먼트가 어느 방향으로 확장해야 하는지 어떻게 알 수 있을까?
  - 세그멘테이션이 메모리 공유를 지원하는 방법은?
  - 세그멘테이션을 위한 운영체제의 역할은?
  - 세그먼트 테이블?
  - 세그멘테이션의 장단점은?
  - 외부 단편화란?
  - 외부 단편화에 대한 대응 방안은?
  - 압축이란? 진행되는 과정은?
  - 압축의 단점은?
  - 빈 공간 리스트를 관리하는 알고리즘에는 어떤 것들이 있나?
- 페이징(Paging)
  - 페이징이란?
  - 페이징이 등장하게 된 배경은?
  - 페이징의 장단점은?
  - 페이징에서 물리 메모리의 구성은 어떻게 다른가?
  - 페이지 테이블(page table)이란?
  - 페이지 테이블 엔트리(PTE, Page Table Entry)란?
  - PTE의 구성 요소에는 어떤 것들이 있는지?
  - 페이징의 가상 주소에서 물리 주소를 얻어내는 과정은?
  - 현재 실행 중인 프로세스의 페이지 테이블 위치를 어떻게 알 수 있을까?
- TLB
  - TLB(Translation-Lookaside Buffer, 변환-색인 버퍼)란?
  - TLB가 필요한 이유는?
  - TLB가 도입된 상태에서 가상 메모리 참조 시 일어나는 과정은?
  - (TLB의) 지역성 2종류와 적용된 예시에 대해 설명?
  - TLB 미스를 처리하는 방법에는 어떤 것들이 있을까?
  - TLB 미스 트랩 핸들러가 실행될 때 TLB 미스가 나지 않도록 대응 방안?
  - TLB Cache가 설계된 방식은? (cache의 associativity와 관련하여)
  - TLB 각 항목의 구성은?
  - 페이지 테이블의 valid bit와 TLB의 valid bit 간 차이점은?
  - TLB에는 여러 VPN이 공존할 수 있다. 하지만 그럴 경우 여러 프로세스 간 VPN을 구분할 수 없다. 이에 대한 방안은?
  - 캐시 교체 정책에는 어떤 것들이 있나?
  - LRU란?
  - Random 정책이란? 장단점은?
  - TLB coverage를 벗어난다는 것의 의미는?
- 스와핑(Swapping)
  - 스와핑이란?
  - swap in과 swap out에 대해 설명?
  - page fault란?
  - 스와핑이 지원되는 상황에서 메모리가 참조되는 과정을 설명?
  - 운영체제가 Page fault를 처리하는 과정은?
  - 운영체제가 페이지 교체(스왑) 알고리즘을 작동시키는 시기는?
  - 페이지 교체(스왑) 알고리즘이 작동될 때(즉, 여유 공간이 최솟값보다 적어질 때) 일어나는 일은?
- Blocking/Non-Blocking & Synchronous/Asynchronous
  - Blocking과 Non-Blocking의 차이점?
  - Synchronous와 Asynchronous의 차이점?
  - Blocking + Sync ?
  - Non-Blocking + Async ?
  - Non-Blocking + Sync ?
  - Blocking + Async ?
- Reference

## 운영체제

### 운영체제란?

하드웨어와 응용 프로그램 사이에서 인터페이스로서 시스템의 동작을 제어하는 시스템 소프트웨어.

### 운영체제의 역할은?

- 자원의 관리와 보호
- 하드웨어 인터페이스, 사용자 인터페이스 제공

## 프로세스와 스레드

### 프로세스란?

- 메모리에 탑재되어(커널에 등록되어) 실행되고 있는 프로그램.
- 운영체제로부터 자원을 할당 받는 작업의 단위.

### 프로그램이란?

- 실행할 수 있는 파일
- 디스크에 저장되어 있지만, 메모리에는 올라가 있지 않은 정적인 상태의 파일.

### 프로세스와 자원의 차이점은?

- 자원은 프로세스에게 할당되고, 프로세스에 의해 반납되는 수동적 객체이다.
- 프로세스는 자원을 요청하고, 할당하고, 반납할 수 있는 능동적 객체이다.

### 프로세스와 작업(job)의 차이점은?

- job은 프로그램과 그 프로그램이 사용할 데이터를 의미한다.  
  (커널에 등록되기 전 디스크에 상주하는 상태)

* 프로세스는 실행을 위해 커널에 등록된 상태의 job이다. (메모리에 상주)

### 메모리는 어떻게 구성되어 있을까?

![OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled.png](OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled.png)

낮은 주소(위)부터 차례로 -

- code(text)
  - 프로그램의 코드 자체. (Hex 파일이나 Bin 파일로 구성되어 있다.)
- data
  - 전역 변수, 정적 변수, 배열, 구조체 등이 저장.
- heap
  - 메모리를 동적으로 할당할 때 사용하는 영역.
  - 낮은 주소에서 높은 주소로 확장해나감.
- (unused memory)
  - heap과 stack 사이에 존재
- stack

  - 프로그램이 임시적으로 사용하는 영역.
  - 지역 변수 등이 저장.
  - 높은 주소에서 낮은 주소로 확장해나감.

> - UNIX 시스템은 실행 중인 프로세스에게 4GB의 가상 메모리 공간을 할당한다.
> - 상위 1GB는 커널이, 하위 3GB는 사용자 프로그램이 차지한다.

> - code와 data 영역은 컴파일 단계에서 크기가 결정되는 정적 메모리 영역, heap과 stack은 런타임 단계에서 크기가 결정되는 동적 메모리 영역이다.
> - heap이 stack을 침범하면 heap overflow, stack이 heap을 침범하면 stack overflow라고 한다.

### 스레드란?

- 프로세스가 할당 받은 자원을 사용하는 실행의 단위
- CPU의 최소 작업 단위

### 스레드가 필요한 이유는? (스레드의 장점은?)

- 같은 프로세스 내 다른 스레드 간 context switching에 비용이 적게 든다.
- 스레드를 새로 생성하는 데 더 적은 비용이 든다.
- 다른 스레드가 지연되더라도 다른 스레드에 의해 작업이 계속될 수 있다.
  (반응성이 좋다.)

### 프로세스보다 스레드 간 context switching이 더 적은 비용이 드는 이유는?

스레드는 stack을 제외한 모든 메모리 영역을 공유하기 때문에, context switching 발생 시 stack 영역만 변경하면 되기 때문이다.

### 프로세스와 스레드의 차이점은?

프로세스

- 자원을 할당 받을 때, 다른 프로세스와 독립된 메모리 공간을 할당 받는다.

> - 프로세스는 기본적으로 서로의 데이터에 접근할 수 없다. 단, IPC를 사용하면 가능하다.
> - 프로세스는 최소 1개의 스레드(→ 메인 스레드)를 가지고 있다.

스레드

- 자원을 할당 받을 때, 자신이 위치한 프로세스 내에서 stack만 따로 할당 받고, 나머지 code, data, heap 영역은 같은 프로세스 내의 다른 스레드와 공유한다.

> - 때문에, 특정 스레드 하나에서 오류가 발생하면, 자원을 공유하고 있는 프로세스 내 다른 스레드가 모두 강제 종료된다.

### 스레드를 지원하는 주체에 따라 나눈다면 어떻게 나뉠까?

- 사용자 레벨 스레드
- 커널 레벨 스레드

### 사용자 레벨 스레드와 커널 레벨 스레드란?

사용자 레벨 스레드

- 사용자 영역에서 스레드 라이브러리로 구현되는 스레드.

커널 레벨 스레드

- 커널에 의해 직접 관리되는 스레드.

### 사용자 레벨 스레드의 장단점?

장점

- 커널에 의해 관리되지 않으므로, 스레드 관리에 대한 오버헤드가 적다.
- 사용자 영역에서 구현되므로, OS나 커널의 종류와 관계 없이 높은 이식성.

단점

- 커널에 의해 관리되지 않으므로, 하나의 스레드가 중단될 경우 나머지 스레드들도 함께 기다려야 한다.

### 커널 레벨 스레드의 장단점?

장점

- 각 스레드가 병렬적으로 실행될 수 있다.
- 커널에 의해 관리되므로, 스레드 관리에 오버헤드가 든다.

단점 `보충`

### 멀티 프로세싱(multi-processing)이란?

여러 프로세서가 작업을 동시에 처리하는 것.

### 멀티 프로그래밍(multi-programming)이란?

프로세서가 특정 프로세스를 처리할 때, I/O로 인한 idle 등 낭비되는 시간에 다른 프로세스를 처리하도록 하는 것.

### 멀티 태스킹(multi-tasking)이란?

OS의 스케줄링에 의해 여러 task를 번갈아가며 수행하는 것.

> - task: 프로세스보다 더 넓은 개념으로, OS에서 처리하는 작업, 또는 명령어 집합.
> - 멀티 태스킹을 통해 사용자는 작업이 동시에 진행되고 있다고 느끼게 된다.

### 멀티 프로그래밍과 멀티 태스킹의 차이는?

멀티 프로그래밍의 목적은 프로세서의 자원 낭비를 막기 위함이다.

반면, 멀티 태스킹의 목적은 여러 태스크를 번갈아 수행하며 동시에 진행되고 있는 것처럼 느끼게 하기 위함이다.

### 멀티 스레딩(multi-threading)이란?

하나의 프로세스를 여러 스레드로 구성해 실행하는 것이다.

### 멀티 프로그래밍와 멀티 스레드의 차이점?

멀티 프로그래밍

- 여러 개의 자식 프로세스 중 하나에 문제가 생기면, 해당 프로세스만 죽고 다른 프로세스에는 영향을 주지 않는다.
- context switching에 오버헤드 발생
- 프로세스 간 통신을 위해 (어렵고 복잡한) IPC 사용

멀티 스레드

- 스레드 중 하나에 문제가 생기면, 다른 스레드를 포함한 전체 프로세스가 영향을 받는다.
- 스레드 간 context switching가 빠르고 더 적은 오버헤드 발생
- 스레드 간 데이터를 주고 받는 것이 간단하다.

## 스케줄링

### Context Switching이란?

- 커널이 레지스터에 있는 현재 프로세스의 컨텍스트를 PCB에 저장하고,
- 다음 프로세스의 컨텍스트를 PCB로부터 읽어와 레지스터에 적재하는 것.

### Context란?

프로세스에 대한 정보들의 모음

### Context에는 예를 들어 어떤 정보들이 있을까?

- Process State: 프로세스 상태
- Process Counter: 다음에 실행할 명령어의 주소값

등이 있다.

### PCB(Process Control Block)란?

OS가 프로세스를 관리할 때 필요한 정보들의 모음.

### PCB가 생성되는 시점은?

프로세스가 생성될 때 같이 생성된다.

### PCB가 위치한 곳은?

커널이 상주하는 메모리에 함께 상주한다.

### Context Switching이 필요한 이유는? `보충`

### 프로세스의 상태가 전이되는 과정은? (프로세스 상태 전이도의 흐름은?)

![OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%201.png](OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%201.png)

**created**

job이 커널이 등록되었을 때의 상태.

> - 프로세스가 생성되고, 프로세스에 PCB가 할당된다.
> - 이 때, 커널은 가용한 메모리 공간이 있는지 확인해서 프로세스 상태(ready/suspended)를 결정한다.

**ready**

프로세스에 프로세서를 제외한 모든 필요한 자원이 할당된 상태.

> - dispatch(schedule): 프로세서 할당, running 상태로 전이.
> - ready 상태의 프로세스는 즉시 실행 가능한 상태이다.

**running**

프로세스에게 필요한 모든 자원이 할당된 상태.

> - preemption: 다른 프로세스에게 프로세서를 선점당하는 것. ready 상태로 전이.  
>   preemption은 time-out, priority 등의 이유로 process scheduling에 의해 발생한다.
>
> - sleep(block): I/O 등의 자원 할당 요청이 완료될 때까지 기다리는 것. asleep 상태로 전이.
> - exit: 모든 자원을 반납하고 프로세스를 종료.

**blocked(asleep)**

프로세서가 아닌 다른 자원의 할당을 기다리고 있는 상태.

> - wake-up: ready 상태로 전이.
>
> - 시스템 콜에 의해 자원 할당이 완료될 수 있다.
> - 물론 프로세서 역시 할당이 되어있지 않은 상태이다.

**Suspended**

메모리를 빼앗긴 상태.

> - 디스크로 swap-out된 상태.
> - suspended ready: ready 상태에 있던 프로세스가 디스크로 swap-out
> - suspended blocked: blocked 상태에 있던 프로세스가 디스크로 swap-out

**terminated**

프로세스 실행이 완료되어 모든 자원을 반납한 상태.

### 프로세스가 종료되면(terminated) PCB도 함께 제거될까?

- 대부분의 PCB는 제거되지만, 몇몇 PCB는 커널이 상주하는 메모리에 함께 남아있다.
- 추후 프로세스 관리에 사용된다.

### 스케줄링이 필요한 이유는?

시스템의 성능을 증가시키기 위해.

### 시스템의 성능을 어떤 기준으로 측정할까?

- response time: 요청으로부터 응답까지 걸리는 시간 (또는, 하나의 작업을 처리하는 데 드는 시간)
- throughput: 단위 시간 내 처리하는 작업의 수
- resource utilization: 주어진 시간 내 자원이 활용되는 시간

시스템의 목적에 따라, 위 기준 중 우선순위를 정해 스케줄링 전략을 택해야 한다.

### (참고) 용어

![OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%202.png](OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%202.png)

waiting time(대기 시간)  
: 작업이 큐에 도착하고 실행되기까지의 시간

response time(응답 시간)  
: 작업이 큐에 도착하고 첫번째 응답하기까지의 시간

burst time(실행 시간)  
: 작업이 실행되고, 실행 종료까지의 시간

turn-around time(반환 시간)  
: 작업이 큐에 도착하고, 실행 종료까지의 시간

### 스케줄링의 주기에 따라 3가지로 나눈다면 어떻게 나뉠까?

- 장기, 중기, 단기 스케줄링

### 장기 스케줄링이란? 예시는?

저빈도로 발생하는 스케줄링.

예시: job 스케줄링

- 커널에 등록되는 job을 결정

- job 스케줄러는 멀티 프로세스의 정도, 즉 시스템 내 돌아가는 프로세스의 수를 조절한다

### 중기 스케줄링이란? 예시는?

중간 빈도로 발생하는 스케줄링.

예시: 메모리에 적재된 프로세스 수 조절

- 너무 많은 프로세스가 메모리에 적재되어 있는 경우 swap out

- 중기 스케줄러는 처음으로는 blocked 상태의 프로세스를, 그래도 부족하면 ready 상태의 프로세스를 순서대로 swap out 한다.

### 단기 스케줄링이란? 예시는?

고빈도로 발생하는 스케줄링.

예시: 프로세스 스케줄링

- 프로세서를 할당할 프로세스를 결정

- 고빈도로 발생하므로, 성능에 가장 큰 영향을 준다.

### 선점형 스케줄링과 비선점형 스케줄링의 차이?

선점형 스케줄링: 할당된 자원이 다른 프로세스에 의해 선점될 수 있다.

비선점 스케줄링: 할당된 자원을 스스로 반납할 때까지 사용.

### 선점형 스케줄링의 장단점?

장점: 짧은 응답 시간

단점: 잦은 context switching로 높은 오버헤드

real time system에 적합하다.

### 비선점형 스케줄링의 장단점?

장점: 저빈도로 발생하는 context switching으로 낮은 오버헤드

단점: 평균적으로 긴 응답 시간

### 자원 관리에 있어서 time sharing과 space sharing의 차이는?

time sharing

- 여러 사용처가 하나의 자원을 차례대로 사용하는 것.
- 예: 여러 스레드가 하나의 스레드를 차례대로 사용 (→ 프로세스 스케줄링)

space sharing

- 여러 사용처가 하나의 자원을 나눠 동시에 사용하는 것.
- 예: 여러 스레드가 하나의 메모리를 나눠서 동시에 사용

### FCFS(First Come First Service)란?

ready queue에 도착한 순서대로 스케줄링하는 전략.

> - 비선점형 스케줄링

### FCFS의 장단점?

장점

- resource utilization이 높다. (쉬지 않고 cpu가 사용되므로)
- 스케줄링 overhead이 낮다.

단점

- convoy effect: 오래 걸리는 작업 하나 때문에 다른 작업들도 덩달아 오래 걸리게 만드는 현상
- response time이 평균적으로 길다.

### FCFS에 적합한 시스템은?

interaction이 없는 batch system에 적절하다.

### 배치 시스템(배치 처리, batch system, batch process)란?

특정 시간에 작업을 일괄적으로 처리하는 시스템.

### Round Robin이란?

ready queue에 도착하는 시간을 기준으로 스케줄링하되, time quantum(제한 시간)이 넘어가면 자원을 반납하도록 하는 전략.

> - 선점형 스케줄링

### Round Robin의 장단점?

장점

- 특정 프로세스가 프로세서를 독점하는 것을 방지한다.

단점

- context switching 오버헤드가 높다.

### time quantum이 짧을 때와 길 때 성능에 어떤 영향을 미칠까?

time quantum이 아주 클때

- FCFS와 동일해진다.

time quantum이 아주 짧을 때

- 마치 모든 프로세스가 프로세서를 동시에 사용하는 것처럼 보인다.
- 그러나 현실적으로는 context switching 오버헤드가 너무 높다.

### Round Robin은 어떤 서비스에 적합할까?

- interactive system
- time-sharing system

### SPN(Shortest Process Next)이란?

burst time이 적은 프로세스를 우선적으로 스케줄링하는 전략.

- 비선점형 스케줄링

### SPN의 장단점

장점

- waiting time이 평균적으로 짧다. (burst time이 짧은 프로세스는 나중에 도착해도 바로바로 서비스)
- 대부분의 프로세스에 대해 response time이 짧다.
- 시스템 내 운용되는 프로세스의 수를 적게 유지할 수 있다.

단점

- starvation: burst time이 긴 프로세스는 한없이 기다려야 한다.
- burst time을 예측하는 것은 복잡하고 어렵다.

### 시스템 내 프로세스 수를 적게 유지했을 때의 좋은 점은?

- context switching 오버헤드가 적다.
- 사용되는 메모리가 적다.

### SRTN(Shortest Remaining Time Next)란?

burst time이 적은 프로세스를 우선적으로 스케줄링하되, 더 짧은 burst time을 가진 프로세스가 준비되면 해당 프로세스를 서비스하는 전략.

- 선점형 스케줄링

### SRTN의 장단점?

장점

- SPN의 장점을 극대화: 짧은 waiting time, response time, 적은 프로세스 수 유지

단점

- starvation
- burst time을 예측해야 한다.
- 추가로, 현재까지 남은 burst time(remaining time)을 tracking해야 한다. (→ 오버헤드)
- context switching 오버헤드

### HRRN(High Response Ratio Next)이란?

response ratio가 높은 프로세스를 먼저 스케줄링하는 전략.

- response ratio = (waiting time + burst time) / burst time

### HRRN의 장단점?

장점

- aging concept가 도입: 프로세스의 waiting time을 스케줄링에 고려
  → starvation이 방지
- SPN의 장점: 짧은 평균 waiting time, 대부분의 프로세스의 짧은 response time, 시스템 내 적은 프로세스 수 유지

단점

- burst time 예측 필요

### MLQ(Multi Level Queue)란?

작업을, 우선 순위에 따라 나뉘어진 여러 개의 큐 중 하나에 넣고, 높은 우선 순위를 가지는 큐의 작업을 먼저 스케줄링하는 전략

- 각각의 큐는 각자의 스케줄링 전략을 갖는다(FCFS 아님)
- 한 번 큐에 들어간 작업은 위치를 옮길 수 없다.

### MLQ의 장단점?

장점

- 높은 우선순위를 가지는 작업은 짧은 response time을 가진다.

단점

- 여러 개의 큐를 운용 → 오버헤드
- 낮은 우선순위를 가진 큐에 대해 stavation 발생

### MFQ(Multi level Feedback Queue)란?

(MLQ와 동일) 작업을, 우선순위에 따라 나뉘어진 여러 개의 큐 중 하나에 넣고, 높은 우선순위를 가지는 큐의 작업을 먼저 스케줄링한다.

단, feedback에 따라 작업이 큐 사이를 옮겨다닐 수 있다.

### feedback에는 어떤 것들이 있을까?

waiting time 등.. MFQ가 취하는 전략에 따라 다르다.

### MFQ의 장단점?

장점

- burst time 등의 사전 정보 없이도 SPN, SRTN, HRRN 전략들의 장점을 취할 수 있다.
  - 평균적으로 짧은 waiting time
  - 대부분의 프로세스가 짧은 response time
  - 시스템 내 적은 수의 프로세스 유지

단점

- 구현하기 어렵다.
- 스케줄링 오버헤드가 크다.
- 전략에 따라, 경우에 따라 낮은 우선순위의 작업은 여전히 starvation 발생 가능.

## 동기화

### 동기화란?

작업들 사이에 실행 시기를 맞추는 것.

### 동기화가 필요한 이유는?

동일한 자원을 여러 프로세스(스레드)가 동시에 수정할 경우, 그 순서에 따라 의도치 않은 결과값이 나올 수 있기 때문이다.

> - 다중 프로그래밍 환경에서는 기본적으로 프로세스들은 서로 엄격하게 구분되어 상호 간섭이 불가하지만, 프로세스들이 메모리를 공유하거나(공유 메모리) 다중 스레드를 지원하는 경우, 여러 프로세스 혹은 스레드가 공유된 자원에 접근하는 상황이 발생할 수 있다.

### Critical section(임계 구역)이란?

공유 자원에 접근하는 코드 일부분(조각).

> - 공유 자원(shared data, critical data): 둘 이상의 프로세스에 의해 공유되는 데이터.

### Race condition(경쟁 상태)이란?

조작의 순서에 따라 결과값이 달라질 수 있는 상태.

### Mutual exclusion(상호 배제)이란?

어떤 프로세스가 공유 데이터를 사용하고 있을 때, 다른 프로세스가 공유 데이터에 접근하지 못하도록 하기 위해 사용되는 알고리즘.

### Mutual exclusion에 사용되는 기본 연산(primitive)의 조건은?

1. Mutual exclusion: 어떤 프로세스가 공유 자원을 사용하고 있다면, 다른 프로세스는 해당 공유 자원에 접근할 수 없다.

2. Progress: 공유 자원을 사용하고 있는 프로세스 이외에는, 어떤 프로세스가 공유 자원에 접근하는 것을 막아서는 안된다.

3. Bounded waiting: 프로세스는 한정된 시간 동안에만 공유 자원을 사용할 수 있다.

### Mutual exclusion을 SW로 구현한 알고리즘에는 어떤 것들이 있나?

Dekker's algorithm

### Dekker's algorithm을 설명해본다면?

- `flag` 변수로 어떤 프로세스가 Critical section(이하 CS)에 접근하기를 원한다는 것을 나타냄.
- `turn` 변수로 누가 CS에 들어갈 차례인지 나타냄.

- 두 개의 프로세스에 대한 상호 배제 알고리즘이다. (두 개 이상의 프로세스에는 적용 불가)

### Dekker's algorithm을 더 자세히 설명해본다면? (간단하게 코드로 표현해본다면?)

```c
/* P0 */
flag[0] <- true // P0이 CS에 접근하길 바래요.
while (flag[1]) { // P1이 CS에 접근하길 바라고 있다면,
	if (turn == 1) { // P1이 사용하고 있다면,
		flag[0] <- false // 우선은 P0이 CS에 접근하고 싶지 않다고 물러서요.
		while (turn == 1) {} // P1이 사용하고 있는 동안 기다려요.
		// 이 때 P1이 CS로부터 나오면서 turn을 0으로 만들어줘요.
		flag[0] <- true // P1이 CS로부터 나왔다면, P0이 다시 들어가고 싶다고 말해요.
	}
} // P1이 CS에 접근하길 바라고 있지 않다면, 바로 CS에 접근해요

/* ..CS.. */
turn <- 1 // turn을 1로 만들어주고 CS에서 나와요.
flag[0] <- false // 사용을 끝냈으니 CS에 접근할 생각이 없다고 밝혀요.

/* P1 */
// P0과 같은 흐름으로 진행.. (flag, turn 변수만 변경)
```

### SW로 구현한 상호 배제 알고리즘의 단점은?

- busy waiting: 다른 프로세스가 CS 접근을 끝낼 때까지 반복문을 돈다.
  → 비효율적
- 구현하기 까다롭다.
- 기본 연산 중에 선점될 수 있다. (OS에서 보장하는 atomic 연산이 아니므로)

### HW로 구현한 상호 배제 알고리즘에는 어떤 것들이 있나?

- TAS(TestAndSet)

### TAS(TestAndSet)란?

test와 set을 한 번에 수행할 수 있는 machine instruction.

```c
boolean TestAndSet(boolean *target) {
	boolean temp = *target; // 이전의 값을 기록.
	*target = true; // target 값을 true로 변경
	return temp; // 이전 값을 반환
}
```

machine instruction이기 때문에, 실행 중에 선점되지 않는다.

### TAS를 이용해 ME가 보장되는 과정을 조금 더 자세히 설명? (코드로 설명?)

```c
// 최초에는 lock = false;
while (TAS(lock)) {} // lock이 true일 동안에는 CS에 접근하지 못한다.
									// lock이 false일 경우에는, lock을 true로 set하고 CS에 접근한다.
/* ..CS.. */
lock <- false // CS를 나올 때 lockㅇ
```

- 위 코드는 3개 이상의 프로세스가 존재할 때, bounded waiting을 위반한다.
- N개의 프로세스에도 유효한 P

### OS로 구현한 상호 배제 알고리즘에는 어떤 것들이 있나?

- Spinlock(스핀락)
- mutex(뮤텍스)
- Semaphore(세마포어)

### 스핀락이란?

- 특정 자료구조를 lock하거나 unlock해서 CS에 대한 접근 권한을 관리하는 방법.  
  (여기서 특정 자료구조란 integer 변수 등이 해당된다.)
- 권한을 획득하기 전까지는 busy waiting 상태로 대기하고 있다가 접근 권한을 얻으면 CS 수행 후 권한을 반납

> "스핀락"은 접근 권한을 관리하는 자료구조(정수값) 자체를 칭하는 단어이기도 하다.

### 스핀락의 장단점은?

장점

- (무의미한 코드를 수행하며) busy waiting 상태로 CPU를 선점하고 있기 때문에, 권한을 얻는 대로 바로 빠르게 작업을 수행할 수 있다.

단점

- 해당 프로세스의 CPU 선점 기간(busy waiting)동안 다른 프로세스의 작업이 지연될 수 있다.
- 단일 프로세서 환경에 사용할 수 없다. (하나의 프로세스가 busy waiting에 들어가면, 다른 프로세스가 lock을 풀어줄 수 없기 때문이다.)

### 스핀락은 어떤 특성의 프로세스에서 사용하기 적절할까?

프로세스가 빠르게 작업을 수행할 수 있을 때.  
(context switching은 비싼 작업이기 때문이다. 프로세스 간 빠르고 잦은 context switching이 이뤄질 때는 스핀락을 사용할 때 context switching 비용을 아낄 수 있다.)

### 뮤텍스란?

- (스핀락과 동일하게) 특정 자료구조를 lock하거나 unlock해서 CS에 대한 접근 권한을 관리하는 방법.
- (스핀락과는 다르게) 권한을 획득하기 전까지 sleep 상태로 대기하고 있다가 wake-up되면 다시 권한 획득을 시도한다.

### 뮤텍스는 어떤 특성의 프로세스에서 사용하기 적절할까?

- 프로세스에게 길게 처리해야 하는 작업이 많을 때.

### 스핀락과 뮤텍스의 차이점?

- 스핀락은 권한을 획득할 때까지 busy waiting 상태로 기다린다.
  → 해당 프로세스가 cpu를 계속 점유하고 있다.
- 뮤텍스는 권한을 획득할 때까지 sleep 상태로 대기한다.

### 세마포어란?

정수형 자료구조를 사용해 여러 개의 공유 자원에 대한 접근 권한을 관리하는 방법.

### 세마포어에 사용되는 연산의 종류와 그 로직은?

`initialization()`

- 세마포어의 값을 사용 가능한 자원의 개수로 초기화

`P()` (또는 `wait()`)

- 세마포어 값이(즉, 사용 가능한 자원의 개수가) 0 이상이면, 값에서 1을 빼고 CS에 접근한다.
- 세마포어 값이 0이면, wait queue에서 기다린다.

- atomic 연산이다.

`V()` (또는 `signal()`)

- wait queue에 프로세스가 대기하고 있으면 그 중 하나를 깨운다.
- 세마포어 값에 1을 더한 뒤, CS로부터 나온다.

- atomic 연산이다.

### 스핀락(혹은 뮤텍스)와 세마포어의 차이는?

- 스핀락(혹은 뮤텍스)은 접근 권한을 관리하는 자료구조가 0과 1(혹은 그와 상응하는 boolean 값)만 값으로 가질 수 있어, 하나의 공유 자원에 대한 접근 권한만을 관리할 수 있다.

  세마포어는 접근 권한을 관리하는 자료구조가 정수형으로, 여러 개의 공유 자원에 대한 사용 가능 여부를 표현할 수 있다.

- 스핀락(뮤텍스)은 자원을 소유하고 있는 프로세스만이 자원을 해제할 수 있다.

  세마포어는 해당 자원을 소유하고 있지 않은 다른 프로세스가 세마포어를 해제할 수 있다.

- 세마포어는 스핀락(뮤텍스)가 될 수 있지만, 스핀락(뮤텍스)는 세마포어가 될 수 없다.

- 0과 1의 값만 가지는 세마포어를 이진 세마포어(binary semaphore)라고 부른다. 이를 스핀락, 혹은 뮤텍스처럼 사용할 수 있다.
- (사소하게는) 스핀락에서는 값이 1일 때가 'locked', 즉 공유 자원을 사용할 수 없는 상태인 것에 반해 세마포어에서는 값이 0 이상이어야 사용 가능하다.

## 데드락

### 데드락(dead lock, 교착 상태)이란?

서로 원하는 자원이 상대방에게 할당되어 있어 두 프로세스가 무한정 wait 상태에 빠지는 상황.

### 데드락이 발생하기 위한 조건은?

1. 상호 배제

- 자원은 한 번에 한 프로세스만 사용할 수 있다.

2. 점유 대기

- 최소한 하나의 자원을 점유하고 있으면서, 다른 프로세스에 할당된 자원을 추가로 점유하기 위해 대기하는 프로세스가 존재한다.

3. 비선점

- 다른 프로세스에 할당된 자원은 사용이 끝날 때까지 강제로 빼앗을 수 없다.

4. 순환 대기

- 프로세스의 집합이 순환 형태로 자원을 대기하고 있어야 한다.

- 위 조건들은 데드락의 필요 조건이다. 즉, 데드락이 발생했다면 위 조건을 만족하지만, 위 조건을 만족한다고 데드락이 발생하는 것은 아니다.

### 데드락을 처리하는 방법은?

- 예방/회피
- 회복
- 무시

### 데드락을 예방하는 방법은?

데드락 조건 중 하나를 만족하지 않도록 하는 방법. (상호 배제, 점유 대기, 비선점, 순환 대기 중 하나를 부정)

### 데드락을 예방하는 방법의 단점은?

자원 낭비가 심하다.

### 데드락을 회피하는 방법은?

데드락이 발생하지 않는 알고리즘을 적용한다.

### 데드락 회피 알고리즘 중 하나를 설명?

은행원 알고리즘

- 안정 상태를 유지할 수 있는 요청만 수락하고,
- 불안정 상태를 초래할 수 있는 요청은 거절한다.

### 은행원 알고리즘의 안정 상태, 불안정 상태란?

안정 상태

- 안전 순서열이 존재하는 상태.
  즉, 시스템이 데드락을 일으키지 않으면서, 각 프로세스가 요구하는 최대 요구량만큼 자원을 할당해줄 수 있는 상태.

불안정 상태

- 안전 순서열이 존재하지 않는 상태.
- 데드락의 필요 조건.  
  (데드락이면 불안정 상태로 갈 수 있지만, 불안정 상태가 곧 데드락은 아니다)

### 은행원 알고리즘이 수행되기 위해 필요한(유지해야 하는) 정보는?

- `Max`: 각 프로세스가 최대로 얼만큼의 자원을 요청할지
- `Allocated`: 각 프로세스가 현재 요청한 자원이 얼마인지
- `Available`: 현재 할당 가능한 자원이 얼마인지

### 은행원 알고리즘의 단점은?

- 최대 자원 요구량(Max)를 미리 알아야 한다.
- 자원 활용률이 낮다. (불안정 상태를 방지해야 하므로)

### 데드락을 회복하는 방법은?

데드락을 일으킨 프로세스를 종료시키거나, 할당된 자원을 회수한다.

### 언제 데드락 발생을 무시할까?

데드락으로 인한 성능 저하보다 회복하는 데 발생하는 성능 저하가 클 때.

## 가상 메모리

### 가상 메모리란? (메모리 가상화란?)

각 프로세스가 그들의 전용 메모리가 있다고 착각하게 만드는 메모리 관리 기법.

> - physical memory address 대신 virtual memory address를 사용하도록 하는 것.

### 메모리의 가상화가 필요한 이유는?

(디스크 같은 느리지만 큰 저장 장치를 활용해서) 한정된 메모리 크기를 극복해 애플리케이션(또는 프로세스)이 더 많은 메모리를 활용할 수 있게끔 해주기 위함.

## 주소 변환(address translation)

### 주소 변환이란?

하드웨어를 통해 가상 주소를 실제 물리 주소로 변환하는 것.

> - 주소 변환은 가상 메모리를 구현하는 간단한 방법 중 하나이다.

### 주소 변환이 필요한 이유는?

프로그램의 모든 메모리 참조를 실제 메모리 위치로 재지정하기 위해.

### 주소 변환을 구현한 기술에는 어떤 것이 있는지?

- base and bound

- base and bound는 동적 재배치(dynamic relocation)이라고도 불리운다. 프로세스가 실행된 후에도 주소를 변경할 수 있기 때문이다(→ "동적").

### base and bound란?

프로세스의 메모리 참조가 사용하는 가상 주소에 베이스 레지스터(base register) 값을 더해 실제 물리 주소 값을 구하는 방법.

### 베이스 레지스터란?

프로그램이 참조하는 가상 주소로부터 물리 주소를 얻기 위해 더해야 하는 주소 값을 가지고 있는 레지스터.

> - 프로그램이 메모리에 접근할 때 offset을 얻어낼 수 있다. 이 offset은 베이스 레지스터가 가리키는 위치로부터 떨어진 만큼을 가리킨다.
> - 즉, `physical address = base register + offset`

### 바운드 레지스터(bound register)란?

다른 프로세스가 사용하는 메모리 침범을 막기 위한 레지스터.

> - 베이스 레지스터와 바운드 레지스터는 하드웨어로 구현된다. 정확히는 CPU 내에, MMU(Memory Management Unit, 메모리 관리 장치)의 일부로서 제공된다.
> - 베이스 레지스터, 바운드 레지스터를 포함한 하드웨어만으로는 메모리 가상화를 구현할 수 없다. 운영체제의 도움이 필요하다.

### 바운드 레지스터가 타 프로세스 메모리 침범을 막는 방법은?

- 가상 주소에 베이스 레지스터 값을 더해 물리 주소를 구한 후, 바운드 레지스터의 값으로 유효 범위를 확인한다.
- 바운드 레지스터는 해당 프로세스에게 할당된 메모리의 크기 값을 가지고 있다.
- 범위를 벗어난 주소로 접근을 시도하면, 하드웨어가 예외를 발생시킨다.  
  (오프셋 값이 바운드 레지스터 값보다 작은지 확인하면 된다.)

> - 하드웨어가 발생시킨 에러는, 운영체제가 제공하는(제공해야 한다) 예외 핸들러에 의해 처리된다.
> - 바운드 레지스터는 할당된 메모리의 크기 값을 가지고 있다.

### base and bound에서 운영체제의 역할은?

- 프로세스가 생성될 떄, 저장될 메모리 공간을 찾는다.
  - 이를 위해 운용되는 빈 공간 리스트(free list)에서 공간을 찾고, 사용 중이라 표시한다.
- 프로세스가 전환될 시, PCB에 베이스-바운드 레지스터 쌍을 저장하거나 복원한다.

> - 운영체제를 실행시키기 위해 커널 모드를 실행해야 한다.
> - process state word 레지스터의 비트 중 일부가 CPU의 실행 모드를 나타낸다.

### base and bound에서 프로세스의 주소 공간을 옮기려면 어떻게 해야 하나?

- 먼저 운영체제가 프로세스의 실행을 중지한다.
- 해당 프로세스의 PCB에 저장된 베이스 레지스터의 값을 갱신해 새로운 위치를 가리키도록 한다.

### base and bound의 장단점은?

장점

- 베이스, 바운드 레지스터가 하드웨어로 구현되어 효율적이다.

단점

- 내부 단편화
- 가상 주소 공간이 실제 물리 메모리 공간보다 큰 경우 실행이 매우 어렵다.

### base and bound의 내부 단편화 문제란?

- 프로세스가 고정된 크기의 슬롯으로(→ 단편화되어) 물리 주소에 배치된다.
- 프로세스의 스택과 힙이 그닥 크지 않기 때문에, 낭비되는 공간이 크다.

## 세그멘테이션(segmentation)

### 세그멘테이션이란?

가상 메모리를 세그먼트로 분할하고 할당하는 메모리 관리 기법.

> - Segmentation Fault는 세그멘테이션을 사용하는 시스템에서 불법적인 주소로 접근 시에 발생하는 에러이다.

### 세그먼트란?

서로 다른 길이를 가지는 연속적인 주소 공간.

> - 3종류의 세그먼트가 존재한다: 코드, 힙, 스택. ('data'는 아님)

### 세그멘테이션에서 가상 주소로부터 물리 주소를 얻는 과정은?

- 각 세그먼트마다 베이스-바운드 레지스터 쌍을 가지고 있다.
- 프로그램에서 접근하는 세그먼트의 메모리의 주소(offset)에, 베이스 레지스터 값을 더해 실제 물리 주소를 구한다.  
  (`physical address = offset + base register`)

  > - 즉, 하나의 프로세스는 3쌍의 베이스-바운드 레지스터를 가지고 있게 된다.
  > - 하드웨어는 프로그램이 어떤 종류의 세그먼트에 접근하는 것인지 파악해야 한다.
  > - 어떤 종류의 세그먼트에 접근하는 것인지 알게되면, 해당 종류의 세그먼트를 위한 베이스-바운드 레지스터를 참조할 수 있다. (예: 힙의 베이스-바운드 레지스터)
  >
  > - 하드웨어는 세그먼트 레지스터를 통해 세그먼트 주소를 가지고 있다.

  > 요약)  
  >  세그먼트 레지스터 → 가상 주소  
  >  가상 주소 = 최상위 2비트(→ 세그먼트 종류) + offset  
  >  → 세그먼트 종류에 해당하는 베이스-바운드 레지스터 & offset  
  >  → 물리 주소

### 세그먼트의 바운드 레지스터의 역할은?

- 세그먼트의 크기를 가지고 있다.
- 프로그램이 메모리에 접근할 때, offset이 바운드 레지스터 값보다 작은지 확인해서 불법적인 메모리에 접근하지 않도록 한다.

### 하드웨어가 가상 주소에서 세그먼트의 종류와 오프셋을 파악하는 방법은?

- 하드웨어는 세그먼트 레지스터를 통해 세그먼트의 가상 주소 값을 얻는다.
- 세그먼트의 종류를 파악하기 위해 가상 주소의 최상위 2비트를 사용한다.
- 최상위 2비트를 제외한 나머지 비트는 offset이 된다.

> - 3종류의 세그먼트가 있으므로, 2비트를 사용해 00, 01, 10으로 3종류의 세그먼트를 가리킬 수 있다.
>
> - 다른 방법: '암묵적 접근' 방식도 있다. 주소가 어떻게 형성되었는지를 관찰해 세그먼트의 종류를 파악한다. 예를 들어, 주소가 Program Counter에서 생성되었다면 코드 세그먼트일 것이다.

### 가상 주소 변환에 있어서 스택과 나머지 종류의 세그먼트 간 차이는?

확장되는 주소의 방향이 다르다.

- 스택은 높은 주소에서 낮은 주소로,
- 나머지 종류의 세그먼트(코드, 힙)은 낮은 주소에서 높은 주소로 확장한다.
- 양수 방향으로 증가하는지(grows positive?)를 나타내는 하드웨어를 통해 파악할 수 있다.

### 하드웨어는 세그먼트가 어느 방향으로 확장해야 하는지 어떻게 알 수 있을까?

세그먼트가 확장하는 방향을 담은 레지스터를 통해 파악한다.  
(베이스-바운드 레지스터 이외의 추가적인 레지스터가 된다.)

- 주소가 커지는 방향으로 확장하면(순방향) 1 (코드, 힙)
- 주소가 작아지는 방향으로 확장하면(역방향) 0을 저장한다. (스택)

### 세그멘테이션이 메모리 공유를 지원하는 방법은?

- 세그먼트마다 protection bit를 통해, 해당 세그먼트가 읽을 수 있는지 / 쓸 수 있는지 / 실행시킬 수 있는지 나타낸다.
- 세그먼트를 읽기 전용으로 설정하면, 여러 프로세스가 해당 세그먼트를 공유할 수 있다.

> - 읽기 전용 세그먼트에 쓰기를 시도하면, 하드웨어가 예외를 발생시킨다. 해당 예외는 운영체제가 처리할 수 있어야 한다.

(참고)

![OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%203.png](OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%203.png)

### 세그멘테이션을 위한 운영체제의 역할은?

- context switching 시 세그먼트 레지스터 값을 저장/복원
- 미사용 중인 물리 메모리 공간 관리

### 세그먼트 테이블?

### 세그멘테이션의 장단점은?

장점

- 내부 단편화가 발생하지 않는다.
  즉, 가상 주소 공간이 물리 메모리를 불필요하게 차지하는 것을 방지할 수 있다.
- 하드웨어 구현에 적합
  (세그먼트 레지스터, 베이스-바운드 레지스터, grows positive, protection bit 등) - 속도가 빠르다. - 구현이 쉽다. - 오버헤드가 적다.

단점

- 외부 단편화

### 외부 단편화란?

작은 메모리(세그먼트)가 물리 메모리의 중간 중간에 위치해, 여유 메모리 공간은 충분하지만 실제로 할당할 수는 없는 현상.

> - 외부 단편화는 가변 길이 할당의 태생적인 문제이다.

### 외부 단편화에 대한 대응 방안은?

- '압축'(compact)
- 빈 공간 리스트를 관리하는 알고리즘을 사용

### 압축이란? 진행되는 과정은?

기존의 세그먼트를 정리해서 물리 메모리를 압축하는 것.

- (현재 실행 중인 프로세스를 중단하고)
- 흩어진 프로세스 데이터들을 하나의 연속된 공간에 복사한다.
- (세그먼트 레지스터가 새로운 주소값을 가리키도록 한다.)

### 압축의 단점은?

비용이 크다.

- 세그먼트 복사는 메모리에 부하가 큰 연산이다.
- 상당량의 프로세서 시간을 사용.

### 빈 공간 리스트를 관리하는 알고리즘에는 어떤 것들이 있나?

- 최초 적합(first-fit): 가장 먼저 발견되는 빈 공간에 넣는다.
- 최적 적합(best-fit): 다 비교해보고, 가장 자투리 공간이 적게 남는 공간에 넣는다.
- 최악 적합(worst-fit): 다 비교해보고, 가장 자투리 공간이 넓게 남는 공간에 넣는다.

> - 빈 공간 관리 알고리즘은 할당 가능한 메모리 영역들을 리스트 형태로 유지한다.
> - 최악 적합은.. 최적 적합으로 할당하면 자투리 공간이 엄청 조금 남게 되는데, 그건 아예 쓰지도 못하게 되지 않느냐, 차라리 조금이나마 넓게 냅두어서 나중에라도 쓸 수 있게 하는 것이 낫다는 논리이다.

## 페이징(Paging)

### 페이징이란?

메모리 공간을 고정된 크기의 단위(→ '페이지')로 분할하는 메모리 관리 기법.

### 페이징이 등장하게 된 배경은?

- 메모리를 가변 길이로 할당하게 됨에 따라 외부 단편화가 발생.
- 고정 길이 할당을 통해 외부 단편화를 방지하기 위해 등장.

### 페이징의 장단점은?

장점

- 유연성: 프로세스가 주소 공간을 어떻게 사용하는지에 대해 신경쓰지 않아도 됨.
  (어떻게 사용되는가, 힙과 스택이 어느 방향으로 커지는가 등)
- 빈 공간 리스트 관리가 용이
  (세그멘테이션이 알고리즘이나 압축으로 외부 단편화에 대응했던 것에 대비되어, 단순히 빈 공간 리스트의 첫 번째 항목을 할당해주면 된다.)

단점

- 상당한 성능 저하를 일으킬 수 있다.
  가상 주소 변환을 위해서는 메모리에 상주하는 페이지 테이블을 읽어야 하는데, 메모리 읽기 작업은 성능 저하를 유발한다. (모든 load/store 명령에 추가적인 메모리 읽기가 수반)

> - 페이징의 성능 저하를 개선하기 위한 방법으로 TLB(Translation-Lookaside Buffer)가 있다.

### 페이징에서 물리 메모리의 구성은 어떻게 다른가?

- 물리 메모리도 고정 크기의 슬롯의 배열, 즉 "페이지 프레임(page frame)"로 취급된다.
- 각각의 슬롯에 하나의 가상 메모리 페이지를 저장할 수 있다.

### 페이지 테이블(page table)이란?

(가상 주소 공간의) 각 가상 페이지의 물리 주소(혹은, 주소 변환 정보)를 저장해놓는 자료구조.

> - 페이지 테이블은 메모리에 저장되어 있다. (메모리 중에서도, 운영체제가 상주하는 메모리에 함께 상주한다.)
> - 페이지 테이블은 프로세스마다(프로세스 수만큼) 존재한다.
> - 운영체제가 다른 프로세스를 실행하려면, 해당 프로세스를 위한 다른 페이지 테이블이 필요하다.(새 프로세스의 가상 페이지는, 공유 중인 페이지가 없는 한 다른 물리 메모리에 존재할 것이다.)

### 페이지 테이블 엔트리(PTE, Page Table Entry)란?

PFN과 기타 여러 정보를 담고 있는 페이지 테이블의 구성 요소.

> - VPN은 페이지 테이블의 인덱스로 활용된다.

### PTE의 구성 요소에는 어떤 것들이 있는지?

- Valid bit: 해당 메모리 공간이 할당된 공간인지 표시.
- Protection bit: 해당 페이지가 읽을 수 있는지, 쓸 수 있는지, 실행될 수 있는지를 표시.
- Present bit: 해당 페이지가 물리 메모리에 있는지, 디스크에 swap-out 되었는지를 표시.

### 페이징의 가상 주소에서 물리 주소를 얻어내는 과정은?

- 가상 주소를 이진 형식으로 변환한다.  
  `"21" → "010101"`
- 이진 주소는 VPN(Virtual Page Number, 가상 페이지 번호)와 offset으로 나뉘어진다.
- VPN을 페이지 테이블의 인덱스로 사용해 PFN(Physical Frame Number)를 얻어낸다.  
  `"01" → [페이지 테이블] → "111"`
- PFN과 offset을 합쳐 물리 주소를 얻어낸다.  
  `"111" + "0101" → "1110101"("117")`

- 오프셋은 변환되지 않는다. "페이지 내"에서의 위치를 나타내기 때문이다.

### 현재 실행 중인 프로세스의 페이지 테이블 위치를 어떻게 알 수 있을까?

페이지 테이블 베이스 레지스터(page table base register)에 페이지 테이블의 시작 주소(물리 주소)가 저장되어 있다.

## TLB

### TLB(Translation-Lookaside Buffer, 변환-색인 버퍼)란?

자주 참조되는 가상 주소와 - 실 주소 변환 정보를 저장하는 하드웨어 캐시.

> - TLB는 하드웨어, CPU 내 MMU(Memory Management Unit, 메모리 관리부)에 위치한다.

### TLB가 필요한 이유는?

페이징의 성능 저하를 극복하기 위한 대안으로 등장했다.

> - 페이징에서는 가상 주소 변환을 위해 메모리에 상주하는 페이지 테이블을 읽어야 하는데, 메모리 읽기 작업은 성능 저하를 유발한다.

### TLB가 도입된 상태에서 가상 메모리 참조 시 일어나는 과정은?

- 가상 주소에서 VPN을 추출한다.
- 하드웨어는 해당 VPN으로 TLB에 원하는 변환 정보가 있는지 확인한다.
  - 있다면(TLB hit), TLB 항목에서 PFN을 추출한다.
  - PFN을 가상 주소의 offset과 합쳐 물리 주소를 구성하고, 메모리에 접근한다.
- 없다면(TLB miss), 하드웨어가 메모리의 페이지 테이블을 조회한다.
  (page table base register로 페이지 테이블의 위치를 알 수 있다.)
- 주소 변환 정보를 TLB로 읽어들인다.
- TLB가 갱신되면, 하드웨어는 명령어를 재실행한다.
  (재실행 되었을 때는 TLB가 갱신되어 TLB hit이 발생할 것이다.)

### (TLB의) 지역성 2종류와 적용된 예시에 대해 설명?

시간 지역성: 한번 참조된 메모리 영역이 짧은 시간 내에 다시 참조되는 현상.

- ex) 반복문 내에서 같은 배열을 다시 사용 / 반복문 후 해당 배열을 바로 다시 사용.

공간 지역성: 참조된 메모리에 가까운 위치의 메모리 영역이 다시 참조되는 현상.

- ex) 배열의 인자를 순회할 때, 페이지의 첫 번째 항목을 접근할 때만 TLB 미스가 발생.

![OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%204.png](OS%20e8aed882f45845d1a8fe27f71d71571b/Untitled%204.png)

> - TLB hit rate = hit / accesses

### TLB 미스를 처리하는 방법에는 어떤 것들이 있을까?

1. 하드웨어가 처리

- 하드웨어가 페이지 테이블에서 원하는 PTE를 찾는다.
- TLB에 읽어들여 TLB를 갱신한다.
- TLB 미스가 발생한 명령어를 재실행한다.

2. 소프트웨어가 처리

- 하드웨어가 예외 시그널을 발생시킨다.
- 시그널을 감지한 운영 체제는 명령어 실행을 중지하고 실행 모드를 커널 모드로 변경한다.
- 운영체제는 '트랩 핸들러(trap handler)'를 실행.
- 트랩 핸들러는 페이지 테이블에서 원하는 PTE를 찾고, TLB 접근이 가능한 특권 명령어로 TLB를 갱신한다.
- 트랩 핸들러가 리턴되면 하드웨어가 명령어를 재실행한다.

> - CISC 기반 하드웨어가 TLB 미스를 하드웨어가 처리하고, RISC 기반 하드웨어가 소프트웨어로 처리한다.
>
> - 시스템 콜 호출 시 사용되는 트랩 핸들러는 리턴 후 시스템 콜을 호출한 명령어의 '다음' 명령어를 실행한다. TLB 미스를 처리하는 트랩 핸들러는 리턴 후 시스템 콜을 호출한 명령어를 '다시' 실행한다. 즉 운영체제는 트랩의 발생 원인에 따라 PC에 현재 명령어의 값, 또는 다음 명령어의 값을 넣어야 한다.

### TLB 미스 트랩 핸들러가 실행될 때 TLB 미스가 나지 않도록 대응 방안?

(가상 주소 공간에 위치한 트랩 핸들러를 실행할 때 TLB 미스가 나면, 트랩 핸들러가 무한 반복으로 호출될 것이다.)

방법 1.  
TLB 미스 핸들러를 가상 메모리가 아닌 물리 메모리에만 위치시킨다.

방법 2.  
TLB의 일부를 트랩 핸들러의 주소 변환 정보를 위해 영구히 할당한다.  
(→ "연결 변환(wired translate)" 라고 한다)

### TLB Cache가 설계된 방식은? (cache의 associativity와 관련하여)

fully associative로 설계된다.

- 변환 정보를 찾는 검색이 TLB 전체에서 병렬로 수행된다.
- 변환 정보가 TLB 내 어디든 위치할 수 있다.

### TLB 각 항목의 구성은?

VPN, PFN, 기타 다른 비트들(valid bit, protection bit, ASID 등)

### 페이지 테이블의 valid bit와 TLB의 valid bit 간 차이점은?

페이지 테이블 valid bit

- PTE의 valid bit가 "무효" 표시 → 해당 페이지가 프로세스에 할당되지 않았음을 의미.

TLB valid bit

- TLB에 탑재된 해당 변환 정보가 유효한지를 표시.
- 최초 시스템이 시작할 때, 또는 context switching이 발생할 때 valid bit를 "무효"로 표시함으로써 이전 context 정보를 사용하는 것을 방지한다.

### TLB에는 여러 VPN이 공존할 수 있다. 하지만 그럴 경우 여러 프로세스 간 VPN을 구분할 수 없다. 이에 대한 방안은?

1. context switching 때마다 TLB의 내용을 지운다. (= valid bit를 0으로 설정한다.)

> - page table base register의 값이 변경될 때가 TLB의 내용을 지워야 하는 타이밍이 된다.
> - OS는 하드웨어 특권 명령어를 통해 TLB의 내용을 지울 수 있다.
>
> 단점
>
> - TLB miss rate가 증가한다.
> - context switching이 빈번하게 발생 시 성능에 큰 부담을 준다.

2. TLB에 ASID(Address Space Identifier, 주소 공간 식별자) 필드를 추가한다.

- TLB 변환 정보를 프로세스 별로 구분할 수 있다.

> - context switching 시 운영체제는 새로운 프로세스의 ASID 값을 특정 레지스터에 탑재한다.

### 캐시 교체 정책에는 어떤 것들이 있나?

- LRU
- Random

### LRU란?

가장 오랫동안 사용되지 않은 항목을 교체하는 정책.

### Random 정책이란? 장단점은?

교체 대상을 무작위로 결정한다.

장점

- 구현이 간단하다.
- 예상치 못한 예외 상황의 발생을 피할 수 있다. 이를테면 TLB coverage를 벗어나는 경우 등을 방지할 수 있다.

단점

- 때때로 잘못된 결정을 내릴 수 있다.

### TLB coverage를 벗어난다는 것의 의미는?

프로그램이 짧은 시간동안 접근하는 페이지들의 수가 TLB에 들어갈 수 있는 수보다 많은 경우, 그 프로그램은 TLB 미스를 많이 발생시키게 되고 느리게 동작한다.

## 스와핑(Swapping)

### 스와핑이란?

디스크와 메모리 사이에서 swap-in, swap-out을 통해 메모리 가상화를 지원하는 방법.

### swap in과 swap out에 대해 설명?

- swap in: 스왑 공간의 페이지를 읽어 메모리에 탑재시키는 것.
- swap out: 메모리의 페이지를 읽어 스왑 공간에 쓰는 것.

> - 스왑 공간(swap space): 디스크에 페이지를 저장할 수 있는 일정 공간
>
> - 시스템이 사용할 수 있는 메모리의 크기는 스왑 공간의 크기가 결정한다.
> - 스왑 공간에만 스왑을 할 수 있는 것은 아니다. 물리 메모리에 추가 공간을 확보해야 할 때, 코드 영역의 페이지들이 차지하는 물리 페이지는 즉시 다른 페이지가 사용할 수 있다. (코드가 저장되어 있는 파일 시스템 영역이 스왑 공간으로 사용되는 셈이다. 해당 페이지는 디스크에 원본이 있으므로, 언제든지 다시 swap in이 가능하다.)

### page fault란?

물리 메모리에 존재하지 않는(디스크에 존재하는) 페이지에 접근할 때 발생하는 예외.

> - 페이지 테이블의 PTE의 present bit가 0인 경우이다.
> - page fault는 운영체제의 page fault handler가 처리한다.

### 스와핑이 지원되는 상황에서 메모리가 참조되는 과정을 설명?

- (프로세스가 가상 메모리를 참조한다.)
- 하드웨어는 가상 주소를 물리 주소로 변환하기 위해 VPN 추출 후 TLB를 참조한다.
  - TLB hit: 물리 주소를 얻은 후 메모리로 가져온다. (끝)
- TLB miss → 하드웨어는 page table base register로 페이지 테이블의 위치를 파악 후, VPN으로 PTE를 추출한다.
  - PTE가 유효하고(valid bit가 1이고), 해당 페이지가 물리 메모리에 존재하면(present bit가 1이면), 하드웨어는 PTE로부터 PFN을 추출해 TLB에 탑재한다. 그리고 명령어를 재실행한다. (끝)
- Page fault → 운영체제로 제어권이 넘어가 운영 체제의 page fault handler가 실행된다.

### 운영체제가 Page fault를 처리하는 과정은?

(page fault가 발생하면 하드웨어는 예외를 발생시킨 후 운영체제로 제어권을 넘긴다.)

- 운영체제는 해당 페이지를 메모리로 swap in 해온다.
- swap in(디스크 I/O)이 완료되면, 해당 PTE의 PFN 값을 물리 메모리에 탑재된 페이지의 위치로 갱신한다.
- page fault가 발생한 명령어를 재실행한다.

> - page fault가 난 페이지의 디스크 상 위치는 페이지 테이블에 저장되어 있다.
> - 명령어 재실행으로 인해 TLB 미스가 발생하면, TLB 미스 핸들러를 실행시킨다. (이를 방지하기 위해 page fault를 처리할 때 TLB도 같이 갱신하도록 할 수 있다.)
>
> - 디스크 I/O 중에는 해당 프로세스가 blocked 상태가 된다. 이때 운영체제는 다른 프로세스들을 실행할 수 있다.

### 운영체제가 페이지 교체(스왑) 알고리즘을 작동시키는 시기는?

운영체제는 물리 메모리 상 여유 공간에 최댓값(high watermark)과 최솟값(low watermark)을 설정해 교체 알고리즘을 작동시킨다.

### 페이지 교체(스왑) 알고리즘이 작동될 때(즉, 여유 공간이 최솟값보다 적어질 때) 일어나는 일은?

- 운영체제가 스왑 데몬을 작동시킨다.
- 스왑 데몬은 여유 공간의 크기가 최댓값에 이를 때까지 페이지를 제거한다.

> - 스왑 데몬(swap daemon, page daemon) : 메모리 여유 공간 확보를 담당하는 백그라운드 스레드.

## Blocking/Non-Blocking & Synchronous/Asynchronous

### Blocking과 Non-Blocking의 차이점?

함수 호출 시, 제어권을 리턴하는지 유무에 차이가 있다.

A가 B를 호출했다고 가정하자.

- B가 자신의 작업을 모두 완료한 후, A에게 제어권을 넘겨주는 것이 Blocking이다.
- B가 바로 제어권을 A에게 넘겨, A가 다른 일을 할 수 있도록 하는 것이 Non-Blocking이다.

### Synchronous와 Asynchronous의 차이점?

함수 호출 시, 작업 완료 여부를 신경쓰는지 여부에 차이가 있다.

A가 B를 호출했다고 가정하자.
추가적으로, A는 B에게 요청한 작업 b가 끝나면 C(: callback) 작업을 수행하기를 요구했다.

- A가 B의 작업 b가 완료되었는지 여부를 지속적으로 체크하는 것이 Sync이다.
- A가 B의 작업 b가 완료되었는지 여부를 신경쓰지 않는 것이 Async이다.

### Blocking + Sync ?

B는 자신의 작업이 완료될 때까지 제어권을 반환하지 않고, A는 B의 b 작업 완료 여부를 지속적으로 체크한다.

### Non-Blocking + Async ?

B는 제어권을 바로 반환하고, A는 B의 b 작업 완료 여부를 신경쓰지 않는다.

### Non-Blocking + Sync ?

B는 제어권을 바로 반환하고, A는 B의 작업 b의 작업 완료 여부를 계속 체크하는 것이다.

즉, A는 다른 일을 계속 할 수 있고, 그 와중에 B의 b 작업 완료 여부를 계속 체크하는 일을 하게 된다.

### Blocking + Async ?

B가 제어권을 바로 반환하지 않고, A는 B의 b 작업 완료 여부를 신경쓰지 않는 것이다.

> Blocking + Async는, 어차피 제어권이 없고 대기하는 입장이기 때문에 Blocking + Sync와 별 다른 차이가 없다. 그리고 Blocking + Sync는 별 이점이 없어 잘 사용되지 않는다.
>
> 그러나, 의도치 않게 Blocking + Async로 동작하는 경우가 있다. (Blocking + Sync를 원했으나 실제로는 Blocking + Async로 동작하는 것이다)
>
> 그 대표적인 케이스가 Node.js + MySQL 조합이다.
> Node.js 쪽에서 Async로 MySQL과 통신을 요청하지만,
> MySQL에서 제공하는 드라이버는 Blocking 방식으로 동작한다.

## Reference

- [Operating System(운영체제) / KOREATECH Prof. Duksu Kim](https://www.youtube.com/playlist?list=PLBrGAFAIyf5rby7QylRc6JxU5lzQ9c4tN)
- [OSTEP(Operating Systems: Three Easy Pieces)](https://github.com/remzi-arpacidusseau/ostep-translations/tree/master/korean)