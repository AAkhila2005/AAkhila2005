//question 1

#include<iostream>
using namespace std;
void checkprime(int n);
int main(){
    int n,i;
    cout<<"enter your number-";
    cin>>n;
	checkprime(n);
	return 0;
}
void checkprime(int n){
	int i,a=0;
	for(i=2;i<=n-1;i++){
		if(n%i==0){
		a=1;
		break;
	}
}
if(n==1)
{
printf("no. is neither prime nor composite");
	}	
  else if(a==0){
		printf("given no. is prime");
	}
	else{
		printf("given no. is composite");
}
}
//question 2

include <iostream>
using namespace std;
int factorial(int n) {
    int fact = 1;
    for(int i = 1; i <= n; ++i) {
        fact *= i;
    }
    return fact;
}


bool strong(int number) {
    int sum = 0;
    int originalNumber = number;

    
    while (number > 0) {
        int digit = number % 10;
        sum += factorial(digit);
        number /= 10; 

    }
    return (sum == originalNumber);
}

int main() {
    int number;
   cout << "Enter a number: ";
    cin >> number;

    if(strong(number)) {
        cout << number << " is a strong number." <<endl;
    } else {
      cout << number << " is not a strong number." <<endl;
    }

    return 0;
}

//question 4

#include<iostream>
using namespace std;
void sumofdigits(int n);
int main(){
	int n;
	cout<<"enter number";
	cin>>n;
	sumofdigits(n);
	return 0;
}
void sumofdigits(int n){
	while(n!=0){
		int sum=0;
		sum=sum+n%10;
		n=n/10;
	}
	cout<<sum;
}
//question 4

#include<iostream>
using namespace std;
void maxarr(int arr[5]);
int main(){
	int arr[5];
	cout<<"enter inputs:";
	for(int i=0;i<5;i++){
		cin>>arr[i];
}
maxarr(arr);
return 0;
}
void maxarr(int arr[]){
	int max=arr[0],i;
 cout<<sizeof(arr);
	cout<<endl;
	for(i=0;i<5;i++)
	{
	if(max<arr[i]){
		max=arr[i];
	}	
	}
		cout<<max;	
}

//question 5

#include<iostream>
using namespace std;
void fibonacci(int n);
int main(){
	int n;
	cout<<"enter no of terms :";
	cin>>n;
	fibonacci(n);
	return 0;
}
void fibonacci(int n){
	int first=0,second=1,next;
	cout<<"fibonacci series:";
	for(int i=0;i<n;i++){
		cout<<first<<" ";
		next=first+second;
		first=second;
		second=next;
	}
}
