---
layout: default
title: Widgets
parent: Flutter Development
---

## Widgets

## stateless widget 

- It composed of childeren
- doen't have any mutable state that it needs to track
- `mutable state` : any state that change over time
- it just need a name that won't change
- `snippit` : **stless** 

## Hot reload and hot restart 

- they only look at the chnages that were made and they will push those chnages onto your testing device(simulator)

- size of the program doesn't matter

## Container ( ) widgets

- Its a lyout box
- container with no children try to be big as possible
- container take up all of the space tha's avaliable 
- Container with children size themselves to their children
- this widget have only one child
- To lay out muttl

![container](./images/1container.png)

![container](./images/3container.png)

![container](./images/2container.png)

- In order to embed container inside safe area hold down `Alt` `+` `ENTER` and select new widget and set as `SafeArea`

### margin and padding around container

```dart
margin: EdgeInsets.symmetric(vertical: 40,horizontal: 50),
padding: EdgeInsets.all(20.0)
```
![margin](./images/14column.png)

### Single child and multichild widgets

#### Columns and rows class

- `Column widget` : `displays children in vertical array`
- `Row widget` : `display children horizontaly`

**Column**
- cause child to fill the avaliable verticle space
- risrict to width of container
- column widget does not scroll
- it considered as error to have more children in a column than fit in avaliable room
- Use `ListView` : if you want to scroll

#### Properties

- `verticalDirection: VerticalDirection.up`
- `mainAxisAlignment: MainAxisAlignment.center`
- `mainAxisAlignment: MainAxisAlignment.spaceEvenly`
- `mainAxisAlignment: MainAxisAlignment.spaceBetween`
- `crossAxisAlignment: CrossAxisAlignment.end`
- `crossAxisAlignment: CrossAxisAlignment.stretch`
- `doluble.infinity` inside container
- `SizedBox(height :20.0)` - gives gap between container


`mainAxisSize: MainAxisSize,min`

mainAxis for column is vertical

![column](./images/5column.png)
![column](./images/6column.png)

- `verticalDirection: VerticalDirection.up`

![col](./images/column7.png)

- `mainAxisAlignment: MainAxisAlignment.center`

![col](./images/8column.png)

- `mainAxisAlignment: MainAxisAlignment.spaceEvenly`

![col](./images/9column.png)

- `mainAxisAlignment: MainAxisAlignment.spaceBetween`

![col](./images/column10.png)

- `MainAxisAlignment: mainAxisAlignment.end`

![col](./images/11column.png)

- `crossAxisAlignment: CrossAxisAlignment.end`

![col](./images/12column.png)

- `crossAxisAlignment: CrossAxisAlignment.strech`

 ![col](./images/13column.png)

- `doluble.infinity` inside container

 ![col](./images/14column.png)

- `SizedBox(height :20.0)` - gives gap between container

 ![col](./images/15sizedBox.png)


- all the wigets  are same for `Rows` as well

![col](./images/14column.png)

```dart
import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

void main(){
  runApp(MyApp());
}
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.deepPurple.shade200,
        body: SafeArea(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget >[
              Container(
                height: 100,
                color: Colors.white,
                child: Text('container 1'),
              ),
              SizedBox(
                  height: 20.0),
              Container(
                  height: 100.0,
                color: Colors.deepPurpleAccent,
                child: Text('container 2')
              ),
              SizedBox(
                  height: 20.0),
              Container(
                  height: 100.0,
                  color: Colors.pinkAccent,
                  child: Text('container 3')
              )
            ],
          ),
        ),
      ),
    );
  }
}

```