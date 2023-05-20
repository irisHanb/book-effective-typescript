# 타입 단언 보다는 타입 선언을 사용하기

- 타입선언을 사용해야한다. 
  - 타입단언은 타입을 강제하는것으로 타입체커를 무시하게 된다.
  - 화살표 함수에서도 마찬가지이다. 
    ```ts
    interface Person {
      name: string
    }
    const people: Person[] = ['alice', 'bob', 'jan'].map(
      (name: Person) => ({name})
    )
    ```
- 타입단언이 꼭 필요한 경우는 타입스크립트보다 타입정보를 잘 알고 있는 상황이다.
  - DOM element 에 대한 판단, null 등
