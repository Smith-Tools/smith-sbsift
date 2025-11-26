---
name: smith-sbsift
description: Swift build analysis and error detection. Automatically triggers for:
             Swift build output, compilation errors, build performance, bottleneck analysis
allowed-tools: [Bash, Read]
executables: ["~/.local/bin/smith-sbsift", ".build/release/smith-sbsift", "smith-sbsift"]
---

# Swift Build Analysis

Analyzes Swift build output to extract errors, warnings, and performance metrics.

## Automatic Usage

This skill activates when users ask about:
- "My Swift build is slow"
- "Analyze this build output"
- "What's causing compilation errors"
- "Build performance analysis"
- "Swift compiler warnings"

## Commands

**Parse build output** (token-optimized):
```bash
swift build 2>&1 | sbsift parse
# Returns: JSON with errors, warnings, timing

# With specific format
swift build 2>&1 | sbsift parse --format json
swift build 2>&1 | sbsift parse --format summary
```

**Analyze Xcode builds**:
```bash
xcodebuild build -scheme MyApp 2>&1 | sbsift
# Returns: Structured analysis of build issues
```

**Monitor build progress**:
```bash
swift build 2>&1 | sbsift monitor --timeout 300
# Returns: Real-time progress with ETA
```

**Validate project configuration**:
```bash
sbsift validate --project /path/to/project
# Returns: Configuration validation report
```

## Output Modes

- **json**: Full JSON structure with all details
- **summary**: Minimal output (default)
- **detailed**: Complete diagnostic information

## Integration with Smith Tools

Works with the Smith Tools ecosystem:

- **smith-spmsift** - SPM dependency analysis
- **smith-validation** - Architectural analysis
- **smith-xcsift** - Xcode-specific builds

## Performance

- Parse time: <100ms for typical builds
- Output size: 43% reduction vs raw output
- Memory: Minimal streaming processing
- Token efficiency: 60-70% savings for Claude

---

**smith-sbsift** - Making Swift build output AI-friendly

Last Updated: November 26, 2025
