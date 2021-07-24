# Quick-Tip-PowerShell-Remove-Accents-From-String

Powershell line to remove accents (known as Diacritics) from a string

Special thanks to [François-Xavier Cat aka LazyAdmin](https://lazywinadmin.com/about.html), the original article with this info is [here](https://lazywinadmin.com/2015/05/powershell-remove-diacritics-accents.html)

```powershell
$StringWithAccents = "J'ai préparé mon sapin de Noël avec Gwénaëlle"

[Text.Encoding]::ASCII.GetString([Text.Encoding]::GetEncoding("Cyrillic").GetBytes($StringWithAccents))

```

The output :

```output
J'ai prepare mon sapin de Noel avec Gwenaelle
```
