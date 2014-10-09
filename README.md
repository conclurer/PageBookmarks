# Page Bookmarks

This module provides a simple API for letting the user bookmark pages. It differentiates between logged on users and guests.

### Bookmark API

```php
$page->bookmark->save();	// bookmarks the current page for the current user
```

This will add a basic bookmark to the current page. You can *optionally* allow the user to set custom tags or a custom comment for the bookmark:

```php
$page->comment = 'I love kittens';
$page->tags = array('cute', 'fluffy', 'pink');
$page->bookmark->save();
```

You can remove the bookmark using `$page->bookmark->delete()`.

### User Bookmarks API

You can get all bookmarks of the user this way:

```php
$user->bookmarks; //Returns an array containing all bookmarks
```

Furthermore, if you want to get the bookmarks grouped by tag, you can use `$user->bookmarks(true)`.

### Demo

You can find a live demo version of this module here: [http://nickel-1vn.lightningpw.com](http://nickel-1vn.lightningpw.com).