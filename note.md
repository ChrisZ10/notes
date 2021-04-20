### 4/19/2021

### **Component Props** *[React]*
```Javascript
const Component = (props) => {
    ...
}
```

### **Tag Function** *[Javascript]*
```Javascript
const name = 'Alfred';
const age = 47;
 
function greet() {
    console.log(arguments[0]);
    console.log(arguments[1]);
    console.log(arguments[2]);
}

greet`I'm ${name}. I'm ${age} years old.`;
```

### **Flex Box** *[CSS]*
[A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) on CSS-Tricks

### **Set Up Footer** *[CSS]*
```scss
.container {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    .content {
        flex-grow: 1;
    }
}
```

### **CSS Units** *[CSS]*
`rem`: relative to font-size of the root element  
`em`: relative to the font-size of the element  
`vw`: relative to 1% of the width of the viewport  
`vh`: relative to 1% of the height of the viewport

### **CSS Modules** *[CSS]*
Change the file name from `file.css` to `file.module.css`.
In JS file, write code like this:
```Javascript
import * as headerStyles from 'header.module.css'
```

### **Mardown Newline** *[MD]*
Enter two space at the end of a line in .md file to start a new line.