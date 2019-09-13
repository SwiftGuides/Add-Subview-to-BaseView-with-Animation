# Add-Subview-to-BaseView-with-Animation
This Code will Add Subviews with animation in baseView

```swift

     @IBOutlet weak var baseView: UIView!

    //MARK: Add Subview in BaseView
    func add(subView childView:UIView){
        childView.frame = baseView.bounds
        childView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        let transition = CATransition()
        transition.type = CATransitionType.push
        transition.subtype = CATransitionSubtype.fromRight
        baseView.layer.add(transition, forKey: nil)
        baseView.addSubview(childView)
    }
    
    //MARK: Remove From BaseView
    func remove(subView subview:UIView){
        subview.removeFromSuperview()
    }
```
