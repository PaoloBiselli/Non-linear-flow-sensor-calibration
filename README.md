# Non-linear-flow-sensor-calibration
Algorithm to calibrate a non-linear flow sensor with accurate syringe

This software was built on top of IgorPro 6.3.4.0 software (WaveMetrics Inc).
It was designed to allow a calibration procedure for a non-linear flow sensor using an accurate syringe.
It retrieves data colletect during pumping of the syringe throungh the flow sensor.
Over many iterations, it finds the parameter for a power equation that minimizes the difference among the various integrals.

To run this code, you need the IgorPro software; you may use the evaluation version of the software, provided by the manufacturer.
