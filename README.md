# crispy-eureka
Electricity board wants to generate the monthly electricity bills for their consumers based on electricity units consumed. They apply following conditions to calculate the bill as per type of the consumer. 
#include <iostream> 
#include<string.h> 
using namespace std; 
 
class Electricity 
{ 
  public: 
  char name[50]; 
  int number; 
  char type[15]; 
  long int cureading; 
  long int lareading; 
  char month[10]; 
  int pamt; 
  int kwh;
  void ReadData() 
  { 
      cout<<"Enter Consumer Name"<<endl; 
      cin >> name ; 
      cout<<"Enter Consumer Number"<<endl; 
      cin >> number; 
      cout<<"Enter Type"<<endl; 
      cin >> type; 
      cout<<"Enter Current Meter Reading"<<endl; 
      cin >> cureading; 
      cout<<"Enter Last Meter Reading"<<endl; 
      cin >> lareading; 
      cout<<"Enter Bill Month"<<endl; 
      cin >> month; 
      cout <<"Data Read "<< endl; 
  } 
   void calculateBill() 
   { 
       kwh=cureading-lareading; 
       if(type=="Commercial") 
       { 
           if(kwh<200) 
           { 
           pamt =kwh5; 
           } 
           else if (kwh>200) 
           { 
             pamt = 2005+(kwh-200)10; 
           } 
       } 
       else if(type=="Non-commercial") 
       { 
           if(kwh<100) 
           { 
               pamt =kwh3; 
           } 
           else if(kwh>100) 
           { 
               pamt = 1005+(kwh-100)5; 
           } 
       } 
   }
void printBill() 
   { 
       cout<<name <<endl; 
       cout<<number <<endl; 
       cout<<type <<endl; 
       cout<<cureading<<endl; 
       cout<<lareading <<endl; 
       cout<<month <<endl; 
       cout<<pamt <<endl; 
   } 
};
int main() 
{ 
   Electricity E; 
   E.ReadData(); 
   E.calculateBill(); 
   E.printBill();
    return 0; 
}
