# ece3301l-lab-6-traffic-light-controller-with-use-of-system-timer-solved
**TO GET THIS SOLUTION VISIT:** [ECE3301L LAB 6-Traffic Light Controller with use of System Timer Solved](https://www.ankitcodinghub.com/product/ece3301l-lab-6-traffic-light-controller-with-use-of-system-timer-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91509&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE3301L LAB 6-Traffic Light Controller with use of System Timer Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Traffic Light Controller with use of System Timer

Design a traffic controller system that uses the PIC. The system will have:

<ol>
<li>I) &nbsp;four RGB LEDs (called NS RGB, NSLT RGB, EW RGB, and EWLT RGB)</li>
<li>II) &nbsp;four input sensors:
<ol>
<li>a) &nbsp;NSLT_SW : to detect cars that want to make a left-turn on NS direction</li>
<li>b) &nbsp;EWLT_SW: for detection of cars wanting to make a left-turn on EW direction</li>
<li>c) &nbsp;NSPED_SW: switch pressed by pedestrians wanting to make a cross in the NS
direction
</li>
<li>d) &nbsp;EWPED_SW: switch pressed by pedestrians wanting to make a cross in the
EW direction
</li>
</ol>
</li>
</ol>
III) two sets of 7-segment display to show the number of seconds left for pedestrian to cross

IV) A buzzer to make sound helping people with blindness to cross the streets

V) a photo sensor (photo resistor) to sense whether the traffic controller is operating in Day Mode or Night Mode.

Before we get into the design of the controller system we need to build some small routines that will help us in the final design.

PART 1)

Write the routine Wait_One_Second() that will wait like the name indicates for 1 second. Actually, this routine will call another routine Wait_Half_Second() twice. In between the two calls, asserts the setting and the resetting the LED called ‘SEC_LED’. Refer to the schematics for the port bit that this LED is connected to.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
void Wait_One_Second() {

SEC_LED = 0;

W ait_Half_Second(); SEC_LED = 1;

W ait_Half_Second();

}

void Wait_Half_Second() {

</div>
<div class="column">
// First, turn off the SEC LED

// Wait for half second (or 500 msec) // then turn on the SEC LED

// Wait for half second (or 500 msec)

// Timer 0, 16-bit mode, prescaler 1:8 // set the lower byte of TMR

// set the upper byte of TMR

// clear the Timer 0 flag

// Turn on the Timer 0

// wait for the Timer Flag to be 1 for done // turn off the Timer 0

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
T0CON = 0x02

TMR0L = 0x??;

TMR0H = 0x??; INTCONbits.TMR0IF = 0; T0CONbits.TMR0ON = 1;

while (INTCONbits.TMR0IF == 0); T0CONbits.TMR0ON = 0;

</div>
</div>
<div class="layoutArea">
<div class="column">
The ‘Wait_Half_Second()’ routine above uses the hardware timer to do the delay function. Through the Timer 0, a timer value is loaded and the timer will count from that value to the 0xFFFF. A Timer Flag (TMR0IF) will be set to ‘1’ when 0xFFFF is reached. The software will wait until that flag is set and that will indicate that the wait is over. You need to specify the value of the TMR0L and TMR0H above so that the ‘Wait_Half_Second()’ lasts exactly one half of a second or 500 msec. Let us go over the calculation of the value to be loaded into the TMR0.

The system clock will run at 4 MHz (make sure to set OSCCON = 0x60). This implies that the timer clock will run a 1 MHz (1/4 of system clock). The period of the timer is then 1 usec. To achieve a wait time of 500 msec, it will take a count of 500 msec / 1 usec = 500, 000 count. The code of the Wait_Half_Second() routine specifies the use of a 1/8 prescaler. This will divide the 500,000 count by 8 giving a new count of 62500. The next step is to convert this number into a hex value and uses it to subtract from the value 0xFFFF. The resulting number is then the one to be loaded into the TMR0 register. The upper byte will go to TMR0H while the lower one goes to TMR0L.

Write the program with an infinite loop calling the Wait_One_Second() routine. Put a scope on the signal ‘SEC_LED’ and measure its width to be 500 msec or the period must be 1 sec. Make any kind of adjustment to the TMR0 register (especially the TMR0L) to get the right period.

Use the ‘#define’ statement to assign the bit location for the variable SEC_LED. For example:

#define SEC_LED PORTDbits.RD7

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
PART 2)

After the ‘Wait_One_Second()’ routine is implemented, write the next support routine to be called ‘Wait_N_Seconds(char seconds)’ that will use the ‘Wait_One_Second()’ function to delay for N seconds:

void Wait_N_Seconds (char seconds) {

char I;

for (I = 0; I&lt; seconds; I++) {

W ait_One_Second();

} }

We will use this new routine for the main development.

PART 3)

Use the ‘#define’ statement, create the following eight signal names: NS_RED, NS_GREEN, NSLT_RED, NSLT_GREEN, EW_RED, EW_GREEN, EWLT_RED, EWLT_GREEN. Use the schematics to determine the bit definitions. For example:

#define NS_RED PORTAbits.RA5 #define NS_GREEN PORTBbits.RB0

Do the same for the other three RGB LEDs. Refer to the schematics for pins assignments.

Next, write a routine to set the proper color for one RGB LED. For example, let us write a routine to set the color for the NS RGB:

</div>
</div>
<div class="layoutArea">
<div class="column">
void Set_NS(char color) {

switch (color) {

case OFF: NS_RED =0;NS_GREEN=0;break;

case RED: NS_RED =1;NS_GREEN=0;break;

case GREEN: NS_RED =0;NS_GREEN=1;break; case YELLOW: NS_RED =1;NS_GREEN=1;break;

</div>
<div class="column">
// Turns off the NS LED // Sets NS LED RED

// sets NS LED GREEN

// sets NS LED YELLOW

</div>
</div>
<div class="layoutArea">
<div class="column">
} }

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
where ‘color’ can have four values:

0: OFF

1: RED

2: GREEN 3: YELLOW

Use #define to declare the value of those colors like:

#define OFF 0 #define RED 1 …

Once completed, you can do the same for the remaining three RGB LEDs and call the three additional routines as:

<ol>
<li>1) &nbsp;Set_NSLT(char color)</li>
<li>2) &nbsp;Set_EW(char color)</li>
<li>3) &nbsp;Set_EWLT(char color)</li>
</ol>
For testing purpose, once these four routines are written, generate a program that has an infinite loop to call all the four routines each displaying all the three colors. Do space each color with a call to the Wait_N_Seconds() (defined in Part 2).

</div>
</div>
<div class="layoutArea">
<div class="column">
For example:

while (1) {

for (int i=0;i i&lt;4;i++) {

SET_NS(i); SET_NSLT(i); SET_EW(i); SET_EWLT(i); Wait_N_Second(1);

} }

This exercise will allow your team to check the connections of the four sets of RGB LEDs.

</div>
</div>
<div class="layoutArea">
<div class="column">
// Set color for North-South direction

// Set color for North-South Left-Turn direction

// Set color for East-West direction

// Set color for East-West Left-Turn direction

// call Wait-N-Second routine to wait for 1 second

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
PART 4)

Write a routine that will control the operation of the only 7-segment display. The name of the routine should be called PED_Control() and it should have two arguments

‘Direction’ and ‘Num_Sec’. Here is the definition of the routine:

Void PED_Control( char Direction, char Num_Sec)

The variable ‘Direction’ will select which direction the pedestrian counter is addressed for.

If ‘Direction’ is set to ‘0’, it will apply for the North-South direction. The lower digit of the 2-digit 7-segment will be turned off while the upper digit will start with the number indicated by the second parameter ‘Num_Sec’. Take the value from that variable subtract 1 from it and display the result on to the 7-segment display. At the start, the display will show the counter to be at ‘Num_Sec’ – 1. Then, on every second, the count will start to decrement by 1 and it will continue to do so until the count reaches 1. On the next second, the display will be completely turned off. The number of seconds elapsed between the number ‘Num_Sec’ – 1 and when the display is turned off is actually ‘Num_Sec’. For example, if ‘Num_Sec’ is 5, then the display will start from 4, 3, 2, 1 and off. The total is then 5 seconds.

If the ‘Direction’ is set to ‘1’, then this will apply to the East-West direction. This time the upper digit will be turned off while the lower digit will start counting from ‘Num_Sec’ – 1 to 1 and then get turned off 1 second later.

While counting in either direction, an audible sound through the buzzer must be generated to indicate that the pedestrian counter is active. To achieve this task while waiting for a second, generate the new ‘Wait_One_Second_With_Beep()’ below and use it for the wait.

</div>
</div>
<div class="layoutArea">
<div class="column">
void Wait_One_Second_With_Beep() {

SEC_LED = 1; Activate_Buzzer()

W ait_Half_Second(); SEC_LED = 0; Deactivate_ Buzzer (); W ait_Half_Second();

}

Note: when one digit is counting in one direction, the other digit must be turned off. When the counting is done, both digits must be off.

After that routine is properly written, write a test program to check its operation. For example, do an infinite loop to check all the possible combinations:

</div>
</div>
<div class="layoutArea">
<div class="column">
// First, turn on the SEC LED

// Activate the buzzer

// Wait for half second (or 500 msec) // then turn off the SEC LED

// Deactivate the buzzer

// Wait for half second (or 500 msec)

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
while (1) {

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
PART 5)

</div>
</div>
<div class="layoutArea">
<div class="column">
PED_Control (0, 8) PED_Control(1, 6)

</div>
<div class="column">
// Set direction 0 and do for 8 seconds // Set direction 1 for 6 seconds

</div>
</div>
<div class="layoutArea">
<div class="column">
This is the main design for the traffic controller.

We have a total of four DIP-Switch inputs: NSLT_SW, NSPED_SW, EWLT_SW, and EWPED_SW (see schematics for pin assignments) and a light sensor input MODE.

The EWLT_SW and NSLT_SW inputs are the sensors (switches) to indicate that a car is requesting to make a left-turn on the direction indicated by the switch’s name: EWLT is for the East-West left-turn sensor while NSLT is for the North-South. When a sensor is 1, there is a car waiting to make a left turn.

The EWPED_SW and NSPED_SW inputs are the sensors used to detect the presence of pedestrians wanting to cross. When the input is ‘0’, no pedestrian is present to cross. When the input is ‘1’, there is at least a pedestrian wishing to cross.

The input ‘MODE’, as mentioned before, is a light sensor used to determine the mode of operation. It is implemented through the use of the photo resistor PR1. When the voltage at PR1 is below 2.5V, the MODE is for the Day Time Mode. When it is above 2.5V, the MODE is Night Time Mode. In addition, the ‘MODE LED’ is turned on when the day mode is on and it will be turned off for the night mode.

A while infinite loop will scan the logic state of the light sensor and based on that logic state the program will call either the routine ‘void Day_Mode()’ or ‘void Night_Mode()’

Traffic Light Night Time Mode:

This is the Mode that operates when at night whereas no Pedestrian Counter is used. The two 7-segment displays must be off during the entire process. The ‘MODE LED’ must be turned off and stays off throughout the entire Night Mode time. This is the simplest mode:

Implement the following steps:

<ol>
<li>1) &nbsp;Next, set the NS RGB to GREEN while the other RGB LEDs remain in RED.</li>
<li>2) &nbsp;Wait for 6 seconds with NS RGB still in GREEN. Then go to step 3). Use the ‘Wait_N_Seconds’ routine to do the delay.</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
<ol start="3">
<li>3) &nbsp;Set the NS RGB to YELLOW and wait for 3 seconds. Go to step 4)</li>
<li>4) &nbsp;Next, change NS RGB to RED and go to step 5)</li>
<li>5) &nbsp;Check the logic state of EWLT_SW switch:
<ol>
<li>If 0, go directly to step 9)</li>
<li>If 1, there is a left-turn request. Go to step 6)</li>
</ol>
</li>
<li>6) &nbsp;Turn on EWLT RGB to GREEN and leave it for 6 seconds. Afterwards, go to step 7)</li>
<li>7) &nbsp;Change EWL T RGB to YELLOW . W ait for 3 seconds and go to step 8)</li>
<li>8) &nbsp;Turn off EWLT RGB to RED. Go to step 9)</li>
<li>9) &nbsp;Turn EW RGB to GREEN and wait for 6 seconds. Next, go to step 10)</li>
<li>10) &nbsp;The EW RGB will be changed to YELLOW and it stays on for 3 seconds. Go to step 11)</li>
<li>11) &nbsp;Change EW RGB to RED. Go to step 12)</li>
<li>12) &nbsp;Check the logic state of the NSLT_SW switch.
<ol>
<li>If 0, go back directly to step 16)</li>
<li>If 1, go to step 13)</li>
</ol>
</li>
<li>13) &nbsp;Turn on NSLT RGB to GREEN and leave it on for 8 seconds. Afterwards, go to step 14)</li>
<li>14) &nbsp;Change NSLT RGB to YELLOW. Wait for 3 seconds. Go to step 15)</li>
<li>15) &nbsp;Turn NSLT RGB to RED. Go to step 16)</li>
<li>16) &nbsp;This completes the sequence of Night_Mode().</li>
</ol>
Traffic Light Day Time Mode:

In this mode, the use of the Pedestrian Counter is added as well as the two inputs EWPED_SW and NSPED_SW. The ‘MODE LED’ must be turned on and stays on throughout the entire Day Mode time.

The design will incorporate the following implementation:

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
<ol>
<li>Next, set the NS RGB to GREEN while the other LEDs remain in RED. Read in the logic state of the NSPED_SW switch:
<ol>
<li>If ‘1’, then do the Pedestrian countdown for the NS direction and wait for 8 seconds (use the PED_Control() routine for this task). When done, go to step 2)</li>
<li>If the input is ‘0’, then go directly to step 2)</li>
</ol>
</li>
<li>Wait for 7 seconds with NS RGB still in GREEN. Then go to step 3)</li>
<li>Set the NS RGB to YELLOW and wait for 3 seconds. Go to step 4)</li>
<li>Next, change NS RGB to RED and go to step 5)</li>
<li>Check the logic state of EWLT_SW switch:
<ol>
<li>If 0, go directly to step 9)</li>
<li>If 1, there is a left-turn request. Go to step 6)</li>
</ol>
</li>
<li>Turn on EWLT RGB to GREEN and leave it for 8 seconds. Afterwards, go to step 7)</li>
<li>Change EWL T RGB to YELLOW . W ait for 3 seconds and go to step 8)</li>
<li>Turn off EWLT RGB to RED. Go to step 9)</li>
<li>Turn on EW RGB to GREEN. Read in the logic of EWPED_SW switch.
<ol>
<li>If ‘1’, then do the Pedestrian Countdown for the EW direction and wait for 9 seconds. When completed, go to step 10)</li>
<li>If ‘0’, then go to step 10) directly.</li>
</ol>
</li>
<li>The EW RGB is GREEN and stays for 9 seconds. Afterwards, go to step 11)</li>
<li>The EW RGB will be changed to YELLOW and it stays on for 3 seconds. Go to step 12)</li>
<li>Change EW RGB to RED. Go to step 13)</li>
<li>Check the logic state of the NSLT switch.
a. If 0, go directly to step 17)

b. If 1, there is a left-turn request. Go to step 14)
</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 9">
<div class="layoutArea">
<div class="column">
14. Turn on NSLT RGB to GREEN and leave it on for 8 seconds. Afterwards, go to step 15)

15. Change NSLT RGB to YELLOW. Wait for 3 seconds. Go to step 16)

16. Turn NSLT RGB to RED. Go to step 17) 17) This completes the sequence of Day_Mode().

</div>
</div>
</div>
