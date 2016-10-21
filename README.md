package test;

import java.util.Scanner;

public class Testing 
{
	public static void main( String[] argv ) throws Exception {
		Scanner sc = new Scanner(System.in);
		int steps = Integer.parseInt(sc.nextLine());
		int time = Integer.parseInt(sc.nextLine());
		int aStep = 0;
		int bStep = 0;
		
		for(int i=0; i<time; i++)
		{
			String[] abSteps = sc.nextLine().split(" ");
			aStep = aStep + Integer.parseInt(abSteps[0]);
			bStep = bStep + Integer.parseInt(abSteps[1]);
			if(aStep == steps && bStep == steps)
			{
				System.out.println("NO WINNER");
				break;
			}
			else if(aStep >= steps)
			{
				System.out.println("A");
				break;
			}
			else if(bStep >= steps)
			{
				System.out.println("B");
				break;
			}
		}
		sc.close();
	}
}
