#include <iostream>
#include <vector>
#include <numeric>
#include <limits>
#include <string.h>
#include <bitset>
using namespace std;
#define ll long long

int main() {
    ll x,k;
    ll y=0;
    while(cin>>x>>k){
       ll bitnumber=1;//the number of bits in the binary is used to determine the position at which x is converted to binary 0.
       while(k){
	       if((x&bitnumber)==0){
	       	    y+=(bitnumber*(k&1));
	       	 
	       	    k>>=1;
		   }
		   bitnumber<<=1;
		  // cout<<bitnumber<<endl;
	   }
	   cout<<y<<endl; 
	   y=0;
	}
    return 0;
}
