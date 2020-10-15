## Input e output su file
Se il nostro programma, invece che leggere da tastiera e stampare a video, dovesse scrivere e leggere da file (solitamente file di estensione .txt), deve usare nuovi oggetti al posto di *cin* e *cout*. Ci serve la libreria *fstream*, che contiene tutto il necessario per lavorare con oggetti di tipo *filestream*. Useremo *ifstream* per leggere dati da file e *ofstream* per scrivere. 

Prima di tutto dobbiamo creare un file di input (ad esempio "input.txt") nella stessa cartella in cui è salvato il programma. In questo file scriviamo i dati da leggere. 

Ora nel nostro programma possiamo aprire il file da cui leggere e il file su cui scrivere (se non esiste viene creato automaticamente).
Con il comando `ifstream in ("input.txt");` andiamo ad aprire "input.txt", da cui possiamo leggere con il comando *in* (che funziona allo stesso modo del *cin*). Con `ofstream out ("output.txt");` viene creato o aperto (se già esistente) un file "output.txt" su cui possiamo scrivere con il comando *out* (analogo al *cout*).

```cpp
#include<fstream>
using namespace std;

int main(){
	ifstream in ("input.txt");
	ofstream out ("output.txt");

	int a;
	in >> a; //inserisco quello che leggo nella variabile a

	out << "Ciao! La variabile a vale " << a;
	
	in.close();
	out.close();
    
	return 0;
}

```
