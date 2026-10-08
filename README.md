# Flow | Production Flow

A lightweight production-flow simulator built as a single-page web dashboard. It models a simple line for receiving, kitting, assembly, inspection, packout, and a repair loop for failed units.

## Overview

This project visualizes a manufacturing process in real time, showing how units move through the production line and how station settings affect throughput and quality.

The dashboard includes:
- A live production floor map
- Station-by-station queue and processing state
- Throughput, WIP, and first-pass yield metrics
- Random inspection failures routed to repair
- Configurable cycle times and inspection fail rates
- Recent activity log for production events

## Features

- Simulated unit movement between stations
- Adjustable processing speed and station configuration
- Repair/rework loop after failed inspection
- Real-time status updates for each station
- Animated unit tracking across the floor
- Clean dark UI for monitoring line performance

## Project structure

- `index.html` – complete app UI, styling, and simulation logic

## How to run

Because this project is a static HTML app, you can run it by opening `index.html` directly in a browser.

Alternatively, serve it locally:

```bash
cd "C:\Users\snimsaff\OneDrive - Flex\Documents\AI_Folder\Assigment1"
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## How it works

The app simulates a production line with the following stages:

1. Receiving
2. Kitting
3. Assembly
4. Inspection
5. Packout
6. Repair loop for failed inspections

Units are spawned into the line, processed at each station, and either continue through the flow or are sent back for rework when inspection fails.

## Configuration

Each station can be configured via its settings gear:
- Processing time (seconds per unit)
- Inspection fail rate (for inspection station only)

These settings update the simulation immediately and affect the resulting flow behavior.

## License

This project is provided as a simple demo and is suitable for educational or assignment use.
