Automated performance testing and telemetry with Drupal core.

1. Install ddev
1. Clone this repo.
1. In the project directory run `ddev config`
1. `ddev start`
1. `composer install`
1. `cp phpunit.xml.example web/core/phpunit.xml`
1. `ddev ssh`
1. `cd web/core`
1. `../../vendor/bin/phpunit profiles/demo_umami/tests/src/FunctionalJavaScript/PerformanceTest.php`
