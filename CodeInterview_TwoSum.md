# Two Sum

## 問題

整数の配列 `nums` と整数 `target` が与えられます。

配列内の異なる2つの要素の合計が `target` となるような、**2つの要素のインデックス**を配列で返してください。

## 条件

- 同じ要素を2回使用することはできません。
- 条件を満たす組み合わせは必ず1つ存在します。
- インデックスの順序は問いません。

## 入出力例

### 例1

**入力：**
```java
nums = [2, 7, 11, 15]
target = 9
```

**出力：**
```java
[0, 1]
```

**説明：**

`nums[0] + nums[1] = 2 + 7 = 9` となるため、`[0, 1]` を返します。

### 例2

**入力：**

```java
nums = [3, 2, 4]
target = 6
```

**出力：**

```java
[1, 2]
```

## Javaソース

```java
import java.util.Arrays;

class Solution {
    public static void main (String[] args) {
        Solution solution = new Solution();
        solution.test();
    }
    
    public int[] twoSum(int[] nums, int target) {
        // このメソッドを実装してください
    }

    /**
     * テストケース
     */
    public void test () {
        /* Basic case */
        int[] result1 = twoSum(new int[]{2, 7, 11, 15}, 9);
        Arrays.sort(result1);
        boolean assert1 = Arrays.equals(result1, new int[]{0, 1});
        System.out.println("Basic case: " + (assert1 ? "PASS" : "FAIL"));
        
        /* Non-adjacent elements */
        int[] result2 = twoSum(new int[]{3, 2, 4}, 6);
        Arrays.sort(result2);
        boolean assert2 = Arrays.equals(result2, new int[]{1, 2});
        System.out.println("Non-adjacent elements: " + (assert2 ? "PASS" : "FAIL"));
        
        /* Duplicate values */
        int[] result3 = twoSum(new int[]{3, 3}, 6);
        Arrays.sort(result3);
        boolean assert3 = Arrays.equals(result3, new int[]{0, 1});
        System.out.println("Duplicate values: " + (assert3 ? "PASS" : "FAIL"));
        
        /* Negative numbers */
        int[] result4 = twoSum(new int[]{-3, 4, 3, 90}, 0);
        Arrays.sort(result4);
        boolean assert4 = Arrays.equals(result4, new int[]{0, 2});
        System.out.println("Negative numbers: " + (assert4 ? "PASS" : "FAIL"));
        
        /* Zero values */
        int[] result5 = twoSum(new int[]{0, 4, 3, 0}, 0);
        Arrays.sort(result5);
        boolean assert5 = Arrays.equals(result5, new int[]{0, 3});
        System.out.println("Zero values: " + (assert5 ? "PASS" : "FAIL"));
        
        /* Large numbers */
        int[] result6 = twoSum(new int[]{1000000, 2000000, 3000000}, 5000000);
        Arrays.sort(result6);
        boolean assert6 = Arrays.equals(result6, new int[]{1, 2});
        System.out.println("Large numbers: " + (assert6 ? "PASS" : "FAIL"));
    }
}
```





