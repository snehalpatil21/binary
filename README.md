# binary
#include<iostream.h>
#include<conio.h>
class arr
{
	int a[10],n,m;
	public:
	void get();
	void bisearch();
	void sort();
	void display();
	
};
void arr::get()
{
	cout<<"enter size of array"<<endl;
	cin>>n;
	cout<<"enter array elements "<<endl;
	for(int i=0;i<=n;i++)
	{
		cin>>a[i];
	}
	cout<<"Elements are"<<endl;
	for(int j=0;j<=n;j++)
	{
		cout<<a[j]<<"  "<<endl;
	}
	cout<<endl;
}
void arr::sort()
{
	for(int i=0;i<=n;i++)
	{
		for(int j=0;j<n-i;j++)
		{
			if(a[j]>a[j+1])
			{
				m=a[j+1];
				a[j+1]=a[j];
				a[j]=m;
			}
		}
	
	}
}
void arr::bisearch()
{
	int b=0,e=n-1,ele;
	int m=int(b+e)/2;
	cout<<"Enter Any Element";
	cin>>ele;
	while((b<=e) && (a[m] !=ele))
	{
		if(a[m]>ele)
		{
			e=m-1;
		}
		else
		{
			b=m+1;
		}
		m=int (b+e)/2;
	}
	if(a[m]==ele)
	{
		cout<<"Element Are Found";
	}
	else
	{
		cout<<"Element Are Not Found";
	}
}
void arr::display()
{
	cout <<"Sorted Element List ...\n";
for(int i = 0; i<=n; i++) 
{
   cout <<a[i]<<endl;
}

}


int main()
{
	clrscr();
	arr a;
	a.get();
	a.sort();
	a.display();
	a.bisearch();
	getch();
	return(0);
}
