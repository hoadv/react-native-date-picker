<p align="center">
  <img src="https://github.com/DieTime/react-native-date-picker/raw/master/assets/logo.png" style="margin-bottom: -30px" width="320"/>
</p>

<p align="center">
    <a href="https://snack.expo.dev/@hoavd106/react-native-date-picker">🎯 Try component at snack.expo.io</a>
</p>

<p align="center">
    <img src="https://img.shields.io/badge/Runs%20with%20Expo-000.svg?style=flat&logo=EXPO&labelColor=ffffff&logoColor=000" alt="npm type definitions"/>
    <img src="https://img.shields.io/npm/types/@hoadv/react-native-date-picker" alt="npm type definitions"/>
    <img src="https://img.shields.io/bundlephobia/min/@hoadv/react-native-date-picker" alt="npm bundle size"/>
</p>

React Native customizable date picker component for iOS and Android. Designed using ScrollView. Looks identical on all
devices. Support more month formats (January, Jan...)

## 💻 Example
<img style="margin-top: 10px" src="https://github.com/DieTime/react-native-date-picker/raw/master/assets/example.gif" height="400" alt="component-gif-preview"/>

## 💬 Installation

1. *Add dependencies to the project*

    ```bash
    yarn add @hoadv/react-native-date-picker
    
    npm install @hoadv/react-native-date-picker --save
    ```

2. *Install additional dependencies*

    ```bash
    yarn add expo-linear-gradient
    
    npm install expo-linear-gradient --save
    ```

3. *Then, import with ...*

    ```js
    import DatePicker from '@hoadv/react-native-date-picker';
    ```

4. *If you are not using Expo*
   > You should also follow these additional [installation instructions](https://github.com/expo/expo/tree/master/packages/expo-linear-gradient#installation-in-bare-react-native-projects).

## 👩‍💻 Usage

- *Simple code example*
    ```javascript
    import React, {useState} from "react";
    import {Text, View} from "react-native";
    
    import DatePicker from "@hoadv/react-native-date-picker";
    
    export default function App() {
        const [date, setDate] = useState();
    
        return (
            <View>
                <Text>{date ? date.toDateString() : "Select date..."}</Text>
                <DatePicker
                    value={date}
                    onChange={(value) => setDate(value)}
                    format="yyyy-MM-dd"
                />
            </View>
        );
    }
    ```

## 📚 Documentation

| Prop       | Required | Type                      | Description                                                   |
|:---------- |:--------:|:------------------------- | ------------------------------------------------------------- |
| value      | ✅        | Date or null or undefined | Initial date for component                                    |
| onChange   | ✅        | (value: Date) : void      | Callback on date change event                                 |
| height     | ⛔        | number                    | Custom component height                                       |
| width      | ⛔        | number or string          | Custom component width such as `100` or `'50%'`                   |
| fontSize   | ⛔        | number                    | Custom digits font size                                       |
| textColor  | ⛔        | string                    | Custom digits text color such as hex, rgb or rgba             |
| endYear    | ⛔        | number                    | Max year in component, default is current year                |
| startYear  | ⛔        | number                    | Min year in component, default is `endYear - 100`             |
| markColor  | ⛔        | string                    | Custom middle mark color such as `hex`, `rgb` or `rgba`             |
| markHeight | ⛔        | number                    | Custom height of middle mark                                  |
| markWidth  | ⛔        | number or string          | Custom width of middle mark such as `100` or `'50%'`              |
| fadeColor  | ⛔        | string                    | Custom color for top and bottom fade effect `only hex colors!` |
| format     | ⛔        | string                    | Custom picker format like reshuffle of `yyyy`, `mm`, `dd`, `MM`, `M`. Example: `'yyyy-mm-dd'` or `'dd-mm-yyyy'` and other |

## 📂 Project Layout

- [`example`](/example) *Simple project with date picker. It is presented on gif.*
- [`src`](/src) *Source code of date picker.*
- [`lib`](/lib) *Shared packages.*
    - [`commonjs`](/lib/commonjs) *Package built as common js library.*
    - [`module`](/lib/module) *Package built as module.*
    - [`typescript`](/lib/typescript) *Built files for static typing.*

## 📃 License

Source code is made available under the [MIT license](LICENSE.md). Some dependencies may be licensed differently.

## ☕ Support

You can support me so that there will be more good open source projects in the future
<p align="center" style="padding: 10px 0 20px 0">
  <a href="https://www.buymeacoffee.com/hdcoder" target="_blank">
    <img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="50" width="220">
  </a>
</p>
