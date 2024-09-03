//question 1
#include<bits/stdc++.h>
using namespace std;
void checkAmstrong(int n);

int main() {
    int n, temp, r, result = 0, c = 0;

    cout << "Enter a n number: ";
    cin >> n;
    checkAmstrong(n);
    return 0;
}
void checkAmstrong(int n){
	 int temp, r, result = 0, c = 0;
    temp = n;
    
    while (temp != 0) {
        temp /= 10;
        ++c;
    }

    temp=n;
    while (temp != 0) {
        r = temp % 10;
        result += pow(r, c);
        temp /= 10;
    }
    
    if (result == n)
        cout << n << " is an Armstrong number." << endl;
    else
        cout << n<< " is not an Armstrong number." << endl;

}
//question 2
#include<bits/stdc++.h>
using namespace std;

bool checkAnagrams(string str1, string str2) {
    
    sort(str1.begin(), str1.end());
    sort(str2.begin(), str2.end());

    return str1 == str2;
}

int main() {
    string string1, string2;

    cout << "Enter the first string: ";
    getline(cin, string1);

    cout << "Enter the second string: ";
    getline(cin, string2);

    if (checkAnagrams(string1, string2)) {
        cout << "'" << string1 << "' and '" << string2 << "' are anagrams." << endl;
    } else {
        cout << "'" << string1 << "' and '" << string2 << "' are not anagrams." << endl;
    }

    return 0;
}

//question 3
#include<bits/stdc++.h>
using namespace std;

int sumEven(int arr[], int size) {
    int sum = 0;

    for (int i = 0; i < size; i++) {
        if (arr[i] % 2 == 0) {
            sum += arr[i];
        }
    }

    return sum;
}

int main() {
    int n;

    cout << "Enter the number of elements in the array: ";
    cin >> n;

    int arr[n];

    cout << "Enter the elements of the array:" << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    int sum = sumEven(arr, n);

    cout << "The sum of even numbers in the array is: " << sum << endl;

    return 0;
}

//question 4
#include<bits/stdc++.h>
using namespace std;
int gcd(int m, int n) {
    if (n == 0) {
        return m;
    }
    return gcd(n, m % n);
}
int main(){
	int m,n;
	cout<<"Enter two numbers-";
	cin>>m>>n;
	 int result=gcd(m,n);
	cout<<"Gcd of the two number is-"<<result;
	return 0;
}

//question 5
#include<bits/stdc++.h>
using namespace std;
void cel(float f);
int main(){
	float f,c;
	cout<<"Enter temprature in celsius -";
	cin>>c;
	cel(c);
	return 0;
}
void cel(float c){
	float f;
	f=((9.0/5.0)*c)+32;
	cout<<"Temprature in farenheit is-"<<f;
}
