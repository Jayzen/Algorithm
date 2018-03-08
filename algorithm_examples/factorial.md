class Integer
  def factorial
    self == 1 ? 1 : self * (self - 1).factorial
  end
end

p 5.factorial
