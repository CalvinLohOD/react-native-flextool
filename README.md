# react-native-flextool

## TOC

* [General Info](#general-info)
* [Installation](#installation)
* [Usage](#usage)
* [API](#api)
* [Release Notes](#release-notes)
* [react-native-web](#react-native-web)

## General Info

A React Native library for [Flex](https://github.com/FLEXTool/FLEX) (formally Flipboard FLEX) tool that is a must for iOS debugging.
The original tool just support iOS, but this wrapper make at least don't fail either for Android or Web.

Forked from https://github.com/fjtrujy/react-native-flipboard-flex with support for FLEX 4.x.

## Installation

Using npm:

```shell
npm install --save react-native-flextool
```

or using yarn:

```shell
yarn add react-native-flextool
```

## Usage

```js
var RNFlipboardFlex = import RNFlipboardFlex from 'react-native-flipboard-flex';
```

## API

| Method                                            | Return Type         |  iOS | Android | Since  |
| ------------------------------------------------- | ------------------- | :--: | :-----: | :-----: |
| [showExplorer()](#showExplorer)                     | `void`              |  ✅  |   ✅    | 1.0.0 |
| [hideExplorer()](#hideExplorer)                     | `void`              |  ✅  |   ✅    | 1.0.3 |
| [toggleExplorer()](#toggleExplorer)                 | `void`              |  ✅  |   ✅    | 1.0.3 |

---

### showExplorer()

Show Flex explorer.

**Examples**

```js
RNFlipboardFlex.showExplorer();

// iOS: Will Show the flex explorer
// Android: Will do nothing
```

### hideExplorer()

Hide Flex explorer.

**Examples**

```js
RNFlipboardFlex.hideExplorer();

// iOS: Will hide the flex explorer
// Android: Will do nothing
```

### toggleExplorer()

Will Show Flex explorer if it is hidden and will hide the exploer if it is shown.

**Examples**

```js
RNFlipboardFlex.toggleExplorer();

// iOS: Will toggle the flex explorer
// Android: Will do nothing
```

**Notes**

Please add the following line to your Podfile to exclude for Release builds.

```
pod 'FLEX', :configurations => ['Debug']
```

The library recognizes `DEBUG` and `BETA` preprocessors to include FLEX.

> See [Flex github](https://github.com/Flipboard/FLEX)

---


## Release Notes

See the [CHANGELOG.md](https://github.com/fjtrujy/react-native-flipboard-flex/blob/master/CHANGELOG.md).

## react-native-web

This library was made compatible with [react-native-web](https://github.com/necolas/react-native-web) by providing an empty polyfill in order to avoid breaking builds.