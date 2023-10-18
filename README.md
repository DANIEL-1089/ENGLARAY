#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <conio.h>
#include <iomanip>



using namespace std;
class Distance {
private:
    int feet;
    float inches;
public:
    void getdist() {
        cout << "\n Enter a feet: "; cin >> feet;
        cout << "\n Enter a inches: "; cin >> inches;
    }
    void showdist() const {
        cout << feet << "\'-" << inches << '\"';
    }
};


int main()
{
    Distance dist[100];
    int n = 0;
    char ans;
    cout << endl;

    do {
        cout << "enter the length of the number " << n + 1;
        dist[n++].getdist();
        cout << "continue typing(y/n)?: ";
        cin >> ans;
    } while (ans != 'n');

    for (int j = 0; j < n; j++) {
        cout << "\nLength number " << j + 1 << " : ";
        dist[j].showdist();
    }
    cout << endl;


    return 0;
}
