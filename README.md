# Leetcode----2529
Maximum Count of Positive Integer and Negative Integer
//code in java 
public class Solution {
    public int maximumCount(int[] nums) {
        int positiveCount = 0;
        int negativeCount = 0;

        for (int num : nums) {
            if (num > 0) {
                positiveCount++;
            } else if (num < 0) {
                negativeCount++;
            }
        }
        
        return Math.max(positiveCount, negativeCount);
    }

    public static void main(String[] args) {
        Solution solution = new Solution();
        int[] nums = {-3, -2, -1, 0, 1, 2, 3};
        System.out.println("Maximum Count: " + solution.maximumCount(nums));
    }
}
