---
title: "Simple Temperature Controller"
collection: projects
type: "Undergraduate projects"
permalink: /projects/SimpleTemperatureController
venue: "Tabriz"
date: 2017-1-1
location: "Tabriz, Iran"
---

SMT160

The SMT160-30 is a three terminal integrated temperature sensor, with a duty-cycle output. Two terminals are used for the power supply of 5 Volts and the third terminal carries the output signal. A duty cycle modulated output is used because this output is interpretable by a micro-processor without A-D converter, while the analogue information is still available.

An easy way of measuring a duty cycle is to use a microcontroller. It is only necessary to connect the sensors output to one of the microcontrollers inputs. With help of a small program it is possible to sense that input wether it is high or low. The speed of this sampling is limited due to the instruction time of the controller. So to achieve the wished accuracy it is necessary to sample over more than one sensor period. This way of working has also the advantage to filter noise. From the theory of signal processing it can be derived that there is a fixed ratio between the sensors signal frequency, the sampling rate and the sampling noise.

with SMT160 we could measure temperature from -45 °C to +130 °C . Output Pulse of sensor is similar to below timing chart, in this special case T0 is constant so we will measure TH and TL by duty cycles :

duty cycle = TH/T0;

temp = (duty cycle -0.32)/0.0047

In practice to measure the temperature we will use ATmega16 microcontroller, 74LS245 buffer, 4514 decoder, BC337 transistors and 8*16 LED matrix so the code is similar to below :
<pre>
#include <b>&ltmega16.h&gt</b>  
#include <delay.h>  
#include <math.h>  
#include <stdlib.h>  

unsigned char  prt1=0,prt2=0,count=0;
signed char    num=0;    
unsigned long pw1=0,sp1=0,h=0;   
flash unsigned char num0[]={126,129,129,129,126};
flash unsigned char num1[]={0,130,255,128,0};  
flash unsigned char num2[]={198,161,145,137,134};  
flash unsigned char num3[]={66,129,137,137,118};  
flash unsigned char num4[]={56,36,34,255,32};  
flash unsigned char num5[]={79,137,137,137,113};  
flash unsigned char num6[]={126,137,137,137,114};  
flash unsigned char num7[]={1,225,17,9,7};  
flash unsigned char num8[]={118,137,137,137,118};  
flash unsigned char num9[]={78,145,145,145,126};  
flash unsigned char positive_sign[]={16,56,16,0,0};  
flash unsigned char minus_sign[]={16,16,16,0,0};  
flash unsigned char text_micro[]={  
0,0,0,0,0,0,0,0,0,0,0,128,224,120,46,39,
46,120,224,128,63,127,192,192,127,63,0,254,255,51,51,127,
238,128,0,0,0,120,192,192,220,118,6,0,31,63,48,48,
60,54,58,156,192,112,48,31,159,192,120,50,50,24,48,50,
24,48,55,55,53,29,129,129,220,116,60,128,192,120,56,48,55,
55,53,29,177,177,56,16,48,56,40,56,0,0,0,0,0,0,0,0,0,0,0,0};  
flash unsigned char temp_text[]={
63,96,96,96,32,112,216,112,0,96,192,204,120,0,0,0};  
//_____________________________________________________        
void main(){  
    float t=0.0;  
    signed int loop,refresh,code;  
    PORTA=0x00;  
    DDRA=0xFF;  
    PORTC=0x00;  
    DDRC=0x0F;  
    PORTD.2=1;  
    DDRD.2=0;  
    TCCR1A=0x00;  
    TCCR1B=0x02;  
    TCNT1H=0x00;  
    TCNT1L=0x00;  
//--------------------------------------  
    for(code=104;code>8;code--){  
        for(refresh=0;refresh<100;refresh++){  
            for(loop=0;loop<16;loop++){  
                PORTC=loop;  
                PORTA=~text_micro[abs(code-loop)];  
                delay_us(100);  
                PORTA=0XFF;  
            }  
          }  
    }  
    PORTA=0XFF;  
    //------------------------------------  
    while(1){  
        if(count==3)  
        {  
            count=0;  
            for(code=104;code>8;code--){   
                for(refresh=0;refresh<100;refresh++){   
                    for(loop=0;loop<16;loop++){  
                        PORTC=loop;  
                        PORTA=~text_micro[abs(code-loop)];  
                        delay_us(100);  
                        PORTA=0XFF;  
                    }  
                }  
            }  
            PORTA=0XFF;  
        }  
    //------------------------------------  
        count++;  
        for(refresh=0;refresh<250;refresh++){  
            for(loop=0;loop<16;loop++){  
                PORTC=~(loop+1);  
                PORTA=~temp_text[loop];  
                delay_us(500);  
                PORTA=0XFF;  
            }  
        }  
        for(h=0;h<60000;h++)  
        {  
            if(PIND & 0x04) pw1++;  
            else sp1++;  
        }  
         t=(float)pw1/h;  
         pw1=0;  
         sp1=0;  
         h=0;  
         t=(t-0.320)/0.00470;  
    //------------------------------------  
        for(refresh=0;refresh<500;refresh++){  
            for(loop=0;loop<5;loop++){  
                num=t;  
                prt2 = (abs(num) % 10);  
                prt1 = (abs(num) / 10);  
    //------------------------------------  
                PORTC=~(loop+4);  
                switch (prt1) {  
                    case 0 : PORTA=~num0[loop];break;  
                    case 1 : PORTA=~num1[loop];break;  
                    case 2 : PORTA=~num2[loop];break;  
                    case 3 : PORTA=~num3[loop];break;  
                    case 4 : PORTA=~num4[loop];break;  
                    case 5 : PORTA=~num5[loop];break;  
                    case 6 : PORTA=~num6[loop];break;  
                    case 7 : PORTA=~num7[loop];break;  
                    case 8 : PORTA=~num8[loop];break;  
                    case 9 : PORTA=~num9[loop];break;  
                    default: PORTA=0XFF;  
                 }  
                delay_us(500);  
                PORTA=0XFF;  
                PORTC=~(loop+10);  
                switch (prt2) {  
                    case 0 : PORTA=~num0[loop];break;  
                    case 1 : PORTA=~num1[loop];break;  
                    case 2 : PORTA=~num2[loop];break;  
                    case 3 : PORTA=~num3[loop];break;  
                    case 4 : PORTA=~num4[loop];break;  
                    case 5 : PORTA=~num5[loop];break;  
                    case 6 : PORTA=~num6[loop];break;  
                    case 7 : PORTA=~num7[loop];break;  
                    case 8 : PORTA=~num8[loop];break;  
                    case 9 : PORTA=~num9[loop];break;  
                    default: PORTA=0XFF;  
                }  
                delay_us(500);  
                PORTA=0XFF;  
    //---------------------------------  
                if(num >= 0){  
                 PORTC=~(loop);  
                 PORTA=~positive_sign[loop];  
                 delay_us(1000);  
                 PORTA=0XFF;  
                 }  
    //---------------------------------  
                else{  
                 PORTC=~(loop);  
                 PORTA=~minus_sign[loop];  
                 delay_us(1000);  
                 PORTA=0XFF;  
                } 
            }  
        }  
     };  
}  
</pre>
