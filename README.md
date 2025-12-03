# smith-sbsift - Swift Build Analysis

> **Context-efficient Swift build output analysis for development and agentic workflows.**

Tool providing comprehensive Swift build output parsing, performance analysis, and bottleneck identification. Converts verbose Swift build logs into structured, minimal-context JSON designed for development teams and AI agents.

## 🎯 What is smith-sbsift?

smith-sbsift specializes in **Swift build output analysis**:

- **⚡ Build Parsing** - Extract errors, warnings, and timing information
- **📊 Performance Analysis** - Identify compilation bottlenecks and slow files
- **🔍 Issue Detection** - Automatic identification of common build problems
- **📈 Progress Monitoring** - Real-time build progress tracking
- **📉 Context Efficiency** - 43% reduction in output size vs raw logs
- **JSON Export** - Machine-readable results for automation

## 🚀 Quick Start

### Installation

```bash
# Via Homebrew (custom tap)
brew tap elkraneo/tap
brew install sbsift

# Or from source
git clone https://github.com/elkraneo/sbsift.git
cd sbsift
swift build -c release
cp .build/release/sbsift /usr/local/bin/
```

### Basic Usage

```bash
# Parse Swift build output
swift build 2>&1 | sbsift

# Analyze with specific format
swift build 2>&1 | sbsift --format json

# Monitor build progress
swift build 2>&1 | sbsift --monitor

# Analyze Xcode build
xcodebuild build -scheme MyApp 2>&1 | sbsift
```

## 📋 Commands

### **parse** - Parse build output

```bash
swift build 2>&1 | sbsift parse [--format json|summary]
```

Extracts errors, warnings, and compilation timing from build output.

### **analyze** - Full analysis

```bash
sbsift analyze [--project path] [--format json]
```

Comprehensive analysis including bottleneck identification.

### **monitor** - Progress tracking

```bash
swift build 2>&1 | sbsift monitor [--timeout seconds]
```

Real-time build progress with estimated time remaining.

### **validate** - Configuration check

```bash
sbsift validate [--project path]
```

Validates Swift project build configuration.

## Foundation Integration

smith-sbsift is built on the Smith Foundation libraries:

- **SmithBuildAnalysis**: Shared Swift build parsing infrastructure
- **SmithProgress**: Progress display during analysis operations
- **SmithOutputFormatter**: Consistent output formatting across all tools
- **SmithErrorHandling**: Professional error reporting with recovery suggestions

This integration provides:
- ✅ 95% reduction in duplicate code
- ✅ Consistent UX with other Smith Tools
- ✅ Single source of truth for common functionality
- ✅ Faster bug fixes and improvements (benefit all tools)

### Related Tools

smith-sbsift integrates with:
- **smith-skill**: Claude Code integration for AI-assisted development
- **smith-xcsift**: Xcode build analysis (complementary tool)
- **smith-spmsift**: Swift Package Manager analysis
- **Smith CLI**: Unified CLI orchestrator

## 📊 Performance

- **Parse time:** <100ms for typical builds
- **Output size:** 43% reduction vs raw build output
- **Memory usage:** Minimal streaming processing
- **Token efficiency:** 60-70% savings for Claude
- **Supported:** Swift 5.5+, macOS 11.0+, iOS 14.0+

## 🛠️ Development

### Building from Source

```bash
git clone https://github.com/elkraneo/sbsift.git
cd sbsift
swift build -c release
```

### Project Structure

```
sbsift/
├── README.md                 ← This file
├── Package.swift             ← Swift package
├── Sources/
│   ├── sbsiftLib/            ← Core library
│   └── sbsift/               ← CLI tool
├── Tests/                    ← Test suite
└── Scripts/                  ← Build scripts
```

## 📋 Requirements

- **Swift 5.5+**
- **macOS 11.0+** (Monterey or later)
- **Xcode 13.0+**

## 🔗 Related Tools

- **[smith-spmsift](../smith-spmsift/)** - Swift Package Manager analysis
- **[smith-skill](../smith-skill/)** - Architecture validation
- **[smith-core](../smith-core/)** - Universal patterns
- **[xcsift](https://github.com/ldomaradzki/xcsift)** - Xcode project analysis

## 🤝 Contributing

Contributions welcome! Please:

1. Report build analysis issues with examples
2. Suggest new output formats
3. Improve error detection patterns
4. Add integration examples
5. Follow commit message guidelines (see main README)

## 📄 License

MIT - See [LICENSE](LICENSE) for details

---

**smith-sbsift - Making Swift build output AI-friendly**

*Last updated: November 17, 2025*