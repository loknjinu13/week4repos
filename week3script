#!/bin/bash
# Chapter 3; Devices
echo "Fongoh"
echo "Home Alone" > /dev/null
#Check if /dev/null receive any info
cat /dev/null
#check the file device
ls -l /dev/null
#create a file that maps block devices
ls -l /dev /dev/mapper | grep '^b' > Mypc.txt
#let's view our new file
cat Mypc.txt
#let's list our devices
lsscsi -s
#if lsscsi doesn't exist
sudo apt-get install lsscsi
#then relaunch system devices command
lsscsi -s >> Mypc.txt
#let's obtain the device messages
dmesg | grep sd >> Mypc.txt
#let's collect all blocks and turn into hexadecimal
cd ~;pwd; dd if=/dev/zero of=./Mypc.txt bs=1M count=3 
#Hexadump
hexdump Mypc.txt
#let's monitor our kernel
udevadm monitor --kernel --subsystem-match=scsi echo "Ctrl C to quit"
#Change teh console to terminal1
sudo chvt 1
#end of script.
