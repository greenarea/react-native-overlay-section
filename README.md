## react-native-overlay-section
Without linking. Сompatible with expo.

![](https://github.com/greenarea/react-native-overlay-section/blob/master/assets/example.gif)
https://github.com/greenarea/react-native-overlay-section
## Usage example

```
npm i react-native-overlay-section --save
```

```javascript
import React, { Component } from 'react';
import {
    View,
    Text,
} from 'react-native';
import SlideUp from 'react-native-overlay-section';

export default class App extends Component {

    constructor (props) {
        super(props);
    }
    
    exampleContent = () => {
        return (
            <View>
                <Text>This is test text</Text>
            </View>
        )
    }
    
    render() {
        return (
            <View style={{flex: 1}}>
                <Text>Hello</Text>
                <SlideUp contentSection={this.exampleContent()} />
            </View>
        )
    }
}
```

| props           | type | description |
|-----------------|------|-------------|
| visibleHeight   | PropTypes.number     | Height of all visible content include dragSection            |
| draggableHeight | PropTypes.number     | Height of dragSection            |
| contentSection  | PropTypes.object     | Pass your custom object to render it            |
| dragSection     | PropTypes.object     | Section with PanResponder            |
| dragBgColor     | PropTypes.string     | Background color of dragSection            |
| contentSectionBgColor  | PropTypes.string     | backgroundColor of contentSection            |
| dragArrowColor  | PropTypes.string     | Color of default arrow            |

All props are not required*