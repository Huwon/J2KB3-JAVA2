# 1-1. static 메서드와 인스턴스 메서드 

* 앞에 static이 붙지 않은 것 : 인스턴스 메서드
* 앞에 static이 붙은 것 : static 메서드
   

### 인스턴스 메서드 
* 인스턴스 생성 후, '참조변수.메서드 이름()'으로 호출
* 인스턴스 멤버(iv, im)와 관련된 작업을 하는 메서드
* 메서드 내에서 인스턴스 변수(iv) 사용 가능
 
### static 메서드(클래스 메서드)       
* 객체 생성 없이 '클래스 이름.메서드 이름()'으로 호출
* 인스턴스 멤버(iv, im)와 관련없는 작업을 하는 메서드
* 메서드 내에서 인스턴스 변수(iv) 사용 불가
* ex. Math.random(), Math.round()
 
### static을 언제 붙여야 할까?      
* 속성 (멤버 변수) 중에서 공통 속성에 static을 붙인다.
     - 인스턴스 변수 : 개별 속성
     - 클래스 변수 : 공통 속성

* 인스턴스 멤버(iv, im)을 사용하지 않는 메서드에 static을 붙인다. 

# 1-2. static 메서드와 인스턴스 메서드 학습코드

### 클래스 : MyMathTest2
	class MyMath2 {
		long a, b;
		
		long add() { // 인스턴스 메서드 
			return a + b;
		}
		
		static long add(long a, long b) { // 클래스 메서드 (static 메서드) -> 매개변수 2개 (iv 필요 X , lv 사용)
			return a + b;
		}
	
	}
	
	class MyMathTest2 {
		public static void main(String args[]) {
			System.out.println(MyMath2.add(200L, 100L)); // 클래스 메서드 호출 (객체 생성 없이 호출 가능) 
			
			MyMath2 mm = new MyMath2(); // 인스턴스 생성 
		    mm.a = 200L;
		    mm.b = 100L;
		    
		    System.out.println(mm.add()); // 인스턴스메서드 호출
		    
		}
	}


## Run 결과
	300
	300


# 2. 메서드 간의 호출과 참조  
* static 메서드는 인스턴스 변수(iv)를 사용할 수 없다.
*  static 메서드는 인스턴스 메서드(im)를 호출할 수 없다.

