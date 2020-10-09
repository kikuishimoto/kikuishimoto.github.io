---
layout: post
title:      "How to make a simple like function using useState"
date:       2020-10-09 15:09:38 -0400
permalink:  how_to_make_a_simple_like_function_using_usestate
---


Hi all. In this blog post, we are going to cover how to create a simple like button using useState. 

**First, let's go over useState, what it is, and what it does.**
useState is a hook that you have to import from react. useStae allows the developer to create state in a funtional component. Prior, we had to convent a functional component to a class component. This makes it a whole lot easier on us.

**Let's get into it! How do we use this thing to create a like button?**
First, you will have to import it in your funtional component file. 
```
import React, { useState } from 'react';

function Example() {
  // ...
}

```

Next, we are going to name out funtion and start using useState.

```
import React, { useState } from 'react';


function LikeButton() {
const [count, setCount] = useState(0)

}

```

Woah woah woah. We did a lot there. Let's go over it:
We are defining a const count and a const setCount. Count is going to be the variable you call when you want to access the value of count in the state. You will use setCount to change the count. The 0 inside useState() is our inital state.

Now, lets create out like button.

```
import React, { useState } from 'react';


function LikeButton() {
const [count, setCount] = useState(0)
return (
<div>
{like}<button> like </button>
</div>
)

}
```


We've displayed the number of likes and created the button, now all we have to do is handle what happens when we click that button 

```
import React, { useState } from 'react';


function LikeButton() {
const [count, setCount] = useState(0)
return (
<div>
{like}<button onClick={() => setLike(like+1)}> like </button>
</div>
)

}
```

We are going to add an eventlistener, onClick. In onClick, we are going to change the value of like to like+1 using setLike.

**THEN BOOM!**


You have a working like button!




