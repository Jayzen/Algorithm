递归实现的实例，实现整数n!
```ruby
class Integer
  def factorial
    self == 1 ? 1 : self * (self - 1).factorial
  end
end

p 5.factorial
```
