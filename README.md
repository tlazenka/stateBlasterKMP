## stateBlasterKMP

### Kotlin/Ktor/Android

`rm -rf ~/.m2/repository/com/stateblaster/`
`ls -al ~/.m2/repository/com/stateblaster`

(Just to make sure we're publishing locally below)

```
./gradlew \
  :witness-annotations:publishToMavenLocal \
  :witness-runtime:publishToMavenLocal \
  :witness-processor:publishToMavenLocal
```
  
`ls -al ~/.m2/repository/com/stateblaster`
  
```
cd examples/ktor-server && \
  gradle clean run --no-daemon \
      --refresh-dependencies
```
  
```
cd examples/android  && \
  gradle clean assembleDebug \
    --refresh-dependencies \
    --no-daemon
```
