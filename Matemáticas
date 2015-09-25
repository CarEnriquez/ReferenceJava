\section{Math}

\subsection{Binary Exponentiation}
Realiza $a^{b}$ y retorna el resultado m\'odulo c. Si se elimina el m\'odulo c, debe tenerse precauci\'on para no exceder el l\'imite

\begin{lstlisting}

static int binaryExponentiation(int a, int b, int c){
    if (b == 0){
    	return 1;
    } 
    if (b % 2 == 0){
        int temp = binaryExponentiation(a,b/2, c);
        return (int)(((long)(temp) * temp) % c);
    }else{
        int temp = binaryExponentiation(a, b-1, c);
        return (int)(((long)(temp) * a) % c);
    }
}
\end{lstlisting}

\subsection{Greatest common divisor}
Calcula el m\'aximo com\'un divisor entre a y b mediante el algoritmo de Euclides

\begin{lstlisting}

int mcd(int a, int b) {
	int aux;
	while(b!=0){
		a %= b;
		aux = b;
		b = a;
		a = aux;
	}
	return a;
}
\end{lstlisting}

\subsection{Sieve of Eratosthenes}
Guarda en primes los n\'umeros primos menores a MAX

\begin{lstlisting}

import java.util.ArrayList;

static int MAX = 10000000;
static ArrayList<Integer> primes = new ArrayList<Integer>();
static boolean sieve[] = new boolean[MAX+5];
	
static void calculatePrimes() {
  sieve[0] = sieve[1] = true;
  int i;
  for (i = 2; i * i <= MAX; ++i) {
    if (!sieve[i]) {
      primes.add(i);
      for (int j = i * i; j <= MAX; j += i)
        sieve[j] = true;
    }
  }
  for(; i <= MAX; i++){
  	if (!sieve[i]) {
      primes.add(i);
    }
  }
}
\end{lstlisting}
