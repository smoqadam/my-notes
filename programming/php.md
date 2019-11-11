# PHP

#### PSRs:

1. PSR-1: [Basic Coding Standard](https://www.php-fig.org/psr/psr-1)
2. PSR-3: [Logger Interface](https://www.php-fig.org/psr/psr-3)
3. PSR-4: [Autoloading Standard](https://www.php-fig.org/psr/psr-4)
4. PSR-6: [Caching Interface](https://www.php-fig.org/psr/psr-6)
5. PSR-7: [HTTP Message Interface](https://www.php-fig.org/psr/psr-7) 
6. PSR-11: [Container Interface](https://www.php-fig.org/psr/psr-11)
7. PSR-12: [Extended Coding Style Guide](https://www.php-fig.org/psr/psr-12)
8. PSR-13: [Hypermedia Links](https://www.php-fig.org/psr/psr-13)
9. PSR-14: [Event Dispatcher](https://www.php-fig.org/psr/psr-14)
10. PSR-15: [HTTP Handlers](https://www.php-fig.org/psr/psr-15)
11. PSR-16: [Simple Cache](https://www.php-fig.org/psr/psr-16)
12. PSR-17: [HTTP Factories](https://www.php-fig.org/psr/psr-17)
13. PSR-18: [HTTP Client ](https://www.php-fig.org/psr/psr-18)

#### Traits

For lack of multiple inheritance, then cannot instantiate

#### Require vs include

 Require cause a fatal error but include cause a warning

#### [ ](https://www.php-fig.org/psr/psr-18)What is declare\(strict\_types=1\)

Without this, php try to convert the values between types if possible, for example, if the parameters would be int and we pass float without declare\(strict\_types=1\); it converts it to an int, but with declare\(strict\_types=1\); it will show a fata\_error

#### Reflection

getting some information about a class, method or function. For example Doctrine use reflection to access entities DocBlock properties.

