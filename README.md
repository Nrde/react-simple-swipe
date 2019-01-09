# react-simple-swipe

[![NPM](https://img.shields.io/npm/v/react-simple-swipe.svg)](https://www.npmjs.com/package/react-simple-swipe) 

![](swiping.gif)


## Install

```bash
yarn add react-simple-swipe
```

## Usage

```tsx
import React from "react";
import Swipes from "react-simple-swipe";

class Example extends React.Component {
  state = {
    index: 0,
    transitionTime: 0
  };
  render() {
    return (
      <Swipes
        images={["/img1.jpg", "/img2.jpg", "/img3.jpg", "/img4.jpg"]}
        width={400}
        height={400}
        index={this.state.index}
        transitionTime={this.state.transitionTime}
        onIndexChange={(index, transitionTime) => {
          this.setState({
            index,
            transitionTime
          });
        }}
        onTransitionComplete={() => {
          this.setState({
            transitionTime: 0
          });
        }}
      />
    );
  }
}
```

## License

MIT © [browniefed](https://github.com/browniefed)
