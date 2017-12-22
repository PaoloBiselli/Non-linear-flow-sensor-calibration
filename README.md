# Non-linear-flow-sensor-calibration
Algorithm to calibrate a non-linear flow sensor with accurate syringe

This software was built on top of IgorPro 6.3.4.0 software (WaveMetrics Inc).
It was designed to allow a calibration procedure for a non-linear flow sensor using an accurate syringe.
It retrieves data collected during pumping of the syringe throungh the flow sensor.
Over many iterations, it finds the parameter for a power equation that minimizes the difference among the various integrals.

To run this code, you need the IgorPro software; you may use the evaluation version of the software, provided by the manufacturer.



Instructions to use Flow_cal.pxp


Flow_cal.pxp works as script file for IgorPro WaveMetrics 6.3.4.0.
After downloading IgorPro, you can start Flow_cal experiment. The menu on the right shows the options.
For proper use, you need the experiments saved in LabView lvm file (10 sec recording of flow, in which the full content of the syringe is emptied). 
All flow experiments (positive or negative flows) should be saved in a folder (ex. pos), under a parent folder (ex: 2017_12_20) and under a another parent folder(ex: Calibration_experiments). The structure would be as follows:

+Calibration_experiments

     +2017_12_20
     
         +Pos
         

Once in the Igor experiment, the button "Browse Folders" allows you to choose in your computed the first parent folder (in our example, Calibration_experiments). The button "Update Folder List", updates the menu on the left according to the subfolders within the first parent folder. You should be able to see your folder "2017_12_20"; the other drop menu allows you to select the second level folder - you should be able to see and select your folder "Pos" (in our example). 
After folder selection, the button load brings the several lvm experiments saved on folder Pos to the Igor environment. You should use the bar to select a initial period of the signals to perform baseline calculation; the calibration button should do the rest (integrate signals and determine A and b) to minimize differences, which would be displayed at the bottom of control window.

PS: I uploaded a structured folder to properly work with this script with some example files
