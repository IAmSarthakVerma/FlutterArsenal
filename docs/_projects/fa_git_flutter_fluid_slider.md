---
title: flutter_fluid_slider
name: flutter_fluid_slider
category: Free
tag: Slider
excerpt: A fluid design slider that works just like the Slider material widget.
teaser: https://camo.githubusercontent.com/d811ab18d6a87537dec815bf1937c48ce9a31dfc/68747470733a2f2f6c68332e676f6f676c6575736572636f6e74656e742e636f6d2f56714d427277485443495f65396e633443304962794432572d4279746a343656564b5764723139384d71564a32556e7a513852335735764b394a726961794c4e47467839526b504b4141436c
github: https://github.com/rvamsikrishna/flutter_fluid_slider
license:
 name: MIT License
 url: http://choosealicense.com/licenses/mit/
rating: 5
version: NA
last_updated: Jul 12, 2019
owner:
 profile_image: https://avatars1.githubusercontent.com/u/31307345?v=4
 name: rvamsikrishna
 url: https://github.com/rvamsikrishna
contributors:
 -
   image: https://avatars2.githubusercontent.com/u/4293508?v=4
   url: https://github.com/jcsena
 -
   image: https://avatars1.githubusercontent.com/u/31307345?v=4
   url: https://github.com/rvamsikrishna
registered_by:
 image: https://avatars3.githubusercontent.com/u/20480867?v=4
 url: https://github.com/IAmSarthakVerma
 on_date: Jul 14th 19
layout: fa_project
---
# Fluid Slider for Flutter

<a href="https://github.com/Solido/awesome-flutter">
   <img alt="Awesome Flutter" src="https://img.shields.io/badge/Awesome-Flutter-blue.svg?longCache=true&style=flat-square" />
</a>

Inspired by a dribbble by [Virgil Pana](https://dribbble.com/virgilpana).

![enter image description here](https://lh3.googleusercontent.com/VqMBrwHTCI_e9nc4C0IbyD2W-Bytj46VVKWdr198MqVJ2UnzQ8R3W5vK9JriayLNGFx9RkPKAACl "Demo gif")

A fluid design slider that works just like the [Slider](https://docs.flutter.io/flutter/material/Slider-class.html) material widget.

Used to select from a range of values.

## Installation

Just add the package to your dependencies in the `pubspec.yaml` file:

```yaml
dependencies:
  flutter_fluid_slider: ^1.0.1
```

### Basic Usage

Place the `FluidSlider` in your widget tree.

```dart
FluidSlider(
  value: _value,
  onChanged: (double newValue) {
    setState(() {
      _value = newValue;
    });
  },
  min: 0.0,
  max: 100.0,
),
```

### Properties

- `value` : [**Required**] The currently selected value for this slider. The slider's thumb is drawn at a position that corresponds to this value.

- `min` : The minimum value the user can select. Defaults to `0.0`. Must be less than or equal to `max`.

- `max` : The maximum value the user can select. Defaults to `1.0`. Must be less than or equal to `min`.

- `start` : The widget to be displayed as the min label. For eg: an Icon can be displayed. If not provided the `min` value is displayed as text.

- `end` : The widget to be displayed as the max label. For eg: an Icon can be displayed. If not provided the `max` value is displayed as text.

- `onChanged` : [**Required**] Called during a drag when the user is selecting a new value for the slider

  by dragging.

  - The slider passes the new value to the callback but does not actually change state until the parent widget rebuilds the slider with the new value.

  - If null, the slider will be displayed as disabled.

- `onChangeStart` : Called when the user starts selecting a new value for the slider. The value passed will be the last `value` that the slider had before the change began.

- `onChangeEnd` : Called when the user is done selecting a new value for the slider.

- `labelsTextStyle` : The styling of the min and max text that gets displayed on the slider. If not provided the ancestor `Theme`'s `accentTextTheme` text style will be applied.

- `valueTextStyle` : The styling of the current value text that gets displayed on the slider. If not provided the ancestor `Theme`'s `textTheme.title` text style with bold will be applied .

- `sliderColor` : The color of the slider. If not provided the ancestor `Theme`'s `primaryColor` will be applied.

- `thumbColor` : The color of the thumb. If not provided the `Colors.white` will be applied.

- `showDecimalValue` : Whether to display the first decimal value of the slider value. Defaults to `false`.


#### Credits:

- [Ramotion](https://dribbble.com/shots/5343166-Fluid-Slider-Optimized-iOS-Control-Open-Source) - implementation for ios and android
- [Virgil Pana](https://dribbble.com/virgilpana) - creating the original concept
