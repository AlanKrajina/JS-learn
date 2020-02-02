* [React Native Basics](#React-Native-Basic)


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

#### Basic React Native `props`

- <Image/> - component

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

- <Text/> & <View/> - components

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
