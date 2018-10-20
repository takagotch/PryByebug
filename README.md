### PryByebug
---


https://github.com/deivid-rodriguez/pry-byebug

```
gem 'pry-byebug'
bundle install

```

```ruby
def some_method
  puts 'Hello'
end
binding.pry
some_method
puts 'Goobye World'

if defined?(PryByebug)
  Pry.commands.alias_command 'c', 'continue'
  Pry.commands.alias_command 's', 'step'
  Pry.commands.alias_command 'n', 'next'
  Pry.commands.alias_command 'f', 'finish'
end

Pry::Commands.command /^$/, "repeat last command" do
  _pry_.run_command Pry.history.to_a.last
end

break SomeClass
break Foo#bar if baz?
break app/models/user.rb:15
break 14

break --condition 4 x > 2
break --condition 3

break --delete 5
break --disable-all

break
break --show 2

```

```
```

