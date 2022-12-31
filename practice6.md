```
public class Practice6 {
    public static int solution(int[] numbers) {
        int answer = 45;
        for (int n : numbers) {
            answer -= n;
        }
        return answer;
    }
    public static void main(String[] args) {
        int[] result = {1,2,3,4,6,7,8};
        System.out.println(solution(result));
    }
}
```
