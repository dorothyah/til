```
public class Practice7 {
    public static int solution(int[] absolutes, boolean[] signs) {
        int answer = 0;

        for (int i = 0; i <signs.length; i++) {
            if (signs[i]) {
                answer += absolutes[i];
            } else {
                answer -= absolutes[i];
            }
        }
//        for (int i = 0; i < absolutes.length; i++) {
//            answer += (signs[i]) ? absolutes[i] : -absolutes[i];
//        } 간략한 코드

        return answer;
    }
    public static void main(String[] args) {
        int[] a = {4,7,12};
        boolean[] s = {true, false, true};
        System.out.println(solution(a,s));
    }
}
```
