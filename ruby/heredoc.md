You know about heredoc already:

```ruby
class Foo
  def something
    puts <<-EOF
      Well here's some lovely debug text
    EOF
  end
end
```

But it's somewhat annoying in that it doesn't strip the leading whitespace from the surrounding context from the output:

```ruby
$> Foo.new.something
      Well here's some lovely debug text
$>
```

Rails introduced a method `strip_heredoc` in version 3 that would fix this problem (also note where the method call goes - that was a surprise for me when I found out)

```ruby
...
    puts <<-EOF.strip_heredoc
      Well here's some lovely debug text
    EOF
...
$> Foo.new.something
Well here's some lovely debug text
$>
```

And with ruby 2.3, it's now part of the language itself, with the squiggly heredoc notation:

```ruby
...
    puts <<~EOF
      Well here's some lovely debug text
    EOF
...
$> Foo.new.something
Well here's some lovely debug text
$>
```
