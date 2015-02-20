#include<iostream>
#include<string>
using namespace std;
class ticket
{
protected:
int ticket_id,train_no,seats,totalamount,doj,ph,age[20],i,n,cls;
string from,to,train_name,name[20],address,m,f;
char gender[20];
public : void accept()
{
cout<<"\t ENTER TICKET ID:";
cin>>ticket_id;
cout<<"\t ENTER TRAIN NO:";
cin>>train_no;
cout<<"\t ENTER TRAIN NAME :";
cin>>train_name;
cout<<"\t ENTER NUMBER OF SEATS:\t";
cin>>seats;
cout<<"\t ENTER  TO :\t";
cin>>to;
cout<<"\t ENTER FROM: ";
cin>>from;
cout<<"\t SELECT CATEGORY  :1.A/C , 2.SLEEPER , 3.GENERAL \t";
cin>>cls;
if(cls==1)
{}
else if(cls==2)
{}
else if(cls==3)
{}
else
{system("clear");
cout<<"WRONG SELECTION";
return accept();
}
for( i=0;i<seats;i++)
{
cout<<"\t ENTER CUSTEMER NAMES :\n\t  ";
cin>>name[i];
cout<<"\t ENTER   AGE :";
cin>>age[i];
cout<<"\t ENTER GENDER :(M/F) ";
cin>>gender[i];
if(gender[i]=='m')
{

}
else if (gender[i]=='f')
{

}

else
{
system("clear");
cout<<"WRONG OUTPUT";
return accept();
}
}
cout<<"\t ENTER DATE OF JOURNEY : ";
cin>>doj;
cout<<"\t ENTER MOBILE NUMBER : ";
cin>>ph;
cout<<"\t ENTER ADDRESS :";
cin>>address;
cout<<"\t TICKET SPARE";
cin>>n;
if(cls==1)
{
totalamount=seats*(n+100);
}
else if(cls==2)
{
totalamount=seats*(n+50);
}
else
{
totalamount=seats*n;
}
}
public : void display()
{
cout<<"\t\t\t\t TICKET RESERVATION COUNTER\n\n"<<endl;
cout<<"\t      TICKET ID:"<<ticket_id;
cout<<"\t TRAIN NAME :"<<train_name;
cout<<"\t TRAIN NUMBER: "<<train_no<<endl<<endl;
cout<<"\t\tSEATS:\t"<<seats;
cout<<"\t TO :\t"<<to;
cout<<" \tFROM: "<<from;
cout<<" \t CLASS : "<<cls<<endl<<endl;
for(int i=0;i<seats;i++)
{
cout<<"\t\t CUSTEMER NAME :\t "<<name[i];
cout<<"\t  AGE :"<<age[i];
cout<<"\t GENDER : "<<gender[i]<<endl;
}
cout<<"\t\t\t\t DATE OF JOURNEY : "<<doj<<endl;
cout<<"\n\t\b MOBILE NUMBER : "<<ph;
cout<<"\t\t\tADDRESS :"<<address<<endl<<endl;
cout<<"\t\t\tTOTALAMOUNT :  "<<totalamount<<endl;
}
};
class Conf_ticket:private ticket
{
private:
int seatno;
string coach;
public:
void accept_cnf()
{
accept();
cout<<"Ener seatno ";
cin>>seatno;
cout<<"Enter coach";
cin>>coach;
}
void disp_cnf()
{
display();
cout<<endl<<"Seat no"<<seatno;
cout<<endl<<"coach "<<coach;
}
};
main()
{
Conf_ticket t1;
t1.accept_cnf();
t1.disp_cnf();
}
                                 
