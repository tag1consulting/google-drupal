Automated performance testing and telemetry with Drupal core.

1. Install ddev
1. Clone this repo.
1. `composer install`
1. In the project directory run `ddev config`
1. `ddev start`
1. `cp phpunit.xml.example web/core/phpunit.xml`
1. Once these steps are working, do the following to run tests and log traces.
1. `ddev ssh`
1. `cd web/core`
1. `../../vendor/bin/phpunit --group OpenTelemetry`
1. Run the tests at least three times to populate time series data.
1. Go to http://localhost:3000/dashboards to get started viewing metrics and traces.
