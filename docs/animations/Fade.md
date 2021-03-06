# Fade

The **Fade animation behavior** fades objects, in and out, over time.

## Syntax

```xaml

    <behaviors:Fade x:Name="FadeBehavior>" 
                Value="0.5" 
                Duration="1500" 
                Delay="500" 
                AutomaticallyStart="True">
    </behaviors:Fade>

```

or directly from code:

```csharp

    MyRectangle.Fade((float)Value, Duration, Delay);

```

## Properties

| Property Name | Type | Description |
| --- | --- | --- |
| Value | float | The amount to fade an element. The value should be between 0.0 and l.0 |
| Duration | double | The number of milliseconds the animation should run for |
| Delay | double | The number of milliseconds before the animation is started |

## Chaining animations

Behavior animations can also be chained and awaited.

```csharp

    Element.Rotate(value: 30f, duration: 0.3).StartAsync();

    await Element.Rotate(value: 30f, duration: 0.3).StartAsync();

    var anim = element.Rotate(30f).Fade(0.5).Blur(5);
    anim.SetDurationForAll(2);
    anim.Completed += animation_completed;
    anim.StartAsync();

    anim.Stop();

```

[Fade Behavior Sample Page Source](https://github.com/Microsoft/UWPCommunityToolkit/tree/master/Microsoft.Toolkit.Uwp.SampleApp/SamplePages/Fade)

## Example Image

![Fade Behavior animation](../resources/images/Animations-Fade.gif "Fade Behavior")

## Requirements (Windows 10 Device Family)

| [Device family](http://go.microsoft.com/fwlink/p/?LinkID=526370) | Universal, 10.0.10586.0 or higher |
| --- | --- |
| Namespace | Microsoft.Toolkit.Uwp.UI.Animations |

## API

* [Fade source code](https://github.com/Microsoft/UWPCommunityToolkit/blob/master/Microsoft.Toolkit.Uwp.UI.Animations/Behaviors/Fade.cs)

