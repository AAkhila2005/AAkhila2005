//question 1 

#include<iostream>
using namespace std;
void Perfectnumber(int n);
int main(){
	int n,sum=0;
	cout<<"Enter your number-";
	cin>>n;
	Perfectnumber(n);
	return 0;
}
void Perfectnumber(int n){
	int sum=0;
	for(int j=1;j<=n/2;j++){
		if(n%j==0){
			sum=sum+j;
		}
	}
	if(sum==n){
		cout<<"The given number is a perfect number.";
	}
	else {
		cout<<"The given number is not a perfect number.";
	}
}


//question 2

#include<iostream>
using namespace std;
void CheckPal(int n);
int main(){
	int n,sum=0;
	cout<<"enter your number-";
	cin>>n;
	CheckPal(n);
	return 0;
}
void CheckPal(int n){
	int sum=0;
	while(n>0){
		sum=sum+n%10;
		sum=sum*10;
		n=n/10;
	}
	sum=sum/10;
	if(sum==n){
		cout<<"The given number is  a pallindrome number.";
	}
	else{
		cout<<"The given number is not a pallindrome number.";
	}
}


//question 3

#include<iostream>
using namespace std;
int Countvow(string s);
int main(){
	string s;
	cout<<"Enter your string-";
	cin>>s;
	Countvow(s);
	return 0;	
}
int Countvow(string s)
{
    int count = 0;
    for(int i = 0; i < s.length(); i++)
    {
        char c = s[i];
        if (c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U'|| c =='a' || c =='e' || c =='i' || c =='o' || c =='u')
            count++;
    }
    cout<<"Number of vowels in the given string are-"<<count;
    return count;
}

//question 4

#include<iostream>
using namespace std;
void reverse(int n);
int main(){
	int n,sum=0;
	cout<<"enter your number-";
	cin>>n;
	reverse(n);
	return 0;
}
void reverse(int n){
	int sum=0;
	while(n>0){
		sum=sum+n%10;
		sum=sum*10;
		n=n/10;
	}
	sum=sum/10;
	cout<<"number after reversing is-"<<sum;
}


//question 5

#include<iostream>
using namespace std;
void factnum(int n);
int main(){
	int n,num=1;
	cout<<"Enter your number-";
	cin>>n;
	factnum(n);
	return 0;
}
void factnum(int n){
	int num=1;
	for(int i=1;i<=n;i++){
		num=num*i;
			}
			cout<<"factorial of the given number is-"<<num;
		}
