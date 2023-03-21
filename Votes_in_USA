#include <bits/stdc++.h>
//#define int long long ; //int
using namespace std;
int main(){
   long long ratata;
 map <string, long long> itog;
 vector <pair <long long, string>> result;
    map <string, long long> vib;
    map <string, map <string, long long> > kon;
    cin>>ratata;
    for(long long i = 0; i<ratata; i++){
        string lol;
        cin>>lol;
        long long o;
        cin>>o;
        vib[lol]=o;
    }
    cin>>ratata;
    for(long long i = 0; i<ratata; i++){
            string state, pre;
            cin>>state>>pre;

            if(itog.find(pre) == itog.end()){

            itog[pre]=0;
            result.push_back({0, pre});
            }
            kon[state][pre]++;
            }
//конец считывания данных
string state_name, lider_stata;
long long y ;
     for (auto stat: kon) {
         state_name = stat.first;
        lider_stata=(*((stat.second).begin())).first;
        y = -1;
      for (auto lud :stat.second) {
            if(y<lud.second){
                lider_stata = lud.first;
                y=lud.second;
            }
            if(lud.second==y and lud.first<lider_stata){
                lider_stata=lud.first;
            }
        }
       itog[lider_stata]-=vib[state_name];// tut cmenil na -=
    }
    for(long long i = 0; i<result.size(); i++){
        string z = result[i].second;
        result[i].first=itog[z];
    }
    sort(result.begin(),result.end());
    //reverse(result.begin(),result.end());
    for(long long i = 0; i<result.size(); i++){
        cout<<result[i].second<<" "<<result[i].first*-1<<endl;
    }
    return 0;
}

