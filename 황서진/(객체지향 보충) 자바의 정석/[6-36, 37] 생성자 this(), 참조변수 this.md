# 1-1. 생성자 this()

* 생성자에서 다른 생성자 호출할 때 사용
* 다른 생성자 호출시 "첫 줄"에서만 사용 가능

# 1-2. 생성자 this() 학습 코드

### 클래스 : Car2
	class Car2 {
		String color; // 색상 
	    String gearType; // 변속기 종류 - auto(자동), manual(수동) 
	    int door;
	    
	    Car2() {
	    	this("white", "auto", 4);
	    }
	    
	    Car2(String color) {
	    	this(color, "auto", 4);
	    }
	    
	    Car2(String color, String gearType, int door) {
	    	this.color = color;
	    	this.gearType = gearType;
	    	this.door = door;
	    }
	}


# 2. 참조변수 this
* 참조변수 this와 생성자 this는 완전히 다른 개념이다!
* 인스턴스(객체) 자신을 가리키는 참조변수
*  인스턴스 메서드(생성자 포함)에서 사용 가능
*  지역변수(lv)와 인스턴스 변수(iv)를 구별할 때 사용

# 3.  참조변수 this와 생성자 this()
* this : 인스턴스 자신을 가리키는 참조변수, 인스턴스 주소가 저장되어 있다. 모든 인스턴스 메서드에 지역변수로 숨겨진 채로 존재한다.
* this(), this(매개변수) : 생성자, 같은 클래스의 다른 생성자를 호출할 때 사용한다.    
