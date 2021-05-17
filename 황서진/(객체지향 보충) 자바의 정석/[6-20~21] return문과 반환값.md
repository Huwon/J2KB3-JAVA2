# 1-1. return문

실행 중인 메서드를 종료하고 호출한 곳으로 되돌아간다.

* 반환타입이 void가 아닌 경우, 반드시 return문 필요
* 메서드 내 조건이 존재한다면 각각의 조건에 대해 return문 필요

# 1-2. return문 학습 코드
### 클래스 : Ex6_4	
		public class Ex6_4 {
		public static void main(String[] args) {
			MyMath mm = new MyMath();
			
			mm.printGugudan(12);
			mm.printGugudan(6);		
			
		}
	
	}
	
	class MyMath {
		void printGugudan(int dan) {
			
			if(!(2<=dan && dan <= 9))
				return;
			
			for (int i=1; i<=9; i++) {
				System.out.printf("%d * %d = %d%n", dan, i, dan*i);
			}
			//return;
		}
	}



## Run 결과
	6 * 1 = 6
	6 * 2 = 12
	6 * 3 = 18
	6 * 4 = 24
	6 * 5 = 30
	6 * 6 = 36
	6 * 7 = 42
	6 * 8 = 48
	6 * 9 = 54
	 

# 2. 반환값

* 반환타입이 void가 아닐 때, 반환값은 반환 타입이 일치(자동형반환)해야 한다.
