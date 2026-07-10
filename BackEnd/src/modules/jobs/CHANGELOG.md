# jobs module changelog

All notable changes to the `jobs` backend module are documented here.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)
and this module adheres to [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added
- Job-level idempotency support for payout-triggering jobs
- `JobIdempotencyService` — wrapper around the existing idempotency layer with job-queue–specific semantics
- `PayoutProcessor` wired to the payouts queue in `JobsService`

### Changed
- `JobsService.constructor` now accepts optional `PayoutProcessor` dependency for payout job processing
