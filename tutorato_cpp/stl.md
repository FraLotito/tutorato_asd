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
![Matrix](https://i.postimg.cc/6qJ2k6rP/Immagine-2020-10-15-154115.png)

## Stack
Un'altra struttura dati molto utilizzata è lo stack.
```cpp
#include <iostream>
#include <stack> //per utilizzare gli stack
using namespace std;

int main() 
{ 
    stack<int> s;
    s.push(5); //La funzione push() inserisce un elemento in cima allo stack
    s.push(6); 
    s.push(7); 
    
    cout << "Lo stack ha dimensione " << s.size() << endl;

    while(!s.empty()){ //La funzione empty() restituisce true se lo stack è vuoto, false altrimenti
        cout << "L'elemento in cima allo stack è: " << s.top() << endl; 
        s.pop(); // La funzione pop() rimuove l'elemento in cima allo stack
        cout << "Lo stack ora ha dimensione " << s.size() << endl;
    }
}
```
![Stack](https://i.postimg.cc/bJKNZ6dS/stack.png)

## Queue
L'utilizzo delle code (queue) è molto simile a quello degli stack, con la differenza dell'ordine di estrazione degli elementi.
```cpp
#include <iostream>
#include <queue> //per utilizzare gli stack
using namespace std;

int main() 
{ 
    queue<int> q;
    q.push(5); //La funzione push() inserisce un elemento in fondo alla coda
    q.push(6); 
    q.push(7); 
    
    cout << "La coda ha dimensione " << q.size() << endl;
    
    while(!q.empty()){ //La funzione empty() restituisce true se la coda è vuota, false altrimenti
        cout << "L'elemento in cima alla coda è: " << q.front() << endl; 
        q.pop();
        cout << "La coda ora ha dimensione " << q.size() << endl;
    }
}
```
![Queue](https://i.postimg.cc/NfvjYPWW/queue.png)

