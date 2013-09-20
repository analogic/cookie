Cookie
======

Simple cookies manipulation (browser side) with api similar to jquery.cookie

Example
-------

```Dart
import 'package:cookie/cookie.dart' as cookie;
```

Create session cookie:
```Dart
cookie.set('the_cookie', 'the_value');
```

Create expiring cookie, 7 days from then:
```Dart
    cookie.set('the_cookie', 'the_value', expires: 7);
```

Create expiring cookie, valid across entire site:
```Dart
    cookie.set('the_cookie', 'the_value', expires: 7, path: '/');
```

Read cookie:
```Dart
    cookie.get('the_cookie'); // => "the_value"
    cookie.get('not_existing'); // => null
```

Delete cookie:
```Dart
    // Same path as when the cookie was written...
    cookie.remove('the_cookie', path: '/');
```

*Note: when deleting a cookie, you must pass the exact same path, domain and secure options that were used to set the cookie, unless you're relying on the default options that is.*