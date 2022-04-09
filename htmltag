#include <iostream>
#include <fstream>
#include <stack>
using namespace std;

int main(){
    string htmlstr;
    // user memasukkan string html
    cout << "Masukkan String HTML anda: ";
    cin >> htmlstr;

    char tanda;
    stack<string> stack;
    int i = 0;

    while(htmlstr[i] == tanda){
        string tag = "";
        if(tanda == '<'){
            while(htmlstr[i] == tanda){
                if(tanda == '>') break;
                tag += tanda;
            }
            if(tag[0] != '/') stack.push(tag);
            else{
                if(tag.substr(1).compare(stack.top()) == 0){
                    stack.pop();
                }
                else{
                    cout << "String HTML anda tidak valid\n";
                    return 0;
                }
            }
        }
    }
    if(stack.empty()) 
        cout << "String HTML anda Valid\n";
    else
        cout << "String HTML anda tidak valid\n";
}
