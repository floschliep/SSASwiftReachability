![SSASideMenu](https://github.com/SSA111/SSASwiftReachability/blob/master/SSASwiftReachabilityCover.png)

[![](http://img.shields.io/badge/iOS-8.0%2B-blue.svg)]() [![](http://img.shields.io/badge/Swift-2.0-blue.svg)]() 

###Usage

```swift
    override func viewDidLoad() {
        super.viewDidLoad()
        
         // Start Monitoring For Network Reachability Changes.
        SSASwiftReachability.sharedManager?.startMonitoring()
        
        // Listen For Network Reachability Changes
        NSNotificationCenter.defaultCenter().addObserver(self, selector: "reachabilityStatusChanged:", name: SSAReachabilityDidChangeNotification, object: nil)
    }
    
    func reachabilityStatusChanged(notification: NSNotification) {
        guard let userInfo = notification.userInfo else { return }
        guard let statusItem = userInfo[SSAReachabilityNotificationStatusItem] as? String else { return }
                
        print(statusItem)
    }
    
```
###Installation 
As for now please clone the repository and drag the source folder into your project to use SSASwiftReachability. (Cocoapods & Carthage
support coming soon) 

###Author

Sebastian Andersen

Inspired by AFNetworkReachabilityManager

###License

SSASwiftReachability is available under the MIT license. See the LICENSE file for more info.
