# chomework
#include <iostream>
#include <string> 
#include <iomanip>
using namespace std;

enum decimalsize {marble = 5, golfBall = 14, baseballBall = 24, basketBall = 80,beachBall = 167, exerciseBall = 250};
enum material { Ice = 55, Aluminum = 168, Gold = 1203, Iron = 491, Cedar = 22, Soil = 80,Paper = 33, Osmium = 1403};
double PI = 3.1416;


void check() {


   int response = 0;

	
	int a, b;
	int x, y;
	cout << "Choose the material of the sphere: " << endl;
	cout << "1. Ice" << endl;
	cout << "2. Aluminum" << endl;
	cout << "3. Gold" << endl;
	cout << "4. Iron" << endl;
	cout << "5. Cedar" << endl;
	cout << "6. Soil" << endl;
	cout << "7. Paper" << endl;
	cout << "8. Osmium" << endl;
	cout << "Use only the number of the element to choose it (eg. 1 for Ice) : ";
	cin >> y;

	cout << endl;

	cout << "Choose the size of the sphere: " << endl;
	cout << "1. Marble" << endl;
	cout << "2. Golf ball" << endl;
	cout << "3. Baseball ball" << endl;
	cout << "4. Basketball" << endl;
	cout << "5. Beach ball" << endl;
	cout << "6. Exercise ball" << endl;
	cout << "Use only the number of the size to choose it (eg. 1 for Marble) : ";
	cin >> x;


	

		if (x == 1) {
			a = decimalsize::marble;
		}
		if (x == 2) {
			a = decimalsize::golfBall;
		}
		if (x == 3) {
			a = decimalsize::baseballBall;
		}
		if (x == 4) {
			a = decimalsize::basketBall;
		}
		if (x == 5) {
			a = decimalsize::beachBall;
		}
		if (x == 6) {
			a = decimalsize::exerciseBall;
		}


		if (y == 1) {
			b = material::Ice;
		}
		if (y == 2) {
			b = material::Aluminum;
		}
		if (y == 3) {
			b = material::Gold;
		}
		if (y == 4) {
			b = material::Iron;
		}
		if (y == 5) {
			b = material::Cedar;
		}
		if (y == 6) {
			b = material::Soil;
		}
		if (y == 7) {
			b = material::Paper;
		}
		if (y == 8) {
			b = material::Osmium;
		}
		
		double d = a * 0.01;

		double radius = (d / 2);
		double sphere_volume = (4.0 / 3.0) * PI * (pow(radius,2));
		double mass = sphere_volume * b;
		double density = mass / sphere_volume;
		cout <<  endl;
		cout << "Density: "<< setprecision(4) << density << " pounds per cubic feet" << endl;
		cout << "Mass: " << setprecision(4)<<mass<< " pounds" << endl;
		cout << "Radius: " << radius *2 << " feet"<< endl;
		cout << "Volume: " << setprecision(2)<< sphere_volume <<" cubic feet"<< endl;
	
		
}

	
int main(){ 
	check();
}
