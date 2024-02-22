# Tema #1 APD - Desenarea paralelă de curbe contur folosind algoritmul Marching Squares

## Student: Girnița Alexandra-Claudia
## Grupa: 332CC

### Descriere
Acest proiect implementează algoritmul **Marching Squares** într-o manieră paralelizată, folosind thread-uri pentru a îmbunătăți performanța. Scopul principal este de a desena curbe contur într-un mod eficient, profitând de puterea de procesare paralelă.

### Implementare
- **Paralelizare**: Fiecare thread execută `threadFunction`, primind ca argument o structură de date `pthread_args`. Toate thread-urile accesează aceleași date (`grid`, `scaled_image`) pentru a asigura distribuirea eficientă a informațiilor.
- **Rescalarea imaginii**: Se utilizează un flag în funcția `main` care este transmis thread-urilor prin structura menționată anterior. Astfel, fiecărui thread îi sunt alocate un număr de linii din imaginea inițială, optimizând timpii de execuție.
- **Construirea grid-ului**: Procesul este, de asemenea, paralelizat, fiecare thread calculând valorile pentru un set de rânduri din imaginea redimensionată. După calcularea grid-ului, se identifică și se actualizează contururile corespunzătoare în imagine.
