# sem-2-practical-
1) Write a program to compute the sum of the first n terms of the following series:
□ =1− 1/2^2+1/3^3−1/4^4+1/5^5− . . ..The number of terms n is to be taken from the user through the command line. If the command line argument is not found then prompt the user to enter the value of n.


#include <iostream>
#include <cmath>
#include <cstdlib>

using namespace std;

double computeSeries(int n) {
    double total = 0.0;
    for (int i = 1; i <= n; ++i) {
        double term = 1.0 / pow(i, i);
        if (i % 2 == 0) {
            term = -term; // Alternate signs for even terms
        }
        total += term;
    }
    return total;
}

int main(int argc, char* argv[]) {
    int n;
    if (argc > 1) {
        n = atoi(argv[1]);
        if (n <= 0) {
            cout << "Invalid input. Please enter a positive integer." << endl;
            return 1;
        }
    } else {
        cout << "Enter the number of terms (n): ";
        cin >> n;
        if (n <= 0) {
            cout << "Invalid input. Please enter a positive integer." << endl;
            return 1;
        }
    }
    
    double result = computeSeries(n);
    cout << "Sum of the series for " << n << " terms: " << result << endl;
    return 0;
}
![Screenshot (29)](https://github.com/user-attachments/assets/2c427a0e-91c3-44cc-9150-1f5613fab70d)

question 2

==Write a program to remove the duplicates from an array!

#include <iostream>
#include <vector>
#include <set>

using namespace std;

void removeDuplicates(vector<int>& arr) {
    set<int> seen;
    vector<int> uniqueArr;
    
    for (int num : arr) {
        if (seen.find(num) == seen.end()) {
            uniqueArr.push_back(num);
            seen.insert(num);
        }
    }
    
    arr = uniqueArr;
}

int main() {
    int n;
    cout << "Enter the number of elements in the array: ";
    cin >> n;
    
    vector<int> arr(n);
    cout << "Enter the elements of the array: ";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    removeDuplicates(arr);
    
    cout << "Array after removing duplicates: ";
    for (int num : arr) {
        cout << num << " ";
    }
    cout << endl;
    
    return 0;
}

![Screenshot (30)](https://github.com/user-attachments/assets/8cb12551-ff26-48b2-a8f3-e60d0d49a76d)














