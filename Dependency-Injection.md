[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/Practices)
# Dependency Injection
The practice of separating the construction of objects and the using of objects. The convention is that an object should know how to receive functionality and use functionality but not how to make its own functionality.<br>

## Preceding Patterns

## Use Cases
I *think* that this is referring to having a class (or object) that mostly knows what it does but can also be passed a function for it to use. I have done this before in an application where a button object would be created that have most of their own functionality, but when it is created it is also passed a function as an argument that will be run when the button is pressed.<br>
<br>
If this is incorrect I don't understand it and am not actually sure what use this would be. It makes me a bit suspicious that what I have found describes it in a way that smells of way too much abstraction, as if instead of creating classes to make objects, you are creaking classes with your functionality which create pass those functions to completely empty classes which are used to create useful objects. If this is the case you're just going to fall into a "classes all the way down" pit. *But* if they are just describing it poorly and functionally it works like how I'm thinking, it makes sense to me.<br>
<br>
## Examples
This is from my own example I had on hand. It is very abridged and mangled for the purpose of demonstration and it likely doesn't work, it is simply shown as an example of how it might function. Also this is python using Tkinter.<br>

```
class setSubmit:
	Interface = tkinter.Tk()
    
    
def createSubmitRow(self,doOnSubmit):
        
		#makes button, checks if the function passed to it is valid
		submit = tkinter.Button(Interface, text="Submit", state="disabled")
		self.__errorCheck(not self.doOnSubmit, "ERROR: doOnSubmit is None")
		submit.configure(command=self.doOnSubmit)
		submit.pack(side="left")
```
```
def makeNewFile():...

setSubmit.createSubmitRow(makeNewFile)
```

## Following Patterns