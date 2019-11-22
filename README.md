/*This is a BMI program that calculates the body mass index
(BMI) given weight in pounds and height in inches and prints
out what you should do..*/

#include<iostream>
  
using namespace std;

int main()
{
    const int BMI_Constant = 703;
    float weight;
    float height;
    float bodymassindex;
    bool dataAreOk;
    cout<<"enter your weight in pounds. "<<endl;
    cin>>weight;
    cout<<"enter your height in inches. "<<endl;
    cin>> height;
    if (weight<0||height<0)
        dataAreOk = false;
    else
        dataAreOk = true;
    if (dataAreOk)
    {
        bodymassindex = weight * BMI_Constant / (height*height);
        cout<< "your mass index is: "<<bodymassindex<<". "<<endl;
        cout<<"interpretation and instructions. "<<endl;
        if (bodymassindex < 20)
            cout<<"Underweight: Have a milk shake and eat more you're too skinny!!! "<<endl;
        else if (bodymassindex <= 25)
        cout<<"Normal: Have a glass of milk or a bear."<<endl;
        else if (bodymassindex<= 30)
            cout<<"Overweight: Have a glass of water and go to the gym."<<endl;
        else
            cout<<"Invalid data::::weight and height must be positive."<<endl;
        return 0;
    }
}
