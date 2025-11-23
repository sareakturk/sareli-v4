# sareli-v4
#include <iostream>
using namespace std;

int main() {

    int yukler[7]     = {350, 600, 200, 450, 500, 100, 400}; 
    int hizlar[7]     = {40, 30, 80, 50, 20, 15, 60};
    int yukseklik[7]  = {50, 70, 150, 90, 210, 30, 120};


    int pil[7];
    for(int i = 0; i < 7; i++) {
        pil[i] = hizlar[i] / 10;  
        pil[i] = 100 - pil[i];    
    }
    
    for(int i = 0; i < 7; i++) {
        cout << "Drone " << i+1 << ": ";

        bool sorun = false;

        if (yukler[i] > 500) {
            cout << "Agir yuk! Ucamaz!" << endl;
            sorun = true;
        }
        
        if (pil[i] < 30) {
            cout << "Pil seviyesi dusuk, ucus guvensiz!" << endl;
            sorun = true;
        }

    
        if (yukseklik[i] < 20 || yukseklik[i] > 200) {
            cout << "Yukseklik/Radar durumu, ucus guvensiz!" << endl;
            sorun = true;
        
        
        if (!sorun) {
            cout << "Ucus guvenli! Kalan pil: " << pil[i] << "%" << endl;
        }

        cout << "----------------------------------" << endl;
    }

    return 0;
}
