# Period

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Tests][ico-tests]][link-tests]

Create date ranges and periods of time with ease.

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
- [Plytas](https://github.com/plytas)
- [All Contributors](../../contributors)

This package was extracted from [gtmassey/laravel-analytics](https://github.com/gtmassey/laravel-analytics). A special thanks goes to [Plytas](https://github.com/plytas) for their help in creating the original package this code is extracted from.

Thank you to the team at [Spatie](https://github.com/spatie) for their awesome packages and inspiration. Their laravel-analytics package was the inspiration for this project and the analytics project.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/gtmassey/period.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/gtmassey/period.svg?style=flat-square
[ico-tests]: https://github.com/gtmassey/period/actions/workflows/run-tests.yml/badge.svg

[link-packagist]: https://packagist.org/packages/gtmassey/period
[link-downloads]: https://packagist.org/packages/gtmassey/period
[link-tests]: https://github.com/gtmassey/period/actions/workflows/run-tests.yml
