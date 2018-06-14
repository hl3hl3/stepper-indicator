[![Release](https://jitpack.io/v/badoualy/stepper-indicator.svg)](https://jitpack.io/#badoualy/stepper-indicator)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-stepper--indicator-green.svg?style=true)](https://android-arsenal.com/details/1/3711)

# ![](https://github.com/badoualy/stepper-indicator/blob/master/sample/src/main/res/mipmap-mdpi/ic_launcher.png) Stepper indicator
> ### Designed by the awesome https://dribbble.com/LeslyPyram :)
> #### iOS (swift) version available at https://github.com/chenyun122/StepIndicator

<img src="https://github.com/badoualy/stepper-indicator/blob/master/ART/screen.gif" width="300">

<img src="https://github.com/hl3hl3/stepper-indicator/blob/master/ART/xml_attr_style_sample.png" >

Sample
----------------

You can checkout the [Sample Application](https://play.google.com/store/apps/details?id=com.badoualy.stepperindicator.sample) on the Play Store

Setup
----------------

First, add jitpack in your build.gradle at the end of repositories:
 ```gradle
repositories {
    // ...       
    maven { url "https://jitpack.io" }
}
```

Then, add the library dependency:
```gradle
compile 'com.github.badoualy:stepper-indicator:1.0.7'
```

Now go do some awesome stuff!

Usage
----------------

```xml
<com.badoualy.stepperindicator.StepperIndicator
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    app:stpi_stepCount="5"/>
```

Attributes:

| Name                   | Description                                         | Default value   |
|------------------------|-----------------------------------------------------|-----------------|
| stpi_animDuration      | duration of the line tracing animation              | 250 ms          |
| stpi_stepCount         | number of pages/steps                               |                 |
| stpi_currentStep       | current page/step                                   | 0               |
| stpi_circleColor       | color of the back circle                            | #b3bdc2 (grey)  |
| stpi_circleRadius      | radius of the circle                                | 10dp            |
| stpi_circleStrokeWidth | width of circle's radius                            | 4dp             |
| stpi_circleStyle       | circle style (fill/stroke)                          | stroke          |
| stpi_indicatorColor    | color for the current page indicator                | #00b47c (green) |
| stpi_indicatorRadius   | radius for the circle of the current page indicator | 4dp             |
| stpi_lineColor         | color of the line between indicators                | #b3bdc2 (grey)  |
| stpi_lineDoneColor     | color of a line when step is done                   | #00b47c (green) |
| stpi_lineStrokeWidth   | width of the line stroke                            | 2dp             |
| stpi_lineMargin        | margin at each side of the line                     | 5dp             |
| stpi_showDoneIcon      | show the done check icon or not                     | true            |
| stpi_showStepNumberInstead| draw the step number inside the back circle or not| false           |
| stpi_showCurrentStepAsBullet| show the current page/step indicator as bullet or not | true            |
| stpi_showCurrentStepLabelAsDone| show the label of current page/step as done color or not| false |
| stpi_stepNumberColor | color of the step number inside the back circle| value of stpi_circleColor|
| stpi_useBottomIndicator | display the indicator for the current step at the bottom instead of inside bullet | false |
| stpi_useBottomIndicatorWithStepColors | use the same color for the bottom indicator as the step color | false |
| stpi_bottomIndicatorHeight | set the height for the bottom indicator component | 3dp |
| stpi_bottomIndicatorWidth | set the width for the bottom indicator component | 50dp |
| stpi_bottomIndicatorMarginTop | set the top margin for the bottom indicator component | 10dp |
| stpi_stepsCircleColors| use multiple colors for each step (array of colors with the size at least the same size as the stpi_stepCount value)| |
| stpi_stepsIndicatorColors | use multiple colors for each step indicator (array of colors with the size at least the same size as the stpi_stepCount value)| |
| stpi_labels | supply an array of strings to show labels for every step indicator | |
| stpi_showLabels | show labels for each step indicator. Useful for timelines or checkpoints.| false |
| stpi_labelMarginTop | top margin for the labels | 2dp |
| stpi_labelSize | size for the labels | 12sp |
| stpi_labelColor | color for the labels | android:textColorSecondary |
| stpi_labelDoneColor | color for the done labels | value of stpi_labelColor |
```java
indicator.setViewPager(pager);
// or keep last page as "end page"
indicator.setViewPager(pager, pager.getAdapter().getCount() - 1); //
// or manual change
indicator.setStepCount(3);
indicator.setCurrentStep(2);
```


Licence
----------------
```
The MIT License (MIT)

Copyright (c) 2016 Yannick Badoual

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
