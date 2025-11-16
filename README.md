# Smith SBSift ⚡

**Enhanced Swift build analysis tool for development workflows**

[![Swift Version](https://img.shields.io/badge/Swift-6.0-orange.svg)](https://swift.org)
[![Platform](https://img.shields.io/badge/Platform-mOS%20%7C%20iOS%20%7C%20visionOS-lightgrey.svg)](https://developer.apple.com)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Smith SBSift provides comprehensive Swift build analysis with Smith Framework integration, converting verbose Swift build output into structured, token-efficient formats designed for AI agents and modern development workflows.

## 🎯 **Overview**

Smith SBSift specializes in **Swift build output analysis**, offering:

- **⚡ Build Parsing** - Extract errors, warnings, and timing from Swift build output
- **📊 Performance Analysis** - Identify compilation bottlenecks and slow files
- **🔍 Issue Detection** - Automatic identification of build problems
- **📈 Progress Monitoring** - Real-time build progress tracking

## 🚀 **Quick Start**

### **Installation**
```bash
# Install via Homebrew
brew install smith-tools/smith/smith-sbsift

# Or build from source
git clone https://github.com/Smith-Tools/smith-sbsift
cd smith-sbsift
swift build
```

### **Basic Usage**
```bash
# Parse Swift build output
swift build 2>&1 | smith-sbsift parse

# Analyze build with timing
smith-sbsift analyze

# Monitor build progress
swift build 2>&1 | smith-sbsift monitor --timeout 300
```

## 📋 **Commands**

### **🔍 analyze**
Comprehensive Swift build analysis.

```bash
smith-sbsift analyze [--project <path>] [--format json]
```

### **📝 parse**
Parse Swift build output from stdin.

```bash
swift build 2>&1 | smith-sbsift parse [--format json] [--verbose]
```

### **⏱️ monitor**
Monitor build progress with timeout.

```bash
smith-sbsift monitor [--timeout <seconds>] [--format summary]
```

### **✅ validate**
Validate Swift build configuration.

```bash
smith-sbsift validate [--project <path>]
```

## 🏗️ **Smith Tools Ecosystem**

Smith SBSift is part of the comprehensive Smith Tools suite:

- **[smith-core](https://github.com/Smith-Tools/smith-core)** - Core framework and data models
- **[smith-cli](https://github.com/Smith-Tools/smith-cli)** - Unified interface
- **[smith-spmsift](https://github.com/Smith-Tools/smith-spmsift)** - SPM analysis
- **[smith-xcsift](https://github.com/Smith-Tools/smith-xcsift)** - Xcode build analysis
- **[xcsift](https://github.com/Smith-Tools/xcsift)** - Clean xcsift implementation

## 📄 **License**

Smith SBSift is available under the [MIT License](LICENSE).

---

**Smith SBSift - Context-efficient Swift build analysis**