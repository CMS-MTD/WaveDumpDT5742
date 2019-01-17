# WaveDumpDT5742
DAQ code for the DT5742 CAEN DRS desktop digitizer - based on the wavedump program

This code has been adapted from the original CAEN wavedump program. Please follow the installation instructions from the CAEN website, including installating all the pre-requisite software and libraries. 

https://www.caen.it/download/?filter=DT5742

Software needed last time I installed this: 
CAENDigitizer_2.12.0_20181015.tgz
CAENComm-1.2-build20140211.tgz
CAENVMELib-2.50.tgz
gnuplus-5.2.5.tar.gz
CAENUSBdrvB-1.5.2.tgz
I included these tarballs in the repository in the AdditionalSoftware directory for convenience. You may need newer versions by the time you install this. 


The main code is located in src/WaveDump.c. 
We have made the following modifications to the default wavedump code:

* disable the keyboard input commands
* by default enable the continuous write mode
* continuously acquire data and write to file while we are running
* check for the "stop" word in the file /tmp/RunFile.txt in order to listen to the OTSDAQ stop run command

