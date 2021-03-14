# PanableModal

Add ModalPresentation.swift to your project

# Usage
In your source view controller (first view controller) Conform to UIViewControllerTransitioningDelegate and add method below:
```swift
func presentationController(forPresented presented: UIViewController, presenting: UIViewController?, source: UIViewController) -> UIPresentationController? {
        ModalPresentation(presentedViewController: presented, presenting: presenting)
    }
```

present destination view controller (second view controller):
```swift
let destVC = DestinationVC()
destVC.modalPresentationStyle = .custom
destVC.transitioningDelegate = self
present(destVC, animated: true, completion: nil)
```
