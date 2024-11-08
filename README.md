# Tether

A Swift-based flight timing and line management system implementing:
- SwiftUI
- Swift 6
- Strict Concurrency
- Protocol-oriented programming
- XCTests

## Core Features
- Flight Timer Management
- Line Input System
- Modal System
- List Management

## Architecture
- MVVM + Protocol-Oriented Design
- Actor-based Concurrency
- Comprehensive Test Coverage

## Requirements
- iOS 15.0+
- Xcode 15.0+
- Swift 6.0

## Project Structure
```
Core/
├── Timer/
│   ├── FlightTimer.swift
│   └── TimerProtocols.swift
├── Line/
│   ├── LineController.swift
│   └── LineProtocols.swift
├── Modal/
│   ├── ModalSystem.swift
│   └── ModalProtocols.swift
Tests/
├── Unit/
├── Integration/
└── System/
```

## Branch Strategy
See BRANCH_STRATEGY.md for detailed branching model
