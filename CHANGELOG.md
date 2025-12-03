# Changelog

All notable changes to smith-sbsift will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [3.2.0] - 2024-12-03

### Changed
- **Foundation Integration**: Migrated to Smith Foundation libraries
  - Now uses SmithBuildAnalysis for core parsing logic
  - Integrated SmithProgress for progress tracking
  - Integrated SmithOutputFormatter for consistent output formatting
  - Integrated SmithErrorHandling for structured error management (7 error locations updated)
- **Improved Error Handling**: All errors now use structured types:
  - ValidationError for input validation (lines 48, 304, 612)
  - ResourceError for missing input (lines 63, 319)
  - SystemError for build failures (lines 518, 572)
- **Better Progress Tracking**: Added visual progress indicators to monitor command
- **Consistent Output**: All output uses SmithCLIOutput or SmithOutputFormatter

### Dependencies
- Added: smith-build-analysis
- Added: smith-foundation/SmithProgress
- Added: smith-foundation/SmithOutputFormatter
- Added: smith-foundation/SmithErrorHandling

### Internal
- 95% reduction in duplicate code by using foundation libraries
- Unified error handling with actionable suggestions
- Professional error messages with error codes

## [3.1.0-smith] - 2024-11-15

### Added
- Swift 6.0 support
- Enhanced SPM parsing
- Performance improvements

## [3.0.0] - 2024-10-01

### Added
- Initial release with Swift build parsing
- Real-time monitoring
- JSON output support