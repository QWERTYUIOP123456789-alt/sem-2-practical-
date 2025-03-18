# sem-2-practical-
1) Write a program to compute the sum of the first n terms of the following series:
□ =1− 1/2^2+1/3^3−1/4^4+1/5^5− . . ..The number of terms n is to be taken from the user through the command line. If the command line argument is not found then prompt the user to enter the value of n.


include  <iostream>

include <cmath>  // For pow()

using namespace std;

double seriesSum(int n) {

double sum = 0;
for (int i = 1; i <= n; i++) {
    double term = 1.0 / pow(i, i);
    if (i % 2 == 0) {
        sum -= term;  // Alternate terms are negative
    } else {
        sum += term;
    }
}
return sum;
}

int main() {

int n;
cout << "Enter the number of terms: ";
cin >> n;

cout << "Sum of series: " << seriesSum(n) << endl;
return 0;

















