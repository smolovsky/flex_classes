# FlexClasses

This gem provides set of CSS classes which adds related CSS properties to dom element

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'flex_classes'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install flex_classes

After it import 'flex_classes' into your sass stylesheet

```sass
@import 'flex_classes'
```

## Usage

### Align child nodes at middle
**HTML**

```html
<div class="flex row middle">
```

**HAML**

```haml
.flex.row.middle
```

### Add vertical margins, allow wrap, align child nodes at center middle with margins

**HAML**
```haml
.flex.row.center.middle.m-v.childs-m.can-wrap
```


## List all classes

### Base
class | description
---   | ---
flex  | display: flex; and allow to use all other classes
row   | flex-direction: row
col   | flex-direction: column


### Align
These classes works only with "row" or "col" class.
Distribute content of flex col/row at middle/center/bottom/top of container frame.

class | description
--- | ---
center   | same as "text-align: center": "justify-content: center" for rows and "align-items: center" for cols
middle   | same as "vertical-align: middle": "align-items: center" for rows and "justify-content: center" for cols
top      | "align-items: flex-start" for rows and "justify-content: flex-start" for cols
bottom   | "align-items: flex-end" for rows and "justify-content: flex-end" for cols
stretch  | full width for flex-col and full height for flex-row


### Margins
class | description
--- | ---
m         | all sides
m-v       | vertical
m-h       | horizontal
m-top     | only top
m-bottom  | only bottom


### Margins for child nodes
class | description
--- | ---
childs-m    | all sides
childs-m-h  | horizontal for children 
childs-m-v  | vertical for children 


### Paddings
class | description
--- | ---
p         | all sides
p-v       | vertical
p-h       | horizontal
p-top     | only top
p-bottom  | only bottom


### Other
class | description
--- | ---
can-wrap      | flex-wrap: wrap
space-between | justify-content: space-between
eq-childs     | element > * { flex: 1 1; }


## Customizing values of margin and padding
You can set next variables in your app stylesheet before @import 'flex_classes':

+ $flex-classes-margin-vertical: 6px
+ $flex-classes-margin-horizontal: 10px
+ $flex-classes-padding-vertical: 6px
+ $flex-classes-padding-vertical: 10px


## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/smolovsky/flex_classes
