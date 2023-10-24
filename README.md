Automated performance testing and telemetry with Drupal core.

1. Install ddev
1. Clone this repo.
1. `ddev start`
1. `ddev composer install`
1. `cp phpunit.xml.example web/core/phpunit.xml`
1. Once these steps are working, do the following to run tests and log traces.
1. `ddev ssh`
1. `OTEL_COLLECTOR=http://otel-collector:4318/v1/traces vendor/bin/phpunit --group OpenTelemetry -c web/core/phpunit.xml`
1. Run either all of the tests or at least one, three times each or more for
   series data to begin showing in the dashboard.
1. Go to <http://localhost:3000/dashboards> to get started viewing metrics and
   traces.

If you are running on an M1 or M2 Mac, add the following steps to get
chromedriver working.

1. `cd .ddev`
1. `rm docker-compose.chromedriver.yml`
1. `ddev get ddev/ddev-selenium-standalone-chrome`
