# mdb
summary description of a compression algorithm based on a subset of prime numbers

any PC file can be represented in decimal. With a file of only 4 bits it will have a value ranging from 0 to 15.
now let's consider the Mersenne prime numbers https://en.wikipedia.org/wiki/Mersenne_prime
in particular their indices:

2,3,4,8,10,12,19,37,54,65,77,314,366,770,1327,1373,1937,2561,2663,5834,5985,6751,
12003,13066,13973,26790,51924,66530,79502,130100,455663,517430,757263,841842,1791864,
1819050,4197919,8107892,12640858,14471465,15632458,18304103,19616714,22370543,25674127,
25956377,34850339,44677235,46498850,4972409

the indices are the number of 1s present in the binary number 3 in binary will be 11
7 in binary will be 111
now if we read any file in a number of bits equal to our largest index (57,885,161)
and we divide it by the maximum index we would obtain a 1 or a 0 with a remainder that will go from a maximum of 57,885,161 to 0
now we take the remainder of the division and divide it by the previous index
then arriving at the first index we would have a series of results and a remainder
by redoing the opposite operations, that is, multiplying the result of the division by the maximum index, 
adding it to the result of the previous division and adding it to the final remainder, we obtain the original file
looking at the numbers we will never get a number greater than 10.
therefore we would have compressed 57,885,161 bits into 49 numbers less than 10 plus a remainder considering that the last number is a 3 will be
maximum 2.
​considering that an operand is always made from a series 1 in binary the operations can be optimized
our results can be stored in 4 bits because they are decimal digits and we are left with unused combinations that could be used for parity or other special functions
we would have compressed 57,885,161 bits into 4*48 bits therefore 192 bits
I can't develop the program and I'm looking for help
my idea is based on the value expressed by the files in binary a series of 1 and 0 in binary can be interpreted as 
a number expressed in powers of two the first bit will be 1 if set to 1 the second 2 the third 4 and so on.
-My idea is based on the value expressed by the files in binary a series of 1s and 0s in binary can be interpreted as a
number expressed in powers of two the first bit will be 1 if set to 1 the second 2 the third 4 and so on.
taking a number of bits equal to 57,885,162 and dividing it by the Mersenne index 57,885,161 I obtain a remainder and a result.
Continuing to divide by the previous Mersenne indices I always obtain remainders and results up to the lowest index equal
to 3 in decimal and a remainder less than 3. When reconstructing the original file I will simply do so
the inverse operation i.e. result index n for index n+ index n-1 for index n-1 until reaching
lowest index. at the end I will add the rest and I will have my original file.
Since the Mersenne numbers are only made up of a series of 1s in binary, this simulifies the calculations by reducing them to shit on the right and shift on the left

Diego Di Battista

descrizione sommaria di una agoritmo di compressione basata sui un sotto insieme di numeri primi :


un qualsiasi files del pc può essere rappresentato in decimale. Con un file di soli 4 bit avrà un valore che va da 0 a 15.
ora consideriamo i Numeri primi di Mersenne https://it.wikipedia.org/wiki/Numero_primo_di_Mersenne
in particolare i loro indici :

2,3,4,8,10,12,19,37,54,65,77,314,366,770,1327,1373,1937,2561,2663,5834,5985,6751,
12003,13066,13973,26790,51924,66530,79502,130100,455663,517430,757263,841842,1791864,
1819050,4197919,8107892,12640858,14471465,15632458,18304103,19616714,22370543,25674127,
25956377,34850339,44677235,46498850,4972409

gli indici sono il numero di 1 presentenel numero binario 3 in binario sara 11
7 in binario sara 111
ora se leggiamo un qualsiasi file in un numero di bit pari al nostro indice più grosso (57.885.161)
e lo dividiamo per l'indice massimo otterremmo un 1 o uno 0 con un resto che andra da un massimo di 57,885,161 a 0
ora prendiamo il resto della divisione e lo dividiamo per l'indice precedente
arrivando poi al primo indice avremmo una serie di risultati ed un resto 
rifacendo le operzioni contrarie cioè moltiplicando il risultato della divisione per il massimo indice sommadolo 
al risulatato  della divisisione precedente e sommnadolo al resto finale riotteniamo il file originale 
quindi avremmo compresso 57.885.161 bit in 49 numeri minori di 10 piu un resto considerando che l'ultimo numero è un 3 sarà 
massimo 2.
considerando che un operando è sempre fatto da una serie 1 in binario le operazioni possono essere ottimizzate
i nostri risulatati possono essere memorizzati in 4 bit perchè sono cifre decimali e ci rimangono combinazioni non usare che potrebbero essere usate per parità o altre funzioni speciali 
noi avremmo compresso 57.885.161 bit in 4*48 bit quindi 192 bit
non riesco a sviluppare il programma e cerco aiuto.
-La mia idea si basa sul valore spresso dai file in binario una serie di 1 e 0 in binario possono essere interpretati come un 
numero espresso in potenze di due il primo bit varra 1 se posto a 1 il secondo 2 il terzo 4 e cosi via.
prendendo un numero di bit pari a 57.885.162  e dividendolo per l'indice di Mersenne 57.885.161 otterro un resto ed un risultato.
Continuando a dividre per gli indici di Mersenne precedenti otterro sempre resti e risuòltati fino al indice più basso pari 
a 3 in decimale ed un resto minore di 3. Nella ricostruzione del file originale faro semplicemente 
l'operzione inversa cioe risultato indice n per indice n+  indice n-1 per indice n-1 fino ad arrivare al 
indice più basso .alla fine sommerò il resto ed avro il mio file originale. 
Essendo i numeri di  Mersenne formati solo da una serie di 1 in binario questo semolifica i calcoli riducendoli a shit a destra  e shift a sinistra
Diego Di Battista

