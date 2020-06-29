![](/static/mb/device/header1.jpg)

# About

## @description A Blocks / Javascript code editor for the micro:bit, a pocket-size computer with 5x5 display, sensors and Bluetooth.

The [Teknikio Bluebird](https://www.teknikio.com/products/bluebird-beta-v1-6) is a [small blue gadget](/device) that can send and receive information wirelessly. The board has a Neopixel LED, speaker, Bluetooth and sensors that can be programmed by both beginners and expert coders. The development of Bluebird was funded by the National Science Foundation.


The Bluebird is a great tool to learn how to build circuits, code, and scale your ideas to an IoT network. It can attach easily to different materials to become a futuristic gizmo or weatable.  Similar to  Arduino, the Bluebird can also  connect with external sensors, and outputs via the central connector.


## [Hardware: The Device](/device)

The Bluebird board is embedded with sensors, radio and other fun stuff. Learn about the [hardware components](/device) of the board to make the most of it!

## ~ hint

**Looking to buy a Bluebird?** Get one here [list of resellers](https://www.teknikio.com/products/bluebird-beta-v1-6).

## ~
## [Getting Started](/device)

* Getting Started with Bluebird
* Tekniverse for Browser
* Tekniverse for macOS
* Arduino IDE

## Programming: [Blocks](/blocks) or [JavaScript](/javascript)

You can program the Bluebird using [Blocks](/blocks) or [JavaScript](/javascript) in your web browser via the [Bluebird APIs](/reference):

```block
input.onButtonPressed(Button.A, () => {
    basic.showString("Hi!");
})
```
```typescript
input.onButtonPressed(Button.A, () => {
    basic.showString("Hi!");
})
```

The editor work in [most modern browsers](/browsers), work [offline](/offline) once loaded and do not require any installation.

## [Compile and Flash: Your Program!](/device/usb)

When you have your code ready, you connect your Bluebird to a computer via a USB cable, so it appears as a mounted drive (named TEKBOOT).

Compilation to ARM thumb machine code from Blocks or JavaScript happens in the browser. You save the ARM binary program to a file, which you then copy to the TEKBOOT drive, which flashes the Bluebird device with the new program.


## Simulator: Test Your Code

You can run your code using the Bluebird simulator, all within the confines of a web browser. The simulator has support for the LED screen, buttons, as well as compass, accelerometer, and digital I/O pins.


```sim
basic.forever(() => {
  basic.showString("Hi!");
})
input.onButtonPressed(Button.A, () => {
    led.stopAnimation();
    basic.showLeds(`
. . . . .
. # . # .
. . . . .
# . . . #
. # # # .`);
});
input.onButtonPressed(Button.B, () => {
    led.stopAnimation();
    basic.showLeds(`
. # . # .
# . # . #
# . . . #
. # . # .
. . # . .`);
});
```

## Learn!

We have loads of [inventions](https://tekniverse.teknikio.com/resources/inventions), tutorials, and [courses](https://tekniverse.teknikio.com/resources/classes) to get you started!


<!--## C++ Runtime

The [C++ micro:bit runtime](http://lancaster-university.github.io/microbit-docs/), created at [Lancaster University](http://www.lancaster.ac.uk/), provides access to the hardware functions of the micro:bit,
as well as a set of helper functions (such as displaying a number/image/string on the LED screen).

The [micro:bit library](/reference) mirrors the functions of the C++ library.
When code is compiled to ARM machine code, the calls to JavaScript micro:bit functions are replaced with calls to the corresponding C++ functions.

## [Command Line Tools](/cli)

Looking to use @homeurl@ in your favorite editor? Install the [command line tools](/cli) and get rolling!

## [Extensions](/extensions)

Create, edit and distribute your own blocks and JavaScript using [extensions](/extensions). Extensions are hosted on GitHub and may be written using C++, JavaScript and/or ARM thumb.

## [Open Source](/open-source)

The code for the micro:bit is [open source](/open-source) on GitHub. Contributors are welcome!

```package
radio
```
-->
