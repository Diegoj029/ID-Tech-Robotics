# c-
my c++ codes
#include<iostream>
#include<string>

using namespace std;
	string flag_check();
	string flag_check()
	{
		int flag_x,flag_y,car_x,car_y,vel_x,vel_y;
		cin>>flag_x>>flag_y>>car_x>>car_y>>vel_x>>vel_y;
	
		int dx=flag_x-car_x;
	
		int dy=flag_y-car_y;		
		
		int b=vel_y*dx;
		int c=vel_x*dy;
		int a=b-c;
		
		if (a<0)
		{
			return "left";		
		}
		else if(a>0)
		{
			return "right";
		}
		else if(a==0)
		{
			//return "dot product";
			if (((vel_x*dx)+(vel_y*dy))>=0)
			{
				return "pointing at";
			}
			else
			{
				return "pointing away";
			}
		}
	}

int main(){
		string q;
		q=flag_check();
		cout<<q;
}
