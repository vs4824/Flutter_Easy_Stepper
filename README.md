# Flutter Easy Stepper

A fully customizable, beautiful and easy to use stepper widgets with different variations.

## Description

The stepper widgets help you to show or collect information from users using organized steps.

### Install

In the pubspec.yaml of your flutter project, add the following dependency:

   ```
   dependencies:
  easy_stepper: <latest_version>
   ```

In your library add the following import:

   ```
   import 'package:easy_stepper/easy_stepper.dart';
   ```

## Getting started

1. Simply import package:easy_stepper/easy_stepper.dart.

2. Important: The direction argument controls whether the stepper is displayed horizontally or vertically. A horizontal Stepper can be wrapped within a Column with no issues. However, if wrapped within a row, it must also be wrapped within the built-in Expanded widget. The same applies to the vertical Stepper.

3. Validation: To enable validation before the next step is reached, set the steppingEnabled property to an appropriate value in a StatefulWidget.

4. Controlling Steppers: All steppers are controlled using the activeStep property. You can control a stepper by tapping individual steps.

5. To customize the color, border, etc., wrap a stepper widget inside a Container and specify it's decoration argument.

## Features

Simple to use icon stepper widget, wherein each icon defines a step. Hence, the total number of icons represents the total number of available steps

### Top And Bottom Title:

   ```
   EasyStepper(
        activeStep: activeStep,
        lineLength: 70,
        lineSpace: 0,
        lineType: LineType.normal,
        defaultLineColor: Colors.white,
        finishedLineColor: Colors.orange,
        activeStepTextColor: Colors.black87,
        finishedStepTextColor: Colors.black87,
        internalPadding: 0,
        showLoadingAnimation: false,
        stepRadius: 8,
        showStepBorder: false,
        lineDotRadius: 1.5,
        steps: [
          EasyStep(
            customStep: CircleAvatar(
              radius: 8,
              backgroundColor: Colors.white,
              child: CircleAvatar(
                radius: 7,
                backgroundColor:
                    activeStep >= 0 ? Colors.orange : Colors.white,
              ),
            ),
            title: 'Waiting',
          ),
          EasyStep(
            customStep: CircleAvatar(
              radius: 8,
              backgroundColor: Colors.white,
              child: CircleAvatar(
                radius: 7,
                backgroundColor:
                    activeStep >= 1 ? Colors.orange : Colors.white,
              ),
            ),
            title: 'Order Received',
            topTitle: true,
          ),
          EasyStep(
            customStep: CircleAvatar(
              radius: 8,
              backgroundColor: Colors.white,
              child: CircleAvatar(
                radius: 7,
                backgroundColor:
                    activeStep >= 2 ? Colors.orange : Colors.white,
              ),
            ),
            title: 'Preparing',
          ),
          EasyStep(
            customStep: CircleAvatar(
              radius: 8,
              backgroundColor: Colors.white,
              child: CircleAvatar(
                radius: 7,
                backgroundColor:
                    activeStep >= 3 ? Colors.orange : Colors.white,
              ),
            ),
            title: 'On Way',
            topTitle: true,
          ),
          EasyStep(
            customStep: CircleAvatar(
              radius: 8,
              backgroundColor: Colors.white,
              child: CircleAvatar(
                radius: 7,
                backgroundColor:
                    activeStep >= 4 ? Colors.orange : Colors.white,
              ),
            ),
            title: 'Delivered',
          ),
        ],
        onStepReached: (index) =>
            setState(() => activeStep = index),
    ),
   ```

## Custom-Stepper

### With Image:

   ```
   EasyStepper(
                  activeStep: activeStep,
                  lineLength: 50,
                  stepShape: StepShape.rRectangle,
                  stepBorderRadius: 15,
                  borderThickness: 2,
                  padding: 20,
                  stepRadius: 28,
                  finishedStepBorderColor: Colors.deepOrange,
                  finishedStepTextColor: Colors.deepOrange,
                  finishedStepBackgroundColor: Colors.deepOrange,
                  activeStepIconColor: Colors.deepOrange,
                  showLoadingAnimation: false,
                  steps: [
                    EasyStep(
                      customStep: ClipRRect(
                        borderRadius: BorderRadius.circular(15),
                        child: Opacity(
                          opacity: activeStep >= 0 ? 1 : 0.3,
                          child: Image.asset('assets/1.png'),
                        ),
                      ),
                      customTitle: const Text(
                        'Dash 1',
                        textAlign: TextAlign.center,
                      ),
                    ),
                    EasyStep(
                      customStep: ClipRRect(
                        borderRadius: BorderRadius.circular(15),
                        child: Opacity(
                          opacity: activeStep >= 1 ? 1 : 0.3,
                          child: Image.asset('assets/2.png'),
                        ),
                      ),
                      customTitle: const Text(
                        'Dash 2',
                        textAlign: TextAlign.center,
                      ),
                    ),
                    EasyStep(
                      customStep: ClipRRect(
                        borderRadius: BorderRadius.circular(15),
                        child: Opacity(
                          opacity: activeStep >= 2 ? 1 : 0.3,
                          child: Image.asset('assets/3.png'),
                        ),
                      ),
                      customTitle: const Text(
                        'Dash 3',
                        textAlign: TextAlign.center,
                      ),
                    ),
                    EasyStep(
                      customStep: ClipRRect(
                        borderRadius: BorderRadius.circular(15),
                        child: Opacity(
                          opacity: activeStep >= 3 ? 1 : 0.3,
                          child: Image.asset('assets/4.png'),
                        ),
                      ),
                      customTitle: const Text(
                        'Dash 4',
                        textAlign: TextAlign.center,
                      ),
                    ),
                    EasyStep(
                      customStep: ClipRRect(
                        borderRadius: BorderRadius.circular(15),
                        child: Opacity(
                          opacity: activeStep >= 4 ? 1 : 0.3,
                          child: Image.asset('assets/5.png'),
                        ),
                      ),
                      customTitle: const Text(
                        'Dash 5',
                        textAlign: TextAlign.center,
                      ),
                    ),
                  ],
                  onStepReached: (index) => setState(() => activeStep = index),
                ),
   ```


