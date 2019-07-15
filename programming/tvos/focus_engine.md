# tvOS Focus Engine Quirks

You are allowed to break the default focus engine behavior in so many ways. Here some of the information to be careful.

Launch your application with: `-UIFocusLoggingEnabled YES` to easily debug your focus problems.

## UIButton

These changes breaks the default focused visual for buttons (elevation and remote nudging)

**Changing Font Attributes**

Don't change the `font` property of `titleLabel`. Try to achieve the same thing by using `NSAttributedString`.
    
