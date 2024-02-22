Tema #1 APD
Desenarea paralela de curbe contur folosind algoritmul Marching Squares

Nume: Girnita Alexandra-Claudia
Grupa: 332CC

	Programul implementeaza marching squares algorithm paralelizat utilizand threaduri pentru imbunatatirea performantei.
	Fiecare thread apeleaza threadFunction si primeste ca argument o structura de date pthread_args. Toate threadurile primesc pointeri catre aceleasi date: grid, scaled_image pentru a asigura distribuirea datelor intre toate hreadurile.
	Programul asigura paralelizarea in metoda threadFunction echivalenta a metodelor rescale_image,sample_grid si march din varianta secventiala.
	Pentru redimensionarea imaginii se seteaza un flag in main care este transmis prin intermediul structurii si seunt impartite fiecarui thread un numar de linii din imaginea initiala, astfel imbunatatind considerabil timpii de rulare pentru testele 6 si 7.
	Construirea matricii grid este de asemenea paralelizata, fiecare thread calculeaza valorile pentru un numar de randuri din imagienea redimensionata, dupa care se cauta conturul care se potriveste si se actualizeaza imaginea.
	
