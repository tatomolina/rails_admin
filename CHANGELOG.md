# RailsAdmin Changelog

## [Unreleased](https://github.com/sferik/rails_admin/tree/HEAD)

[Full Changelog](https://github.com/sferik/rails_admin/compare/v1.0.0.rc...HEAD)

### Changed
- Change parent controller to ActionController::Base for out-of-box support of Rails 5 API mode([#2688](https://github.com/sferik/rails_admin/issues/2688))
  - To keep old behavior, add `config.parent_controller = '::ApplicationController'` in your RailsAdmin initializer.

## [1.0.0.rc](https://github.com/sferik/rails_admin/tree/v1.0.0.rc) - 2016-07-18

[Full Changelog](https://github.com/sferik/rails_admin/compare/v0.8.1...v1.0.0.rc)

### Added
- Rails 5 support
- PaperTrail 5 support([9c42783a](https://github.com/sferik/rails_admin/commit/9c42783aa65b704f4a5d467608c49b746c47b81b))
- Support for multiple configuration blocks([#1781](https://github.com/sferik/rails_admin/pull/1781), [#2670](https://github.com/sferik/rails_admin/pull/2670))
- Default association limit is now configurable([#2508](https://github.com/sferik/rails_admin/pull/2058))

### Changed
- Prefix kaminari bootstrap views with `ra-` to avoid name conflict([#2283](https://github.com/sferik/rails_admin/issues/2283), [#2651](https://github.com/sferik/rails_admin/pull/2651))
- Gravatar icon is now optional([#2570](https://github.com/sferik/rails_admin/pull/2570))
- Improve bootstrap-wysihtml5-rails support([#2650](https://github.com/sferik/rails_admin/pull/2650))
- Explicitly call the #t method on I18n([#2564](https://github.com/sferik/rails_admin/pull/2564))
- Improve dashboard performance by querying with id instead of updated_at([#2514](https://github.com/sferik/rails_admin/issues/2514), [#2551](https://github.com/sferik/rails_admin/pull/2551))
- Improve encoding support in CSV converter([#2508](https://github.com/sferik/rails_admin/pull/2508), [dca8911f](https://github.com/sferik/rails_admin/commit/dca8911f240ea11ebb186c33573188aa9e1b031d))
- Add SVG file extension to the image detection method([#2533](https://github.com/sferik/rails_admin/pull/2533))
- Update linear gradient syntax to make autoprefixer happy([#2531](https://github.com/sferik/rails_admin/pull/2531))
- Improve export layout ([#2505](https://github.com/sferik/rails_admin/pull/2505))

### Removed
- Remove safe_yaml dependency([#2397](https://github.com/sferik/rails_admin/pull/2397))
- Drop support for Ruby < 2.1.0

### Fixed
- Pagination did not work when showing all history([#2553](https://github.com/sferik/rails_admin/pull/2553))
- Make filter-box label clickable([#2573](https://github.com/sferik/rails_admin/pull/2573))
- Colorpicker form did not have the default css class `form-control`([#2571](https://github.com/sferik/rails_admin/pull/2571))
- Stop assuming locale en is available([#2155](https://github.com/sferik/rails_admin/issues/2155))
- Fix undefined method error with nested polymorphics([#1338](https://github.com/sferik/rails_admin/issues/1338), [#2110](https://github.com/sferik/rails_admin/pull/2110))
- Fix issue with nav does not check pjax config from an action([#2309](https://github.com/sferik/rails_admin/pull/2309))
- Model label should be pluralized with locale([#1983](https://github.com/sferik/rails_admin/pull/1983))
- Fix delocalize strftime_format for DateTime.strptime to support minus([#2547](https://github.com/sferik/rails_admin/pull/2547))
- Fix Syntax Error in removal of new nested entity([#2539](https://github.com/sferik/rails_admin/pull/2539))
- Fix momentjs translations for '%-d' format day of the month([#2540](https://github.com/sferik/rails_admin/pull/2540))
- Fix Mongoid BSON object field ([#2495](https://github.com/sferik/rails_admin/issues/2495))
- Make browser ignore validaitons of removed nested child models([#2443](https://github.com/sferik/rails_admin/issues/2443), [#2490](https://github.com/sferik/rails_admin/pull/2490))


## [0.8.1](https://github.com/sferik/rails_admin/tree/v0.8.1) - 2015-11-24

[Full Changelog](https://github.com/sferik/rails_admin/compare/v0.8.0...v0.8.1)

### Fixed
- `vendor/` directory was missing from gemspec([#2481](https://github.com/sferik/rails_admin/issues/2481), [#2482](https://github.com/sferik/rails_admin/pull/2482))


## [0.8.0](https://github.com/sferik/rails_admin/tree/v0.8.0) - 2015-11-23

[Full Changelog](https://github.com/sferik/rails_admin/compare/v0.7.0...v0.8.0)

### Added
- Feature to deactivate filtering-multiselect widget's remove buttons through `removable?` field option([#2446](https://github.com/sferik/rails_admin/issues/2446))
- Pundit integration([#2399](https://github.com/sferik/rails_admin/pull/2399) by Team CodeBenders, RGSoC'15)
- Refile support([#2385](https://github.com/sferik/rails_admin/pull/2385))

### Changed
- Some UI improvements in export view([#2394](https://github.com/sferik/rails_admin/pull/2394))
- `rails_admin/custom/variables.scss` is now imported first to take advantage of Sass's `default!`([#2404](https://github.com/sferik/rails_admin/pull/2404))
- Proxy classes now inherit from BasicObject([#2434](https://github.com/sferik/rails_admin/issues/2434))
- Show sidebar scrollbar only on demand([#2419](https://github.com/sferik/rails_admin/pull/2419))
- RailsAdmin no longer gets excluded from NewRelic instrumentation by default([#2402](https://github.com/sferik/rails_admin/pull/2402))
- Improve efficiency of filter query in Postgres([#2401](https://github.com/sferik/rails_admin/pull/2401))
- Replace old jQueryUI datepicker with jQuery Bootstrap datetimepicker ([#2391](https://github.com/sferik/rails_admin/pull/2391))
- Turn Hash#symbolize into a helper to prevent namespace conflict([#2388](https://github.com/sferik/rails_admin/pull/2388))

### Removed
- The L10n translation `admin.misc.filter_date_format` datepicker search filters, has been dropped in favor of field oriented configuration ([#2391](https://github.com/sferik/rails_admin/pull/2391))

### Fixed
- AR#count broke when default-scoped with select([#2129](https://github.com/sferik/rails_admin/pull/2129), [#2447](https://github.com/sferik/rails_admin/issues/2447))
- Datepicker could not handle Spanish date properly([#982](https://github.com/sferik/rails_admin/issues/982), [#2451](https://github.com/sferik/rails_admin/pull/2451))
- Paperclip's `attachment_definitions` does not exist unless `has_attached_file`-ed([#1674](https://github.com/sferik/rails_admin/issues/1674))
- `.btn` class was used without a modifier([#2417](https://github.com/sferik/rails_admin/pull/2417))
- Filtering-multiselect widget ignored order([#2231](https://github.com/sferik/rails_admin/issues/2231), [#2412](https://github.com/sferik/rails_admin/pull/2412))
- Add missing .alert-dismissible class to flash([#2411](https://github.com/sferik/rails_admin/pull/2411))
- Keep field order on changing the existing field's type([#2409](https://github.com/sferik/rails_admin/pull/2409))
- Add button for nested-many form in modal disappeared on click([#2372](https://github.com/sferik/rails_admin/issues/2372), [#2383](https://github.com/sferik/rails_admin/pull/2383))

### Security
- Fix XSS vulnerability in polymorphic select([#2479](https://github.com/sferik/rails_admin/pull/2479))


## [0.7.0](https://github.com/sferik/rails_admin/tree/v0.7.0) - 2015-08-16

[Full Changelog](https://github.com/sferik/rails_admin/compare/v0.6.8...v0.7.0)

### Added
- Support for ActiveRecord::Enum ([#1993](https://github.com/sferik/rails_admin/issues/1993))
- Multiselect-widget shows user friendly message, instead of just being blank ([#1369](https://github.com/sferik/rails_admin/issues/1369), [#2360](https://github.com/sferik/rails_admin/pull/2360))
- Configuration option to turn browser validation off ([#2339](https://github.com/sferik/rails_admin/pull/2339), [#2373](https://github.com/sferik/rails_admin/pull/2373))

### Changed
- Multiselect-widget inserts a new item to the bottom, instead of top ([#2167](https://github.com/sferik/rails_admin/pull/2167))
- Migrated Cerulean theme to Bootstrap3 ([#2352](https://github.com/sferik/rails_admin/pull/2352))
- Better html markup for input fields ([#2336](https://github.com/sferik/rails_admin/pull/2336))
- Update filter dropdown button to Bootstrap3 ([#2277](https://github.com/sferik/rails_admin/pull/2277))
- Improve navbar appearance ([#2310](https://github.com/sferik/rails_admin/pull/2310))
- Do not monkey patch the app's YAML ([#2331](https://github.com/sferik/rails_admin/pull/2331))

### Fixed
- Browser validation prevented saving of persisted upload fields ([#2376](https://github.com/sferik/rails_admin/issues/2376))
- Fix inconsistent styling in static_navigation ([#2378](https://github.com/sferik/rails_admin/pull/2378))
- Fix css regression for has_one and has_many nested form ([#2337](https://github.com/sferik/rails_admin/pull/2337))
- HTML string inputs should not have a size attribute valorized with 0 ([#2335](https://github.com/sferik/rails_admin/pull/2335))

### Security
- Fix XSS vulnerability in filtering-select widget
- Fix XSS vulnerability in association fields ([#2343](https://github.com/sferik/rails_admin/issues/2343))
