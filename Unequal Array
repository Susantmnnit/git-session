# git-session
gitclass
//{ Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


class Array
{
public:
    template <class T>
    static void input(vector<T> &A,int n)
    {
        for (int i = 0; i < n; i++)
        {
            scanf("%d ",&A[i]);
        }
    }

    template <class T>
    static void print(vector<T> &A)
    {
        for (int i = 0; i < A.size(); i++)
        {
            cout << A[i] << " ";
        }
        cout << endl;
    }
};


// } Driver Code Ends
class Solution {
  public:
    long long solve(int N, vector<int> &A, vector<int> &B) {
        long long sum1=0,sum2=0;
        sort(A.begin(),A.end());
        sort(B.begin(),B.end());
        vector<int>even1,odd1,even2,odd2;
        for(int i=0;i<N;i++){
            sum1=sum1+(long long)A[i];
            if(A[i]%2==0){
                even1.push_back(A[i]);
            }
            else{
                odd1.push_back(A[i]);
            }
            sum2=sum2+(long long)B[i];
            if(B[i]%2==0){
                even2.push_back(B[i]);
            }
            else{
                odd2.push_back(B[i]);
            }
        }
        if( sum1 != sum2 || (even1.size()!=even2.size())||(odd1.size()!=odd2.size())){
            return -1;
        }
        long long evendiff=0,odddiff=0;
        for(int i=0;i<even1.size();i++){
            evendiff+=abs(even2[i]-even1[i])/2;
        }
        for(int i=0;i<odd1.size();i++){
            odddiff+=abs(odd2[i]-odd1[i])/2;
        }
        return (evendiff+odddiff)/2;
    }
};


//{ Driver Code Starts.

int main(){
    int t;
    scanf("%d ",&t);
    while(t--){
        
        int N;
        scanf("%d",&N);
        
        
        vector<int> A(N);
        Array::input(A,N);
        
        
        vector<int> B(N);
        Array::input(B,N);
        
        Solution obj;
        long long res = obj.solve(N, A, B);
        
        cout<<res<<endl;
        
    }
}

// } Driver Code Ends
