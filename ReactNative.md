* [React Native Basics](#React-Native-Basic)
* [Props](#Props)
* [State](#State)
* [Style](#Style)
* [Fixed Dimensions](#Fixed-Dimensions)
* [Flex Dimensions](#Flex-Dimensions)
* [Layout with Flexbox](#Layout-with-flexbox)


### React Native Basic

React Native is like React, but it uses `native components` instead of `web components` as building blocks.

```jsx
import React, { Component } from 'react';
import { Text, View } from 'react-native';

export default class HelloWorldApp extends Component {

  render() {
    return (
      <View style={{ flex: 1, justifyContent: "center", alignItems: "center" }}>
        <Text>Hello, world!</Text>
      </View>
    );
  }
}
```

#### Props

##### Image - component

```jsx
import React, { Component } from 'react';
import { Image } from 'react-native';

export default class Bananas extends Component {

  render() {
    let pic = {
      uri: 'https://upload.wikimedia.org/wikipedia/commons/d/de/Bananavarieties.jpg'
    };
    
    return (
      <Image source={pic} style={{width: 193, height: 110}}/>                 // image component
    );
  }
```

##### Text & View - components

```jsx
import React, { Component } from 'react';
import { Text, View } from 'react-native';                        


export default class LotsOfGreetings extends Component {
  render() {
    return (
      <View style={{alignItems: 'center', top: 50}}>
        <Greeting name='Rexxar' />                                  // sending props 
        <Greeting name='Jaina' />
        <Greeting name='Valeera' />
      </View>
    );
  }
}


class Greeting extends Component {
  render() {
    return (
      <View style={{alignItems: 'center'}}>                         // view component
        <Text>Hello {this.props.name}!</Text>                       // text component
      </View>
    );
  }
}
```

#### State

For data that is going to change, we have to use `state`.

In general, you should initialize state in the `constructor`, and then call `setState` when you want to change it.

```jsx
import React, { Component } from 'react';
import { Text, View } from 'react-native';

export default class BlinkApp extends Component {
  render() {
    return (
      <View>
        <Blink text='I love to blink' />
        <Blink text='Yes blinking is so great' />
        <Blink text='Why did they ever take this out of HTML' />
        <Blink text='Look at me look at me look at me' />
      </View>
    );
  }
}


class Blink extends Component {

  componentDidMount(){                           // on mounting this function is called                                             
    setInterval(() => (                          
      this.setState(previousState => (                    // sets new STATE with previous state
        { isShowingText: !previousState.isShowingText }
      ))
    ), 1000);                                    // Toggle the state every second 
  }

  //state object
  state = { isShowingText: true };               // initial state

  render() {
    if (!this.state.isShowingText) {
      return null;
    }

    return (
      <Text>{this.props.text}</Text>
    );
  }
}
```


### Style

The `style` prop can be a plain old `JavaScript object`. That's the simplest and what we usually use for example code. You can also pass an `array of styles` - the last style in the array has precedence, so you can use this to inherit styles.

As a component grows in complexity, it is often cleaner to use `StyleSheet.create` to define several styles in one place. Here's an example:

```jsx
import React, { Component } from 'react';
import { StyleSheet, Text, View } from 'react-native';

const styles = StyleSheet.create({                        // StyleSheet.create
  bigBlue: {
    color: 'blue',
    fontWeight: 'bold',
    fontSize: 30,
  },
  red: {
    color: 'red',
  },
});

export default class LotsOfStyles extends Component {
  render() {
    return (
      <View>
        <Text style={styles.red}>just red</Text>                         // object
        <Text style={styles.bigBlue}>just bigBlue</Text>
        <Text style={[styles.bigBlue, styles.red]}>bigBlue, then red</Text>   // array
        <Text style={[styles.red, styles.bigBlue]}>red, then bigBlue</Text>
      </View>
    );
  }
}

```


### Fixed Dimensions

- `width`, `height`

```jsx
import React, { Component } from 'react';
import { View } from 'react-native';

export default class FixedDimensionsBasics extends Component {
  render() {
    return (
      <View>
        <View style={{width: 50, height: 50, backgroundColor: 'powderblue'}} />
        <View style={{width: 100, height: 100, backgroundColor: 'skyblue'}} />
        <View style={{width: 150, height: 150, backgroundColor: 'steelblue'}} />
      </View>
    );
  }
}

```

### Flex Dimensions

- `flex`

Use `flex` in a component's style to have the component expand and shrink dynamically based on available space. Normally you will use `flex: 1`, which tells a component to fill all available space, shared evenly amongst other components with the same parent. The larger the `flex` given, the higher the ratio of space a component will take compared to its siblings.

```jsx
import React, { Component } from 'react';
import { View } from 'react-native';

export default class FlexDimensionsBasics extends Component {
  render() {
    return (
      // Try removing the `flex: 1` on the parent View.
      // The parent will not have dimensions, so the children can't expand.
      // What if you add `height: 300` instead of `flex: 1`?
      <View style={{flex: 1}}>
        <View style={{flex: 1, backgroundColor: 'powderblue'}} />
        <View style={{flex: 2, backgroundColor: 'skyblue'}} />
        <View style={{flex: 3, backgroundColor: 'steelblue'}} />
      </View>
    );
  }
}
```
https://facebook.github.io/react-native/docs/height-and-width


### Layout with Flexbox

https://facebook.github.io/react-native/docs/flexbox

You will normally use a combination of `flexDirection`, `alignItems`, and `justifyContent` to achieve the right layout.

#### Flex

`flex` will define how your items are going to “fill” over the available space along your main axis. Space will be divided according to each element's flex property.

#### Flex Direction

`flexDirection` controls the direction in which the children of a node are laid out. This is also referred to as the main axis. The cross axis is the axis perpendicular to the main axis, or the axis which the wrapping lines are laid out in.

`row` Align children from left to right. If wrapping is enabled then the next line will start under the first item on the left of the container.

`column` (default value) Align children from top to bottom. If wrapping is enabled then the next line will start to the left first item on the top of the container.

`row-reverse` Align children from right to left. If wrapping is enabled then the next line will start under the first item on the right of the container.

`column-reverse` Align children from bottom to top. If wrapping is enabled then the next line will start to the left first item on the bottom of the container.

```jsx
import React, { Component } from 'react';
import { View } from 'react-native';

export default class FlexDirectionBasics extends Component {
  render() {
    return (
      // Try setting `flexDirection` to `column`.
      <View style={{flex: 1, flexDirection: 'row'}}>                                    // row -> from left to right
        <View style={{width: 50, height: 50, backgroundColor: 'powderblue'}} />
        <View style={{width: 50, height: 50, backgroundColor: 'skyblue'}} />
        <View style={{width: 50, height: 50, backgroundColor: 'steelblue'}} />
      </View>
    );
  }
};
```

#### Layout Direction

`LTR` (default value) Text and children are laid out from left to right. Margin and padding applied the start of an element are applied on the left side.

`RTL` Text and children are laid out from right to left. Margin and padding applied the start of an element are applied on the right side.

#### Justify Content

`flex-start`(default value) Align children of a container to the start of the container's main axis.

`flex-end` Align children of a container to the end of the container's main axis.

`center` Align children of a container in the center of the container's main axis.

`space-between` Evenly space of children across the container's main axis, distributing remaining space between the children.

`space-around` Evenly space of children across the container's main axis, distributing remaining space around the children. Compared to space-between using space-around will result in space being distributed to the beginning of the first child and end of the last child.

`space-evenly` Evenly distributed within the alignment container along the main axis. The spacing between each pair of adjacent items, the main-start edge and the first item, and the main-end edge and the last item, are all exactly the same.

```jsx
import React, { Component } from 'react';
import { View } from 'react-native';

export default class JustifyContentBasics extends Component {
  render() {
    return (
      <View style={{                          // parent component
        flex: 1,
        flexDirection: 'column',
        justifyContent: 'space-between',
      }}>
      
        <View style={{width: 50, height: 50, backgroundColor: 'powderblue'}} />
        <View style={{width: 50, height: 50, backgroundColor: 'skyblue'}} />
        <View style={{width: 50, height: 50, backgroundColor: 'steelblue'}} />
        
      </View>
    );
  }
};
```

#### Align Items
`stretch` (default value) Stretch children of a container to match the height of the container's cross axis.

`flex-start` Align children of a container to the start of the container's cross axis.

`flex-end` Align children of a container to the end of the container's cross axis.

`center` Align children of a container in the center of the container's cross axis.

`baseline` Align children of a container along a common baseline. Individual children can be set to be the reference baseline for their 
parents.

#### Align Self
`allign-self`

#### Align Content
`allignContent`

#### Flex Wrap
`flexWrap`

#### Flex Basis, Grow, and Shrink
`flexGrow`

`flexShink`

`flexBasis`
