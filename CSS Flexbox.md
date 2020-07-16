20200625125108

### CSS Flexbox

used to auto structure items on a webpage
to use, enclose items in a div with css property `display: flex;`

by default (flex-direction: row), **main-axis is x** and **cross-axis is y**

#### important properties:

spacing and positioning related to the **main-axis**:
`justify-content`: flex-start, flex-end, center, space-between, space-around, initial (inherit from parent).

`align-items`use this for the **cross-axis behavior** of items, values include same as above. If default flex-direction (row) then 
—

`flex-direction`
`flex-wrap`
–
use `flex-grow`, `flex-shrink`,  and `flex-basis:0`to make items some multiple greater than another, e.g. flex-grow: 3 flex-grow: 1

flex: <grow> <shrink> <basis>  /* shorthand for items inside flex container*/

ex:
![flexbox.png](flexbox.png)


src: [https://www.youtube.com/watch?v=fYq5PXgSsbE](https://www.youtube.com/watch?v=fYq5PXgSsbE)

#css #web #webdev #code