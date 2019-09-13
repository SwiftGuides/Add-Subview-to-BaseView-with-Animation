# Add-Subview-to-BaseView-with-Animation
This Code will Add Subviews with animation in baseView

```swift

     @IBOutlet weak var baseView: UIView!  //This is the container view in which we have to add the subview
     @IBOutlet weak var childView: UIView! // This is the view we have to add in the baseView as a subview

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
