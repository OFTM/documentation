[yuml.me Diagram](https://www.yuml.me/ed7fc722.png)

```
[fencer|fid:int(pkey);forename:string;surname:string;birthdate:date;sex:sex(fs);ids:ids(fs);weapon:weapon(fs);ageclass:ageclass(fs)]n-1[sex|sid:int(pkey);name:string],
[fencer]n-m[tournament|tid:int(pkey);name:string;type:ttype(fs);ageclass:ageclass(fs);sex:sex(fs);fencer:fencer(fs)],[sex]1-n[tournament],
[tournament]1-1[leaderboard|lid:int(pkey);tournamet:tournament(fs);fencer:fencer(fs);hitsrecv:int;hitsdealt:int],[fencer]n-m[leaderboard],[tournament]1-n[combats|cid:int(pkey);fencer1:fencer(fs);fencer2:fencer(fs);tournament:tournament(fs);referee:referee(fs)],
[combats]1-n[referee|rid:int(pkey);forename:string;surename:string],
```
