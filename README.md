#include<iostream>
#include<string.h>
#include<stdlib.h>
using namespace std; 
class Printer{ 
 private : 
 string nomi,turi,kortredji,davlati; 
 int yili; 
 
 int hajmi; 
 float narxi; 
 public : 
  void show() 
  { 
   static int k=0; 
   cout<<++k<<" - printer"<<endl<<endl; 
   cout<<"Turi: "<<turi<<endl;
   cout<<"Nomi: "<<nomi<<endl;  
   cout<<"Yili: "<<yili<<endl; 
   cout<<"Kortredji: "<<kortredji<<endl; 
   cout<<"Davlati: "<<davlati<<endl; 
   cout<<"Pozitsiyasi: "<<hajmi<<endl; 
   cout<<"Narxi: "<<narxi<<endl; 
  }; 
  void input(){ 
   static int k=0; 

   cout<<++k<<" - printer"<<endl<<endl; 
   cout<<"Turi: ";cin>>turi;
   cout<<"Nomi: ";cin>>nomi;  
   cout<<"Yili: ";cin>>yili; 
   cout<<"Kortredji: ";cin>>kortredji; 
   cout<<"Ishlab chiqarilgan davlati: ";cin>>davlati; 
   cout<<"Pozitsiyasi: ";cin>>hajmi; 
   cout<<"Narxi: ";cin>>narxi;
   cout<<endl; 
  }; 
  void qidir(string s){ 
   if(nomi.compare(s)==0) 
   { 
    cout<<"Bunday nomli printer yoq"; 
    show(); 
   } 


}; 
void qidir1(string d){ 
   if(turi.compare(d)==0) 
   { 
    cout<<"Bunday tur printer yoq"; 
    show(); 
   } 
  }; 
}; 
int main() 
{ 
 Printer t[100]; 
 int N;cout<<"Printer sonni kriting";cin>>N;  
 for(int i=0;i<N;i++) 
 { 
  t[i].input(); 
 } 
 string s; 
 cout<<endl<<"Qidirilayotgan printer nomini kriting";cin>>s; 
 for(int i;i<N;i++) 
 { 
  t[i].qidir(s); 
 } 
 string d; 
 cout<<endl<<"Qidirilayotgan printerni  kiriting";cin>>d; 

 for(int i;i<N;i++) 
 { 
  t[i].qidir1(d); 
 } 
}
