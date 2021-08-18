# Google Summer of Code 2021

<div align='center'>
<img src='assets/header.png' width='900'/>
</div>

## 📑 Project Details

- Organization: [React Native Elements](https://github.com/react-native-elements)

- Project: [Migrating Hooks, Tests & APIs](https://summerofcode.withgoogle.com/projects/#5514659471294464)

- Mentors: [Jeremy Hamilton](https://github.com/flyingcircle), [Pranshu Chittora](https://github.com/pranshuchittora), [Dhruvdutt](https://github.com/dhruvdutt)

- Student: [Arpit Bhalla](https://github.com/arpitBhalla)

## 🚀 Overview

The **Google Summer of Code 2021** has been a fantastic and cheerful learning experience for me over the past few months. I have learned a lot from the community, especially how to organize commits and write readable code. **React Native Elements** is an amazing community to work with, as mentors are really helpful and experienced. I had started contributing to React Native Elements from March 2021 and till now, I have 40+ commits (10,803 additions and 13,826 deletions) merged. Over the past few months, I had great exposure writing maintainable code, communicating with the mentors, etc. I had completed some of my work in the coding period started as some issues mentioned in my proposal had a high priority for the release.

<div align='center'>
<img src='assets/contri.png' width='900' />
</div>

## 🚘 Work Abstract

### Refactor components to use `Pressable` API [(#3170)](https://github.com/react-native-elements/react-native-elements/pull/3170)

> `Pressable` is preferred to `Touchable` components according to React Native official docs. `Pressable` component offers a more extensive and future-proof way of handling the touch-based inputs.

- `Touchable` Component:

  - It includes the styles and effects that do not meet the platform interactions.
  - It does not support high-quality interaction experience on different platforms.

- `Pressable` Component:

  - It detects various types of interactions.
  - Its API provides direct access to the current state of interaction.
  - Its capabilities could be extended to include hover, blur, focus, and more.
    `Pressable` contains a lot of new props and cool features such as:
    delayLongPress: Duration in milliseconds from onPressIn by the time onLongPress is called.

Reference : [Pressable vs. Touchable in React Native](https://medium.com/@mahyarmohammadi/react-native-pressable-vs-touchable-5fec6b332f15)

### Migrate Tests to React Native Testing Library

> Rather than tests focusing on the implementation (Enzyme), tests are more focused on user behavior (react-native-testing-library).

Enzyme allows us to access the internal workings of your components. You can read and set the state, and we can mock children to make tests run faster. On the other hand, RN testing-library doesn't give us any access to the implementation details. It renders the components and provides utility methods to interact with them. The idea is that you should communicate with our application in the same way a user would. So rather than set the state of a component we reproduce the actions a user would do to reach that state.

### Class to Functions Migration

Some components like **Input, Image, ToolTip, Search Bar** which further include SearchBar android & SearchBar iOS were Class Components and the code was messy, These are migrated to Functional Components and added hooks like, useState, useEffect, useCallBack, which would increase performance.

- **Using classes** - We need to describe lifecycle methods, state of the component, component’s methods that will change our state or work with the store. Also, we need to bind all the methods for the component instance. The component becomes large, and it becomes more difficult to read each time.
- **Using hooks** - We can get the state of the component so that it can be easily tested and reused. Now we can facilitate the exchange of links between components or our entire application - using hooks. Hooks allow you to encapsulate logic without affecting the hierarchy of components.

## 🎊 Contributions

### Some new components

- [Added New component: LinearProgress (#2867)](https://github.com/react-native-elements/react-native-elements/pull/2867)
- [Added New Component: FAB (#2885)](https://github.com/react-native-elements/react-native-elements/pull/2885)
- [Added New Component: Speed dial (#2896)](https://github.com/react-native-elements/react-native-elements/pull/2896)
- [Added New Component: Tab & TabItem (#2919)](https://github.com/react-native-elements/react-native-elements/pull/2919)
- [Added New Component: CircularSlider (#1)](https://github.com/react-native-elements/react-native-elements-universe/pull/1)
- [Added New Component: TabView & TabView.Item (#2983)](https://github.com/react-native-elements/react-native-elements/pull/2983)
- [Added New Sub Component: ListItem Accordion (#2953)](https://github.com/react-native-elements/react-native-elements/pull/2953)
- [Added New Sub Component: ListItem Swipeable (#2982)](https://github.com/react-native-elements/react-native-elements/pull/2982)

### Core Changes

- [Migrate build to Github Actions (#3036)](https://github.com/react-native-elements/react-native-elements/pull/3036)
- [Strict TypeScript (#2930)](https://github.com/react-native-elements/react-native-elements/pull/2930)
- [Website Redesigned & Snack for demo (#3108)](https://github.com/react-native-elements/react-native-elements/pull/3108)
- [Removed ts-ignore and transformed to Functional Component (#2834)](https://github.com/react-native-elements/react-native-elements/pull/2834)

## 🚧 What's next?

### New `Stack` Component

Stack is concerned with one-dimensional layouts. This is not yet in our priority but I wish I could work on this.

Example

```js
<Stack spacing={2}>
  <Item>Item 1</Item>
  <Item>Item 2</Item>
  <Item>Item 3</Item>
</Stack>
```

### Improving VS Code Extension

RNEv4 would introduce some breaking changes, I need to update snippets to support latest API
