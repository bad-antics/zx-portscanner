# ZX PortScanner Documentation

## Overview

ZX PortScanner is a network port scanner with a retro ZX Spectrum-inspired terminal interface. Combines modern scanning capabilities with classic 8-bit aesthetics.

## Features

- **Full Port Scanning** — TCP/UDP with configurable ranges
- **Service Detection** — Banner grabbing and service fingerprinting
- **Retro UI** — ZX Spectrum color scheme and border effects
- **Fast Scanning** — Async I/O with configurable concurrency
- **Export** — Results in JSON, CSV, or retro-formatted text

## Usage

```bash
# Quick scan common ports
zx-scan target.local

# Full scan with service detection
zx-scan -p 1-65535 -sV target.local

# Scan multiple targets
zx-scan -iL targets.txt -o results.json
```

## Interface

The UI features the iconic ZX Spectrum loading screen bars during scan progress, with results displayed in the classic Sinclair BASIC style.

## Configuration

```yaml
# ~/.zx-scanner.yml
defaults:
  threads: 100
  timeout: 3
  retries: 2
  style: spectrum  # or spectrum128, plus2
```
