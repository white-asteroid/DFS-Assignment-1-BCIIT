/* 
1. WAP to perform following operations on arrays data structures:

a) Insertion b) Deletion

c) Linear Search

d) Binary Search with and without recursion

e) Insertion Sort

f) Selection Sort

g) Bubble Sort

h) Counting Sort
*/

#include <stdlib.h>
#include <stdio.h>

/* =============== SEARCHING OPERATIONS */
void linearSearch(int arr[],int k,int len)
{
    int i,f=-1;
    for( i = 0;i<len;i++)
    {
        if(arr[i]==k)
            {
                f=i;
                break;
            }

    }
    if(f!=-1)
    {
        printf("found at %d \n",i);
    }
    else
    {
        printf("not found \n");
    }
}

void binarySearch(int arr[],int k,int len)
{
    int l=0, h =len,mid;
    while(l<=h)
    {
        mid = l + (h-l)/2;
        if(arr[mid]==k)
        {
            printf("Found at %d \n ",mid);
            return;
        }
        else if(arr[mid]>k)
            h=mid-1;
        else
            l=mid+1;
    }
}

/* =============== SORTING OPERATIONS */
void binarySearchRec(int arr[] , int k ,int h,int l)
{
    int mid;
        mid = l + (h-l)/2;
        if(arr[mid]==k)
        {
            printf("Found at %d \n ",mid);
            return;
        }
        else if(arr[mid]>k)
            binarySearchRec(arr,k,mid-1,l);
        else
             binarySearchRec(arr,k,h,mid+1);

}

void insertionSort(int arr[] , int len){
    int i , j ,x;
    for(i=1;i<len;i++)
    {
        j=i-1;
        x = arr[i];
        while(j>-1 && arr[j]>x)
        {
            arr[j+1]=arr[j];
            j--;
        }
        arr[j+1]=x;
    }
}

void selectionSort(int arr[],int len){
    int i, k , j ;
    for(i=0;i<len-1;i++)
    {
        k=i;
        for(j=k;j<len;j++)
        {
            if(arr[j]<arr[k])
                k=j;
        }
        if(i!=k)
            swap(&arr[i],&arr[k]);
    }
}

void bubbleSort(int arr[],int len)
{
    int i,j,f=0;
    for(int i = 0;i<len-1;i++)
    {
        for(j=0;j<len-i-1;j++)
            if(arr[j+1]<arr[j])
            {
                swap(&arr[j],&arr[j+1]);
                f=1;
            }
        if(f==0)
        {
            break;
        }
    }
}

void countSort(int arr[],int len)
{
    int farr[7]={0};
    int sarr[7]={0};
    int oarr[6];
   int i,j,max=arr[0],sum=0;
    for(i=1;i<len;i++)
    {
        if(arr[i]>max)
            max=arr[i];
    }
    for(i=0;i<len;i++)
        farr[arr[i]]++;

    for(i=0;i<len;i++)
    {

        sum+=farr[i];
        sarr[i]=sum;
    }

    for(i=0;i<len;i++)
    {

        sarr[arr[i]]--;
        oarr[sarr[arr[i]]] = arr[i];
    }
    printArr(oarr);
    for(i=0;i<len;i++)
    {
        arr[i] = oarr[i];
    }

}
/* =============== BASIC OPERATION (INSERTION DELETION TYPES) */
void deleteArr(int arr[],int p,int len)
{
     int i ;
    if(p<len)
    {
        for(i=p;i<len-1;i++)
            arr[i]=arr[i+1];
        // len--;
    }
    else
    {
        printf("wrong input \n ");
    }

}
void swap(int *a , int *b)
{
    int t = *a;
    *a=*b;
    *b=t;
}
void printArr(int arr[],int len)
{
    int i;
    for(i=0;i<len;i++)
        printf(" %d ",arr[i]);
        printf("\n");
}

void reWriteArr(int arr[])
{
    int i,len=6;
     printf("Enter 6 elements in array \n");
    for(i=0;i<len;i++)
        scanf("%d",&arr[i]);
}
int main()
{
    int arr[10],len=6,i,j,p,c,f=1;
    printf("Enter 6 elements in array \n");
    for(i=0;i<len;i++)
        scanf("%d",&arr[i]);
    while(f){
    //clrscr;
    printf("1.Display array\n");
    printf("2.Delete from array\n");
    printf("3.linear search array\n");
    printf("4.binary search array\n");
    printf("5.Rewrite array\n");
    printf("6.binary search recursion array\n");
    printf("7.insertion sort array\n");
    printf("8.selection sort array\n");
    printf("9.bubble sort array\n");
    printf("10.count sort array\n");
    printf("11.count sort array\n");
    printf(" \nChoose operation to perform : \n");
    scanf("%d",&c);

    switch(c){
    case 1:
        printArr(arr,len);
        break;
    case 2:
        printf("Enter position you want to delete in array \n");
        scanf("%d",&p);
        deleteArr(arr,p,len--);
        break;
    case 3 :
        printf("Enter value you want to search in array \n");
        scanf("%d",&p);
        linearSearch(arr,p,len);
        break;
    case 4:
        printf("Enter value you want to search in array \n");
        scanf("%d",&p);
        binarySearch(arr,p,len);
        break;
    case 5:
        printf("Rewrite array \n");
        reWriteArr(arr);
        printf("new array : \n");
        printArr(arr,len);
        break;
    case 6:
        printf("Enter value you want to search in array \n");
        scanf("%d",&p);
        binarySearchRec(arr,p,len,0);
        break;
    case 7:
        insertionSort(arr,len);
        printf("new array : ");

        printArr(arr,len);
        break;
    case 8:
        selectionSort(arr,len);
        printf("new array : ");

        printArr(arr,len);
        break;
     case 9:
        bubbleSort(arr,len);
        printf("new array : ");

        printArr(arr,len);
        break;
     case 10:
        countSort(arr,len);
        printf("new array : ");

        printArr(arr,len);
        break;
    }
    printf("Do you want to perform more operations ? 1/0");
    scanf("%d",&f);
    }
    return 0;
}
