```
public class Practice2 {
    public static String solution(int num) {
        //return num % 2 == 0 ? "Even" : "Odd"; 삼항연산자를 사용한 풀이
        if (num % 2 == 0) {
            return ("Even");
        } else {
            return ("Odd");
        }
    }
    public static void main(String[] args) {
        System.out.println(solution(5));
    }
}
```
