#### I have not idea what I am doing, please help me fix my code! I seem to have made some mistakes.

```ruby
class Document
   attr_accessor :content, :title

  def initialize(content, title)
    @content = content
    @title = title
  end

  def to_s
    "#{@title}: #{@content}"
  end
end

doc = Document.new("Ruby Exam", "TODO some questions")

puts doc.title
puts doc.content
puts doc
```

#### I made a mistake in the RubyExam, can you find it?

```ruby
class RubyExam
  def initialize
    @score = 0
    @current_question = 1
  end

  def got_one_right
    @score += 1
    next_question
  end

  def got_one_wrong
    @score +- 1
    next_question
  end

  def next_question
    @current_question += 1
  end

  def perfect_score
    puts "I made no mistake!"
  end
  
  def complete
    if @score < 10
      puts 'Game Over'
    else
      perfect_score
    end
    puts "Final Score: #{@score}"
  end

end

exam = RubyExam.new
exam.got_one_right
exam.got_one_wrong
exam.got_one_wrong
exam.complete
```

#### What are 3 ways to create a new Hash?

- Hash.new
- hash = {'key': 'value'}
- Hash['key','value']

#### Which of the following are valid for __X__?

```ruby
def save!(array)
  raise ArgumentError.new('arg should be array') unless array.is_a?(Array)

  # do stuff ..
rescue ArgumentError
  puts 'Failed to save!'
  puts $1
  puts $1.message
  puts $1.backtrace
  puts $@
end
```

- [ ] `Error => e`
- [ ] *nothing*
- [ ] `SystemError => e`
- [ ] `ArgumentError => e`
- [ ] `StandardError => e`
- [ ] `ArgumentError`
- [ ] ` => ArgumentError`
- [ ] ` => argument_error`

#### What is the correct output for:

```ruby
d = Date.parse('01-02-99') << 1
p d.to_s
```

- [ ] `"1999-01-02"`
- [ ] `"1998-01-01"`
- [ ] `"1998-12-31"`
- [ ] `"1998-12-01"`
- [x] an exception

#### What is the correct output for:

```ruby
d = Date.parse('2019-01-31') >> 1
p d.to_s
```

- [ ] `"2018-12-31"`
- [ ] `"2020-01-31"`
- [ ] `"2019-02-31"`
- [x] `"2019-02-28"`
- [ ] an exception


#### What is the correct ways to access the value of this Hash?

```ruby
toybox = { "doll" => 'Sally' }
```

- [ ] `toybox.doll`
- [x] `toybox['doll']`
- [x] `toybox["doll"]`
- [ ] `toybox[:doll]`
- [ ] `toybox.try('doll')`

#### The following regexp is incorrect please fix it, it should *ONLY* match:

- .ts
- .ts.erb
- .tsx
- .tsx.erb

`/^\.ts(x)?(\.erb)?$/`

Here is a good editor for regexp, maybe try and do it without using it first tho: https://rubular.com/

#### Given the following file locations, what are the outputs?

```ruby
# /User/gollum/precious/ring.rb
File.dirname(__FILE__)

File.dirname("/User/gollum/precious/")
```


```ruby
# /User/tom/junk/ring.rb
File.path(__dir__)

File.path("/User/tom/junk/ring.rb")
```


#### Write the following method that would give me the correct return value:

```ruby
bark { "Oki" }
=> "Oki yips!"

def bark (dogs_name)
  puts "#{dogs_name} yips!"
end
```


#### What is the result of the following:

```ruby
teams = [['greg', 'bob']]
teams << if teams.size < 2
  ['jim', 'jerry']
elseif teams > 2
  ['sam']
else
  ['tony']
end

p teams.flat_map { |t| t }

[greg, bob, jim, jerry]
```
