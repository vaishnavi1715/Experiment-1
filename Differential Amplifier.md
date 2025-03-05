## LIC EXPERIMENT-3
### Differential Amplifier

Aim:
Design and analyze the differential amplifier for the following steps VDD=3.3v, P<=3mw, Vicm =1.65v,Vocm=1.7v,Vp=0.5v perform DC analysis,transient analysis,frequency response and extract the parameters.

Differential Amplifier:

Differential amplifiers consist of two transistors M1 and M2, whose sources are joined together. If the two transistors are connected to different voltage inputs, then the current across M1 and M2 are different due to the gate voltage. If the voltage supply at the gate terminal is the same, then the current through M1 and M2 is also the same. This configuration is called "Common-Mode Input Voltage Differential Amplifier". Whatever may be the load resistor, the MOSFET M1 and M2 should not enter the Triode region. It should be verified that the MOSFETs remain in the Saturation Region for proper operation.

![image](https://github.com/user-attachments/assets/4eb84cae-5379-486c-aa73-88f36549f949)


Procedure : Make the circuit connection as given above. connect the resister at the source terminal of both mosfet now calculate the value of Iss as power and vdd is given and calculate the Id1 and Id2 now calculate the Rss and Rd

To find the all the values of resistor and current value. we need solve the given queston specification. P=3mA

Iss=P/VDD=3*10^3/3.3=0.909mA

Is1=Is2=Iss/2=0.4545mA

RD=VDD-Vocm/Iss=3.3-1.7/0.45*10^3=3.55kΩ

Rss=Vp/Iss=0.5/0.909*10^3=0.555kΩ

Finially by solving we get

Iss=0.909mA

I1=I2=0.4545mA

RD=3.55kΩ

Rss=0.555kΩ

Circuit-1
Components Required: MOSFET(M1,M2 and M3), Resistor,voltage supply's

![image](https://github.com/user-attachments/assets/c81c08e7-7b59-4b83-bf1e-9ce87b0820e0)


Now to get the desired values of output voltage and current we have to vary the width and length of both the mosfet we got Length=180nm and width=1.810um


![image](https://github.com/user-attachments/assets/ece443b2-90c3-48f9-94a7-8d4bae0a1df5)

DC analysis:
To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation the figure below is the values obtained from the DC analysis
![image](https://github.com/user-attachments/assets/63184a21-e925-4ae5-9eab-f4982e879fca)


Here in dc analysis we got the vout as expected and id1 and id2 we got the same

Transient analysis:
To perform transient analysis we have to select the transient analysis in the edit simulation and give the stop time as 5ms and run the simulation . and the graph velow shows the transient response of the design.

![image](https://github.com/user-attachments/assets/ffa4c271-164c-4e53-8a63-831b71a738aa)

voltage gain AV=voutp-p/vinp-p

AV=(1.768-1.632)/(1.697-1.601)

AV=1.424

AC analysis:
TO perform AC analysis we have to select the ac analysis in the edit simulation command given the values as shown below 
![image](https://github.com/user-attachments/assets/06ee5227-5030-4692-9a97-d3addcec1f0f)


Gain in db= 20log(AV)

=20log(1.424)

=3.0707

Circuit-2:
Now replace the R3 resister with a current source : connect a current souce of 0.9mA

![image](https://github.com/user-attachments/assets/72db4af8-827f-40bc-9a5e-b3344fa22451)


DC analysis:
To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation the figure below is the values obtained from the DC analysis

![image](https://github.com/user-attachments/assets/d4bcc08f-c6bf-4262-96af-af777d3c71de)



Trasient analysis:
To perform transient analysis we have to select the transient analysis in the edit simulation and give the stop time as 5ms and run the simulation . and the graph b elow shows the transient response of the design

we have to give deg of 180deg to one mosfet and 0deg to the other mosfet and ac amplitude 1 for one mosfet and 0 for other mosfet

![image](https://github.com/user-attachments/assets/b9ea1f3f-0160-46eb-b65c-378e63908925)


voltage gain AV=voutp-p/vinp-p

AV=(1.83-1.5702)/(1.7-1.6)

AV=2.598

AC analysis:
![image](https://github.com/user-attachments/assets/f5a78764-8bd2-4092-86b4-486275c6c5c7)


Gain in db= 20log(AV)

=20log(2.598)

=8.292

Circuit-3:
Now replace the R3 resister with a Mosfet : Given vp=0.4v and wkt vt=0.36v we got the gate voltage of the new mosfet as 0.866v

![image](https://github.com/user-attachments/assets/98d6e8a1-856e-4e2a-8a6d-2073e248c971)


To get the output voltage and vp and current desired value we have to vary the width and length of the mosfets

![image](https://github.com/user-attachments/assets/0f53f2b3-3850-474b-a11b-1489ea95ece0)

![image](https://github.com/user-attachments/assets/8fa8dfef-52d3-446f-95bd-bfe21b8b4571)


DC analysis:

![image](https://github.com/user-attachments/assets/b700051d-54ee-4686-81b8-d07e67de8ae3)


Transient analysis:
give ac amplitude as 1 for one mosfet and 0 for other mosfet
![image](https://github.com/user-attachments/assets/732086b5-6c88-4894-854c-530b00be7090)


AC analysis:

![image](https://github.com/user-attachments/assets/2a4f2a81-f553-4322-ac95-4ba4393d074f)

INFERENCE:
In this experiment, we seen the working principles of a differential amplifier and its types and configuration.

There are three types of configurations were implemented: resistor , current source , and an NMOS . All the implements work on different ways that results into the cahnge in Voltage gain and stabillity of a mosfet.

when resistor is connected it provides low CMRR,deduce gain voltage,but high bandwidth and also provide negative feedback

But in the case of current source connection it is reciprocal of resistor connection because it has high gain volatge, high CMRR,but slight reduce in the bandwidth compared to the resistor connection.

Highest gain volltage is drewn by the circuit of CMOSN connection

By this we can say at what time/situation is required we can use that configuration.

1.Need more Band width-Use Resistor configuration

2.Need more Gain-Use CMOSN Configuration

3.Need precise CMRR-Use current or CMOSN configuration
