# [3단계] for문

* 백준 알고리즘에서는 "**_클래스명_**"을 "**_Main_**"으로 해주어야 한다!
* "**BufferedReader**", "**BufferedWriter**", 그리고 "**StringTokenize**"에 대한 자세한 내용은 따로 정리해서 업로드 할 예정!

## 1. [1330번] 두 수 비교하기

### 문제
	N을 입력받은 뒤, 구구단 N단을 출력하는 프로그램을 작성하시오. 출력 형식에 맞춰서 출력하면 된다.

### 입력
	첫째 줄에 N이 주어진다. N은 1보다 크거나 같고, 9보다 작거나 같다.

### 출력
	출력형식과 같게 N*1부터 N*9까지 출력한다.

### 예제 입력 1 
`2`
### 예제 출력 1
	2 * 1 = 2
	2 * 2 = 4
	2 * 3 = 6
	2 * 4 = 8
	2 * 5 = 10
	2 * 6 = 12
	2 * 7 = 14
	2 * 8 = 16
	2 * 9 = 18



### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int N = in.nextInt();
			
			for(int i = 0; i < 9; i++)
			{
				System.out.println(N + " * " + (i+1) + " = " + (N*(i+1)));
				//System.out.printf("%d * %d = %d\n",N,(i+1), N*(i+1));도 가능!
			}
			
			in.close();
		}
	}

* `printf`와 `println` 중 문제에서 더 쉽게 쓰일 수 있는 걸 골라 쓰면 된다.
		
## 2. [10950번] A + B - 3

### 문제
	두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 테스트 케이스의 개수 T가 주어진다.
	
	각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

### 출력
	각 테스트 케이스마다 A+B를 출력한다.

### 예제 입력 1 
	5
	1 1
	2 3
	3 4
	9 8
	5 2

### 예제 출력 1 
	2
	5
	7
	17
	7    


### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int T = in.nextInt();
			
			for(int i = 0; i < T; i++)
			{
				int A = in.nextInt();
				int B = in.nextInt();
				System.out.println((A+B));
			}
			
			in.close();
		}
	}
	

## 3. [8393번] 합

### 문제
	n이 주어졌을 때, 1부터 n까지 합을 구하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 n (1 ≤ n ≤ 10,000)이 주어진다.

### 출력
	1부터 n까지 합을 출력한다.

### 예제 입력 1 
`3`

### 예제 출력 1 
`6`

  
### 내 제출 코드 
	import java.util.Scanner;
	
	public class Main {
		public static void main(String[] args) {
			
			Scanner in = new Scanner(System.in);
			int n = in.nextInt();
			int sum = 0;
			
			for(int i = 0; i < n; i++)
			{
				sum += (i+1);
			}
			
			System.out.println(sum);
			in.close();
		}
	}	
	
## 4. [15552번] 빠른 A + B

### 문제
	본격적으로 for문 문제를 풀기 전에 주의해야 할 점이 있다. 입출력 방식이 느리면 여러 줄을 입력받거나 출력할 때 시간초과가 날 수 있다는 점이다.
	
	C++을 사용하고 있고 cin/cout을 사용하고자 한다면, cin.tie(NULL)과 sync_with_stdio(false)를 둘 다 적용해 주고, endl 대신 개행문자(\n)를 쓰자. 단, 이렇게 하면 더 이상 scanf/printf/puts/getchar/putchar 등 C의 입출력 방식을 사용하면 안 된다.
	
	Java를 사용하고 있다면, Scanner와 System.out.println 대신 BufferedReader와 BufferedWriter를 사용할 수 있다. BufferedWriter.flush는 맨 마지막에 한 번만 하면 된다.
	
	Python을 사용하고 있다면, input 대신 sys.stdin.readline을 사용할 수 있다. 단, 이때는 맨 끝의 개행문자까지 같이 입력받기 때문에 문자열을 저장하고 싶을 경우 .rstrip()을 추가로 해 주는 것이 좋다.
	
	또한 입력과 출력 스트림은 별개이므로, 테스트케이스를 전부 입력받아서 저장한 뒤 전부 출력할 필요는 없다. 테스트케이스를 하나 받은 뒤 하나 출력해도 된다.

### 입력
	첫 줄에 테스트케이스의 개수 T가 주어진다. T는 최대 1,000,000이다. 다음 T줄에는 각각 두 정수 A와 B가 주어진다. A와 B는 1 이상, 1,000 이하이다.

### 출력
	각 테스트케이스마다 A+B를 한 줄에 하나씩 순서대로 출력한다.

### 예제 입력 1 
	5
	1 1
	12 34
	5 500
	40 60
	1000 1000

### 예제 출력 1 
	2
	46
	505
	100
	2000
  
  
### 내 제출 코드 
	import java.io.BufferedReader;
	import java.io.BufferedWriter;
	import java.io.IOException;
	import java.io.InputStreamReader;
	import java.io.OutputStreamWriter;
	import java.util.StringTokenizer;
	 
	public class Main {
	 
		public static void main(String[] args) throws IOException {
	 
			//BufferedReader와 BufferedWriter 선언 
			BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
			BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
	 
			//String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
			int T = Integer.parseInt(br.readLine());
	        
			StringTokenizer st;
	 
			for (int i = 0; i < T; i++) {
				//테스트 케이스에서 주어지는 두 정수는 문자열 분리를 위해 매 반복마다 StringTokenizer 생성과 동시에 문자를 입력받는다.
				//public StringTokenizer(String str, String delim) : 특정 delim으로 문자열을 분리한다.
				st = new StringTokenizer(br.readLine()," "); //한 줄씩 읽어와서(readline), 공백으로 문자열 분리("") 
				bw.write((Integer.parseInt(st.nextToken()) + Integer.parseInt(st.nextToken()))+ "\n");
			}
			br.close();
	        
			bw.flush();
			bw.close();
	 
		}
	}	
## 5. [2741번] N 찍기

### 문제
	자연수 N이 주어졌을 때, 1부터 N까지 한 줄에 하나씩 출력하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 100,000보다 작거나 같은 자연수 N이 주어진다.

### 출력
	첫째 줄부터 N번째 줄 까지 차례대로 출력한다.

### 예제 입력 1 
	5

### 예제 출력 1 
	1
	2
	3
	4
	5
  
  
### 내 제출 코드 

1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.IOException;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		 
		public class Main {
		 
			public static void main(String[] args) throws IOException {
		 
				//BufferedReader와 BufferedWriter 선언 
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		 
				//String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
				int N = Integer.parseInt(br.readLine());
		 
				for (int i = 1; i <= N; i++) {
					bw.write(i + "\n");
				}
				br.close();
		        
				bw.flush();
				bw.close();
		 
			}
		}
	
2. "**Scanner 사용**"

		import java.util.Scanner;
			
			public class Main {
				public static void main(String[] args) {
					
					Scanner in = new Scanner(System.in);
					int N = in.nextInt();
					
					for(int i = 1; i <=N; i++)
					{
						System.out.println(i);
						//System.out.printf("%d\n",i);도 가능!
					}
					
					in.close();
				}
			}
			
* ## 6. [2742번] 기찍 N

### 문제
	자연수 N이 주어졌을 때, N부터 1까지 한 줄에 하나씩 출력하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 100,000보다 작거나 같은 자연수 N이 주어진다.

### 출력
	첫째 줄부터 N번째 줄 까지 차례대로 출력한다.

### 예제 입력 1 
	5

### 예제 출력 1 
	5
	4
	3
	2
	1
  
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.IOException;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		 
		public class Main {
		 
			public static void main(String[] args) throws IOException {
		 
				//BufferedReader와 BufferedWriter 선언 
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		 
				//String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
				int N = Integer.parseInt(br.readLine());
		 
				for (int i = N; i >= 1; i--) {
					bw.write(i + "\n");
				}
				br.close();
		        
				bw.flush();
				bw.close();
		 
			}
		}
	
2. "**Scanner 사용**"

		import java.util.Scanner;
			
			public class Main {
				public static void main(String[] args) {
					
					Scanner in = new Scanner(System.in);
					int N = in.nextInt();
					
					for(int i = N; i >= 1; i--)
					{
						System.out.println(i);
						//System.out.printf("%d\n",i);도 가능!
					}
					
					in.close();
				}
			}
	
## 7. [11021번] A+B - 7

### 문제
	두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 테스트 케이스의 개수 T가 주어진다.
	
	각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

### 출력
	각 테스트 케이스마다 "Case #x: "를 출력한 다음, A+B를 출력한다. 테스트 케이스 번호는 1부터 시작한다.

### 예제 입력 1 
	5
	1 1
	2 3
	3 4
	9 8
	5 2

### 예제 출력 1 
	Case #1: 2
	Case #2: 5
	Case #3: 7
	Case #4: 17
	Case #5: 7
  
  
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.InputStreamReader;
		import java.util.StringTokenizer;
		import java.io.IOException;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
		 
				BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
				
				int T = Integer.parseInt(br.readLine());
				int A;
				int B;
		        
				StringTokenizer st;
				for (int i = 1; i <= T; i++) {
					st = new StringTokenizer(br.readLine()," ");
					A = Integer.parseInt(st.nextToken());
					B = Integer.parseInt(st.nextToken());
					System.out.println("Case #" + i + ": " + A + " + " + B + " = " + (A+B));
				}
				br.close();
			}
		 
		}	
		
2. "**Scanner 사용**"

		import java.util.Scanner;
		
		public class Main {
			public static void main(String[] args) {
				
				Scanner in = new Scanner(System.in);
				int T = in.nextInt();
				
				for(int i = 1; i <= T; i++)
				{
					int A = in.nextInt();
					int B = in.nextInt();
					System.out.println("Case #" + i +": " + A + " + " + B + " = " + (A+B));
					//System.out.printf("Case #%d: %d + %d = %d\n",i, A, B, (A+B));
				}
				
				in.close();
			}
		}

	
## 8. [11022번] A+B - 8

### 문제
	두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 테스트 케이스의 개수 T가 주어진다.
	
	각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

### 출력
	각 테스트 케이스마다 "Case #x: A + B = C" 형식으로 출력한다. x는 테스트 케이스 번호이고 1부터 시작하며, C는 A+B이다.

### 예제 입력 1 
	5
	1 1
	2 3
	3 4
	9 8
	5 2

### 예제 출력 1 
	Case #1: 1 + 1 = 2
	Case #2: 2 + 3 = 5
	Case #3: 3 + 4 = 7
	Case #4: 9 + 8 = 17
	Case #5: 5 + 2 = 7
  
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.IOException;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		import java.util.StringTokenizer;
		 
		public class Main {
		 
			public static void main(String[] args) throws IOException {
		 
				//BufferedReader와 BufferedWriter 선언 
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		 
				//String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
				int T = Integer.parseInt(br.readLine());
		        
				StringTokenizer st;
		 
				for (int i = 1; i <= T; i++) {
					//테스트 케이스에서 주어지는 두 정수는 문자열 분리를 위해 매 반복마다 StringTokenizer 생성과 동시에 문자를 입력받는다.
					//public StringTokenizer(String str, String delim) : 특정 delim으로 문자열을 분리한다.
					st = new StringTokenizer(br.readLine()," "); //한 줄씩 읽어와서(readline), 공백으로 문자열 분리("") 
					int A = Integer.parseInt(st.nextToken());
					int B = Integer.parseInt(st.nextToken());
					bw.write("Case #" + i + ": " + A + " + " + B + " = " + (A+B) + "\n");
				}
				br.close();
		        
				bw.flush();
				bw.close();
		 
			}
		}	
	
2. "**Scanner 사용**"

		import java.util.Scanner;
		
		public class Main {
			public static void main(String[] args) {
				
				Scanner in = new Scanner(System.in);
				int T = in.nextInt();
				
				for(int i = 1; i <= 5; i++)
				{
					int A = in.nextInt();
					int B = in.nextInt();
					System.out.println("Case #" + i +": " + (A+B));
					//System.out.printf("Case #%d: %d\n",i, (A+B));도 가능!
				}
				
				in.close();
			}
		}
		
## 9. [2438번] 별 찍기 - 1

### 문제 
	첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제 
### 입력
	첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

### 출력
	첫째 줄부터 N번째 줄까지 차례대로 별을 출력한다.

### 예제 입력 1 
	5

### 예제 출력 1 
	*
	**
	***
	****
	*****
	
  
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		import java.io.IOException;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
		 
				BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
				int N = Integer.parseInt(br.readLine());
		        
				for (int i = 1; i <= N; i++) {
					for(int j = 1; j<=i; j++) {
						bw.write("*");
					}
					bw.write("\n");
				}
				
				br.close();
				
				bw.flush();
				bw.close();
			}
		 
		}
	
2. "**Scanner 사용**"

		import java.util.Scanner;
		
		public class Main {
			public static void main(String[] args) {
				
				Scanner in = new Scanner(System.in);
				int N = in.nextInt();
				
				for(int i = 1; i <= N; i++)
				{
					for(int j =1; j<=i; j++)
					{
						System.out.printf("*");
					}
					System.out.printf("\n");
				}
				
				in.close();
			}
		}


## 10. [2439번] 별 찍기 - 2

### 문제 
	첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제
	
	하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오. 
### 입력
	첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

### 출력
	첫째 줄부터 N번째 줄까지 차례대로 별을 출력한다.

### 예제 입력 1 
	5

### 예제 출력 1 
	    *
	   **
	  ***
	 ****
	*****
  
  
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		import java.io.IOException;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
		 
				BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
				int N = Integer.parseInt(br.readLine());
		        
				for (int i = 1; i <= N; i++) {
					for(int j = 1; j<=N-i; j++) {
						bw.write(" ");
					}
					for(int j = 1; j<=i; j++) {
						bw.write("*");
					}
					bw.write("\n");
				}
				
				br.close();
				
				bw.flush();
				bw.close();
			}
		 
		}


	
2. "**Scanner 사용**"

		import java.util.Scanner;
		
		public class Main {
			public static void main(String[] args) {
				
				Scanner in = new Scanner(System.in);
				int N = in.nextInt();
				
				for(int i = 1; i <= N; i++)
				{
					for(int j =1; j<=N-i; j++)
					{
						System.out.printf(" ");
					}
					for(int j = 1; j<=i; j++) {
						System.out.printf("*");
					}
					System.out.printf("\n");
				}
				
				in.close();
			}
		}
	
## 11. [10871번] X보다 작은 수

### 문제 
	정수 N개로 이루어진 수열 A와 정수 X가 주어진다. 이때, A에서 X보다 작은 수를 모두 출력하는 프로그램을 작성하시오.
	
### 입력
	첫째 줄에 N과 X가 주어진다. (1 ≤ N, X ≤ 10,000)
	
	둘째 줄에 수열 A를 이루는 정수 N개가 주어진다. 주어지는 정수는 모두 1보다 크거나 같고, 10,000보다 작거나 같은 정수이다.

### 출력
	X보다 작은 수를 입력받은 순서대로 공백으로 구분해 출력한다. X보다 작은 수는 적어도 하나 존재한다.

### 예제 입력 1 
	10 5
	1 10 4 9 2 3 8 5 7 6

### 예제 출력 1 
	1 4 2 3
	
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 더 efficient
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.IOException;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		import java.util.StringTokenizer;
		 
		public class Main {
		 
			public static void main(String[] args) throws IOException {
		 
				//BufferedReader 선언 
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		        
				StringTokenizer st = new StringTokenizer(br.readLine(), " ");
				
				int N = Integer.parseInt(st.nextToken());
				int X = Integer.parseInt(st.nextToken());
		
				StringBuilder sb = new StringBuilder();
				
				st = new StringTokenizer(br.readLine()," ");
		 
				for (int i = 0; i < N; i++) {
					int value = Integer.parseInt(st.nextToken());
					
					if (value < X)
						sb.append(value).append(' ');
				}
				System.out.println(sb);
		 
			}
		}	



	
2. "**Scanner 사용**"


[1] 따로 입력값들을 저장하지 않고, 바로바로 값을 입력받고 바로바로 체크해서 출력하는 방법

		import java.util.Scanner;
		
		public class Main {
			public static void main(String[] args) {
				
				Scanner in = new Scanner(System.in);
				int N = in.nextInt();
				int X = in.nextInt();
				
				for(int i = 1; i <= N; i++)
				{
					int input = in.nextInt();
					if( input < X )
						System.out.printf("%d ",input);
				}
				
				in.close();
			}
		}
		
[2] 입력받음과 동시에 if 문으로 검사해서 주어진 수 보다 작은 경우 "**StringBuilder**" 에 저장해주는 방법

	import java.util.Scanner;
	
	public class Main {
	 
		public static void main(String[] args) {
			Scanner in = new Scanner(System.in);
			int N = in.nextInt();
			int X = in.nextInt();
	        
			StringBuilder sb = new StringBuilder();
	 
			for(int i = 0 ; i < N ; i++) {
				
				int value = in.nextInt();
				if(value < X) {
					sb.append(value+" ");
				}
			}
			System.out.println(sb);	
		}
	}
