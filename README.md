# C---Mortal-Kombat-Tower
#include <bits/stdc++.h>
using namespace std;
#define ull unsigned long long
#define ll long long
#define ld long double


int main() {

    int t;
    cin>>t;
    while(t--){
        int n;
        cin>>n;
        vector<int> A(n);
        vector<int> zero;
        zero.push_back(0);
        for(int i=0;i<n;i++){
            cin>>A[i];
            if(i!=0)
            if(A[i]==0) zero.push_back(i);
        }

        int moves=0;
        if(A[0]==1) moves++;
        for(int i=1;i<zero.size();i++){
            moves+=(zero[i]-zero[i-1]-1)/3;
        }
        moves+=(n-1-zero[zero.size()-1])/3;
        cout<<moves<<endl;
    }

}





