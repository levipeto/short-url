# Changelog

**2.0.0 (released 2020-02-14):**
- Added the functionality to track a visitor's referer URL.
- Added the functionality to track a user's device type.
- Added the functionality to explicitly set the tracking options on for each specific short URL. Previously, the options
were set in the config and affected all new and existing short URLs.
- Added the functionality to explicitly set the HTTP status code for the redirect.
- Added a ``` ShortURLVisited``` event that is dispatched when the short URL is used.
- Added the ``` trackingEnabled() ``` and ``` trackingFields() ``` helper methods to the ``` ShortURL ``` model.

**1.2.1 (released 2020-01-13):**
- Fixed a bug that allowed multiple visits to a single-use URL if the URL's visit tracking was disabled.
[Pull Request #23](https://github.com/ash-jc-allen/short-url/pull/23)

**1.2.0 (released 2020-01-03):**
- Renamed the underlying facade class from ``` BuilderFacade ``` to ``` ShortURLBuilder ``` for consistency.

    Note: This isn't
    changing the name of the facade. It's just changing the underlying class name for if you want to use ``` use AshAllenDesign\ShortURL\Facades\ShortURLBuilder; ```
    rather than ``` use ShortURLBuilder; ```.

- Added methods to the facade docblock. This will display the methods in the IDE's autocomplete.

**1.1.0 (released 2020-01-03):**
- Enforced a minimum length of 3 for the URL ``` key_length ``` that is specified in the config.
- Included [hashids/hasids](https://github.com/vinkla/hashids) as a dependency. This is now used for generating the random, unique URL keys.
- Updated documentation.

**1.0.0 (released 2020-01-02):**
- Release for production.
- Added a ```ShortURLBuilder``` facade.
- Refactored folder structure to meet standards.
- Updated documentation (thanks [@NathanGiesbrecht](https://github.com/NathanGiesbrecht))
- Updated tests and Travis CI configuration for PHP 7.4 testing.

**0.0.1 (pre-release):**
- Initial work and pre-release testing.