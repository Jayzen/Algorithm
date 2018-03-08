算法实现
```ruby
class Array
  def selection_sort
    for i in 0...self.length
      for j in (i+1)...self.length
        if self[j]<self[i]
          self[i], self[j]=self[j], self[i]
        end
      end
    end
    return self
  end
end

demo = [3,87,9,1,17,2,2,1]
p demo.selection_sort #[1, 1, 2, 2, 3, 9, 17, 87]
```
