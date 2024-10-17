# Project in Wireless Communications

## Overview
Evaluate 5g latency and throughput under environmental conditions like noise, rain, and urban settings by testing different paramters:
- Modulation Schemes: QPSK to 64-QAM
- Antenna Configurations: Single-Antenna (SISO) vs MIMO (2x2, 4x4 antenna arrays)

## Parameters
- **Fixed Parameters:**
    - **Transmit Power:** 5 watts, adjustable as needed
    - **Frequency:** 28 GHz (mmWave)
- **Antenna Heights:**
    - **Transmitter Height:** 30m
    - **Receiver Height:** 1.5m
- **Environmental Conditions:**
    - **Noise Levels:** AWGN with varying SNR values
    - **Rain Attenuation:** Simulate effects of rain on signal propagation
    - **Urban Environment:** Include buildings and obstacles to mimic city conditions

### Temporary parameters code
```
function fixedParams = defineFixedParameters()
    fixedParams.carrierFreq = 28e9; % 28 GHz
    fixedParams.bandwidth = 100e6; % 100 MHz
    fixedParams.txPower_W = 5; % 5 Watts
    fixedParams.h_tx = 30; % 30 meters
    fixedParams.h_rx = 1.5; % 1.5 meters
    fixedParams.numBits = 1e6; % Number of bits to transmit
    fixedParams.SNR = 20; % SNR in dB
    fixedParams.environment = 'Urban';
end

function variableParams = defineVariableParameters()
    variableParams.modulationSchemes = {'QPSK', '16QAM', '64QAM'};
    variableParams.antennaConfigs = {'SISO', 'MIMO_2x2', 'MIMO_4x4'};
end
```
