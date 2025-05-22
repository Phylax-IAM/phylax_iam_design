# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/)
and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [1.3.0] - 2025-05-22
### Added
- Introduced `analytics-service` for tracking clicks via Kafka
- Added OpenAPI spec validation to CI pipeline

### Changed
- Improved Redis caching TTL strategy in `url-service`
- Upgraded PostgreSQL from 13 → 15

### Fixed
- Bug where custom slugs weren't checked for collisions

---

## [1.2.0] - 2025-04-10
### Added
- Added support for expiring links
- User authentication with API key added to gateway

### Deprecated
- Legacy GET /shorten endpoint (to be removed in 1.4.0)

---

## [1.0.0] - 2025-03-01
### Added
- Initial release: Phylax IAM
