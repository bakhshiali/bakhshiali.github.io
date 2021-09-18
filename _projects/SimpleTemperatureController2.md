---
title: "Simple Temperature Controller (LM35)"
collection: projects
type: "Undergraduate projects"
permalink: /projects/SimpleTemperatureController2
venue: "Tabriz"
date: 2017-1-1
location: "Tabriz, Iran"
---

LM35

The LM35 series are precision integrated-circuit temperature sensors, whose output voltage is linearly proportional to the Celsius (Centigrade) temperature. The LM35 thus has an advantage over linear temperature sensors calibrated in ° Kelvin, as the user is not required to subtract a large constant voltage from its output to obtain convenient Centigrade scaling. The LM35 does not require any external calibration or trimming to provide typical accuracies of ±1⁄4°C at room temperature and ±3⁄4°C over a full −55 to +150°C temperature range.


Low cost is assured by trimming and calibration at the wafer level. The LM35’s low output impedance, linear output, and precise inherent calibration make interfacing to readout or control circuitry especially easy. It can be used with single power supplies, or with plus and minus supplies. As it draws only 60 μA from its supply, it has very low self-heating, less than 0.1°C in still air. The LM35 is rated to operate over a −55° to +150°C temperature range, while the LM35C is rated for a −40° to +110°C range (−10° with improved accuracy).

<pre>
#include "mega16.h"
#include "stdio.h"
#include "delay.h"
#asm
   .equ __lcd_port=0x18 ;PORTB
#endasm
#include "lcd.h"  
#define  Up        PIND.0
#define  Down      PIND.1
#define  Enter     PIND.2  
#define  high_LED  PORTA.1
unsigned char compare=0,set=0xff;
float   temp;  
//__________________________________________
void display(){   
  char   lcd_buf[32];
  sprintf(lcd_buf,"Temp=%3.1f\xdfC\nHigh Temp=%i",temp,compare);
  lcd_clear(); 
  lcd_gotoxy(0,0); 
  lcd_puts(lcd_buf);
  lcd_gotoxy(13,1); 
  if(high_LED==1) lcd_putsf("on ");
  if(high_LED==0) lcd_putsf("off");
}  
//_________________________________________                         
interrupt [ADC_INT] void adc_isr(void){
  unsigned int adc_data;
  adc_data=ADCW;
  temp=adc_data*256/1024; 
  if(temp>=set) high_LED=1;
  else high_LED=0;
} 
//_________________________________________up
void inc_set_temp(){
  if(compare<99) compare++; 
}
//__________________________________________Down
void dec_set_temp(){
  if(compare!=0) compare--; 
}              
//__________________________________________
void main(){ 
  PORTD=0XFF;
  DDRD=0X00;
  PORTA.1=0;
  DDRA.1=1;  
  ACSR=0XC0;
  SFIOR=0X00;
  ADMUX=0XC0;
  ADCSRA=0X8F;
  lcd_init(16);
  #asm("sei")
  ADCSRA=0XCF;
  while(1){
     display();
     delay_ms(250);
     ADCSRA=0XCF; 
     if(Up==0)    inc_set_temp();
     if(Down==0)  dec_set_temp();
     if(Enter==0) set=compare; 
  };
} 
</pre>
