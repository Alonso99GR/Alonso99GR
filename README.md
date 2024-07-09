#include <iostream>
using namespace std;

// "bubbleSort"
void bubbleSort(int arr[], int size) {
    for (int i = 0; i < size - 1; ++i) {
        for (int j = 0; j < size - i - 1; ++j) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

void printArray(int arr[], int size) {
    for (int i = 0; i < size; ++i) {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int main() {
    int arr[] = {54, 37, 81, 12, 95, 6, 23, 68, 47, 76, 29, 42};
    int size = sizeof(arr) / sizeof(arr[0]);

    cout << "Lista original: ";
    printArray(arr, size);

    bubbleSort(arr, size);

    cout << "Lista ordenada: ";
    printArray(arr, size);

    return 0;
}
/////////////////////////////////////////////////////////
#include <iostream>
using namespace std;

//"Sort"

void insertionSort(int arr[], int size) {
    for (int i = 1; i < size; ++i) {
        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }

        arr[j + 1] = key;
    }
}

void printArray(int arr[], int size) {
    for (int i = 0; i < size; ++i) {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int main() {
    int arr[] = {54, 37, 81, 12, 95, 6, 23, 68, 47, 76, 29, 42};
    int size = sizeof(arr) / sizeof(arr[0]);

    cout << "Lista original: ";
    printArray(arr, size);

    insertionSort(arr, size);

    cout << "Lista ordenada: ";
    printArray(arr, size);

    return 0;
}

/////////////////////////////////////
#include <iostream>
//"Busqueda binaria"
const size_t nElementos = 10;

int bBinaria(int V, int *A, int N);

int main() {

    int A[nElementos] = {0,3,5,7,12,23,24,30,31,39};

    int V;

    int pos;

    V=12;

    pos = bBinaria(V, A, nElementos);

    if(pos>0) std::cout << "posicion de " << V << ": " << pos << std::endl; 

    else std::cout << "Valor " << V << " No encontrado" << std::endl;

    V=24;

    pos = bBinaria(V, A, nElementos);

    if(pos>0) std::cout << "posicion de " << V << ": " << pos << std::endl; 

    else std::cout << "Valor " << V << " No encontrado" << std::endl;

    V=39;

    pos = bBinaria(V, A, nElementos);

    if(pos>0) std::cout << "posicion de " << V << ": " << pos << std::endl; 

    else std::cout << "Valor " << V << " No encontrado" << std::endl;

    V=22;

    pos = bBinaria(V, A, nElementos);

    if(pos>0) std::cout << "posicion de " << V << ": " << pos << std::endl; 

    else std::cout << "Valor " << V << " No encontrado" << std::endl;

    return 0;

}

int bBinaria(int V, int *A, int N) {

    int Li, Ls, Lc;

    Li = 0;

    Ls = N-1;

    while(Li <= Ls) {

        Lc = Li+(Ls-Li)/2;

        if(A[Lc] == V) return Lc;

        if(A[Lc] > V) Ls = Lc-1;

        else Li = Lc+1;

    }

    return -1;

}


///////////////////////////////

#include<stdio.h>
//"Lineal "
int main(void){
  int lista[51];
  int i;

  for(i = 0; i <= 50; i++){
               lista[i] = i * 2; 
  } 
  for(i = 0; i <= 50; i++){
               printf("%d ",lista[i]);
             if(i % 10 == 0 && i != 0) 
                        printf("\n");
  }
return 0;
}








