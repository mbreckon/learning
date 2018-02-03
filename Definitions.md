# Definitions

The definitions I've gathered here are an attempt to build a shared language on some of the concepts around OOP and other topics.

## "getters"
Methods or properties that expose the objects that an object composes (i.e. is passed in the constructor) as opposed to one that creates a new object from the result of some activity. 

    class ObjA
    {
        public ObjA(ObjB obj)
           => this_is_a_getter = obj
           
        public ObjB this_is_a_getter { get; }
    }
    
    class ObjA
    {
        public ObjA(ObjC obj)
           => this.obj = obj;
           
        public ObjB not_a_getter
           => new ObjB(obj.DoSomething());
    }
    
### Discussion (ongoing)
This particular definition was formed during a discussion with a colleague who was arguing that there is no place for a "getter" in OO code. On reflection it is hard to find the references to back the above definition up and this remains something that needs further debate.

What is clear is that public methods that simply return internal data of an object in a form that means you cannot later change it's representation without knock on impact in the wider code base should be avoided.  

[Getters and Setters are Evil. Period. (Yegor Bugayenko)](http://www.yegor256.com/2014/09/16/getters-and-setters-are-evil.html)

[Why getters and setter methods are evil (Allen Hollub)](https://www.javaworld.com/article/2073723/core-java/why-getter-and-setter-methods-are-evil.html)
