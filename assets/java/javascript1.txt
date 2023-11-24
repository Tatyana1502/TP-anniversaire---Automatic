const joursSemaine = ["dimanche", "lundi", "mardi", "mercredi", "jeudi", "vendredi", "samedi"]
const now = new Date();
let option = {
  year: 'numeric',
  month: 'numeric',
  day: 'numeric',
  weekday: 'long',
 };

console.log("Aujourdhui :" , now.toLocaleString(option));
const DateAujourdhui = now.getDate();
const MoisAujourdhui = now.getMonth();
const YearAujourdhui = now.getFullYear();
const DayAujourdhui = now.getDay();
let data = document.querySelector("#data");
let mois = document.querySelector("#mois");

console.log("DateAujourdhui: ", DateAujourdhui);
console.log("MoisAujourdhui: ", MoisAujourdhui+1);
console.log("YearAujourdhui: ", YearAujourdhui);
console.log("DayAujourdhui: ", DayAujourdhui);
console.log("dataClient: ", data.value);
console.log("moisClient: ", mois.value);

document.querySelector("button").addEventListener("click", () => {
    console.log("moi aujourd'hui :", MoisAujourdhui);
    if (mois.value == MoisAujourdhui+1) {
        if (data.value > DateAujourdhui) {
            let novelleDate = data.value - DateAujourdhui;
            console.log("novelleDate: ", novelleDate);
            console.log("date nouvelle :", novelleDate.getDay());
            console.log("Jour de la semaine : ", joursSemaine[dataNovelle.getDay()]);
            document.querySelector(".ecran").innerText = resultat.toFixed(0) + " jours" + " à " + joursSemaine[dataNovelle.getDay()];
        }
        else { 
            let dataNovelle = new Date(YearAujourdhui+1, mois.value-1, data.value,  DayAujourdhui);
            console.log("date nouvelle :", dataNovelle.getDay());
            console.log("Jour de la semaine : ", joursSemaine[dataNovelle.getDay()]);
            console.log("dataClient: ", data.value);
            console.log("moisClient: ", mois.value);  
            console.log("YearClient: ", YearAujourdhui+1); 
            console.log("Client :" , now.toLocaleString(dataNovelle));
            let resultData = (dataNovelle - now)/86400000;
            console.log("Client :" , resultData);
            let resultat = Number(resultData);
            console.log("Client :" , resultat);
            document.querySelector(".ecran").innerText = resultat.toFixed(0) + " jours" + " à " + joursSemaine[dataNovelle.getDay()] ;

        }
    }
    if (mois.value > MoisAujourdhui+1) {
        let dataNovelle = new Date(YearAujourdhui, mois.value-1, data.value,  DayAujourdhui);
        console.log("date nouvelle :", dataNovelle.getDay());
        console.log("Jour de la semaine : ", joursSemaine[dataNovelle.getDay()]);
        console.log("dataClientFull: ", dataNovelle);
        console.log("dataClient: ", data.value);
        console.log("moisClient: ", mois.value);  
        console.log("YearClient: ", YearAujourdhui); 
        let resultData = (dataNovelle - now)/86400000;
        console.log("Client :" , resultData);
        let resultat = Number(resultData);
        console.log("Client :" , resultat);
        document.querySelector(".ecran").innerText = resultat.toFixed(0) + " jours" + " à " + joursSemaine[dataNovelle.getDay()] ;
   }
    if (mois.value < MoisAujourdhui+1) {
         let dataNovelle = new Date(YearAujourdhui+1, mois.value-1, data.value,  DayAujourdhui);
         console.log("date nouvelle :", dataNovelle.getDay());
         console.log("Jour de la semaine : ", joursSemaine[dataNovelle.getDay()]);
         console.log("dataClientFull: ", dataNovelle);
         console.log("dataClient: ", data.value);
         console.log("moisClient: ", mois.value);  
         console.log("YearClient: ", YearAujourdhui+1); 
         let resultData = (dataNovelle - now)/86400000;
         console.log("Client :" , resultData);
         let resultat = Number(resultData);
         console.log("Client :" , resultat);
         document.querySelector(".ecran").innerText = resultat.toFixed(0) + " jours" + " à " + joursSemaine[dataNovelle.getDay()] ;
    }
})

