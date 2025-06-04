**# RAPPORPOLYUFYP**

Tristan WONG's Final Year Project about RAPPOR algorithm in the Hong Kong Polytechnic University

```
The following source code is developed by Tristan WONG based on RAPPOR algorithm in 2022

With JavaScript, capture data value on the console of a browser：

//true return
document.getElementsByName('q-5-dW2n')
    .forEach(radio => {
        if (radio.checked){
            x = radio.value;
            console.log(x);
        }
})


//false return
document.getElementsByName('q-5-dW2n')
    .forEach(radio => {
        if (!(radio.checked)){
            y = radio.value;
            console.log(y);
        }
})
```

>How to capture value with JavaScript: https://www.youtube.com/watch?v=cSuEAD-Tnd4

```
//divide a string in Tencent Survey into a number of independent strings
const at1 = x.split("-")
const at2 = y.split("-")

//transform the string value to a number
num1 = parseInt(at1[1])
num2 =parseInt(at2[1])

//Generate a random number with the typed value, i.e. the number between num1 and num2:
var mrpr = MemoizingRandom.prototype.randint(num1, num2)


//how to use JS to select a value automatically:
var labels = document.getElementsByTagName('label'); 
for (var i = 0; i < labels.length; ++i) { 
    if (labels[i].getAttribute('for').includes(MemoizingRandom.prototype.randint(num1, num2))) { 
        labels[i].click(); 
    }
}
```

>To help familiarize myself with the RAPPOR JS implementation:

>Counts file (8*29 = 232 records)
>1st col -> no. of reports
>remaining cols (28) -> no. of times the bit is set
>Required. This file must have as many rows as cohorts. The first column contains the number of reports in the cohort. 
>The remaining k columns specify the number of times the corresponding bit was set in all reports (in the corresponding cohort).
>This file cannot have a CSV header line.

>Map file
>1st col -> strings
>remaining cols -> which bit each string is hashed
>cohorts -> 64 (given by the alg., not by the simulation website)
>Required. The first column contains candidate strings. The remaining columns show which bit each string is hashed to within each cohort.
>Indices are specified in the extended format, starting with index 1 (not 0!). 
>Because we do not specify a cohort in the map file, indices must be adjusted in the following way. 
>For example, if bits i and j are set in cohort 2, then their corresponding indices are i + k and j + k in the map file. 
>The number of columns is equal to (h * m). This file cannot have a CSV header line.
