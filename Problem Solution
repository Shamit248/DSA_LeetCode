class Solution {
    public int missingMultiple(int[] nums, int k) {
        int m = 0;
        int[] A = new int[100];
        int s = 0;
        int miss = 0;

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] % k == 0) {
                A[m++] = nums[i];
            }
        }

        if (m == 0) {
            s = k;
            System.out.println(s);
            return s;
        }

        if (m == 1 && A[0] / k == 1) {
            s = A[0] + k;
            System.out.println(s);
            return s;
        } else if (m == 1 && A[0] / k != 1) {
            s = k;
            System.out.println(s);
            return s;
        }

        for (int i = 0; i < m - 1; i++) {
            for (int j = 0; j < m - i - 1; j++) {
                if (A[j] >= A[j + 1]) {
                    int temp = A[j];
                    A[j] = A[j + 1];
                    A[j + 1] = temp;
                }
            }
        }

        for (int i = 0; i < m - 1; i++) {
            if (A[i + 1] - A[i] > k && (A[0] / k == 1)) {
                s = A[i] + k;
                System.out.println(s);
                return s;
            }

            if (A[i + 1] - A[i] >= k && (A[0] / k) >= 2) {
                miss = k;
                System.out.println(miss);
                return miss;
            }

            if (A[i + 1] - A[i] >= 0 && (A[0] / k) >= 2) {
                miss = k;
                System.out.println(miss);
                return miss;
            }
        }

        miss = A[m - 1] + k;
        System.out.println(miss);
        return miss;
    }
}
