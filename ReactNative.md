* [React Native Basics](#React-Native-Basic)
* [Props](#Props)
* [State](#State)


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
