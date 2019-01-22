## 자원을 직접 명시하지 말고, 의존 객체 주입을 사용하라.

---

### 요약
`클래스가 내부적으로 하나 이상의 자원에 의존하고, 그 자원이 클래스 동작에 영향을 준다면
싱글턴과 정적 유틸리티 클래스는 사용하지 않는 것이 좋다. 이 자원들을 클래스가 직접
만들게 해서도 안된다. 대신 필요한 자원을 생성자에 넘겨주자. 의존성 주입 기법은 클래스의 
유연성, 재사용성, 테스트 용이성을 기막히게 개선해 준다.`

---

```java
public class Dog {
    private final Drees drees;
    
    public Dog(Drees drees){
        this.drees = drees;
    }
}
```