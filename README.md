# DayZ Livonia Seasonal Weather Configurations

XML weather configuration files for DayZ Livonia servers on Xbox. Four complete seasonal presets included.

## Overview

Control your server's weather patterns with these optimised seasonal configurations. Each file provides distinct atmospheric conditions for immersive gameplay.

## Features

- Four complete seasonal weather presets
- Optimised for Livonia map
- Xbox server compatible
- Ready to deploy configurations
- Detailed parameter documentation

## Installation

1. Access your server mission folder
2. Locate `cfgweather.xml`
3. Back up your current file
4. Replace with chosen seasonal configuration
5. Restart the server

## Seasonal Configurations

### Spring (cfgweather-spring.xml)
Moderate conditions with variable weather patterns.

- Cloud coverage: 20-80%
- Fog intensity: 0-40%
- Rain threshold: 60-80% overcast
- Max wind speed: 12 m/s
- Storms: Active at 90%+ overcast

### Summer (cfgweather-summer.xml)
Clear skies with minimal precipitation.

- Cloud coverage: 0-60%
- Fog intensity: 0-10%
- Rain threshold: Any overcast level
- Max wind speed: 15 m/s
- Storms: Active at 90%+ overcast

### Autumn (cfgweather-autumn.xml)
Clear conditions with strong winds.

- Cloud coverage: 0-60%
- Fog intensity: 0-10%
- Rain threshold: Any overcast level
- Max wind speed: 15 m/s
- Storms: Active at 90%+ overcast

### Winter (cfgweather-winter.xml)
Harsh conditions with snow and heavy fog.

- Cloud coverage: 75-85%
- Fog intensity: 30-80%
- Rain threshold: 75-78% overcast
- Snow threshold: 78-85% overcast
- Max wind speed: 12 m/s
- Storms: Active at 100% overcast only

## Parameter Reference

### Overcast
Controls cloud coverage across the map.
- Range: 0.0 (clear) to 1.0 (fully overcast)
- Affects precipitation triggers

### Fog
Controls visibility distance and atmosphere.
- Range: 0.0 (no fog) to 1.0 (dense fog)
- Impacts player navigation

### Rain
Controls rainfall intensity.
- Range: 0.0 (none) to 1.0 (heavy)
- Requires a minimum overcast threshold

### Snowfall
Controls snow precipitation (winter only).
- Range: 0.0 (none) to 1.0 (heavy)
- Requires higher overcast than rain

### Wind
Controls wind speed and variation.
- Measured in meters per second (m/s)
- Affects player movement and sound

### Storms
Controls lightning frequency.
- Density: Lightning intensity (0.0-1.0)
- Threshold: Overcast level required
- Timeout: Seconds between strikes

## Customisation Guide

### Increase Sunshine
Lower the overcast max value:
```xml
<limits min="0.0" max="0.4" />
```

### Add More Fog
Increase fog max value:
```xml
<limits min="0.2" max="0.9" />
```

### Control Rain Frequency
Adjust rain thresholds:
```xml
<thresholds min="0.5" max="0.8" end="120" />
```

### Speed Up Weather Changes
Reduce time limits:
```xml
<timelimits min="300" max="600" />
```

### Increase Wind
Raise max wind speed:
```xml
<maxspeed>20</maxspeed>
```

## Technical Details

### File Attributes
- `reset="1"`: Loads fresh weather (ignores saved state)
- `enable="1"`: Activates the configuration file

### Value Ranges
- Weather parameters: 0.0 to 1.0
- Time values: seconds
- Wind speed: meters per second

### Thresholds
Define when precipitation starts based on overcast levels. Rain and snow have separate threshold ranges to prevent overlap.

## Testing

1. Deploy configuration to test server
2. Monitor weather transitions
3. Adjust parameters as needed
4. Back up working configurations

## Requirements

- DayZ server (Xbox)
- Livonia map
- Server file access
- Basic XML knowledge (for customisation)

## Support

Submit issues or suggestions through GitHub Issues. Include your configuration file and description of the problem.

## Credits

Created by FixitDaz
Date: November 23, 2025

## License

Free to use and modify for your DayZ servers. Attribution appreciated.
