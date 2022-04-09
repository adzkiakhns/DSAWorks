#include <iostream>
#include <stack>
#include <algorithm>
using namespace std;

// function untuk menghilangkan spasi
string spasi_hilang(string kal)
{
    
    kal.erase(remove(kal.begin(), kal.end(), ' '), kal.end());
    return kal;
}

// function untuk menentukan apakah betul kalimat merupakan sebuah palindrome
bool palindrome(string kalimat)
{
    // mendeklarasikan variabel
    int panjang = kalimat.length();

    //membuat sebuah stack yang berisikan huruf - huruf pada kalimat tersebut
    stack<char> huruf;

    int i, tengah = panjang / 2;


    for (int i = 0; i <= panjang; i++)
    {
        // membuat semua huruf di kalimat non-kapital
        kalimat[i] = tolower(kalimat[i]);
    }
 
    for (i = 0; i < tengah; i++) {
        // memasukkan huruf di top dari stack
        huruf.push(kalimat[i]);
    }
 
    if (panjang % 2 != 0) {
        i++;
    }
   
    char urut;
    while (kalimat[i] != '\0')
    {
         urut = huruf.top();
         huruf.pop();
 
    if ( urut != kalimat[i])
        return false;
        i++;
    }
 
return true;
}
 
int main()
{
    string kalimat, kal;
    cout<<"Input kalimat / kata anda: ";
    cin >> kalimat;
    kal = spasi_hilang(kalimat);

    if (palindrome(kal))
    {
    cout << "Kalimat anda merupakan sebuah palindrom";
    }
    else
    {
    cout << "Kalimat anda bukan merupakan palindrom.";
    }
}
