# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

### Added
- Configurable log retention days per log level. Added specific log-level retention preferences in `LOGGER_PREFS` (e.g., `PURGE_AFTER_DAYS_DEBUG`, `PURGE_AFTER_DAYS_INFORMATION`). If a specific preference is not set (i.e. does not exist in `LOGGER_PREFS`), the logs for that level will **not** be purged automatically. The general `PURGE_AFTER_DAYS` acts as a fallback only for undefined or custom log levels not covered by these preferences. Providing an explicit value via the `p_purge_after_days` parameter in `logger.purge` will override all preferences and enforce that retention across all purged levels.
