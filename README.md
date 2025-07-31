# c-
#include<iostream>
#include<algorithm>
using namespace std;
// Function declaration
void addofarray();
void addof2Darray();
void max_element();
void insert_element();

// main method
int main(){
    // addofarray();
    // addof2Darray();
    // max_element();
    insert_element();
    return 0;
}


// define the function
// addition of 1D Array
void addofarray(){
    int arr[5]={3,4,5,6,7};
    int n = sizeof(arr)/sizeof(int);
    int sum =0;
    for(int i=0; i<n; i++){
        sum += arr[i];
    }

    cout<<"Sum of an array : "<<sum;
}

// Addition of 2D Array elements
void  addof2Darray(){
    int arr[3][3];

    for(int i =0; i<3; i++){
        for(int j=0; j<3; j++){
            cout<<"Enter element at position ["<<i<<"]["<<j<<"]: ";
            cin>>arr[i][j];

        }
    }
    int sum = 0;
    for (int i=0; i<3; i++){
        for (int j = 0; j<3; j++){
            sum += arr[i][j];
        }
    }
    cout<<"Sum of an 2D array Elements : "<<sum;
}


// max element in an array
void max_element(){
    int arr[5]={3,4,5,6,7};
    int n = sizeof(arr)/sizeof(int);

    int max = *max_element(arr, arr + n);
    cout<< "max Element is : "<<max;
}

// insertion of element
void insert_element(){
    int arr[10]={4,5,7,2,3};
    int pos=4;
    int ele=50;
    int n = sizeof(arr)/sizeof(int);
    cout<<n;
    for(int i=n ; i>=pos; i--){
        arr[i]=arr[i-1];
    }
    arr[pos-1]=ele;

    cout<<"Updated array: "<<arr;
    
}
