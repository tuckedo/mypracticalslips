#include <iostream.h>
#include <conio.h>
#include <string.h>
class student  //base class
{
protected:
int roll_no;
char name[20];
char div[2];
public:
void get();
void display();
};
void student::get()
{
cout<<"\nEnter roll no: ";
cin>>roll_no;
cout<<"\nEnter name: ";
cin>>name;
cout<<"\nEnter class: ";
cin>>div;
}
void student::display()
{
cout<<"\nRoll no: "<<roll_no;
cout<<"\nName: "<<name;
cout<<"\nClass: "<<div;
}
class internals:public virtual student
{
protected:
int in[5];
public:
void get()
{
cout<<"\nEnter Internal marks for 5 subjects: \n";
for(int i=0;i<5;i++)
cin>>in[i];
}
void display()
{
cout<<"\nInternal marks for 5 subjects: \n";
for(int i=0;i<5;i++)
cout<<in[i]<<"\t";
}
void check()
{
int sum=0;
for(int i=0;i<5;i++)
sum=sum+in[i];
if(sum<10)
cout<<"\nStudent Failed in Internals!";
else
cout<<"\nStudent Passed in internals!";
}
};
class externals:public virtual student
{
protected:
int ex[5];
public:
void get()
{
 cout<<"\nEnter External marks in 5 subjects: \n";
 for(int i=0;i<5;i++)
 cin>>ex[i];
}
void display()
{
cout<<"\nDisplaying External marks: \n";
for(int i=0;i<5;i++)
cout<<ex[i]<<"\t";
}
void check()
{
int sum=0;
for(int i=0;i<5;i++)
sum=sum+ex[i];
if(sum<40)
cout<<"\nStudent Failed in Externals!";
else
cout<<"\nStudent Passed in Externals!";
}

};
class result:public internals, public externals
{
protected:
int r[5];
public:
void get()
{
student::get();
internals::get();
externals::get();
for(int i=0;i<5;i++)
r[i]=in[i]+ex[i];
}
void display()
{
student::display();
internals::display();
externals::display();
cout<<"\nDisplaying total marks in each subject: ";
for(int i=0;i<5;i++)
cout<<r[i]<<"\t";
}
void check()
{
int sum=0;
internals::check();
externals::check();
for(int i=0;i<5;i++)
sum=sum+r[i];
if(sum<50)
cout<<"\nStudent Failed in Semester!";
else
cout<<"\nStudent Passed in Semester!";
}

};
int main()
{
clrscr();
result obj;
obj.get();
obj.display();
obj.check();
getch();
return 0;
}