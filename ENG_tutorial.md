## Hvor langt væk er lynet?
Med denne kode kan du regne ud hvor langt ISS har fløjet

## Kodning af knap A
Når knap A bliver trykket ind, skal @boardname@ starte en tidsmåling. Opret variablen `||variables:startTid||`

## Kodning af knap A 
Træk blokken `||variables: sæt startTid til 0||` ind i blokken `||input.knap A||` 

```blocks
input.onButtonPressed(Button.A, function () {
    startTid = (0)
})
```

## Kodning af knap A
Sæt blokken `||input.køretid (ms)||` ind i `||variables: sæt startTid til 0||`. 

```blocks
input.onButtonPressed(Button.A, function () {
    startTid = input.runningTime()
})
```

## Kodning af knap A
Træk blokken `||basic.vis LED'er||` ind under under `||variables: sæt||`

```blocks
input.onButtonPressed(Button.A, function () {
    startTid = input.runningTime()
    basic.showLeds(`
    . . . . .
    . . . . .
    . . . . .
    . . . . .
    . . . . .
    `)
})
```

## Kodning af knap A
Tegn et symbol for at tidsmåling er startet

```blocks
input.onButtonPressed(Button.A, function () {
    startTid = input.runningTime()
    basic.showLeds(`
    . . . . .
    . . # . .
    . . # . .
    . . # . .
    . . . . .
    `)
})
```

## Kodning af knap B
Find en blok til `||input.knap B||`

```blocks
input.onButtonPressed(Button.B, function () {
})
``` 

## Kodning af knap B 
Opret variablen `||variables:slutTid||`

## Kodning af knap B 
Træk blokken `||variables: sæt slutTid til 0||` ind i blokken knap B

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = 0
})
```

## Kodning af knap B 
Træk blokken `||input: køretid (ms)||` ind i blokken `||variables: sæt slutTid til 0||`

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
})
```

## Kodning af knap B 
Opret variablen `||variables:beregnetTid||`

## Kodning af knap B 
Træk `||variables: sæt beregnetTid til 0||` ind under `||variables: sæt slutTid til køretid (ms)||`

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = 0
})
```

## Kodning af knap B 
Træk `||math:0 - 0||` ind i blokken `||variables: sæt beregnetTid til 0||`. 

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    måltTid = 0 - 0
})
```

## Kodning af knap B  
Træk `||variables: slutTid||` ind på det første 0's plads

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    måltTid = slutTid - 0
})
```

## Kodning af knap B  
Træk `||variables: startTid||` ind på det andet 0's plads

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    måltTid = slutTid - startTid
})
```

## Kodning af knap B 
@boardname@ måler tiden i milisekunder. Vi skal måle i sekunder. 
Derfor skal beregnetTid divideres med 1000. Indsæt blokken `||variables: sæt beregnetTid til 0||`.

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid = 0
})
```

## Kodning af knap B 
Indsæt `||math:0 / 0||` i `||variables: sæt beregnetTid til 0||`

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid = 0 / 0
})
```

## Kodning af knap B 
Indsæt `||variables: beregnetTid||` på første 0's plads

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid = beregnetTid / 0
})
```

## Kodning af knap B 
Skriv 1000 på andet 0's plads

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid = beregnetTid / 1000
})
```

## Kodning af knap B 
Opret variablen `||variables:afstand||`

## Kodning af knap B  
Indsæt blokken `||variables: sæt afstand til 0||`

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    måltTid = slutTid - startTid
    måltTid = måltTid / 1000
    afstand = 0
})
```

## Kodning af knap B  
Indsæt blokken `||math:0 * 0||` i `||variables: sæt afstand til 0||`

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid = måltTid / 1000
    afstand = 0 * 0
})
```

## Kodning af knap B  
Indsæt blokken `||variables: beregnetTid||` på første 0's plads 

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 0
})
```

## Kodning af knap B  
Skriv 7.77 på andet 0's plads. 7.77 er hastigheden af ISS målt i km / s. Bemærk brug punktum i stedet for komma.  

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 7.77
})
```

## Kodning af knap B  
Indsæt blokken `||basic.vis nummer||`
```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 7.77
})
```

## Kodning af knap B  
Indsæt variablen `||variables: afstand ||` i blokken `||basic.vis nummer||`

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 7.77
    basic.showNumber(afstand)
    basic.showString(" km")})
```


## Tillykke!
Nu er du færdig med din kode. Du kan nu afprøve om du kan: 
* Let: Kan du ændre pausens længde?
* Let: Kan du ændre så du skriver afstanden i kilometer i stedet for meter? 
* Mellem: Kan du gøre koden kortere? 
* Mellem: Kan du udvide koden, så den animerer at lynet slår ned?
* SVÆR: Bruge 3 eller flere @boardname@ med programmet til at bestemme positionen til en ven der klapper langt væk?
* SVÆR: Finde på noget andet at bruge programmet til?

```template
input.onButtonPressed(Button.A, function () {
}
```