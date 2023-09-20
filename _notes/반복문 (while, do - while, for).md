
반복문(Repetition)의 특징은 조건에 만족하지 않을 때 까지 계속
Repeat the action until the condition is not satisfied


## while 먼저 살펴봅시다

```C++
// Calculate the sum of 1 through n int n, sum = 0;
std::cin >> n; // n을 입력받습니다.

while (n > 0) // n이 0 이하가 될 때까지(조건문에 만족 안할 때까지) 계속 반복합니다.
{
  sum += n; // sum에 n을 더합니다. 2번째 반복부턴 n이 더 줄어들 것이니 
  n--; // n = n - 1과 같은 말로 n의 값을 1 줄여줍니다. 

  // 다시 while 문 내의 내용을 반복합니다.
  // n은 0이하가 될 때까지 반복해서 줄여집니다.
}
```
while(condition){} 으로 while문의 조건에 맞으면 아래 내용을 실행하게 됩니다.

모든 반복문이 다 그렇지만 특히나 while문은 ==**무한반복**== 에러가 나지않도록
조건문을 잘 설정해야만 합니다.

## do - while을 살펴봅시다

```C++
do{
	std::cout<< "do while 반복" <<std::endl; //일단 한번 실행
}
while (n > 0); //조건에 맞으면 do 문의 내용을 한번 더 실행
```

일단 do 문 {} 아래 내용을 다 실행을 합니다.
모든 do 문의 내용을 다 실행한 후 while문을 실행해서 조건에 맞으면 do문을 반복합니다. 

일반 while문과 마찬가지로 조건을 잘못 설정하면 ==**무한반복**== 할 수 있으니 조심하세요.


## 마지막 for문을 살펴봅시다

```C++
for (initialization; condition; update)
{
	std::cout << “Action”;
}
```
각각 끊어서 봅시다
initialization : 초기값을 설정하는 부분
condition : 조건문이 될 부분
update : 한번 반복 후 실행할 부분

따라서 initialization에서 반복할 횟수를 관리해줄 변수를 선언합니다.
	Initialize the variable that uses in condition

그리고 condition에서 조건이 맞는지 검사합니다.
Check that condition is satisfied. 
	The compound statement runs as long as the condition is “true

condition에 맞다면 실행을 하고 한번 실행 후엔 update 부분에 있는 내용을 실행합니다.
보통은 그냥 반복 횟수 변수를 증가/감소 시킵니다.
	Update the variable used in condition

## 반복을 제어할 키워드들

#### break;
우선 break; 키워드가 있습니다.
반복문에서 코드 실행중 break;를 만나면 그 즉시 반복문을 종료하고 탈출합니다.

예시)
``` C++
while (1) {
	sum += n;
	n--;
	if (n <= 0) 
		break; 
}
```
#### continue;
continue; 키워드는 종료하고 탈출하는 대신 다음 반복으로 넘어갑니다.
즉, 반복문에서 실행중에 continue 만나게 되면 continue 밑 부분은 생략하고 다음 반복으로 넘어갑니다.

예시)
```C++
while (n > 0) { 
	if ((n % 2) == 0) continue; 
	sum += n; 
}
```


