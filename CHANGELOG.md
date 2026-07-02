# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2026-07-02

### Added

- `reduce` and `transfer` methods now accept an optional `bool allowNegative` parameter (default: `false`), allowing callers to explicitly permit balances going negative.

### Changed

- `LegacyMoneyEconomy::reduce` / `transfer` now check the current balance before deducting when `allowNegative` is `false`, returning `false` if funds are insufficient.
- `ScoreboardEconomy::reduce` / `transfer` now check the current balance before deducting when `allowNegative` is `false`, returning `false` if funds are insufficient.

## [0.3.0]

### Changed

- Updated LeviLamina to version 26.10.0.
- Adapted to Minecraft Bedrock 26.1.

## [0.2.0]

### Changed

- Upgraded LeviLamina to 1.9.0.
- Added `LL_PLAT_S` define for server platform target.

## [0.1.0]

### Added

- Initial release with `IEconomy` interface.
- `LegacyMoneyEconomy` backend via Windows DLL symbol calls.
- `ScoreboardEconomy` backend via Minecraft scoreboard API.
- `NullEconomy` no-op backend for disabling the economy.
- C++20 `EconomyImpl` concept for compile-time implementation validation.
