
1.-leap
Definición de la función:

La función isLeap toma un parámetro year que es un número.
Condiciones para un año bisiesto:

La función devuelve true si el año es divisible por 400.
Si no, la función devuelve true si el año es divisible por 4 pero no por 100.
Si ninguna de estas condiciones se cumple, la función devuelve false.
Retorno del resultado:

El valor de retorno de la función es un booleano (true o false), que indica si el año es bisiesto o no.


export function isLeap(year: number): boolean {
  return year % 400 === 0 || (year % 100 !== 0 && year % 4 === 0)
}
 
 
 2.-
 RNA Transcription
 Mapa de Transcripción: Crea un mapa que relaciona cada nucleótido de ADN con su correspondiente nucleótido de ARN.
Validación: Verifica que la cadena de ADN solo contenga caracteres válidos (A, C, G, T).
Transcripción: Reemplaza cada nucleótido de ADN con su equivalente de ARN utilizando el mapa de transcripción.

 interface M {
    [key: string]: string
}
const Map: M = { 
    G: 'C',
    C: 'G',
    T: 'A',
    A: 'U'
}

export function toRna(dna: string): string {
    if(/[^ACGT]/.test(dna)) {
        throw 'Invalid input DNA.'
    }

    return dna.replace(/[ATCG]/g, m => Map[m])
}