---
title: Key Features
page_title: Key Features
position: 2
slug: numericinput-key-features
---

# Key Features

The purpose of this help article is to show you the key features of the **RadNumericInput** control. 

## Setting and reading numbers

RadNumericInput exposes a **Value** property that is used to set and read the number presented by the control. 

The **Value** property is of type nullable double, which enables the NumericInput control to accept null value as well.

<snippet id='numericinput-features-value'/>

Where:

<snippet id='xmlns-telerikinput'/>

## Restricting the input

RadNumericInput provides **Minimum** and **Maximum** properties used to define the allowed range of its value:

<snippet id='numericinput-features-minmax'/>

## Setting the step for decrement/increment the value

The **Step** property defines the value step that will be applied to the input value upon each decrease/increase action. The default step is 1.

<snippet id='numericinput-features-step'/>

## Setting buttons’ text

You could use **IncreaseButtonText** and **DecreaseButtonText** properties to specify the text of the NumericInput buttons, so that it’s applicable to your scenario.

<snippet id='numericinput-features-btntext'/>

## Read-only mode

RadNumericInput supports read-only mode in which the end user cannot type into the input field – updating the value is possible only through the increase/decrease buttons.  You could enable the read-only mode through **IsReadOnly** property:

<snippet id='numericinput-features-readonly'/>

## Formatting the value

**RadNumericInput** provides you the option to define the format of its numeric value through the **StringFormat** property. You can set it to the desired format which will be applied when the control loses focus.

<snippet id='numericinput-features-strformat'/>

>tip You can find detailed information about the supported numeric formats here: [Standard Numeric Format Strings](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings).

## See Also

- [Globalization]({%slug numericinput-globalization%})
- [Commands]({%slug numericinput-commands%})
