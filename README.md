# spring-boot1
package test;

import java.util.Scanner;

public class Testing 
{
	public static void main( String[] argv ) throws Exception {
		Scanner sc = new Scanner(System.in);
		int steps = Integer.parseInt(sc.nextLine());
		int time = Integer.parseInt(sc.nextLine());
		
		while(sc.hasNext())
		{
			String[] abSteps = sc.nextLine().split(" ");
			int aStep = Integer.parseInt(abSteps[0]);
			int bStep = Integer.parseInt(abSteps[1]);
			int chrono = 1;
			while(aStep < steps && bStep < steps && chrono < time)
			{
				aStep = aStep + aStep;
				bStep = bStep + bStep;
				chrono = chrono + chrono;
			}
			if(aStep == steps && bStep == steps)
			{
				System.out.println("NO WINNER");
			}
			else if(aStep >= steps)
			{
				System.out.println("A");
			}
			else
			{
				System.out.println("B");
			}
		}
		sc.close();
	}
}
