# reactNativeAppTips
Tips for building react native apps


## redux 

You can use redux with react-native. However, some of the newer versions Do Not work with react-native.
### Symptoms
  errors when using connect   e.g. `export default connect(mapStateToProps)(myComponent)`
### Solution
ensure react-redux version is  "react-redux": "6.0.1". If using npm, yarn or similar, this can be set in the apps package.json file.


## Navigation

### Symptoms
  errors when createMaterialTopTabNavigator is used.
 e.g   Warning: Failed prop type: The prop \`bounces\` is marked as required in \`PagerAndroid\`, but its value is \`undefined\`.
### Solution
  ensure `bounces` is passed in TabNavigatorConfig
  e.g. 
```javascript
    createMaterialTopTabNavigator({ HomeStack, LinkStack, SettingsStack, }, {bounces: false});
 ```
 #### Further Info
 [Original pull request to add bounces to PagerScroll](https://github.com/react-native-community/react-native-tab-view/pull/722 "react-native-tab-view") 
