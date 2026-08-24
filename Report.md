## Val av TOTP i stället för SMS

Jag valde TOTP eftersom koderna skapas lokalt i en autentiseringsapp och därför inte skickas via mobilnätet. SMS-koder kan utsättas för exempelvis SIM-kapning, avlyssning eller omdirigering, vilket gör dem mer sårbara. Vad jag förstår så skyddar TOTP däremot inte helt mot avancerade phishing-proxyer som kan fånga upp och använda en kod direkt innan den hinner gå ut. Trots detta är TOTP ett bättre förstahandsval i den här applikationen, dock hade SMS fortfarande varit säkrare än att inte använda någon andra faktor alls.

## Antal inloggningsförsök och låsningstid

Jag valde att låsa kontot efter fem misslyckade inloggningsförsök eftersom det begränsar möjligheten att testa många lösenord genom en brute force-attack. En låsningstid på 15 minuter ger ett tydligt skydd samtidigt som en riktig användare inte behöver vänta orimligt länge om lösenordet skrivs fel flera gånger. En alltför hård eller långvarig låsning kan utnyttjas av en angripare för att medvetet stänga ute riktiga användare. Inställningarna är därför en avvägning mellan säkerhet och tillgänglighet.

