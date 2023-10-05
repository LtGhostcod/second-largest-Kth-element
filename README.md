# second-largest-Kth-element
finding the second largest inside the array using a single traversal 
public class sLarge {
    public static int secLargest(int arr[]){
        int n = arr.length;
        int res = -1;
        int largest = 0;

        for (int i = 1; i < n; i++){
            if (arr[i] > arr[largest]){
                res = largest;
                largest = i;
            } else if (arr[i] != arr[largest]) {
                if (res == -1 || arr[i] > arr[res]){
                    res = i;
                }
            }
        }
        return res;
    }
    public static void main(String[] args) {
        int[] arr = {5, 8, 20, 13, 15};
        int ans = secLargest(arr);
        System.out.println(ans);
    }
}
