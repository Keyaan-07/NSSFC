# 14 sept 2026
Today is the first day for third-space, and i am starting this project, i am really exceited to build a flight controller and coordinate different sensors!

I lowkey wanna make it look like those traditional flight controllers that you see on FPV drones, and i will try my best to make it look like that! Here's how i began:  

I set up my image paste CDN plugin by qcoral as it is amazing!
First and foremost, i began by putting two capacitors to the VCAP_1 and VCAP_2 pins, which connect to internal voltages and provide decoupling, and it is important that one must not connect anything else to them:  
![image](https://cdn.hackclub.com/01a0a023-6e9a-7904-ad62-b1e02d3c347a/paste-1789393072116.png)  

I added a crystal by reading the datasheet, and i've decided that i'll probably use a 10pF crystal:  
![image](https://cdn.hackclub.com/01a0a025-ae9b-71d6-acd4-55b735885372/paste-1789393220110.png)  

added decoupling caps too!  
![image](https://cdn.hackclub.com/01a0a026-22dd-76bc-91c6-a138cee531d8/paste-1789393250327.png)

I feel like the W25Q128JVP is a goated flash IC, not just because it has good amount of storage, but the package is so awesome too, and it satisfies all my requirements, thus i chose 25q128jvp with a wSON package. 

I also worked on some minor stuff, such as pull up to the reset, and adding a note to the future for adding a button:  
![image](https://cdn.hackclub.com/01a0a025-242a-7361-a993-bfebaa98967c/paste-1789393184626.png)  

Okay so the magnetometer i decided on is called the QMC5883P and is supported by betaflight(yes i think this is a good time to tell i am leaning towards betaflight firmware!), and thus i went with it. There was no default symbol or footprint for the LGA, thus i had to make it myself, they can be located in /hardware/nssfc.pretty and /harwdare/nssfc.kicad_sym which were created by me!
![image](https://cdn.hackclub.com/01a0a04a-2ff3-7551-b3a3-ae14483aff70/paste-1789395611937.png)
![image](https://cdn.hackclub.com/01a0a04b-4434-702d-8153-ddcd3433dca0/paste-1789395682357.png)

Oh btw i chose BMP580 for the pressure sensor, because it is not that expensive and gets the work done perfectly, there was no symbol for this as well, and i made my own, tho the footprint was there:  
![image](https://cdn.hackclub.com/01a0a07b-f783-76fa-a438-394816824475/paste-1789398874870.png)
That is all for this session, time spent: 1 hour 46 mins


# 15 sept 2026

I worked on the schematic today, after ahad. and i think i am done with the schematic. did a lot of stuff today, so here is it:  

completed work on all 3 sensors:  
![image](https://cdn.hackclub.com/01a0a502-2e8a-7477-a641-1166f06feb77/paste-1789474777770.png)  
![image](https://cdn.hackclub.com/01a0a501-f78c-7c07-8b71-03fad1783b4d/paste-1789474762971.png)  
made the buck converter and the LDO:  
![image](https://cdn.hackclub.com/01a0a502-6e3e-7389-9c58-00749a4cd721/paste-1789474794680.png)  
worked on the USB Port:  
![image](https://cdn.hackclub.com/01a0a502-f1bc-726f-a621-8c13cf010e30/paste-1789474828355.png)  
main MCU looks like this:  
![image](https://cdn.hackclub.com/01a0a504-6f7f-7a66-8e98-b4782a5e9e18/paste-1789474926168.png)  
now the only part left out is a buck-boost IC for the VTX port, and probably a uSD card slot(tho we'll probably not add it)  
I assigned all the footprints as well, and i have not yet found an inductor so i did not add that footprint. For the schottky diodes, i have added [this](https://www.lcsc.com/product-detail/Schottky-Barrier-Diodes-SBD_LGE_C432153.html) diode's footprint. 
Did a bit of placement of the PCB, here is how it looks:  
![image](https://cdn.hackclub.com/01a0a52d-06cb-723f-b37e-bb4dd224fbf1/paste-1789477585231.png)  
I found a footprint for the inductor, here it is:  
![image](https://cdn.hackclub.com/01a0a52e-dba1-7003-a0c6-f0f55b8b23da/paste-1789477705764.png)  
okay so i am done with the project for the day, and i am exhausted, so here is the final pic:  
![image](https://cdn.hackclub.com/01a0a531-7b14-786b-870c-cde7930ec93c/paste-1789477877032.png)  
![image](https://cdn.hackclub.com/01a0a531-b1a9-70d1-9f7f-c246fe31e01a/paste-1789477892176.png)  