# [2단계] if문

* 백준 알고리즘에서는 "**_클래스명_**"을 "**_Main_**"으로 해주어야 한다!

## 1. [1330번] 두 수 비교하기

### 문제
	두 정수 A와 B가 주어졌을 때, A와 B를 비교하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 A와 B가 주어진다. A와 B는 공백 한 칸으로 구분되어져 있다.

### 출력
	첫째 줄에 다음 세 가지 중 하나를 출력한다.
	
	* A가 B보다 큰 경우에는 '>'를 출력한다.
	* A가 B보다 작은 경우에는 '<'를 출력한다.
	* A와 B가 같은 경우에는 '=='를 출력한다.

### 제한 
	-10,000 ≤ A, B ≤ 10,000

### 예제 입력 1 
`1 2`
### 예제 출력 1
`<`

### 예제 입력 2 
`10 2`
### 예제 출력 2
`>`

### 예제 입력 3 
`5 5`
### 예제 출력 3
`==`



### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int A = in.nextInt();
			int B = in.nextInt();
			
			if(A>B)
				System.out.println(">");
			else if(A<B)
				System.out.println("<");
			else if(A == B)
				System.out.println("==");
			
			in.close();
		}
	}

		
## 2. [9498번] 시험 성적

### 문제
	시험 점수를 입력받아 90 ~ 100점은 A, 80 ~ 89점은 B, 70 ~ 79점은 C, 60 ~ 69점은 D, 나머지 점수는 F를 출력하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 시험 점수가 주어진다. 시험 점수는 0보다 크거나 같고, 100보다 작거나 같은 정수이다.

### 출력
	시험 성적을 출력한다.

### 예제 입력 1 
`100`

### 예제 출력 1 
`A`     



### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int score = in.nextInt();
			
			if(score>=90)
				System.out.println("A");
			else if(score>=80)
				System.out.println("B");
			else if(score>=70)
				System.out.println("C");
			else if(score>=60)
				System.out.println("D");
			else
				System.out.println("F");
			
			in.close();
		}
	}
	

## 3. [2753번] 윤년

### 문제
	연도가 주어졌을 때, 윤년이면 1, 아니면 0을 출력하는 프로그램을 작성하시오.
	
	윤년은 연도가 4의 배수이면서, 100의 배수가 아닐 때 또는 400의 배수일 때이다.
	
	예를 들어, 2012년은 4의 배수이면서 100의 배수가 아니라서 윤년이다. 1900년은 100의 배수이고 400의 배수는 아니기 때문에 윤년이 아니다. 하지만, 2000년은 400의 배수이기 때문에 윤년이다.

### 입력
	첫째 줄에 연도가 주어진다. 연도는 1보다 크거나 같고, 4000보다 작거나 같은 자연수이다.

### 출력
	첫째 줄에 윤년이면 1, 아니면 0을 출력한다.

### 예제 입력 1 
`2000`

### 예제 출력 1 
`1`

### 예제 입력 2 
`1999`

### 예제 출력 2 
`0`


* `&&` (논리곱) : 두 조건이 **모두 참**일때만 참을 반환     
* `||` (논리합) : 두 조건 중 **하나만 참**일 때도 참을 반환
  
### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int year = in.nextInt();
			
			if(year%4 == 0 && year%100 != 0)
				System.out.println("1");
			else if(year%400 == 0)
				System.out.println("1");
			else
				System.out.println("0");
			
			in.close();
		}
	}
	
## 4. [14681번] 사분면 고르기

### 문제
	흔한 수학 문제 중 하나는 주어진 점이 어느 사분면에 속하는지 알아내는 것이다. 사분면은 아래 그림처럼 1부터 4까지 번호를 갖는다. "Quadrant n"은 "제n사분면"이라는 뜻이다.
	
	
	
	예를 들어, 좌표가 (12, 5)인 점 A는 x좌표와 y좌표가 모두 양수이므로 제1사분면에 속한다. 점 B는 x좌표가 음수이고 y좌표가 양수이므로 제2사분면에 속한다.
	
	점의 좌표를 입력받아 그 점이 어느 사분면에 속하는지 알아내는 프로그램을 작성하시오. 단, x좌표와 y좌표는 모두 양수나 음수라고 가정한다.

### 입력
	첫 줄에는 정수 x가 주어진다. (−1000 ≤ x ≤ 1000; x ≠ 0) 다음 줄에는 정수 y가 주어진다. (−1000 ≤ y ≤ 1000; y ≠ 0)

### 출력
	점 (x, y)의 사분면 번호(1, 2, 3, 4 중 하나)를 출력한다.

### 예제 입력 1 
	12
	5

### 예제 출력 1 
	1

### 예제 입력 2 
	9
	-13

### 예제 출력 2 
	4

  
  
### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int x = in.nextInt();
			int y = in.nextInt();
			
			if(x > 0 && y > 0)
				System.out.println("1");
			else if(x < 0 && y > 0)
				System.out.println("2");
			else if(x < 0 && y < 0)
				System.out.println("3");
			else if(x > 0 && y < 0)
				System.out.println("4");
			
			in.close();
		}
	}
	
## 5. [2884번] 알람 시계

### 문제
	상근이는 매일 아침 알람을 듣고 일어난다. 알람을 듣고 바로 일어나면 다행이겠지만, 항상 조금만 더 자려는 마음 때문에 매일 학교를 지각하고 있다.
	
	상근이는 모든 방법을 동원해보았지만, 조금만 더 자려는 마음은 그 어떤 것도 없앨 수가 없었다.
	
	이런 상근이를 불쌍하게 보던, 창영이는 자신이 사용하는 방법을 추천해 주었다.
	
	바로 "45분 일찍 알람 설정하기"이다.
	
	이 방법은 단순하다. 원래 설정되어 있는 알람을 45분 앞서는 시간으로 바꾸는 것이다. 어차피 알람 소리를 들으면, 알람을 끄고 조금 더 잘 것이기 때문이다. 이 방법을 사용하면, 매일 아침 더 잤다는 기분을 느낄 수 있고, 학교도 지각하지 않게 된다.
	
	현재 상근이가 설정한 알람 시각이 주어졌을 때, 창영이의 방법을 사용한다면, 이를 언제로 고쳐야 하는지 구하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 두 정수 H와 M이 주어진다. (0 ≤ H ≤ 23, 0 ≤ M ≤ 59) 그리고 이것은 현재 상근이가 설정한 놓은 알람 시간 H시 M분을 의미한다.
	
	입력 시간은 24시간 표현을 사용한다. 24시간 표현에서 하루의 시작은 0:0(자정)이고, 끝은 23:59(다음날 자정 1분 전)이다. 시간을 나타낼 때, 불필요한 0은 사용하지 않는다.

### 출력
	첫째 줄에 상근이가 창영이의 방법을 사용할 때, 설정해야 하는 알람 시간을 출력한다. (입력과 같은 형태로 출력하면 된다.)

### 예제 입력 1 
	10 10

### 예제 출력 1 
	9 25

### 예제 입력 2 
	0 30

### 예제 출력 2
	23 45
	
### 예제 입력 3 
	23 40

### 예제 출력 3
	22 55
	
  
  
### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int H = in.nextInt();
			int M = in.nextInt();
			
			if(M>=45)
				
				System.out.printf("%d %d", H, M-45);
			else if(M<45 && H == 0)
				System.out.printf("23 %d", 60-(45-M));
			else if(M<45 && H != 0)
				System.out.printf("%d %d", H-1, 60-(45-M));
			
			in.close();
		}
	}
