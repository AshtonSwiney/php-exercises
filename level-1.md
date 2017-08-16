# Level 1 - Build a HTML template

PHP can create HTML files for you. With this new ability, you can use PHP to include parts of your websites and apps without repeating yourself.

## The old way
With plain HTML you have to edit the navigation on each of your pages.

With PHP, and other server scripting languages, you can include the one file that needs to be edited.

Now your navigation could be managed from one file that gets used on all pages. Huge time saver!

Let's see this in action...

## Require a file
You can inject whole files into another file. We're using the native `require(PATH)` function here. If the file `inc/nav.php` doesn't exist then PHP will return an error.

/// PHP index.php
```php
<html>
  <body>
    <?php require('inc/nav.php'); ?>
    <div class="content">...</div>
  </body>
</html>
```

/// PHP nav.php
```php
<nav>
  <li><a href="index.php">Home</a></li>
  <li><a href="services.php">Services</a></li>
  <li><a href="about.php">About</a></li>
  <li><a href="contact.php">Contact</a></li>
</nav>
```

/// Output index.php
```php
<html>
  <body>
    <nav>
      <li><a href="index.php">Home</a></li>
      <li><a href="services.php">Services</a></li>
      <li><a href="about.php">About</a></li>
      <li><a href="contact.php">Contact</a></li>
    </nav>
    <div class="content">...</div>
  </body>
</html>
```



## Let's let you give this a try
Take the three pages given in Exercise one and do the following for all three pages:
- use a `nav.php` for the navigation of each page
- move the `<nav>` element, and it's contents, into the `nav.php`
- use a `footer.php` for the footer of each page
- move the `<footer>` element, and it's contents, into the `footer.php`

## Exercise #1
Let's put this to practice in Cloud9
- open you `exercises/level-1/exercise-1.js`
- add a mix of 7 comments and console logs
- test your code at `exercises/level-1/exercise-1.html`
- when done, push your changes to Github to be graded

## Exercise #2
- open you `exercises/level-1/exercise-2.js`
- add a mix of 7 comments and console logs
- test your code at `exercises/level-1/exercise-2.html`
- when done, push your changes to Github to be graded

## Next up
Start [Level 2](level-2.md) - Meet my friend DOM
