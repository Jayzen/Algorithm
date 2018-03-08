二分查找的算法实现
应用场景: 将需要查找的数每次和查找范围之内的中位数最比较
```ruby
class Array
  def binary_search(value)
    low = 0
    high = self.size - 1

    while(low <= high) do
      mid = low + (high - low) / 2 #如果分母是整数，那么结果也是整数，而且向下圆整

      if self[mid] == value
        return mid
      elsif self[mid] < value
        low = mid + 1
      else
        high = mid - 1
      end
    end
    return nil 
  end
end
```

#Realization
```ruby
p (1..100).to_a.binary_search(100) #99
p (1..100).to_a.binary_search(199) #nil
```


#Terminology
```ruby
#iteration(迭代) : update the value of the variables
#recursion(递归) : call self in the inner function
```
