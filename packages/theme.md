# react-native-theme

A HOC for theming your react-native app



## Installation

**Using yarn**  
`$ yarn add @postillon/react-native-theme`

**Using npm**  
`$ npm install @postillon/react-native-theme --save`



## Example

Try it on [Expo](https://snack.expo.io/@danielang/react-native-theme).


## Usage

This part of the documentation is missing. If you need it please create an issue or if you want to contribute create a pull request.


## API

### ThemeManger

**Methods**

`addStyleSheet(stylesheet: StyleSheet, component: string, theme: string = 'default'): void`

`getStyleSheetForComponent(component: string, theme: string = 'default'): StyleSheet`

`addConstants(constants: object, theme: string): void`

`getConstantsForTheme(theme: string): object`


### ThemeProvider

**Props**

`theme: string` -> Name of the theme, which is registered in the ThemeManager.


### connectStyle

```javascript
connectStyle('style', {
    // options
    themePropsName: 'theme',
    stylesPropsName: 'styles',
    constantsPropsName: 'constants',
    callback: (nextTheme, ownProps) => {},
})(ScreenComponent)
```
