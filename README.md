

# react-blur-modals

![npm version](https://img.shields.io/npm/v/react-blur-modals.svg)
![License](https://img.shields.io/npm/l/react-blur-modals.svg)

A collection of beautiful mobile-friendly modals built with React, Framer Motion, and Tailwind CSS. Easily create stylish and interactive modals for your mobile applications.

## Installation

To install `react-blur-modals`, you can use npm or yarn:

```bash
npm install react-blur-modals --save
```

or

```bash
yarn add react-blur-modals
```

## Usage

```js
import { ModalContent, ModalButton } from 'react-blur-modals';
import { useState } from 'react';

export default function Test() {
  const [modalOpen, setModalOpen] = useState(false);

  const handleModalToggle = () => {
    setModalOpen(!modalOpen);
  };

  return (
    <>
      <ModalButton text="Open Modal" backgroundColor="blue-600" onClick={handleModalToggle} />
      <ModalContent isOpen={modalOpen} onClose={handleModalToggle} closeButtonColor="blue-600" animationType="easeInOut" blurPx="10px">
        <h1>React Blur Modals</h1>
      </ModalContent>

      {/** 
      *     animationType parameter supports framer-motion animation types
      */}
    </>
  );
}
```

## Props

### ModalButton

| Prop              | Type     | Default | Description                                 |
|-------------------|----------|---------|---------------------------------------------|
| text              | string   |         | The text to display on the button          |
| backgroundColor   | string   |         | The background color of the button         |
| onClick           | function |         | The function to be called on button click  |

### ModalContent

| Prop              | Type                     | Default   | Description                                           |
|-------------------|--------------------------|-----------|-------------------------------------------------------|
| isOpen            | boolean                  |           | Controls whether the modal is open or closed         |
| onClose           | function                 |           | The function to be called when the modal is closed   |
| closeButtonColor  | string                   |           | The color of the close button                        |
| animationType     | string | easeInOut | The animation type for opening and closing the modal |
| blurPx            | string                   | "10px"    | The amount of blur to apply to the modal background  |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

