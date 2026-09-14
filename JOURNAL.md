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