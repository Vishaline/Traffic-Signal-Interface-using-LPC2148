#include <LPC214X.H>

void Delay(int); 			//Delay Routine


int main()
{
	PINSEL0 = 0X00000000; // P0.0 TO P0.15 as GPIO
	IO0DIR = 0X0000FFF0; // P0.4 TO P0.15 Configured as Output port.

	while(1)			// The program runs until it is stopped
	{

		IO0SET=0x00003090;	  // D7 [EAST] [PORT 0.12 connected to the GREEN light and all the other RED light i.e., PORT 0.13,0.7 and 0.4 are turned on]
		Delay(2500);	  	  

		IO0CLR=0x00001000;	  // will set logic 0, i.e, the green light is turned off
		
		IO0SET=0x00002890;	  // D8 [EAST] [PORT 0.11 connected to the YELLOW light is turned on and all the other red rights continue to be on]
		Delay(300);

		IO0CLR=0x000002890;	  // will set logic to 0, i.e, lights are turned off
		Delay(1);

		IO0SET=0x00008490;	 // D10 [SOUTH] [PORT 0.15 connected to the GREEN light and all the other RED lights i.e., PORT 0.4, 0.7, 0.10 are turned on]
		Delay(2500);

		IO0CLR=0x00008000;	 // will set logic 0, i.e, the green light is turned off

		IO0SET=0x00004490;	// D11 [SOUTH] [PORT 0.14 connected to the YELLOW light is turned on and all the other red rights continue to be on] 
		Delay(300);

		IO0CLR=0x00004490;	// (will set logic to 0), i.e, lights are turned off
		Delay(1);

		IO0SET=0x000024C0;   // D1 [WEST] GREEN [PORT 0.6 connected to the GREEN light and all the other RED lights i.e., PORT 0.7, 0.10 and 0.13 are turned on]
		Delay(2500);

		IO0CLR=0x00000040;	// will set logic 0, i.e., the green light is turned off

		IO0SET=0x000024A0;	// D2 [WEST] YELLOW [PORT 0.5 connected to the YELLOW light is turned on and all the other red rights continue to be on]
		Delay(300);

		IO0CLR=0x000024A0;	// (will set logic to 0), i.e, lights are turned off
		Delay(1);
		
		IO0SET=0x00002610;	// D4 [NORTH] GREEN [PORT 0.9 connected to the GREEN light and all the other RED lights i.e., PORT 0.4, 0.10 and 0.13 are turned on]
		Delay(2500);

		IO0CLR=0x00000200;	// will set logic 0, i.e., the green light is turned off


		IO0SET=0x00002510;	// D5 [WEST] YELLOW [PORT 0.8 connected to the YELLOW light is turned on and all the other red rights continue to be on]
		Delay(300);

		IO0CLR=0x00002510;	// (will set logic to 0), i.e, lights are turned off
		Delay(1);



		
		
	}
}


void Delay(int n)		//function for Delay
{
	int p,q;

	for(p=0;p<n;p++)
	{
		for(q=0;q<0xFFF0;q++);
	}
} 
