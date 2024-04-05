``` python
def count_combinations(numbers, target_sum, path=[], count=0):
    current_sum = sum(path)
    if current_sum == target_sum:
        return 1
    if current_sum > target_sum:
        return 0

    for i in range(len(numbers)):
        count += count_combinations(numbers[i:], target_sum, path + [numbers[i]])

    return count

numbers = [5, 1, 0.5, 0.25]
target_sum = 10

result_count = count_combinations(numbers, target_sum)
print("Number of combinations that sum up to", target_sum, ":", result_count)
```

- this is a [[recursion]] solution 
