# React-Native-App-Food-delivery-flow

## Step 1
1. Initialized a new react native app using 

<code>$ react-native init FoodDeliveryApp</code>

2. Imported **assets** containing sub folders

```
assets
│   
└───icons - Store icons in png format
│   
└───images - Store images in jpg format
│ 
└───fonts - Store fonts to be used in the app
```
3. These assets are constant assets, so we created a folder in the rootfile with the name **constants**

```
constants
│   
└───icons.js - import each icon using the JS require() and setting them as a constant,then export all as default.
│   
└───images.js - import each images using the JS require() and setting them as a constant, then export all as default.
│ 
└───theme.js - Import Colors fonts and sizes needs for the app.
│ 
└───map.js - Import GOOGLE-API-KEY for the map.
│ 
└───index.js - Import icon.js, images.js, theme.js and map.js, then exports all.
```


## Step 2 Navigation & Screens

1. intall navigation modules and other plugins

<code>$ yarn add @react-navigation/native react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view @react-navigation/stack @react-navigation/bottom-tabs </code>


2. Run <code>$ npm start</code> in one terminal
3. Open another termial and run <code> $ react-native run-android </code>
4. A **Screens** folder stores all views

```
Screens
│   
└───Home.js
│   
└───Restaurant.js
│ 
└───OrderDelivery.js
│ 
└───index.js - Import Home,Restaurant and OrderDelivery
```

5. in the App.js, the createStackNavigator was imported from @react-navigation/stack and also the navigatorContainer from @react-navigation/native

<code> import {createStackNavigator} from '@react-navigation/stack
  
  import {NavigationContainer} from '@react-navigation/native'
  
  const Stack=createStackNavigator()
</code>

 

  ```
         const App=()=>{
    return (
        <NavigationContainer>
            <Stack.Navigator
             screenOptions={{
                 headerShown:false
             }}
             initialRouteName={"Home"}
            >
                <Stack.Screen name="Home" component={Home} />
                <Stack.Screen name="Restaurant" component={Restaurant} />
                <Stack.Screen name="OrderDelivery" component={OrderDelivery} />
                
            </Stack.Navigator>
        </NavigationContainer>
    )
}

export default App
```

6. Run app to ensure it is working perfectly.


## Step 3 Bottom Navigation Part 1

1. Create a folder called **navigation** and add a file called **tabs.js**

```
navigation
│   
└───tabs.js
```
2. Import createBottomTabNavigator,BottomTabBar from '@react-navigation/bottom-tabs'
3. Initialize createBottomTabNavigator() to a variable called **Tab**

<code> const Tab=createBottomTabNavigator() </code>

4. 
