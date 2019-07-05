---
title: arkit_flutter_plugin
name: arkit_flutter_plugin
category: Free
tag: ""
excerpt: "ARKit Flutter Plugin"
github: https://github.com/olexale/arkit_flutter_plugin
license:
 name: MIT License
 url: http://choosealicense.com/licenses/mit/
rating: 5
version: NA
last_updated: Jul 01, 2019
owner:
 profile_image: https://avatars2.githubusercontent.com/u/4376913?v=4
 name: olexale
 on_date: June 27, 2019
contributors:
 -
   image: https://avatars1.githubusercontent.com/u/4256832?v=4
   url: https://github.com/shalex9154
 -
   image: https://avatars2.githubusercontent.com/u/4376913?v=4
   url: https://github.com/olexale
registered_by:
 image: https://avatars3.githubusercontent.com/u/7826138?s=460&v=4
 url: https://github.com/karx
layout: fa_project
---
# arkit_flutter_plugin
[![Codemagic build status](https://api.codemagic.io/apps/5cb0a01178f5790010ab6978/5cb0a01178f5790010ab6977/status_badge.svg)](https://codemagic.io/apps/5cb0a01178f5790010ab6978/5cb0a01178f5790010ab6977/latest_build) [![flutter awesome](https://img.shields.io/badge/Awesome-Flutter-blue.svg?longCache=true&style=flat-square)](https://github.com/Solido/awesome-flutter)
[![pub package](https://img.shields.io/pub/v/arkit_plugin.svg)](https://pub.dartlang.org/packages/arkit_plugin)

**Note**: ARKit is only supported by mobile devices with A9 or later processors (iPhone 6s/7/SE/8/X, iPad 2017/Pro) on iOS 11 and newer. For some features iOS 12 is required.

## Usage

### Depend on it

Follow the [installation instructions](https://pub.dartlang.org/packages/arkit_plugin#-installing-tab-) from Dart Packages site.

### Update Info.plist

The plugin use native view from ARKit, which is not yet supported by default. To make it work add the following code to `Info.plist`:
```xml
    <key>io.flutter.embedded_views_preview</key>
    <string>YES</string>
```
ARKit uses the device camera, so do not forget to provide the `NSCameraUsageDescription`. You may specify it in `Info.plist` like that:
```xml
    <key>NSCameraUsageDescription</key>
    <string>Describe why your app needs AR here.</string>
```

### Write the app

The simplest code example:

```dart
import 'package:flutter/material.dart';
import 'package:arkit_plugin/arkit_plugin.dart';
import 'package:vector_math/vector_math_64.dart';

void main() => runApp(MaterialApp(home: MyApp()));

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  ARKitController arkitController;

  @override
  void dispose() {
    arkitController?.dispose();
    super.dispose();
  }

  @override
  Widget build(BuildContext context) => Scaffold(
      appBar: AppBar(title: const Text('ARKit in Flutter')),
      body: ARKitSceneView(onARKitViewCreated: onARKitViewCreated));

  void onARKitViewCreated(ARKitController arkitController) {
    this.arkitController = arkitController;
    final node = ARKitNode(
        geometry: ARKitSphere(radius: 0.1), position: Vector3(0, 0, -0.5));
    this.arkitController.add(node);
  }
}
```
Result:

![flutter](./demo.gif)

## Examples

I would highly recommend to review the [sample](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/main.dart) from the `Example` folder. You may find a couple of samples in the `Example` folder of the plugin.

| Name        | Description                                          | Link | Demo |
|-------------|------------------------------------------------------|------------------------------------------------------|----|
| Hello World | The simplest scene with different geometries.           | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/hello_world.dart)| [twitter](https://twitter.com/OlexaLe/status/1118441432707149824) |
| Earth       | Sphere with an image texture and rotation animation. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/earth_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1118441432707149824) |
| Tap         | Sphere which handles tap event.                      | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/tap_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1118441432707149824) |
| Plane Detection | Detects horizontal plane. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/plane_detection_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1118870195743883266) |
| Distance tracking | Detects horizontal plane and track distance on it. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/distance_tracking_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1121022506180149248) |
| Measure | Measures distances | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/measure_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1121022506180149248) |
| Physics | A sphere and a plane with dynamic and static physics                      | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/physics_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1119233047851884547) |
| Image Detection | Detects an earth image and puts a 3D object near it. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/image_detection_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1120287361974378496) |
| Custom Light | Hello World scene with a custom light spot. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/custom_light_page.dart) | |
| Light Estimation | Estimates and applies the light around you. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/light_estimate_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1120671744426221573) |
| Custom Object | Place custom object on plane. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/custom_object_page.dart) | [twitter](https://twitter.com/OlexaLe/status/1121037162852569090) |
| Occlusion | Spheres which are not visible after horizontal and vertical planes. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/occlusion_page.dart)|[twitter](https://twitter.com/OlexaLe/status/1121421315364274177) |
| Manipulation | Custom objects with pinch and rotation events. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/manipulation_page.dart)|[twitter](https://twitter.com/OlexaLe/status/1123893412279791616) |
| Face Tracking | Face mask sample. | [code](https://github.com/olexale/arkit_flutter_plugin/blob/master/example/lib/face_detection_page.dart)|[twitter](https://twitter.com/OlexaLe/status/1143483440278454277) |

## Contributing

If you find a bug or would like to request a new feature, just [open an issue](https://github.com/olexale/arkit_flutter_plugin/issues/new). Your contributions are always welcome!
