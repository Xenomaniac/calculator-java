READ ME

1. Broj linija koda (LOC)
Ukupno linija koda u projektu (bez praznih linija i komentara): 148
Ukupno linija (bez praznih linija i komentara): 148, Dobio sam broj preko powershell-a i komande:
Get-ChildItem -Recurse -Include *.java | Get-Content | Where-Object { $_.Trim().Length -gt 0 -and -not ($_.Trim().StartsWith("//")) } | Measure-Object -Line)

(Ovaj broj je dobijen pomoću PowerShell komande za brojanje linija u .java fajlovima.)
2. Izveštaj sa PMD statičke analize koda
Fajl	                Linija	        Zapazanje
Calculator.java	        34	          Ponovno dodeljivanje vrednosti parametrima AvoiReassigningParameters
Calculator.java	        53	          Umesto for petlja bolje bi isla foreach petlja.
Calucaltor.java	        55	          U poredjenju stavljati literale na prvo mesto (LiteralsFirstInComparasions)
Calculator.java	        57	          U poredjenju stavljati literale na prvo mesto (LiteralsFirstInComparasions)
Start.java	            8	            Nije preporucljivo da se koristi System.out/err za ispis
Start.java 	            15	          U poredjenju stavljati literale na prvo mesto (LiteralsFirstInComparasions)

3. Zaključak
Ukupno, projekat sadrži 148 linija aktivnog koda.

PMD je identifikovao nekoliko potencijalnih problema u kodu, kao što su ponovna dodela vrednosti parametrima, nepotrebne for petlje koje mogu biti pojednostavljene u foreach petlje, kao i poboljšanja u pisanju uslova poređenja Stringova.

Korišćenje System.out/err nije preporučljivo u produkciji i trebalo bi ga zameniti odgovarajućim loggerima ili drugim mehanizmima.

