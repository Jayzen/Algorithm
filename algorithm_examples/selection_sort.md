选择排序的实现
选择排序的说明:把数组的首个字段拿出来依次做对比,如果是最小，放第一位，然后开始比较第二字段的数值。
```ruby
class Array
  def selection_sort
    for i in 0...self.length
      for j in (i+1)...self.length
        if self[j]<self[i]
          self[i], self[j]=self[j], self[i] #多重赋值，交换两个值
        end
      end
    end
    return self
  end
end

demo = [3,87,9,1,17,2,2,1]
p demo.selection_sort #[1, 1, 2, 2, 3, 9, 17, 87]
```
