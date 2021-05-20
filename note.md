[4/19/2021](#4-19-2021)  
[4/20/2021](#4-20-2021)  
[4/21/2021](#4-21-2021)  
[4/22/2021](#4-22-2021)  
[5/10/2021](#5-10-2021)  
[5/12/2021](#5-12-2021)  
[5/15/2021](#5-15-2021)

### 4-19-2021

---

### **Component Props** *[React]*
```Javascript
const Component = (props) => {
    ...
}
```
Or you can destructure it by coding like this:
```Javascript
const Component = ({ data }) => {
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
>The main reason to use tag functions is actually that they look very clean and at the same time give you the ability to ***handle the strings and arguments in a variable way.***  
[Reference](https://typesafe.blog/article/the-logic-behind-javascript-tag-functions)

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
>Common browser default is 16px

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

### 4-20-2021

---

### **module.exports vs exports** *[JS]*
Remember: `module.exports` wins  
[The difference between module.exports and exports](https://blog.tableflip.io/the-difference-between-module-exports-and-exports/)
![Illustration](https://ucarecdn.com/af1c810c-72f4-43cb-a0da-fcd67bed2a80/initial.svg)

### **Useful Gatsby Plugins** *[Gatsby]*
- [gatsby-source-filesystem](https://www.gatsbyjs.com/plugins/gatsby-source-filesystem/?=gatsby-source-f)  
A Gatsby source plugin for sourcing data into your Gatsby application from your local filesystem.
- [gatsby-transformer-remark](https://www.gatsbyjs.com/plugins/gatsby-transformer-remark/?=gatsby-transformer)  
Parses Markdown files using `Remark`

### **gatsby-node-js** *[Gatsby]*
Code in the file gatsby-node.js is run once in the process of building your site. You can use its APIs to create pages dynamically, add data into GraphQL, or respond to events during the build lifecycle.  
[Reference](https://www.gatsbyjs.com/docs/reference/config-files/gatsby-node/)

### **Frontmatter for Metadata in Markdown Files** *[MD]*
When you create a Markdown file, you can include a set of key value pairs that can be used to provide additional data relevant to specific pages in the GraphQL data layer. This data is called frontmatter and is denoted by the triple dashes at the start and end of the block. This block will be parsed by gatsby-transformer-remark as frontmatter. The GraphQL API will provide the key value pairs as data in your React components.  

What is important in this step is the key pair slug. The value that is assigned to the key slug is used in order to navigate to your post.  
[Reference](https://www.gatsbyjs.com/docs/how-to/routing/adding-markdown-pages/)

### **Disable Git Credential Manager** *[Git]*
[How do I disable Git Credential Manager for Windows?](https://stackoverflow.com/questions/37182847/how-do-i-disable-git-credential-manager-for-windows) on Stack Overflow

### 4-21-2021

---

### **createPages** *[Gatsby]*
Create pages dynamically. This extension point is called only after the initial sourcing and transformation of nodes plus creation of the GraphQL schema are complete so you can query your data in order to create pages.

### **GraphQL Variables and Arguments** *[GraphQL]*
Example:
```graphql
query($id: ID!) { //variables
        wpContent {
            post(id: $id) { //arguments
                title
                content
            }
        }
    }
```

### **dangerouslySetInnerHTML** *[React]*
`dangerouslySetInnerHTML` is React’s replacement for using `innerHTML` in the browser DOM. In general, setting HTML from code is risky because it’s easy to inadvertently expose your users to a cross-site scripting (XSS) attack. So, you can set HTML directly from React, but you have to type out dangerouslySetInnerHTML and pass an object with a `__html` key, to remind yourself that it’s dangerous.

### **Useful Gatsby Plugins** *[Gatsby]*
- [gatsby-plugin-sharp](https://www.gatsbyjs.com/plugins/gatsby-plugin-sharp/?=sharp)  
Exposes several image processing functions built on the Sharp image processing library. This is a low-level helper plugin generally used by other Gatsby plugins. You generally shouldn’t be using this directly.
- [gatsby-remark-images](https://www.gatsbyjs.com/plugins/gatsby-remark-images/?=images)  
Processes images in markdown so they can be used in the production build.
- [gatsby-remark-relative-images](https://www.gatsbyjs.com/plugins/gatsby-remark-relative-images/?=relative)  
Convert image src(s) in markdown/html/frontmatter to be relative to their node’s parent directory.

### **Fetch Specific WordPress Post** *[GraphQL]*
```JS
export const query = graphql`
    query($id: ID!) {
        wpContent {
            post(id: $id) {
                title
                content
            }
        }
    }
`;
```

### **Git Pull** *[Git]*
[Article about Git Pull](https://www.atlassian.com/git/tutorials/syncing/git-pull) on Bitbucket  
![Illustration](https://wac-cdn.atlassian.com/dam/jcr:00d011ed-03dc-440f-afc5-9b13d5e14fbf/bubble%20diagram-01.svg?cdnVersion=1568)
![Illustration](https://wac-cdn.atlassian.com/dam/jcr:b3a663dc-1985-40df-b0a5-c6bcbacd71af/bubble%20diagram-02.svg?cdnVersion=1568)

### 4-22-2021

### **React Helmet** *[React]*
Manage all of your changes to the document head.  
[Reference](https://www.npmjs.com/package/react-helmet)  
Gatsby plugin for using react-helmet:  
[gatsby-plugin-react-helmet](https://www.gatsbyjs.com/plugins/gatsby-plugin-react-helmet/)

### 5-10-2021

### **CSS Attribute Selector** *[CSS]*
![Exactly Equal](https://i1.wp.com/css-tricks.com/wp-content/uploads/2020/06/rel-equals.png?w=570&ssl=1)
![Contains](https://i1.wp.com/css-tricks.com/wp-content/uploads/2020/06/rel-anywhere.png?w=570&ssl=1)
![Begins With](https://i0.wp.com/css-tricks.com/wp-content/uploads/2020/06/rel-begins.png?w=570&ssl=1)
![Ends With](https://i2.wp.com/css-tricks.com/wp-content/uploads/2020/06/rel-ends.png?w=570&ssl=1)
![Within Space Separated List](https://i0.wp.com/css-tricks.com/wp-content/uploads/2020/06/rel-space.png?w=570&ssl=1)
![Within Dash Separated List](https://i1.wp.com/css-tricks.com/wp-content/uploads/2020/06/rel-dash.png?w=570&ssl=1) 

[Reference](https://css-tricks.com/attribute-selectors/)

### **Absolute, Relative, and Fixed Positioning** *[CSS]*
There are two other things that happen when you set position: relative; on an element that you should be aware of. One is that it `introduces the ability to use z-index on that element`, which doesn’t work with statically positioned elements. Even if you don’t set a z-index value, this element will now appear on top of any other statically positioned element.

The other thing that happens is `it limits the scope of absolutely positioned child elements`. Any element that is a child of the relatively positioned element can be absolutely positioned within that block.  
[Absolute, Relative, Fixed Positioning: How do they differ?](https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/)

### 5-12-2021

### **Commonly Used CSS Syntax** *[CSS]*
```scss
background: linear-gradient(120deg, white, black);

transform: skew(120deg) translate(50%, 50%) rotateZ(60deg);

mix-blend-mode: multiply;

@keyframes animation-name {
    0% {
        /* status at that point */
    }
    100% {

    }
    ...
}
animation: animation-name 3s forwards;

transition: property 3s ease-in-out;
```

### **GSAP Basics** *[GSAP]*
A `Tween` is what does all the animation work - think of it like a high-performance property setter. You feed in targets (the objects you want to animate), a duration, and any properties you want to animate and when its playhead moves to a new position, it figures out what the property values should be at that point applies them accordingly.
```JS
gsap.to(".box", {rotation: 27, x: 100, duration: 1});
```

### 5-15-2021

### **GSAP ScrollTrigger** *[GSAP]*
```JS
let tl = gsap.timeline({
    scrollTrigger: {
        trigger: ".className",
        start: "top 50%", // when the top of the trigger hits 50% down from the top of the viewport
        end: () => "+=" + document.querySelector(".className").offsetWidth * 2, // a function to dynamically calculate the value
        scrub: 1
    }
});
tl.to(".className", {x: 400, rotate: 360, ease: "none", duration: 3});
```

### **GSAP Text** *[GSAP]*
```JS
const tl = gsap.timeline({
    paused: true    
});
tl.to(".textSelector", {
    text: {
        value: "new text"
    },
    duration: 3,
    ease: "none"
});
document.querySelector(".buttonSelector").onclick = () => {
    tl.play();
}
```

### **CSS Grid Layout** *[CSS]*
To get started you have to define a `container element` as a grid with `display: grid`, set the column and row sizes with `grid-template-columns` and `grid-template-rows`, and then place its child elements into the grid with `grid-column` and `grid-row`.

**Important terminology**:  
`Grid Container` (Direct parent of all the grid items), `Grid Line`, `Grid Track` (The space between two adjacent grid lines), `Grid Area` (The total space surrounded by four grid lines), `Grid Item` (Direct descendants of the grid container), `Grid Cell` (The space between two adjacent row and two adjacent column grid lines).

**grid-template-columns  
grid-template-rows**  
```css
.container {
  grid-template-columns: [first] 40px [line2] 50px [line3] auto [col4-start] 50px [five] 40px [end];
  grid-template-rows: [row1-start] 25% [row1-end] 100px [third-line] auto [last-line];
}

/* a line can have more than one name */ 
.container {
  grid-template-rows: [row1-start] 25% [row1-end row2-start] 25% [row2-end];
}

.container {
  grid-template-columns: repeat(3, 20px [col-start]);
}
/* is equivalent to */
.container {
  grid-template-columns: 20px [col-start] 20px [col-start] 20px [col-start];
}

/* If multiple lines share the same name, they can be referenced by their line name and count */
.item {
  grid-column-start: col-start 2;
}

/* The fr unit allows you to set the size of a track as a fraction of the free space of the grid container */
.container {
  grid-template-columns: 1fr 1fr 1fr;
}

/* The free space is calculated after any non-flexible items */
.container {
  grid-template-columns: 1fr 50px 1fr 1fr;
} /* the free space doesn't include the 50px */
```

### **space-around/space-between/space-evenly**
`space-around`: items are evenly distributed in the line with equal space around them.   
`space-between`: items are evenly distributed in the line; first item is on the start line, last item on the end line.  
`space-evenly`: items are distributed so that the spacing between any two adjacent alignment subjects, before the first alignment subject, and after the last alignment subject is the same.  

### **inline-size/block-size**
`inline-size`:   
- The inline-size CSS property defines the horizontal or vertical size of an element's block, depending on its writing mode. It corresponds to either the width or the height property, depending on the value of writing-mode.   
- If the writing mode is vertically oriented, the value of inline-size relates to the height of the element; otherwise, it relates to the width of the element.   

`block-size`:   
the corresponding axis

### **SVG**
`Scalable Vector Graphics (SVG)` are an XML-based markup language for describing two-dimensional based vector graphics. As such, it's a `text-based`, open Web standard for describing images that can be rendered cleanly at any size and are designed specifically to work well with other web standards including CSS, DOM, JavaScript, and SMIL. SVG is, essentially, to graphics what HTML is to text.

### **:root**
The `:root CSS pseudo-class` matches the **root element of a tree representing the document**. `In HTML, :root represents the html element and is identical to the selector html`, except that **its specificity is higher**.