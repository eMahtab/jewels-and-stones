# Jewels and Stones

### Implementation

```java
public int numJewelsInStones(String J, String S) {
        int jewelStones = 0;
        for(int i = 0; i < S.length(); i++){
            if(J.indexOf(S.charAt(i)+"") != -1){
                jewelStones++;
            }
        }
        return jewelStones;
}
```


```java
public int numJewelsInStones(String J, String S) {
        Set<Character> jewels = new HashSet<Character>();
        for(int i = 0; i < J.length(); i++){
            jewels.add(J.charAt(i));
        }
        int jewelStones = 0;
        
        for(int i = 0; i < S.length(); i++){
            if(jewels.contains(S.charAt(i))){
                jewelStones++;
            }
        }
        return jewelStones;
}

```
