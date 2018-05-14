#242

```ruby
# @param {String} s
# @param {String} t
# @return {Boolean}
def is_anagram(s, t)
    arr1 = {}
    arr2 = {}
    
    s.each_byte do |c|
        arr1[c] = (arr1[c] || 0) + 1
    end
    
    t.each_byte do |c|
        arr2[c] = (arr2[c] || 0) + 1
    end
    
    if arr1.keys.length != arr2.keys.length
        return false
    end
    
    arr1.each do |key, value|
        if arr1[key] != arr2[key]
            return false
        end
    end
    
    return true
end
```
