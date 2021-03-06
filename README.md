# Modalize

[![npm version](https://badge.fury.io/js/react-native-modalize.svg)](https://badge.fury.io/js/react-native-modalize)

A highly customizable modal that loves scrolling content.

This component has been built with `react-native-gesture-handler` to address the common issue of **scrolling**, **swiping** and handling the **keyboard** behaviors, you can face with react-native's modal.

This component comes with a ScrollView, the default renderer, a FlatList or a SectionList. They are all three built-in and make your life easier, just pass your content and Modalize will handle the rest for you. You can also have the possibility to pass your own custom renderer.

<p align="left">
  <img src="https://user-images.githubusercontent.com/937328/59955680-22f6d200-947b-11e9-8744-991a728596df.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955681-22f6d200-947b-11e9-9288-9142e98ffae8.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955682-22f6d200-947b-11e9-8ed5-6a29042e72f1.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955683-22f6d200-947b-11e9-89e8-3608eea34e8d.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955684-22f6d200-947b-11e9-97d2-0687a29921db.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955685-238f6880-947b-11e9-81f9-6345fba118f5.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955686-238f6880-947b-11e9-896a-bcdb34e827b7.gif" height="450" />
  <img src="https://user-images.githubusercontent.com/937328/59955687-238f6880-947b-11e9-9345-55ea2bc8e458.gif" height="450" />
</p>

## Installation

```bash
yarn add react-native-modalize react-native-gesture-handler
npx pod-install ios
```

Check out the [guide](https://jeremybarbet.github.io/react-native-modalize/#/INSTALLATION) to complete the Android installation.

## Usage

Here is a quick example, using the default ScrollView renderer.

```tsx
import React, { useRef } from 'react';
import { View, Text, TouchableOpacity } from 'react-native';
import { Modalize } from 'react-native-modalize';

export const App = () => {
  const modalizeRef = useRef<Modalize>(null);

  const onOpen = () => {
    modalizeRef.current?.open();
  };

  return (
    <>
      <TouchableOpacity onPress={onOpen}>
        <Text>Open the modal</Text>
      </TouchableOpacity>

      <Modalize ref={modalizeRef}>...your content</Modalize>
    </>
  );
};
```

## Documentation

Please check out the full [documentation available here](https://jeremybarbet.github.io/react-native-modalize) to find all about the props, methods and examples of Modalize's usage.
