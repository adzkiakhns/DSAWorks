#include <iostream>
#include <stack>
using namespace std;

void arekmalang(){
    string kalimat;
    cout << "Masukkan kalimat anda: ";
    cin >> kalimat;

    stack<char> swap;

    int i;
    //make an array from the kalimat
    int panjang_kalimat = kalimat.length();
    for(i = 0; i < panjang_kalimat; i++){
        //when a sentence is ended with ng
        if(kalimat[i] == 'n' && kalimat[i+1] == 'g'){
            kalimat[i] = 'g';
            kalimat[i+1] = 'n';
        }
    }

    //make a stack
    for(i = 0; i<panjang_kalimat; i++){
        char huruf = kalimat[i];
        swap.push(huruf);

        while(!swap.empty()){
            cout << swap.top();
            swap.pop();
        }
    }

}
int main(){
    arekmalang();
    return 0;
}
