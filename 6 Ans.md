public class permcom { public static boolean isPerm(int m, int n) {
int[] arr = new int[10];

        int temp = n;
        while (temp > 0) {
            arr[temp % 10]++;
            temp /= 10;
        }

        temp = m;
        while (temp > 0) {
            arr[temp % 10]--;
            temp /= 10;
        }


        for (int i = 0; i < 10; i++) {
            if (arr[i] != 0) return false;                
        }
        return true;
    }
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int start = 1;
        boolean found = false;
        int result = 0;
         
        while (!found) {
            start *= 10;
            for (int i = start; i < start * 10 / 6; i++) {
                found = true;
                for (int j = 2; j <= 6; j++) {
                    boolean che=isPerm(i,j*i);
                    if (!(che)) {
                        found = false;
                        break;
                    }
                }
                if (found) {
                    result = i;
                    break;
                }
            }
        }
        System.out.println(result);
        }

}
