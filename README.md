# Quiz app for Device Agnostic Design
A small fun quiz app.

## Getting Started
Visit https://awenna.github.io/DAD-Project-1/

## NOTE
Two tests fail on rendering overflows. I've spent about 3-4 hours trying to fix this, but as it's not within the scope of the project (the topic seems to be handled in chapters after the project) I've elected not to spend further time on it, as the app works otherwise. Let me know if fixing them is required for passing with merits.

## Key learnings
1. Solidifying learnings from course exercises. Felt like starting to get some grasp on how to write Flutter apps from scratch.
2. Use the debugger when writing and debugging tests, otherwise you won't get good error messages.
3. Don't trust AI. It either hallucinates too much or recommends different libraries to be useful. Stackoverflow + trial and error is still king.

## Key challenges
1. Flutter feels like a very cumbersome and verbose framework, even simple things seemed to require lots of boilerplate or tricks. Styles and container structure is very very verbose and cumbersome to write. Tests don't bubble up errors unless you go into debugger (taking away about half of the benefits of automated testing). Error messages are unhelpful, e.g. realizing a provider wasn't defined/overridden in a test took 30 minutes of digging down with debugger.
2. I found course material insufficient for preparing me how structure and test a larger application. Folder structure, sure, but how to create data stores for multipe pages, how to create a header and styles common for all pages, that tests sometimes need manually created providers / overrides and various other smaller problems. 
3. I could not figure how to programmatically save n states to SharedPreferences. Tried saving statistics as json, but ended up having too many problems with it. I settled on an ugly solution and simplified my functionality, which initially exceeded requirements.

## Dependencies
### Normal
flutter:
    sdk: flutter
http: any
hooks_riverpod: ^2.4.0
flutter_hooks: ^0.18.0
flutter_riverpod: ^2.4.0
go_router: ^11.0.0
shared_preferences: ^2.2.1

### Dev
  flutter_test:
    sdk: flutter
  flutter_lints: ^2.0.0
  test: any
  nock: ^1.2.3

## Test coverage
Measured to be >60%