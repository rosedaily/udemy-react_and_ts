🌼 섹션 1 : 시작하기
- 웹사이트는 버튼을 클릭하면 요청을 서버에 전송 - 새로운 html 페이지를 브라우저로 보냄 - 화면에 보여줌. 새로운 html이 로딩되는 동안 기다릴 수 밖에 없음.
- 브라우저에서 js는 dom을 조작해서 이를 통해 html요소가 화면에 랜더링 된다.
- 리액트 : 클라이언트 사이드의 js 라이브러리
- 리액트가 필요한 이유
  - 하나의 작업에 필요한 코드수가 줄어들고 동작 등을 코드를 통해 명확하게 알 수 있다.
- SPAs : Single-Page-Application. 단일 페이지 애플리케이션

- 컴포넌트 기반의 UI 라이브러리. 컴포넌트에 중점을 둠.
- 컴포넌트에만 초점을 맞추고 있어, 내장된 기능이 많지 않아 라우터 등 서드파티 라이브러리는 추가로 설치 해야 함. 
- 앵귤러 역시 컴포넌트 기반이지만, 내장된 기능이 많고, 처음부터 타입스크립트를 수용함. 기능이 많아 작은 프로젝트에는 부적합.
- 뷰는 앵귤러와 리액트를 합친것 같은 느낌. 기능이 많지만, 앵귤러보단 적고, 리액트보다는 많음. 라우팅 같은 핵심기능 포함. 커뮤니티 의존성은 낮지만, 앵귤러만큼 과부화되지는 않음.


- 첫번째 섹션 : 리액트에 대한 기본적인 것들. 리액트에서의 핵심기능. 어떤 것들을 만들건간에 배워야 함.
  - 사용자 인터페이스 구축이 목표.
  - 컴포넌트. 구축, 결합, 접근방식으로 인터페이스 구축
  - 이벤트와 데이터를 다루는 방법. 버튼을 클릭 했을 때의 동작, 화면 내용 변경. props(속성)와 state(상태)
  - 리액트의 앱과 컴포넌트 스타일링, 사용자 인터페이스를 리액트로 구축하는 방법
  - 리액트 훅 
- 두번째 섹션 : 고급주제. 심화기능. 실제 앱에 필요한 기능등.
  - 부수 효과와 Refs, 더 많은 리액트 훅으로 작업하는 것에 대한 섹션 포함.
  - 리액트의 context API와 리덕스로 앱의 상태관리
  - 리덕스 : 중요한 서드파티 라이브러리. 
  - 폼에서 사용자 입력을 처리하는 방법, 백그라운드에서 http 요청을 전송해서 db에 저장하거나 불러오는 방법.
  - 훅을 만드는 방법과 정의
  - 라우팅을 구현하는 방법과 라우팅이 무엇인지. 
  - 싱글페이지 앱이지만, 여러 페이지인 것 같게.
  - 리액트 앱 배포방법. next.js(프로덕션 레디 리액트앱을 쉽게 구축하도록 도와줌)
- 개념 정리 등.
  - 자바스크립트 리프레시를 통해 js를 제대로 이해했는지 확인. 
  - 리액트 요약.


- 강의를 수강하는 두가지 방법.
  - 1. 전체를 차례로 수강. 나중에 리액트 요약을 봄
  - 2. 전체과정을 건너뛰고 리액트 요약을 먼저 본 뒤 전체 강의를 다시 수강.


- 반복해서 듣기, 속도 조절하며 듣기. 
- 코딩해보고 연습. 같이 해보기 전에 스스로 해보기. 잠시 멈춰서 작성해보기.
- 오류를 만났을 때 스스로 해답을 찾아야 함. 모듈 마지막에 첨부된 코드를 사용해서 비교해보고 스스로 해결하는 능력을 가져야 함.

🌼 섹션 2 : 자바스크립트 새로고침
- 🌱 12. let, const
- let : 값을 수정할 수 있는 변수
- const : 값을 수정할 수 없는 상수. 

- 🌱 12. 화살표 함수 
  - 예 : const myFunc = () => {}
  - this로 인해 발생했던 많은 이슈를 해결해주는 장점을 가짐.
  - 기존에 원하는 객체를 참조하지 않았던 this를 정의한 객체를 나타내고, 실행 중 갑자기 변경되지 않음.

  - 인수가 한개인 경우 ()생략 가능. return만 있는 짧은 구문은 중괄호와 return을 생략해서 작성
    - 예 : const myFunc = (number) => { return number; };
          const myFunc = number => number;

- 🌱 13. Export, Import
  - 기본으로 내보낸 단일 값 가져오기
    - export default a; 
    - import 원하는 명칭 from "가져올 파일"
    - 내보낸 값은 1개이기에 가져올땐 임의의 원하는 명칭으로 가져올 수 있음
  - 다중 값 가져오기
    - named export. 이름을 정확히 입력해서 가져와야 함.
    - export a; export b; 
    - import {a} from "가져올 파일";  import {b} from "가져올 파일"; 
    - import {a, b} from "가져올 파일" 처럼 여러개를 한번에 가져오기 가능.
    - import {a as aaa} from "가져올 파일"; 처럼 명칭 변경가능
    - import * as bundled from "가져올 파일"; 로 한번에 가져오기 가능. 모든 상수로 된 자바스크립트 객체가 됨. bundled.명칭 의 형태로 사용.

- 🌱 14. 클래스 이해하기
  - classes : 객체를 위한 청사진 같은 것.
  - 사용 예 
    class Person { 
      name='Max'         //프로퍼티. 클래스에 정의한 변수.
      call = () => {...} //메소드. 클래스에 정의한 함수.
    }
  - new Person() 과 같은 식으로 인스턴스 생성.
  - 상속 가능. 다른 클래스의 프로메터와 메소드를 상속하면 새로운 프로퍼티와 메소드를 추가
    - class Person extends Master
    - 사용 예 
      class Human {
        constructor(){ //생성자 함수. 이 명칭은 고정. 클래스의 객체를 생성할 때마다 실행.
          this.gender = 'male'; //this키워드로 프로퍼티 설정.
        } 
        printGernder(){
          console.log(this.gender);
        }
      }
      class Person extends Human { //master를 상속 받음
        constructor(){
          super(); //상위클래스(master)의 생성자 함수를 실행해서 초기화
          this.name = 'rose';
          this.gender = 'female'; //Human클래스의 printGernder를 호출했지만, Person 클래스에서 확장되어서 변경 가능.
        } 
        aa(){  //메소드 생성. 생성자 함수에서 생성한 걸 가져올 수 있음.
          console.log(this.name);
        }
      }

      const person = new Person();
      person.aa();
      person.printGernder를(); //예로 상위인 Human에 printGernder를 있다면 이런식으로 불러오기도 가능. 

- 🌱 15. 클래스 속성 및 메서드
  - 프로퍼티 : 클래스와 객체에 추가되는 변수같은 것.
  - 메소드 : 클래스와 객체에 추가되는 함수같은 것.
  - this구문 : 프로퍼티와 생성자 함수 설정.
  - es7 에서는 클래스에 바로 프로퍼티 할당가능. 예. myProperty = 'value' 따로 생성자 함수를 호출하지 않아도 됨.
  - 메서드 생성시에도 es7에서는 화살표 함수형태로 사용. myMethod = () => {...} this 키워드를 사용하지 않아도 됨.(사용하는 이유)
    -ES7 클래스 구문 예.
      class Human {
        gender = 'male'; //생성자와 this키워드 없이 프로퍼티 설정.

        printGernder(){
          console.log(this.gender);
        }
      }

      class Person extends Human {
        constructor(){
          //super(); //상위 생성자 함수 초기화도 불필요.
          name = 'rose';
          gender = 'female'; //this없이 상위클래스도 할당 가능.
        } 
        aa = () => { //화살표함수로 변경. 
          console.log(this.name);
        }
      }

      const person = new Person();
      person.aa();
      person.printGernder를(); //예로 상위인 Human에 printGernder를 있다면 이런식으로 불러오기도 가능. 


- 🌱 16. 스프레드 및 나머지 연산자
  - ... 어디서 사용하는지에 따라 스프레드 or 레스트라고 불림
    - Spread : 스프레드 연산자. 배열의 원소나 객체의 프로퍼티를 나누는데 사용. 배열이나 객체를 펼쳐놓음.
      const newArray = [...oldArray, 1,2] //oldArray의 모든 원소들을 새로운 배열에 추가 후 1,2를 더 추가. 
      const newObject= {...oldObject, newProp:5} //oldObject의 모든 프로퍼티와 값을 꺼내서 새 객체의 키 값으로 추가.oldObject에 newProp를 추가. 갖고 있는 프로퍼티가 우선권을 갖음. 만약 newProp와 동일한 명칭이 존재하면 값이 새로 변경 됨.

    - Rest : 함수의 인수목록을 배열로 합치는데 사용.
      function sortArgs(...args){ //매개변수를 무제한으로 받음. 1개 이상 매개변수를 가질 때.
        return args.sort()  
      }
      매개변수 목록에 배열 메소드를 적용하거나, 원하는 방법으로 매개변수를 저장 가능.

- 🌱 17. 구조분해할당(Destructuring)
  - 배열의 원소나 객체의 프로퍼티를 하나만 추출해서 변수에 저장
    배열 : [a,b,c]=['hello','rose','11'] // a에는 hello, b에는 rose이런식으로 각각 할당. 만약 이중 rose를 제외하고 쓰고 싶다면 [a,,c]이렇게 선언없이 공백으로 사용.
    객체 : {name,age,aa}={name:'rose', age:28, aa:11} //객체명과 동일하게 맞춰줘야하고, 이중 age를 제외하고 쓰고 싶다면{name,aa} 이렇게 써도 됨. 이름으로 가져오기 때문.

- 🌱 18. 참조형 및 원시형 데이터 타입
  - 객체와 배열은 참조형 자료 타입. 
  - 재할당 한다는 것은 값이 아닌 포인터를 복사하는 것이기에 진짜 복사는 new객체에 전체 객체 복사가 아닌, 프로퍼티를 복사해야 함.
  - 객체를 새로운 객체로 가져온 뒤 기존 객체를 변경하면, 새로운 객체는 포인터만 복사해서 메모리의 동일한 객체를 보기 때문에 같이 변경된다.
  - 이렇게 되면 같은 객체를 변경하기에 실수가 발생될 수 있어 변경할 수 없는 방법으로 복사를 해야함. 즉, 포인터가 아닌 객체를 복사해야함.
  - 스프레드 연산자를 사용해서 객체의 프로퍼티와 값을 가져와서 새로운 객체로 생성해줄 수 있다.
    const a = { ...b }; b의 값을 새로운 a객체로 생성

- 🌱 19. Array functions
  - map() : 내장된 배열 메소드. 예전 값을 새 값으로 반환 

    const nums = [1,2,3];
    const dobleNumArray = nums.map((num) => { //nums의 값을 num이라는 매개변수명으로 받음
      return num *2;  //nums의 값들을 각각 받아서 *2를 해줌.
    })

- 🌱 20. 마무리
  - map()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
    find()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find
    findIndex()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex
    filter()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
    reduce()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce?v=b
    concat()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat?v=b
    slice()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice
    splice()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice