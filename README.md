# reactNativeAppTips
Tips for building react native apps


## redux 

You can use redux with react-native. However, some of the newer versions Do Not work with react-native.
### Symptoms
  errors when using connect   e.g. export default connect(mapStateToProps)(myComponent)
### Solution
ensure react-redux version is  "react-redux": "6.0.1". If using npm, yarn or similar, this can be set in the apps package.json file.
