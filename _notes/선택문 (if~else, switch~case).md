
선택문의 **특징**은 조건에 따라 맞으면 실행하고, 그렇지 않으면 지나갑니다.


## if~else 먼저 살펴봅시다

```C++
if (condition) { 
	// write your own code when the condition is satisfied 
	// 조건에 맞을 때 실핼할 코드를 쓰세요
	std::cout << “It is true!!\n”; 
}
```

condition에 알맞으면 아래 "It is true"가 실행되는 코드입니다.

만약에 실행할 내용이 둘 이상이라면, 복합 명령문으로 코드를 짜야합니다.
If the action is more than one, you must put your actions 
in a ==**compound statement**== to execute sequentially

예시)
```C++
if (condition) {
	std::cout << “It is true!!\n”; 
} else {
	std::cout << “It is false…\n”; 
}
```
condition에 만족하면 "It is true!!"가 출력이되고
만족하지 않으면 지나가고 바로 "It is false..."가 출력되게 됩니다.


## 이번엔 switch~case를 살펴봅시다

```C++
switch (expression) { 
	case alter_1 : statement_1; 
		break;
	case alter_2 : statement_2;
		break;
		 ... 
		 
	default statement_d; 
	break; 
}
```

가장 큰 특징은 expression에는 무조건 단일 값이고, 유형은 int 또는 char만 가능합니다.
Expression is a single value and the type can be either int or char

각 case 뒤에 세미클론(;)까지 단일 값이 될 수 있는 값을 써주면 
switch의 expression의 값이 각 case 값일 때 각각 break; 부분까지 코드를 실행합니다.

![[Pasted image 20230920133036.png]]

알맞는게 없으면 default: 부분의 내용을 break;까지 실행하게 됩니다.

## switch~case는 언제 씀?

보다시피 switch~case는 if~else랑 똑같습니다.
다만 차이점은 더 눈에 잘 들어오고 조건문이 엄청 많아질수록 성능이 if~else보단 좋다고 합니다.
~~(어차피 엄청 큰 차이는 아니지만..)

그래서 조건문이 너무 많으면 switch~case로 코드를 정리하면 좋습니다.