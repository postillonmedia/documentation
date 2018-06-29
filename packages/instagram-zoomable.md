# react-native-instagram-zoomable

A component to implement the Instagram Zoom-Draggable-Effect for any component in React-Native.



## Installation

**Using yarn**

`$ yarn add @postillon/react-native-instagram-zoomable`

**Using npm**

`$ npm install @postillon/react-native-instagram-zoomable --save`



## Example

Try it on [Expo](https://snack.expo.io/@danielang/react-native-instagram-zoomable).



## Usage

```javascript
import React, { Component } from 'react';
import { Image, Text, View, StyleSheet, ScrollView } from 'react-native';
import { Card } from 'react-native-elements';

import AssetExample from './components/AssetExample';

import { InstagramProvider, ElementContainer } from '@postillon/react-native-instagram-zoomable';


export default class App extends Component {
  render() {
    return (
      <InstagramProvider>
        <View style={{flex: 1}}>
          <Text>Pitch to zoom the Cards in the ScrollView below:</Text>

          <ScrollView>
            <ElementContainer key={'card-1'}>
              <Card title="Local Modules">
                <AssetExample />
              </Card>
            </ElementContainer>

            <ElementContainer key={'card-2'}>
              <Card title="Local Modules">
                <AssetExample />
              </Card>
            </ElementContainer>

            <Card title="Only the content" key={'card-3'}>
              <ElementContainer>
                <AssetExample />
              </ElementContainer>
            </Card>

            <Card title="Only the Image" key={'card-4'}>
              <ElementContainer>
                <Image style={{backgroundColor: "#056ecf", flex: 1, alignSelf: 'center'}} source={require("./assets/expo.symbol.white.png")} />
              </ElementContainer>
            </Card>

          </ScrollView>
        </View>
      </InstagramProvider>
    );
  }
}
```



## API

### InstagramProvider
**Props**

`children`

`renderBackground` -> _(selected , scaleValue, gesturePosition) => React.Component_



### ElementContainer
**Props**

`children`



## Thank you

Thank you to [Audy Tanudjaja](https://medium.com/@audytanudjaja) and his article on Medium: [React Native UI Challenge: Building Instagram Zoom-Draggable Photo](https://medium.com/@audytanudjaja/react-native-ui-challenge-building-instagram-zoom-draggable-photo-9127413b1d29)