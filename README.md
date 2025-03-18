# sem-2-practical-
1) practical 1
include <iostream>

include<cmath>  // for pow()

using namespace std;

double seriesSum(int n){

double sum=0;
for (int i=1;i<=n;i++){
  double term=1.0/pow(i,i);
  if(i%2==0){
   sum-=term; //alterenative terms are negetive
  }
  else{
   sum+=term;
  }
}
return sum;
}
int main()
int n ;
cout<<"enter the number of terms:";
cin>>n;
cout<<"sum of series:"<< seriessum(n)<< end1;
return 0 ;

















