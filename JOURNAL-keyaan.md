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


# 16 sept 2026

i did a part of the placement of the board, and i think that we'll be done with less than 10 hours each sob. This is what the board looks like right now:  
![image](https://cdn.hackclub.com/01a0aa81-97fc-7966-b5db-63db2453a81a/paste-1789567014094.png)


# 18 sept 2026

I have been given the placement task by ahad, as he says he is bad at placement, thus i'll take my time out today and complete the placement! Here is progress 30 mins in the session:  
![image](https://cdn.hackclub.com/01a0b2f6-4600-773e-8119-3541cb4d721f/paste-1789708878975.png)  
Me tryna make it look like a commercial FPV drone flight controller!!  

I did some footprint manipulation for easier routing for my IMU circuitry, and i have informed ahad to do the same too. Here is the updated footprint:  
![image](https://cdn.hackclub.com/01a0b312-6bae-7d73-9486-c689b7236680/paste-1789710723892.png)  

I removed the two pins on the bottom right. The actual routing will be done like this:  
![image](https://cdn.hackclub.com/01a0b313-019b-7785-96e1-8f0bf7388fc2/paste-1789710761592.png)  

Oh also, i dont know if i have told it, but i have made these pads myself :3c  
![image](https://cdn.hackclub.com/01a0b314-05bd-7715-97ad-511c65f4ebc4/paste-1789710828839.png)  

I am done with the placement and some routing, and it looks beautiful:  
![image](https://cdn.hackclub.com/01a0b340-df09-7fb5-b179-a890f4982036/paste-1789713767706.png)

# 19 sept 2026
i did some routing fixes, and this is what the PCB looks like in one type of view, so amazing:  
![image](https://cdn.hackclub.com/01a0ba58-536f-7bce-8a00-a66f5eb0897c/paste-1789832746248.png)  
Okay so now everything is done, here is how the final PCB looks:  
![image](https://cdn.hackclub.com/01a0ba83-a98f-7af1-b296-952830e9895b/paste-1789835585427.png)  
![image](https://cdn.hackclub.com/01a0ba83-d46f-7f36-84a9-5efe2a550db8/paste-1789835597711.png)  
Now time for rendering!!

# 20 september 2026
It is a few hours before midnight, and i am doing final renders, because ahad had to re-route his PCB for some reason. Thus, i have to do a new render for the README images, thus me doing that.  

Time spent: about 30 minutes. 