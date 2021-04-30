# [3단계] while문

* 백준 알고리즘에서는 "**_클래스명_**"을 "**_Main_**"으로 해주어야 한다!
* "**BufferedReader**", "**BufferedWriter**", 그리고 "**StringTokenize**"에 대한 자세한 내용은 따로 정리해서 업로드 할 예정!
* EOF 관련 내용도 따로 업로드 할 예정!

## 1. [10952번] A+B - 5

### 문제
	두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### 입력
	입력은 여러 개의 테스트 케이스로 이루어져 있다.
	
	각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)
	
	입력의 마지막에는 0 두 개가 들어온다.

### 출력
	각 테스트 케이스마다 A+B를 출력한다.

### 예제 입력 1 
	1 1
	2 3
	3 4
	9 8
	5 2
	0 0
### 예제 출력 1
	2
	5
	7
	17
	7



### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 코드는 더 길어도 더 efficient!
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.InputStreamReader;
		import java.util.StringTokenizer;
		import java.io.IOException;
		import java.io.OutputStreamWriter;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
		 
				BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
				int A;
				int B;
		        
				StringTokenizer st;
		            do {
					st = new StringTokenizer(br.readLine()," ");
					A = Integer.parseInt(st.nextToken());
					B = Integer.parseInt(st.nextToken());
					
					if(A == 0 && B == 0)
						break;
					
					bw.write((A+B) + "\n");
					
				}while(A != 0 || B != 0);
		            
				br.close();
				
				bw.flush();
				bw.close();
			}
		 
		}	
	
2. "**Scanner 사용**"

		* while(true), 그리고 break로 따로 빠져나올 조건을 명시해서 무한 루프 구문을 작성해 봤는데 런타임 에러가 발생했다. 
		* 또 while(A != 0 || B != 0); 로 do while구문을 작성하고 if 조건을 빼봤는데 마지막 0 0이 입력되었을 때도 합인 0이 출력되어 버려서 또 오류가 발생...  
		
		그래서 최종 작성 답안은 아래 코드와 같다!
		
		import java.util.Scanner;
		
		public class Main {
		
			public static void main(String[] args) {
				Scanner in = new Scanner(System.in);
				int A = 1;
				int B = 1;
		        
				do {
					A = in.nextInt();
					B = in.nextInt();
					
					if(A == 0 && B == 0)
						break;
					
					System.out.println(A+B);
					
					
				}while(A != 0 || B != 0);
					
				in.close();
			}
		}
		
		
## 2. [10951번] A+B - 4

### 문제
	두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### 입력
	입력은 여러 개의 테스트 케이스로 이루어져 있다.
	
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
1. "**BufferedReader & BufferedWriter 사용**"

		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		import java.io.IOException;
		import java.util.StringTokenizer;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
				
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
				StringTokenizer st;
				String str = "";
		 
				while( (str=br.readLine()) != null ){
				    
					st = new StringTokenizer(str," ");
					int a = Integer.parseInt(st.nextToken());
					int b = Integer.parseInt(st.nextToken());
					bw.write(String.valueOf(a+b));
					bw.newLine();
				
				}
			    bw.flush();
			    bw.close();
			    
			    br.close();
			    
			}
		}
2. "**BufferedReader & StringBuilder 사용**"  -> 코드는 더 길어도 더 efficient!
		
		
		 
		import java.io.BufferedReader;
		import java.io.InputStreamReader;
		import java.io.IOException;
		import java.util.StringTokenizer;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
				
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
				StringBuilder sb = new StringBuilder();
				StringTokenizer st;
				String str;
		 
				while( (str=br.readLine()) != null ){
				    
					st = new StringTokenizer(str," ");
					int a = Integer.parseInt(st.nextToken());
					int b = Integer.parseInt(st.nextToken());
					sb.append(a+b).append("\n");
				
				}
				System.out.print(sb);
			}
		}
	
3. "**Scanner 사용**"

		import java.util.Scanner;
		
		public class Main {
		
			public static void main(String[] args) {
				Scanner in = new Scanner(System.in);
				int A = 1;
				int B = 1;
		        
				while(in.hasNextInt()){
					
					A = in.nextInt();
					B = in.nextInt();
					System.out.println(A+B);
					
				}
					
				in.close();
			}
		}	
		
		* hasNextInt()의 경우 입력값이 정수일 경우 true를 반환하며 정수가 아닐 경우 바로 예외를 던지며 더 이상 입력을 받지 않고 hasNextInt()에서 false를 반환하면서 반복문이 종료된다.

## 3. [1110번] 더하기 사이클

### 문제
	0보다 크거나 같고, 99보다 작거나 같은 정수가 주어질 때 다음과 같은 연산을 할 수 있다. 먼저 주어진 수가 10보다 작다면 앞에 0을 붙여 두 자리 수로 만들고, 각 자리의 숫자를 더한다. 그 다음, 주어진 수의 가장 오른쪽 자리 수와 앞에서 구한 합의 가장 오른쪽 자리 수를 이어 붙이면 새로운 수를 만들 수 있다. 다음 예를 보자.
	
	26부터 시작한다. 2+6 = 8이다. 새로운 수는 68이다. 6+8 = 14이다. 새로운 수는 84이다. 8+4 = 12이다. 새로운 수는 42이다. 4+2 = 6이다. 새로운 수는 26이다.
	
	위의 예는 4번만에 원래 수로 돌아올 수 있다. 따라서 26의 사이클의 길이는 4이다.
	
	N이 주어졌을 때, N의 사이클의 길이를 구하는 프로그램을 작성하시오.

### 입력
	첫째 줄에 N이 주어진다. N은 0보다 크거나 같고, 99보다 작거나 같은 정수이다.

### 출력
	첫째 줄에 N의 사이클 길이를 출력한다.

### 예제 입력 1 
`26`

### 예제 출력 1 
`4`
### 예제 입력 2 
`55`

### 예제 출력 2 
`3`
### 예제 입력 3 
`1`

### 예제 출력 3 
`60`
### 예제 입력 4 
`0`

### 예제 출력 4 
`1`
  
### 내 제출 코드 
1. "**BufferedReader & BufferedWriter 사용**"  -> 코드는 더 길어도 더 efficient!
		
		import java.io.BufferedReader;
		import java.io.BufferedWriter;
		import java.io.InputStreamReader;
		import java.io.OutputStreamWriter;
		import java.io.IOException;
		 
		public class Main {
			public static void main(String args[]) throws IOException {
				
				BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
				BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
				
				
				int count = 0;
				
				int a = Integer.parseInt(br.readLine());
				int A = a;
		
				do{
				    
					int b = A%10;
					int c = ((A/10) + b)%10;
					
					A = b*10 + c;
					
					count++;
					
				
				}while(a != A);
				
				bw.write(String.valueOf(count));
				
			    bw.flush();
			    bw.close();
			    
			    br.close();
			    
			}
		}	
		
2. "**Scanner 사용**"
		
		import java.util.Scanner;
		
		public class Main {
		
			public static void main(String[] args) {
				Scanner in = new Scanner(System.in);
				int N = in.nextInt();
				int n = N;
				int count = 0;
		        
				do {
					
					int a = N%10;
					int b = a + N/10;
					
					N = a*10 + b%10;
					count ++;
					
					
				}while(N != n);
					
				System.out.println(count);
			}
		}
