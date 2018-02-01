# Definitions

**"getters"**
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
