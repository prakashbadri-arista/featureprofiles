# TRANSCEIVER-3 (400ZR_PLUS): Telemetry: 400ZR_PLUS Optics firmware version streaming

## Summary

Validate 400ZR_PLUS optics module reports correct firmware version.

## Procedure

*   Plug in the ZR_PLUS module in the host port and make sure the transceiver 
    state is enabled and host is able to detect the module.
*   With the module correctly recognized verify it reports correct firmware
    version through the following telemetry path
    *   /platform/components/component/state/firmware-version

*   Verify that the modules firmware version is reported correctly after a
    optic software reset.

    *   With ZR_PLUS module plugged in the host and properly recognized 
    *   Verify the ZR_PLUS optics firmware version is correctly reported via the 
        streaming telemetry path above.
    *   Reset the optic through software
    *   Verify the ZR_PLUS optics still reports correct firmware version. 

## Config Parameter coverage

*   /components/component/oc-transceiver:transceiver/oc-transceiver/config/enabled

## Telemetry Parameter coverage

    *  /platform/components/component/state/firmware-version

## OpenConfig Path and RPC Coverage
```yaml
rpcs:
  gnmi:
    gNMI.Get:
    gNMI.Set:
    gNMI.Subscribe:
```
