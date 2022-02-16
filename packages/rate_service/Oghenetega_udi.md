
# Rate Service

The is a driver rating and issue reporting package on Flutter with a heart of gold. Interactive module that helps users rate drivers on a five star scale with provision to report issues for the ride.

## Preview

| Rating Page | Issues Selection |
| :--------------: | :---------------------: |
|          |         |

| More Issues Page | More Issues List |
| :--------------: | :---------------------: |
|          |         |

## Installation

For this version, pull the package into your project.

In your `pubspec.yaml` file within your Flutter Project:

```yaml
dependencies:
 rate_service: <path_to_package>
```

## Use it

```dart
import 'package:flutter/material.dart';
import 'package:rate_service/rate_service.dart';
import 'package:driver_rate_example/model/driver_model.dart';
 
Widget regularButton(BuildContext context,
  double? height,
  double? width,
  Color color,
  String? text,
  DriverModel driver
  ){
return SizedBox(
  height: MediaQuery.of(context).size.height *height!,
  width: MediaQuery.of(context).size.width *width!,
  child: GestureDetector(
    onTap: (){
      showModalBottomSheet(
          context: context,
          isScrollControlled: true,
          backgroundColor: Colors.transparent,
          builder: (_){
            return RateService(
              id: driver.id,
              imgUrl: driver.imgUrl,
              driverName: driver.driverName,
              address: driver.address,
              ratings: driver.ratings,
            );
          }
      );
    },
    child: Card(
      shape: RoundedRectangleBorder(
          borderRadius: BorderRadius.circular(10)
      ),
      elevation: 0,
      color: color,
      child:  Center(
        child: Text('$text',
          style: const TextStyle(
            color: Colors.white,
            fontSize: 15,
            fontFamily: 'Poppins_Regular',
            decoration: TextDecoration.none,
          ),
        ),
      ),
    ),
  ),
);
}
```

## Dependencies
```
N/A
```

## Roadmap

- [x] Add ride tips
- [x]
 
 
 

