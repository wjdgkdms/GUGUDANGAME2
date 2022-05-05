package s21300_java00;
import java.util.*;
import java.io.*;

public class S21300_Gugudan_Game {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
	    int x, y;
	    Random r= new Random();	//랜덤 객체 생성 0.0 이상 1.0 미만 난수 

	    //System.out.print("args.length: " + args.length);
	    //기본 변환함수 사용 int형으로 형변환
	    x= Math.abs(r.nextInt() % 9) + 1;
	    y= Math.abs(r.nextInt() % 9) + 1;
	    
	    //커맨드 라인으로부터 받는 외부 변수가 있다면
	    //main으로부터 받는 외부 입력된 자료의 수(길이) args.length
	    if ( args.length > 0) {
	      x = Integer.parseInt(args[0]); //랩퍼 클래스를 통하여 int형으로 변경
	    }

	    int num= x*y;

	    System.out.println();
	    System.out.println("* 구구단 "+ x + "단에 대한 문제입니다");
	    System.out.println();

	    System.out.print(x +" * "+ y +" = ");

	    //Scanner 입력 값->랩퍼 크래스를 이용하여 int형으로 형변환
	    Scanner scan = new Scanner(System.in);
	    //int inputNum = scan.nextInt(); 	  //표준 입출력
	    
	    String tmp = scan.nextLine();         //입력된 값 String
	    int inputNum = Integer.parseInt(tmp); //랩퍼 크래스를 이용하여 int형으로 형변환
	    
	    if(num==inputNum){
	      System.out.println("맞았습니다!");
	    }else{
	      System.out.println("틀렸습니다. 정답은 "+ num +"입니다.");
	    }
	}

}
