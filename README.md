# Algorithme-Convert-Number-into-Romanian-Number

`

function solution(number){
  
    // Array qui prend en objet les valeurs et les symboles correspondant:
    const romanNumerals = [
        {value: 1000, symbol: 'M'},
        {value: 900, symbol: 'CM'},
        {value: 500, symbol: 'D'},
        {value: 400, symbol: 'CD'},
        {value: 100, symbol: 'C'},
        {value: 90, symbol: 'XC'},
        {value: 50, symbol: 'L'},
        {value: 40, symbol: 'XL'},
        {value: 10, symbol: 'X'},
        {value: 9, symbol: 'IX'},
        {value: 5, symbol: 'V'},
        {value: 4, symbol: 'IV'},
        {value: 1, symbol: 'I'},
    ]
    

    let result = '';
    

    // 1er Boucle qui parcours tout les objets et les valeurs dans l'array
    for(let i = 0; i< romanNumerals.length; i++){
      
        // 2eme Bouble qui parcours chaque valeur
        // Si la valeur est inférieur au nombre 
        // Ajoute le symbol correspond au nombre dans la variable result
        // Soustrait la valeur au nombre
      while(romanNumerals[i].value <= number){
        
        result += romanNumerals[i].symbol;
        
        number -= romanNumerals[i].value;
        
      }
      
    }
    
    return result;
}

console.log(solution(1441));

`

La logique pour résoudre cet algorithme est de soustraire le plus grand symbole romain correspondant au nombre quelconque.
Par exemple : 1990 => 1000: M + 900: CM + 90: XC;
