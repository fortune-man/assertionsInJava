
>
assert      : 절대로 일어나서는 안될일 
exception : 일어날 법한 일

## Reference
[when-to-use-an-assertion-and-when-to-use-an-exception](https://stackoverflow.com/questions/1957645/when-to-use-an-assertion-and-when-to-use-an-exception)
[exception-vs-assertion](https://stackoverflow.com/questions/1276308/exception-vs-assertion)
[assertions](https://www.geeksforgeeks.org/assertions-in-java/)
---

## Assert vs Exception

오류를 방지하기 위해 단위 테스트 시 사용되는 assertion과
예외 작업 처리에 사용되는 exception의 차이는 뭘까?

### 주요 차이점 
- Assertion : 버그라고도 불리는 프로그래밍 오류를 감지하는 수단으로만 사용
  - 코드 내의 내부 논리 검사
  - on / off 가능하다고 함
- 다른 종류의 오류 또는 "예외적인" 조건을 나타는게 가능
예) 잘못된 사용자 입력, 누락된 파일, 힙 전체 ..
  - 즉각적인 코드가 통제할 수 없는 오류 조건에 대처
  - 




|Excepton|Assrtion|
|:----:|:----:|
|공용 또는 보호된 메서드와 생성자에게 전달된 매개 변수를 확인할 때  사용|자신이나 개발자 팀에 피드백을 제공하기 위해 사용|
|사용자와 상호 작용하거나 클라이언트 코드가 예외적인 상황에서 복구될 것으로 예상할 때 사용|일어날 것 같지 않은 일을 확인할 때 주장을 사용( 그렇지 않으면 애플리케이션에 심각한 결함이 있다는 것을 의미)|
|발생할 수 있는 문제를 해결하기 위해 사용|사전 조건, 사후 조건 및 개인/내부 코드의 불변성을 확인할 때 사용|
-|사실이라고 알고 있는 것을 진술하기 위해 사용 |


---

## Assertion이 사용되는 이유?

주로 논리적으로 불가능한 상황을 확인하는 데 사용된다. 
예를 들어, 코드가 실행되기 전에 기대하는 상태나 실행이 끝난 후 상태를 확인하는 데 사용할 수 있다고 한다. 
일반적인 예외/오류 처리와 달리, assertion은 일반적으로 런타임에 비활성화된다.

즉, 프로그램에서 만들어진 가정의 정확성을 테스트할 수 있게 해준다. 
assertion 자바의 assert 문을 사용하여 달성된다. 
assertion을 실행하는 동안, 그것은 사실로 여겨지며
실패 시 JVM이 AssertionError라는 오류를 발생시킨다. 
주로 개발 중에 테스트 목적으로 사용된다.

Assert 문은 부울 표현식과 함께 사용되며 두 가지 방법으로 작성할 수 있습니다.


