# Lizard Specs

This document contains (conceptual*) description of Lizard grammar.
##### with ❤ by Alexey Yurchenko

---

# Types

* Identifier
* Integer
* Float
* String
* Object
* Array

---

# Variables

### Defult variable
```
x = 1 # => var x = 1;
``` 

### Prefixed variable
```
@x = Fruits # => var x = new Fruits();
&x = greetings("Bob") # => this.x = greetings("Bob");
@&x = Date # => this.x = new Date();
```

### One-line multiple variable assignment

```
x, y, z = 0, 0, 0
```

Compiles to:

```
var x = 0;
var y = 0;
var z = 0;
```

With prefixes:
```
@x, &y, z = Date, 1, 2;
```

Compiles to:
```
var x = new Date();
this.y = 1;
var z = 2;
```

--- 

### more be later
