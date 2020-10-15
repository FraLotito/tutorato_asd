# Libreria standard C++
Nella libreria standard del C++ ci sono molte strutture dati già implementate, noi andremo a vedere le più utilizzate.

## Vector
La struttura dati `vector` implementa i vettori dinamici.
```cpp

#include <iostream>
#include <vector> //per utilizzare i vector
using namespace std;

int main() 
{ 
    vector<int> v; //Dichiaro un array di nome v, e specifico che conterrà elementi `int`
    
    v.push_back(10); //La funzione push_back inserisce un elemento (in questo caso il numero 10) in fondo all'array
    v.push_back(20);
    v.push_back(30);
    
    for(int i = 0; i < v.size(); i++){  // La funzione size() ritorna il numero di elementi all'interno dell'array
        cout << v[i] << endl; // Per accedere all' i-esimo elemento, v[i]
    }
    
}
```
Il risultato sarà così:
![Vector](https://i.postimg.cc/3xH1X7zn/Immagine-2020-10-15-153955.png)

## Matrici
Ovviamente possiamo anche non limitarci agli array di interi, ad esempio potremmo pensare ad avere delle matrici dinamiche.

```cpp

#include <iostream>
#include <vector>
using namespace std;

int main() 
{ 
    vector<vector<int>> matrix; // Inizializzo una matrice di interi
    
    for(int i = 0; i < 5; i++){
        vector<int> tmp(5); // Voglio riempire le righe con dei vettori di 5 elementi
        for(int j = 0; j < 5; j++){
          tmp[j] = i+j; 
        }
        matrix.push_back(tmp);
    }

    for(int i = 0; i < 5; i++){
        for(int j = 0; j < 5; j++){ //questo ciclo stampa tutta la riga i-esima
            cout << matrix[i][j] << " ";
        }
        cout << endl; //manda a capo dopo aver stampato la riga
    }
    
}
```
Il risultato sarà così:
![Matrix](https://i.postimg.cc/6qJ2k6rP/Immagine-2020-10-15-154115.png)
