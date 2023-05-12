# 구조적 타이핑에 익숙해지기

- 구조적 타이핑: 오직 멤버만으로 타입을 관계시키는 방식
- 타입스크립트는 구조적 타이핑을 모델링하므로 가끔 당황스러운 결과가 발생하기도 한다. 
  - 타입이 열려있으므로 객체를 순회시 타입을 특정할 수 없다. -> 모든 속성에 대해 계산되어지는 구현방법이 더 낮다. 
  - 클래스와 관련된 할당문에서도 특이한 결과를 볼 수 있다.
  ```ts
  class C {
    foo: string; 
    constructor(foo: string){
      this.foo = foo;
    }
  }
  const c = new C('instance of C');
  const d: C = {foot: 'object literal'}; // 정상 // constructor, foo 존재하기에 정상
  ``
- 유닛 테스트에도 유리하다. 
