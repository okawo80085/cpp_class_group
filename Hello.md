927894955904890878904889894900892889902890898904894884904899894890902892948950943953


#include <iostream>
#include <string>
#include <vector>
#include <cstdlib>

using namespace std;

int main()
{
    vector<int> hi,hello;
    vector<string> numbers;
    string code,text,num;
    int n,f,f1,f2,f3;
    char g;
    cout << "Choose the action" << endl << "(1 - text to code," << endl << "2 - code to text)" << endl << "Action: ";
    cin >> n;
    if(n!=1&&n!=2){
        cout << "Nope";
        return -1;
    }
    system("CLS");
    if(n==1){
    for(int i=0,e=57;i<10;i++,e--){
        hi.push_back(e);
    }
    cout << "Text - ";
    cin >> text;
    for(int i=0;i<text.length();i++){
        g = text[i];
        f = g;
        code.push_back(hi[f/100]);
        code.push_back(hi[(f%100-f%10)/10]);
        code.push_back(hi[f%10]);
    }
    cout << endl << "Code - " << code << endl;
    }
    if(n==2){
    cout << "Code - ";
    cin >> code;
    for(int i=0;i<60;i++){
        hi.push_back(0);
    }
    for(int i=0,e=57;i<10;i++,e--){
        hi[e]=i;
    }
    for(int i=0;i<code.length();i+=3){
        num.push_back(code[i]);
        num.push_back(code[i+1]);
        num.push_back(code[i+2]);
        numbers.push_back(num);
        num. clear();
    }
    for(int i=0;i<numbers.size();i++){
        num = numbers[i];
        f3=0;
        for(int w=0,r=100;w<3;w++,r/=10){
            f1=num[w];
            f2=hi[f1];
            f3+=f2*r;
        }
        g=f3;
        text.push_back(g);
    }
    cout << endl << "Text - " << text << endl;
    }
    return 0;
}