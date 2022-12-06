# Create date ranges and periods of time with ease.

[![Latest Version on Packagist](https://img.shields.io/packagist/v/gtmassey/period.svg?style=flat-square)](https://packagist.org/packages/gtmassey/period)
[![GitHub Tests Action Status](https://img.shields.io/github/workflow/status/gtmassey/period/run-tests?label=tests)](https://github.com/gtmassey/period/actions?query=workflow%3Arun-tests+branch%3Amain)
[![GitHub Code Style Action Status](https://img.shields.io/github/workflow/status/gtmassey/period/Fix%20PHP%20code%20style%20issues?label=code%20style)](https://github.com/gtmassey/period/actions?query=workflow%3A"Fix+PHP+code+style+issues"+branch%3Amain)
[![Total Downloads](https://img.shields.io/packagist/dt/gtmassey/period.svg?style=flat-square)](https://packagist.org/packages/gtmassey/period)

This is where your description should go. Limit it to a paragraph or two. Consider adding a small example.

## Support us

[<img src="https://github-ads.s3.eu-central-1.amazonaws.com/period.jpg?t=1" width="419px" />](https://spatie.be/github-ad-click/period)

We invest a lot of resources into creating [best in class open source packages](https://spatie.be/open-source). You can support us by [buying one of our paid products](https://spatie.be/open-source/support-us).

We highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using. You'll find our address on [our contact page](https://spatie.be/about-us). We publish all received postcards on [our virtual postcard wall](https://spatie.be/open-source/postcards).

## Installation

You can install the package via composer:

```bash
composer require gtmassey/period
```

## Usage

All instances of Period take in Carbon instances for the `startDate` and `endDate`. 

You can define a period by passing a start and end date to the static `create` method:

```php

$customPeriod = Period::create(Carbon::now()->subDays(3), Carbon::now());

```

You can also use one of the many methods provided for you to generate pre-defined periods of time:

```php

//days
Period::today();
Period::yesterday();
Period::lastDays(int $days); //$days = 2
Period::lastDaysExcludingToday(int $days); //$days = 2

//weeks
Period::thisWeek();
Period::thisWeekExcludingToday();
Period::lastWeek();
Period::lastWeeks(int $weeks);

//months
Period::thisMonth();
Period::thisMonthExcludingToday();
Period::lastMonth();
Period::lastMonths(int $months);

//quarters (3 months)
Period::thisQuarter();
Period::thisQuarterExcludingToday();
Period::lastQuarter();
Period::lastQuarters(int $quarters);

//years
Period::thisYear();
Period::thisYearExcludingToday();
Period::lastYear();
Period::lastYears(int $years);

```

## Testing

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [Garrett Massey](https://github.com/gtmassey)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
