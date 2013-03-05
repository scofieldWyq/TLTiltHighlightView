TLTiltHighlightView
===================

`TLTiltHighlightView` is a `UIView` subclass with a horiztontal gradient which adjusts its appearance based on the positional attitude of the device. The movement of the gradient when re-orientating the device is *subtle* – it's meant to augment keylines. This mimicks the iOS 6 Music app (notice the gradient keylines at the very top and bottom of the images).

![Left hightlight](https://github.com/TeehanLax/TLTiltHighlightView/raw/master/images/left.png)
![Right hightlight](https://github.com/TeehanLax/TLTiltHighlightView/raw/master/images/right.png)

How to Use
-----------------------

Drag `TLTiltHighlightView.h` and `TLTiltHighlightView.m` into your project. Make sure to [add](http://stackoverflow.com/questions/3352664/how-to-add-existing-frameworks-in-xcode-4) QuartzCore and CoreMotion to the list of libraries you link against. 

Create an instance of `TLTiltHighlightView` and add it to a view hierarchy. Optimal size is any width and 2pt tall (the keyline will always sit at the bottom of the `TLTiltHighlightView`).

    TLTiltHighlightView *highlightView = [[TLTiltHighlightView alloc] initWithFrame:CGRectMake(0, 44, CGRectGetWidth(self.view.bounds), 2)];
    [self.view addSubview:highlightView];
    
You can also change the background color and the highlight colours. 
    
    highlightView.highlightColor = [UIColor redColor];
    highlightView.backgroundColor = [UIColor clearColor];
    
Alternatively to instantiating the class programmatically, you can also use Interface Builder by selecting the Identity Inspector and changing the class of a view.

![Interface Builer](https://github.com/TeehanLax/TLTiltHighlightView/raw/master/images/interface_builder.png)


The `TLTiltHighlightView` class supports all four interface orientations of iPhones and iPads. 

Requirements
-----------------------

You must link with QuartzCore and CoreMotion. This project requires ARC and has been tested on iOS 6. It should work on iOS 5, but it has not been rigourously tested. If you use it successfully on iOS 5, please let us know!