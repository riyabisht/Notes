---
layout: default
title: Package
parent: Dart
---

# DArt

## importing libraries from packages

To import libraries found in packages use `package:`
```dart
import 'pakage:js/js.dart' as js;
import 'pakage:intl/intl.dart';
```
- dart runtime takes everything after `pakage:` and look for it in the `pakage_config.jason`(under .dart_tool/directory) file for your app

- this can be used to import libraries within your own pakage

```
myapp/
  lib/
    own_pakage.dart
    parser.dart
  test/
    parser/
      parser_test.dart
```

```dart
import 'pakage:myapp/my_ownpakage.dart';
```