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
