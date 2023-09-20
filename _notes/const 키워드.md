
Constant - A situation or state of affairs that does not change
한마디로 Constant 변수는 변하지 않는 변수입니다.

##### 변수 선언에 const 키워드를 추가하면?

값을 변경할 수 없음을 컴파일러에 알릴 수 있습니다.

ex)
```C++
const double factor = 5.0/9.0; // 0.555556

const double offset = 32.0; 

celcius = (fahr - offset)*factor; // -17.7778
```

위와 같은 방식으로 const를 선언 하면 factor과 offset은 고정된 값이 됩니다.
소소한 팁으론 const로 선언하면서 연산한 결과 값을 바로 할당하는 것도 가능함.


##### const를 왜 쓰는건가요? 

컴파일러가 더 성능이 좋은 실행 파일을 생성하는 데 도움이 될 수 있습니다.
그리고 용도에 맞는 변수를 선언함으로써 코드 퀄리티를 좀 더 올릴 수 있습니다. 