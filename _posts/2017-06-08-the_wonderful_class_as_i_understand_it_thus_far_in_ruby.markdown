---
layout: post
title:  "The wonderful 'class' as I understand it thus far in Ruby"
date:   2017-06-08 19:40:37 +0000
---



 
Oh how I love class. I have just discovered this beautiul time saving machine and its pretty exciting. A class is essentially a blueprint for whatever you want it to be. When you are building a class you are building the foundation for other objects and giving them readable and writable containers that can be changed at will... or not changed at all depending on what you would like them to do.

Let's say you are building an app for a Wizard's spellbook. ( What? Wizards use apps too, get with the times man! ). Each spell is different of course but all will share the same fundamental qualites. Lets look at an example.


```
class Spells



def type=(type)
@type = type
end

#this first bit of code is our setter method. With this we can set and change the element whenever we choose. 


def type
  @type
end

#And this bit is our getter method. This allows us to get what element has been set.


#Below we will repeat what we have done above.



def power=(power)
  @power = power
end

def power
  @power
end

def cost=(cost)
  @cost = cost
end

def cost
  @cost
end

end


end
```

Before we go on it's important to talk about instance variables. A instance varaiable is a variable that only exist in each instance of the class that is created. So below when we use @type ( the @ is what makes it an instance variable ). That info stored in @type is only avalabile inside of the object we have created. Check this [link](http://ruby-for-beginners.rubymonstas.org/writing_classes/instance_variables.html) out for more info on instance variables.

Now that we have created our Class lets create a fireball spell, and oldy but a goody. 

```
fireball = Spells.new
 
 #=> #<Spells:0x00000001c85b08> 
 # Boom! Your fireball is created. These numbers above represent where the fireball is stored in your computer. You don't need to know much about that now just that thats what they are.
```

Now will add some details to the fireball using our setter method.

```
fireball.type= "Fire"
#=> "Fire"

fireball.cost= 100
#=>100

fireball.power= 9000
#=> 9000
```

Our Wizard, who wish's to remain nameless ( That's probably because he dosen't know what a fireball spell is. Jeez, talk about basics ) can now refrence our new fireball for information using the getter method.

```
fireball.type
#=> "Fire

fireball.power
#=>9000
```

Awesome right! Our Wizard can also change the values of any of these elements whenever he likes. For example maybe he figured out how to make his fireball spell more powerful.

```
fireball.power
#=>9000

fireball.power= (9001)
#=>9001
```

Now his fireball power is over 9000 ![](https://68.media.tumblr.com/avatar_21dc9a2ee318_128.png)

Without class we would have to rewrite the following code everytime we wanted to make a new spell with the same elements.

```
def type=(type)
@type = type
end

def type
  @type
end

def power=(power)
  @power = power
end

def power
  @power
end

def cost=(cost)
  @cost = cost
end

def cost
  @cost
end

end

```

Thanks to class, all we have to write is:

```
ice_blast = Spells.new

lighting_whip = Spells.new
```

And bam! Two more spells created!


This is just the begining and I am sure that we are in store for whole bunch more uses for class'. I can't wait to see what's next.


