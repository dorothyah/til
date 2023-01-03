```
public class Practice8 {
    public static double solution(int[] arr) {
        double sum = 0;

        for (int i = 0; i < arr.length; i++) {
            sum += arr[i];
        }
        double answer = sum / arr.length;
        return answer;
    }
    public static void main(String[] args) {
        int[] result = {1,2,3,4};
        System.out.println(solution(result));
    }
}
```
