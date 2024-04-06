
[Insert Delete GetRandom O(1)](https://leetcode.com/problems/insert-delete-getrandom-o1/)
subject: array / strings
difficulty: medium 
---

``` python
class RandomizedSet:

  

    def __init__(self):

        self.values = set()

  

    def insert(self, val: int) -> bool:

        if val not in self.values:

            self.values.add(val)

            return True

        return False

  

    def remove(self, val: int) -> bool:

        if val in self.values:

            self.values.remove(val)

            return True

        return False

  

    def getRandom(self) -> int:

        return choice(list(self.values))

  
  

# Your RandomizedSet object will be instantiated and called as such:

# obj = RandomizedSet()

# param_1 = obj.insert(val)

# param_2 = obj.remove(val)

# param_3 = obj.getRandom()
```

-- init is a special function that is automatically called whenever the class is called and it initializes new variables then. 

---
next problem: [[leetcode intreview prep 150.12]]
