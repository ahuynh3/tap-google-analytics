# Changelog

## 0.4.1
  * Removed `ga:searchKeyword` from `Behavior Overview` default dimensions to closer match the Google Analytics UI report [#20](https://github.com/singer-io/tap-google-analytics/pull/20)

## 0.4.0
  * Add ability to specify multiple profile IDs (e.g., `view_ids`) in config [#18](https://github.com/singer-io/tap-google-analytics/pull/18)
    * Note: Custom metrics/dimensions and goal-related fields will be discovered as the intersection of all fields for all selected profiles. Selecting profiles across properties may result in some custom fields being marked `unsupported`
    * If custom fields between profiles have different data types, their JSON schemas will be merged into an `anyOf` schema
  * Will translate state to multiple profile format if not already formatted [#18](https://github.com/singer-io/tap-google-analytics/pull/18)
  * Add `currently_syncing` and `currently_syncing_view` for resuming if many reports and profiles are selected [#18](https://github.com/singer-io/tap-google-analytics/pull/18)
  * Increase 429 retry count to 10 [#18](https://github.com/singer-io/tap-google-analytics/pull/18)

## 0.3.0
  * Add pre-made reports that are always returned during discovery [#16](https://github.com/singer-io/tap-google-analytics/pull/16)
  * Report day-pagination now includes current day [#16](https://github.com/singer-io/tap-google-analytics/pull/16)
  * Make raw report data parsing safe for reports without dimensions [#16](https://github.com/singer-io/tap-google-analytics/pull/16)

## 0.2.1
  * Handles top-level exceptions through Singer function [#14](https://github.com/singer-io/tap-google-analytics/pull/11)

## 0.2.0
  * Adds a 'report_definitions' config parameter to add support for syncing multiple reports [#11](https://github.com/singer-io/tap-google-analytics/pull/11)
