---
title:  Flutter reaction button
name:  Flutter reaction button
category: Free
tag: reaction
excerpt: Flutter button reaction . it is fully customizable widget like facebook reaction button for flutter
teaser: https://raw.githubusercontent.com/GeekAbdelouahed/flutter-reaction-button/master/images/Flutter%20Reaction%20Button%20Preview.png
github: https://github.com/GeekAbdelouahed/flutter-reaction-button
license:
 name: MIT License
 url: http://choosealicense.com/licenses/mit/
rating: 5
version: NA
last_updated: Jul 18, 2019
owner:
 profile_image: https://avatars0.githubusercontent.com/u/22131872?v=4
 name: GeekAbdelouahed
 url: https://github.com/GeekAbdelouahed
contributors:
 -
   image: https://avatars0.githubusercontent.com/u/22131872?v=4
   url: https://github.com/GeekAbdelouahed
registered_by:
 image: https://avatars0.githubusercontent.com/u/22131872?v=4
 url: https://github.com/GeekAbdelouahed
 on_date: Jul 18th 19
layout: fa_project
---
# Flutter Reaction Button

Flutter button reaction it is fully customizable widget such as Facebook reaction button.

- [Pub Package](https://pub.dev/packages/flutter_reaction_button)
- [GitHub Repository](https://github.com/GeekAbdelouahed/flutter-reaction-button)

## Usage

This is example Flutter Reaction Button:

```dart
FlutterReactionButton(
    onReactionChanged: (reaction) {
        print('reaction changed');
    },
    reactions: <Reaction>[
        Reaction(
            previewIcon: buildWidgetPreview(
                title: 'English',
                icon: 'united-kingdom-round.png',
            ),
            icon: buildWidget(
                icon: 'united-kingdom.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                title: 'Arabic',
                icon: 'algeria-round.png',
            ),
            icon: buildWidget(
                icon: 'algeria.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                title: 'German',
                icon: 'germany-round.png',
            ),
            icon: buildWidget(
                icon: 'germany.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                title: 'Spanish',
                icon: 'spain-round.png',
            ),
            icon: buildWidget(
                icon: 'spain.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                title: 'Chinese',
                icon: 'china-round.png',
            ),
            icon: buildWidget(
                icon: 'china.png'
            ),
        ),
    ],
    initialReaction: Reaction(
        previewIcon: buildWidgetPreview(
            title: 'English',
            icon: 'united-kingdom-round.png',
        ),
        icon: buildWidget(
            icon: 'united-kingdom.png'
        ),
    ),
    radius: 10,
    elevation: 10,
    position: Position.TOP,
    color: Colors.black.withOpacity(0.5),
    duration: Duration(milliseconds: 500),
)
```
<img src="https://github.com/GeekAbdelouahed/flutter-reaction-button/raw/master/images/Flutter-Reaction-Button.gif"/>

This is a example Flutter Reaction Button Check ( you can also customize everything ):

```dart
FlutterReactionButtonCheck(
    onReactionChanged: (isChecked, reaction) {
        print('reaction changed $isChecked');
    },
    reaction: <Reaction>[
        Reaction(
            previewIcon: buildWidgetPreview(
                icon: 'like.gif',
            ),
            icon: buildWidget(
                icon: 'like_fill.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                icon: 'love.gif',
            ),
            icon: buildWidget(
                icon: 'love.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                icon: 'wow.gif',
            ),
            icon: buildWidget(
                icon: 'wow.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                icon: 'haha.gif',
            ),
            icon: buildWidget(
                icon: 'haha.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                icon: 'sad.gif',
            ),
            icon: buildWidget(
                icon: 'sad.png'
            ),
        ),
        Reaction(
            previewIcon: buildWidgetPreview(
                icon: 'angry.gif',
            ),
            icon: buildWidget(
                icon: 'angry.png'
            ),
        ),
    ],
    initialReaction: Reaction(
        icon: buildWidget(
            icon: 'like.png'
        ),
    ),
    selectedReaction: Reaction(
        icon: buildWidget(
            icon: 'like_fill.png'
        ),
    ),
)
```

<img src="https://github.com/GeekAbdelouahed/flutter-reaction-button/raw/master/images/Flutter-Reaction-Button-Check.gif"/>

## LICENSE

```legal
MIT License

Copyright (c) 2019 Abdelouahed Medjoudja

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
