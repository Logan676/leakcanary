# Dev Environment for LeakCanary contributors

## Setup
* Download [Android Studio](https://developer.android.com/studio)
* We use two spaces code indentation, use `SquareAndroid` code style settings from https://github.com/square/java-code-styles
* Build with `./gradlew build`
* Running the failing UI tests to confirm leak detection correctly fails UI tests: `./gradlew leakcanary-sample:connectedCheck`
* Normal UI tests: `./gradlew leakcanary-support-fragment:connectedCheck`


## Static Code Analysis 
* LeakCanary [uses](https://github.com/square/leakcanary/pull/1535) tool [Detekt](https://arturbosch.github.io/detekt/) for static Code analysis
* Analyze whole project with `./gradlew check` or particular modules with `./gradlew :module-name:check`. Detekt will fail the build if any ruleset violations are found. **You should fix all issues before pushing the branch to remote**.
  * There's also a **git pre-push** hook that will run analysis automatically before pushing branch to remote. If there are any violations - it will prevent the push. Fix the issues!
  * You can bypass the git hook though; Travis CI will still run checks and will fail if any violations are found. 
* Detekt report will be printed in console and saved to `/moduleDir/build/reports/
