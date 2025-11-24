# DayZ Weather Configuration Files for Livonia

XML weather configuration files for DayZ Livonia map on Xbox servers. Four seasonal presets included.

**Creator**: FixitDaz  
**Date**: November 23, 2025

## Files Overview

Each XML file controls weather parameters on your Livonia server. Place these in your server's mission folder.

## Installation

1. Navigate to your server mission folder
2. Locate the existing `cfgweather.xml` file
3. Back up the original file
4. Replace with your chosen seasonal configuration
5. Restart the server

## Seasonal Configurations

### Spring Weather
Moderate conditions with variable cloud cover and occasional rain.

- Overcast: 50-75% cloud coverage
- Fog: Light (0-60% intensity)
- Rain: Triggers at 85%+ overcast
- Wind: Moderate (max 8 m/s)
- Storms: Active at 90%+ overcast, 60s between strikes

### Summer Weather
Clear skies with minimal precipitation. Best visibility conditions.

- Overcast: 20-80% cloud coverage
- Fog: Minimal (0-40% intensity)
- Rain: Triggers at 60-80% overcast
- Wind: Stronger (max 12 m/s)
- Storms: Active at 90%+ overcast, 60s between strikes

### Autumn (Fall) Weather
Clearer conditions with increasing wind. Reduced fog and rain.

- Overcast: 0-60% cloud coverage
- Fog: Rare (0-10% intensity)
- Rain: Light (max 50% intensity), triggers at any overcast level
- Wind: Strong (max 15 m/s)
- Storms: Active at 90%+ overcast, 60s between strikes

### Winter Weather
Heavy overcast with fog and snowfall. Harsh survival conditions.

- Overcast: 75-85% cloud coverage
- Fog: Heavy (30-80% intensity)
- Rain: Triggers at 75-78% overcast
- Snowfall: Triggers at 78-85% overcast
- Wind: Moderate (max 12 m/s)
- Storms: Rare (triggers at 100% overcast only)

## Key Parameters Explained

**Overcast**: Controls cloud coverage (0.0 = clear, 1.0 = fully overcast)

**Fog**: Controls visibility distance (0.0 = no fog, 1.0 = dense fog)

**Rain/Snowfall**: Precipitation intensity (0.0 = none, 1.0 = heavy)

**Thresholds**: Overcast levels required for precipitation to start

**Wind Speed**: Maximum wind speed in meters per second

**Storm Settings**: Lightning frequency and conditions

## Customization Tips

- Lower overcast limits for sunnier weather
- Increase fog limits for spooky atmosphere
- Adjust rain thresholds to control when precipitation starts
- Modify time limits to control how quickly weather changes
- Change wind speed to affect player movement and sound

## Technical Notes

- All values range from 0.0 to 1.0 unless specified otherwise
- Time values are in seconds
- Reset attribute loads fresh weather instead of saved state
- Enable attribute must be set to "1" for file to work

## Support

Test changes on a private server first. Back up files before editing. Each seasonal file is standalone and complete.