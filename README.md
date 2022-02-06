# Admin Menu Page Builder
An easy way to create `admin pages` in WordPress


## How to use in managed environments

If you wish to use this extension in a managed environment, simply install using `composer`:

```
composer require stephenharris/wp-query-builder
```

To use the Query builder

```php
include('vendor/autoload.php');

// create a example page like this:
$pathPage = get_template_directory().'/example-page.php';


use \WpAdminPage\BuildPage;

BuildPage::start()
->setPageTitle('titolo pagina') // required
->setMenuTitle('Menu title')    // required
->setCapability('manage_options') // optional default manage_options
->setPageName('Page-name')       // required
->setDashIcon('dashicons-admin-site')  // optional
->setPosition('80')   // optional
->setPathPage($pathPage)
->createPage();
```
