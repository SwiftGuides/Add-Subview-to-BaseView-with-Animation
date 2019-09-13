# Add-Subview-to-BaseView-with-Animation
This Code will Add Subviews with animation in baseView

```swift
    //MARK: Add Subview in BaseView
    func add(subView childView:UIView){
        childView.frame = containerVIew.bounds
        childView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        let transition = CATransition()
        transition.type = CATransitionType.push
        transition.subtype = CATransitionSubtype.fromRight
        containerVIew.layer.add(transition, forKey: nil)
        containerVIew.addSubview(childView)
    }
    
    //MARK: Remove From BaseView
    func remove(subView subview:UIView){
        subview.removeFromSuperview()
    }
```
