# Changelog

## [2.1.0](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/2.1.0) (2022-05-19)
* added 'trackScores' method to 'Search' class
* minor update of related tests 
* updated documentation and changelog

## [2.0.0](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/2.0.0) (2022-05-18)
* supports Manticore Search 5.0.0
* supports http `options` parameter
* removed `Query\Match` class as deprecated
* optimized the connection strategy name resolution 
* unified the response format for `raw` select queries
* minor changes in tests
* minor updates of documentation

**Breaking changes:**
* returns 'sql-over-http' response as an array

## [1.8.0](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/1.8.0) (2022-01-06)
* changed license from Apache 2.0 to more permissive MIT for compatibility with GPL licenses
* switched to Github actions from Travis CI
* minor changes in tests
* preparation for 4.2.0+ which returns sql-over-http response as an array

## [1.7.0](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/1.7.0) (2021-11-15)
* https://github.com/manticoresoftware/manticoresearch-php/issues/59 - Issue with umlauts when using the keywords call
* minor changes in code and tests related with Manticore Search 4.0.2 specifics

## [1.6.2](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/1.6.2) (2021-07-02)
* fixes in a number of functions that use SQL over HTTP, e.g. #56.
* code style fixes
* fixes in phpunit tests

**Breaking changes:**
* output structure of some of the functions that use SQL over HTTP is changed. Commonly used functions work as previously.


## [1.6.0](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/1.6.0) (2021-01-05)
This release adds compatibility for PHP 8.
* `Match` class is now deprecated and replaced with `MatchQuery`. You can still use the `Match` class with PHP 7.x, but a E_USER_DEPRECATED warning will be raised.
*  fixed issue generated by PHP 8 curl 

## [1.5.2](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/1.5.2) (2020-11-23)
* allow index settings to have multiple values (like `local`) in [Create](src/Manticoresearch/Endpoints/Indices/Create.php) 
* remove  hirak/prestissimo as not needed (and not compatible) with Composer 2

## [1.5.0](https://github.com/manticoresoftware/manticoresearch-php/releases/tag/1.5.0) (2020-10-26)
* add Search:facet (8a280232572eb070ed26548076bf0e2fbbe3a303) (Manticore Search 3.5.2+)
* allow docs to be StdClass or string at addDocument and addDocuments; allow no id in addDocuments; use id=0 if not specified in addDocument  (ecb363ab37101c40e40ceb2a233acfb1b4014d2d)

## [1.4](https://github.com/manticoresoftware/manticoresearch-php/tree/1.4) (2020-07-22)

[Full Changelog](https://github.com/manticoresoftware/manticoresearch-php/compare/1.3...1.4)

**Closed issues:**

- Next release [\#44](https://github.com/manticoresoftware/manticoresearch-php/issues/44)

**Merged pull requests:**

- Additional "index" method added to Client class [\#45](https://github.com/manticoresoftware/manticoresearch-php/pull/45) ([EvilFreelancer](https://github.com/EvilFreelancer))

## [1.3](https://github.com/manticoresoftware/manticoresearch-php/tree/1.3) (2020-07-09)

[Full Changelog](https://github.com/manticoresoftware/manticoresearch-php/compare/1.2...1.3)

**Closed issues:**

- Connection pool is not reset when no more retries left [\#43](https://github.com/manticoresoftware/manticoresearch-php/issues/43)
- Unable to Create Cluster [\#37](https://github.com/manticoresoftware/manticoresearch-php/issues/37)
- Coding Standards Compliance [\#36](https://github.com/manticoresoftware/manticoresearch-php/issues/36)
- Minor Error in Cluster Documentation [\#31](https://github.com/manticoresoftware/manticoresearch-php/issues/31)
- MatchPhrase Document Minorly Incorrect [\#21](https://github.com/manticoresoftware/manticoresearch-php/issues/21)
- Wrong Runtime Exception Thrown [\#19](https://github.com/manticoresoftware/manticoresearch-php/issues/19)
- In ResultHit setId and getId Do Not Mirror Each Other [\#17](https://github.com/manticoresoftware/manticoresearch-php/issues/17)
- Bulk Upload Fails Silently [\#9](https://github.com/manticoresoftware/manticoresearch-php/issues/9)

**Merged pull requests:**

- FIX: Documentation was missing a quote for the set example [\#40](https://github.com/manticoresoftware/manticoresearch-php/pull/40) ([gordonbanderson](https://github.com/gordonbanderson))
- Static Analysis Fixes [\#38](https://github.com/manticoresoftware/manticoresearch-php/pull/38) ([gordonbanderson](https://github.com/gordonbanderson))
- FIX: PhpHttp transport now works, test suite passing in Travis [\#35](https://github.com/manticoresoftware/manticoresearch-php/pull/35) ([gordonbanderson](https://github.com/gordonbanderson))
- 100% Test Coverage for Connection subdir [\#34](https://github.com/manticoresoftware/manticoresearch-php/pull/34) ([gordonbanderson](https://github.com/gordonbanderson))
- Dockerized Testing Suite [\#32](https://github.com/manticoresoftware/manticoresearch-php/pull/32) ([gordonbanderson](https://github.com/gordonbanderson))
- 100% Coverage for Index.php [\#30](https://github.com/manticoresoftware/manticoresearch-php/pull/30) ([gordonbanderson](https://github.com/gordonbanderson))
- FIX: Erroneous $ prefixing a variable name as a JSON parameter [\#29](https://github.com/manticoresoftware/manticoresearch-php/pull/29) ([gordonbanderson](https://github.com/gordonbanderson))
- ENHANCEMENT: BulkTest now 100% coverage [\#28](https://github.com/manticoresoftware/manticoresearch-php/pull/28) ([gordonbanderson](https://github.com/gordonbanderson))
- ENHANCEMENT: 100% coverage for Set and Threads in Endpoint Nodes [\#27](https://github.com/manticoresoftware/manticoresearch-php/pull/27) ([gordonbanderson](https://github.com/gordonbanderson))
- Improved Coverage of Client Test [\#25](https://github.com/manticoresoftware/manticoresearch-php/pull/25) ([gordonbanderson](https://github.com/gordonbanderson))
- ENHANCEMENT: Added test for setUpURI method [\#24](https://github.com/manticoresoftware/manticoresearch-php/pull/24) ([gordonbanderson](https://github.com/gordonbanderson))
- More Coverage for SearchTest [\#23](https://github.com/manticoresoftware/manticoresearch-php/pull/23) ([gordonbanderson](https://github.com/gordonbanderson))
- ENHANCEMENT: Tests for MatchPhrase search component [\#22](https://github.com/manticoresoftware/manticoresearch-php/pull/22) ([gordonbanderson](https://github.com/gordonbanderson))
- Distance search test [\#20](https://github.com/manticoresoftware/manticoresearch-php/pull/20) ([gordonbanderson](https://github.com/gordonbanderson))
- Unit Test for Query.php and a Fix [\#18](https://github.com/manticoresoftware/manticoresearch-php/pull/18) ([gordonbanderson](https://github.com/gordonbanderson))
- Unit Tests to 50% Coverage [\#16](https://github.com/manticoresoftware/manticoresearch-php/pull/16) ([gordonbanderson](https://github.com/gordonbanderson))

## [1.2](https://github.com/manticoresoftware/manticoresearch-php/tree/1.2) (2020-04-16)

[Full Changelog](https://github.com/manticoresoftware/manticoresearch-php/compare/1.1...1.2)

**Closed issues:**

- Update Failing With Unknown Attribute Error [\#10](https://github.com/manticoresoftware/manticoresearch-php/issues/10)
- Incorrect Documentation On Bulk Upload [\#8](https://github.com/manticoresoftware/manticoresearch-php/issues/8)

## [1.1](https://github.com/manticoresoftware/manticoresearch-php/tree/1.1) (2020-04-09)

[Full Changelog](https://github.com/manticoresoftware/manticoresearch-php/compare/1.0...1.1)

**Closed issues:**

- Suggest is Broken - Fails With "'Index name is missing.'" [\#6](https://github.com/manticoresoftware/manticoresearch-php/issues/6)
- Mva properties are updated via API /json [\#5](https://github.com/manticoresoftware/manticoresearch-php/issues/5)

## [1.0](https://github.com/manticoresoftware/manticoresearch-php/tree/1.0) (2020-03-16)

[Full Changelog](https://github.com/manticoresoftware/manticoresearch-php/compare/c156463601c60c7288a5d25e714a5caf5b99dbb6...1.0)



\* *This Changelog was automatically generated by [github_changelog_generator](https://github.com/github-changelog-generator/github-changelog-generator)*