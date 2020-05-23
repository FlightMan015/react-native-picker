# React Native Picker

Picker or Selector for React Native with **zero dependency** and **cross-platform**.

## [Changelog](https://github.com/rawewhat/react-native-paper/blob/master/CHANGELOG.md)

## Content

- [Install](#install)
- [Usage](#usage)
- [API](#api)
- [Example](#example)
- [License](#license)

## Install

using npm  
`npm install @rawewhat/react-native-paper`

using yarn  
`yarn add @rawewhat/react-native-paper`

## Usage

- just import Picker in any component you want to use it

`import { Picker } from '@rawewhat/react-native-picker'`  
`import Picker from '@rawewhat/react-native-picker'`

- then use it in your return function or render function

`return <Picker />`

## API

| Name               | Type           | Default                        | Description                                                                             |
| ------------------ | -------------- | ------------------------------ | --------------------------------------------------------------------------------------- |
| data               | array          | [{ label: "None", value: "" }] | Array of object to generate picker items.                                               |
| label              | string         | undefined                      | Label that show above the picker text.                                                  |
| labelField         | string         | "label"                        | Set this to tell Picker which object property to genrate picker item label.             |
| placeholder        | string         | "Press to select"              | When there is no selected value, placeholder text will be show.                         |
| title              | string         | "Picker"                       | Title of picker modal.                                                                  |
| value              | string         | undefined                      | Set this to control picker selected value.                                              |
| valueField         | string         | "value"                        | Set this to tell Picker which object property to use for getting selected value.        |
| canTouchOutside    | boolean        | true                           | Whether user can click outside picker modal to close.                                   |
| caretPng           | .png           | undefined                      | Caret icon in png format.                                                               |
| caretSvg           | component      | undefined                      | Caret icon in react-native-svg format.                                                  |
| disabled           | boolean        | undefined                      | Disable picker onPress event.                                                           |
| error              | boolean        | false                          | Show red border when there is error.                                                    |
| withLine           | boolean        | undefined                      | Show line below picker and picker modal title.                                          |
| height             | number\|string | 50                             | Height of the picker button.                                                            |
| modalElevation     | number         | 10                             | Control picker modal drop shadow and zIndex on Android.                                 |
| modalRadius        | number         | 10                             | Control picker modal top-left and top-right border radius.                              |
| overlayOpacity     | float          | 0.0                            | Control opacity of backdrop outside picker modal.                                       |
| pickerElevation    | number         | 2                              | Control picker button drop shadow and zIndex on Android.                                |
| pickerRadius       | number         | 5                              | Control picker button border radius.                                                    |
| spacing            | number         | 0                              | Control picker button margin bottom.                                                    |
| width              | number\|string | "auto"                         | Width of the picker button.                                                             |
| listProps          | object         | undefined                      | Override picker modal FlatList props.                                                   |
| listItemProps      | object         | undefined                      | Override picker modal FlatList item TouchableOpacity props.                             |
| modalProps         | object         | undefined                      | Override picker modal container View props.                                             |
| pickerProps        | object         | undefined                      | Override picker container TouchableOpacity props.                                       |
| style              | object         | undefined                      | Override picker container TouchableOpacity style.                                       |
| caretStyle         | object         | undefined                      | Override picker caret png or svg component style.                                       |
| itemTextStyle      | object         | undefined                      | Override picker modal item text style.                                                  |
| labelStyle         | object         | undefined                      | Override picker label text style.                                                       |
| lineStyle          | object         | undefined                      | Override picker button and picker modal title line <View /> style.                      |
| listContentStyle   | object         | undefined                      | Override picker modal FlatList contentContainer style.                                  |
| listSeparatorStyle | object         | undefined                      | Override picker modal FlatList ItemSeparator component style.                           |
| listStyle          | object         | undefined                      | Override picker modal FlatList style.                                                   |
| listTitleStyle     | object         | undefined                      | Override picker modal title <Text /> style.                                             |
| modalStyle         | object         | undefined                      | Override picker modal style.                                                            |
| overlayStyle       | object         | undefined                      | Override picker modal overlay style.                                                    |
| textStyle          | object         | undefined                      | Override picker text style.                                                             |
| onChange           | function       | undefined                      | Callback function when picker modal item pressed. `(item: object, index: number) => {}` |
| onClose            | function       | undefined                      | Callback function when picker modal closed.                                             |

## Example

```javascript
import React from "react";
import { StyleSheet, View } from "react-native";
import { Picker } from "@rawewhat/react-native-picker";

const data = [
  { id: "1", label: "Label 1", value: "value1" },
  { id: "2", label: "Label 2", value: "value2" },
];

const App = () => {
  const _handleChange = (item, index) => {
    console.log("_handleChange", item);
  };

  return (
    <View>
      <Picker data={data} onChange={_handleChange} />
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: "center",
    paddingHorizontal: 20,
  },
});

export default App;
```

## License

```
MIT License
-----------

Copyright (c) 2019 Cheng Sokdara (https://rawewhat-team.com)
Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
```