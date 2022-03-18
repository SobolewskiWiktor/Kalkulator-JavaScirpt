const btns = document.querySelectorAll('.number')
const btns_two = document.querySelectorAll('.number_zero')
const btns_three = document.querySelectorAll('.option')
const result = document.querySelector('#result')
const table = [] 

let L1 = 0
let L2 = 0 
let liczba_pierwsza = 0
let liczba_druga = 0
let suma = 0 
let swit = "false"
let ile_jest = 0 
let typ = "+"

btns.forEach (btn => 
    btn.addEventListener('click', (e=>{

         let click = e.target;
         let temp = 0
         let temp2 = 0
         let zmienna = 1

         table.push(btn.value)

         if (swit == "false")
         {
          liczba_pierwsza = liczba_pierwsza + 1
          ile_jest = ile_jest + 1
         }
         else if (swit == "true")
         {
          liczba_druga = liczba_druga + 1
          ile_jest = ile_jest + 1
         }
         
         if (swit == "false")
         {
            for(let i = liczba_pierwsza-1; i>=0; i--)
            {   
                temp = parseInt(table[i])*zmienna
                zmienna = zmienna * 10
                temp2 = temp2 + temp
                console.log("wykonije obliczanie 1 liczby")
                console.log(L1)

            }
            result.innerHTML = "<h1>"+temp2+"</h1>"
         }
         else if (swit == "true")
         {
            for(let i = liczba_druga-1 + liczba_pierwsza; i>=liczba_pierwsza; i--)
            {
                temp = parseInt(table[i])*zmienna
                zmienna = zmienna * 10
                temp2 = temp2 + temp
    
            }
            result.innerHTML = "<h1>"+temp2+"</h1>"
         }

         console.log("l pierwsza: "+liczba_pierwsza)
         console.log("l druga: "+liczba_druga)
    })))

    
btns_two.forEach (btn => 
        btn.addEventListener('click', (e=>{
            let click = e.target;
            let temp = 0
            let temp2 = 0
            let zmienna = 1
   
            table.push(btn.value)
   
            if (swit == "false")
            {
             liczba_pierwsza = liczba_pierwsza + 1
             ile_jest = ile_jest + 1
            }
            else if (swit == "true")
            {
             liczba_druga = liczba_druga + 1
             ile_jest = ile_jest + 1
            }
            
            if (swit == "false")
            {
               for(let i = liczba_pierwsza-1; i>=0; i--)
               {   
                   temp = parseInt(table[i])*zmienna
                   zmienna = zmienna * 10
                   temp2 = temp2 + temp
                   console.log("wykonije obliczanie 1 liczby")
                   console.log(L1)
   
               }
               result.innerHTML = "<h1>"+temp2+"</h1>"
            }
            else if (swit == "true")
            {
               for(let i = liczba_druga-1 + liczba_pierwsza; i>=liczba_pierwsza; i--)
               {
                   temp = parseInt(table[i])*zmienna
                   zmienna = zmienna * 10
                   temp2 = temp2 + temp
       
               }
               result.innerHTML = "<h1>"+temp2+"</h1>"
            }
   
            console.log("l pierwsza: "+liczba_pierwsza)
            console.log("l druga: "+liczba_druga)
    
        })))
btns_three.forEach (btn => 
            btn.addEventListener('click', (e=>{

                let wynik
                
                 
                let click = e.target;
                let  value_option = click.textContent

                console.log(value_option)

                if(value_option == "AC")
                {
                    for(let i=0; i<=ile_jest; i++)
                    {
                        table.pop()
                    }
                    ile_jest = 0 
                    liczba_pierwsza = 0
                    liczba_druga = 0 
                    swit = "false"
                    result.innerHTML = "<h1>0</h1>"
                    wynik = 0; 
                    L1 = 0 
                    L2 = 0 
                }
                if (value_option == "+")
                {
                  swit = "true"
                  typ = "+"
                  zmiana_na_liczbe()
                  console.log("jestem w dodawaniu")
                }
                if (value_option == "-")
                {
                  swit = "true"
                  typ = "-"
                  zmiana_na_liczbe()
                }
                if (value_option == "*")
                {
                  swit = "true"
                  typ = "*"
                  zmiana_na_liczbe()
                }
                if (value_option == "/")
                {
                  swit = "true"
                  typ = "/"
                  zmiana_na_liczbe()
                }
                if (value_option == "=")
                {
                  swit = "true"
                  zmiana_na_liczbe()
                  if(typ == "+")
                  {
                      console.log("Jestem w + po kliknieciu = ")
                   wynik = L1 + L2
                   result.innerHTML = "<h1>"+wynik+"</h1>" 
                  }
                  else if (typ == "-")
                  {
                    wynik = L1 - L2
                    result.innerHTML = "<h1>"+wynik+"</h1>"
                  }
                  else if (typ == "*")
                  {
                    wynik = L1 * L2
                    result.innerHTML = "<h1>"+wynik+"</h1>"
                }
                  else if (typ == "/")
                  {
                      wynik = L1/L2
                      result.innerHTML = "<h1>"+wynik+"</h1>"
                  }
                }
            })))

function zmiana_na_liczbe()
{
    let temp = 1;
    let zmienna = 1; 
    if (liczba_druga == 0)
    {
        for(let i = liczba_pierwsza-1; i>=0; i--)
        {
            temp = parseInt(table[i])*zmienna
            zmienna = zmienna * 10
            L1 = L1 + temp
            console.log("wykonije obliczanie 1 liczby")
            console.log(L1)

        }
        
    }
    else
    {
        console.log("Jestem w 2 if ")
        for(let i = liczba_druga-1 + liczba_pierwsza; i>=liczba_pierwsza; i--)
        {
            temp = parseInt(table[i])*zmienna
            zmienna = zmienna * 10
            L2 = L2 + temp
            console.log("Wynokuje obliczanie 2 liczby")
            console.log(L2)

        }
    }
}
