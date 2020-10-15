# Flow
Spesso è utile dividere il programma in più funzioni, in modo da evitare la duplicazione codice. Ora vedremo come dichiarare e chiamare una funzione.

## Firma
La firma di una funzione è costituita da vari elementi:
* Tipo di ritorno
* Nome della funzione
* Lista degli argomenti

![Funzione](https://i.postimg.cc/wM1yPWbw/Immagine.png)

## Funzioni in azione
La prima funzione che viene chiamata quando viene eseguito un programma è la funzione `main`. 
```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<int> riempi_vettore(int dim){
    vector<int> v;
    for(int i = 0; i < dim; i++)
        v.push_back(i);

    return v;
}

void stampa_vettore(vector<int> &vect){
    for(int i = 0; i < vect.size(); i++)
        cout << vect[i] << " ";
}

int main(){ 
    vector<int> v;
    v = riempi_vettore(5);
    stampa_vettore(v);
}
```

## Passaggio dei parametri per valore
Quando un parametro viene passato per valore (o copia) a una funzione, viene creata una copia di quell'oggetto che verrà utilizzata all'interno della funzione senza influenzare l'oggetto originale.
```cpp
#include <iostream>
using namespace std;

void passaggio_per_valore(int x){
    x = 2;
    cout << "All'interno della funzione x vale: " << x << endl;
}

int main() { 
    int val = 10;
    passaggio_per_valore(val);
    cout << "Dopo la chiamata, non è cambiato il valore originale di val: " << val << endl;
}
```
![Valore](https://i.postimg.cc/qqmRk2Wz/Immagine-2020-10-15-171109.png)

Tuttavia, questo significa che se viene passata una struttura dati molto grande, verrà copiata per intero: spesso non è una buona idea passare per valore un vettore di milioni di elementi.

## Passaggio dei parametri per riferimento
Quando un parametro viene passato per riferimento a una funzione, viene semplicemente passato un puntatore alla struttura dati. Qualsiasi cambiamento all'oggetto all'interno della funzione chiamata, si rifletterà nell'oggetto originale. 
Per indicare a una funzione che si vuole passare un parametro per riferimento, occorre mettere un `&` prima del nome del parametro.

```cpp
#include <iostream>
using namespace std;

void passaggio_per_valore(int &x){
    x = 2;
    cout << "All'interno della funzione x vale: " << x << endl;
}

int main() { 
    int val = 10;
    passaggio_per_valore(val);
    cout << "Dopo la chiamata, è cambiato il valore originale di val: " << val << endl;
}
```
![Riferimento](https://i.postimg.cc/dVNx8Dcr/Immagine-2020-10-15-171728.png)










