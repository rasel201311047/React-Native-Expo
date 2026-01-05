# React-Native-Expo

### *** exactly how to hide Android back / home / recent buttons automatically in Expo + Expo Router

   ```bash
   npx expo install expo-navigation-bar
   ```

after the root layout add:
```bash
import * as NavigationBar from "expo-navigation-bar";

  useEffect(() => {
    if (fontsLoaded) {
      SplashScreen.hideAsync();
      if (Platform.OS === "android") {
        NavigationBar.setVisibilityAsync("hidden");
        NavigationBar.setBehaviorAsync("overlay-swipe");
      }
    }
  }, []);
```
