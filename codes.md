problem 1

```java
class Solution {
    public int timeRequiredToBuy(int[] tickets, int k) {
        int time = 0, index = 0;

        while (tickets[k] != 0) {
            index = index % tickets.length;
            if (tickets[index] != 0) {
                tickets[index] -= 1;
                time += 1;
            }
            index += 1;
        }

        return time;
    }
}
```

problem 2

```java

```
