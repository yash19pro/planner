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
class RecentCounter {
    List<Integer> pingTimings;

    public RecentCounter() {
        pingTimings = new ArrayList<>();
    }

    public int ping(int t) {
        pingTimings.add(t);
        return getAllLessThanTminus3000(t);
    }

    private int getAllLessThanTminus3000(int t) {
        int t_ = Math.max(0, t - 3000);
        int counter = 0;

        for (int i = 0; i < pingTimings.size(); i++) {
            if (pingTimings.get(i) >= t_) {
                counter++;
            }
        }

        return counter;
    }
}
```
