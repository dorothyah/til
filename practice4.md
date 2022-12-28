```
public class Practice4 {
    public static long solution(int a, int b) {
        long answer = 0;
        if (a <= b) {
            for (int i = a; i <= b; i++) {
                answer += i;
            }
        } else {
            for (int i = b; i <= a; i++) {
                answer += i;
            }
        }
        return answer;

//        long answer = 0;
//        for (int i = ((a < b) ? a : b); i <= ((a < b) ? b : a); i++)
//            answer += i;
//
//        return answer; 간단한 풀이
    }
    public static void main(String[] args) {
        long result = solution(3,5);
        System.out.println(result);
    }
}
```
