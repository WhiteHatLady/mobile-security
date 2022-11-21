[TOC]

# Quiz dla studentów - pytania


## Opracowała Magdalena Powałowska - Lecturer

1. Jak się nazywa czysty Android wyprodukowany przez Google a nie społeczność? 

<details>
<summary>Zobacz odpowiedź</summary>
ODP.  AOSP (Android Open Source Project)
</details>

2. Partycja recovery służy tylko do przywrócenia czegoś?  Prawada czy Fałsz?. Uzasadnij.

<details><summary>Zobacz odpowiedź</summary>
ODP.  Fałsz. Partycja jest alternatywą gdy system się wysypie, a zarazem że partycja ta  jest również zapasową partycją rozruchowa.
</details>

3. Po co nam pliki z rozszerzeniem .dex?  Gdzie są wykorzystywane? Czy dotyczą Androida czy IOS? 

<details><summary>Zobacz odpowiedź</summary>

ODP.  Przedroskiem przed .dex zazwczaj jest classes. Pliki te wykorzystywane są przez maszynę wirtualną DALVIK lub ART w telefonie Androida. 
</details>

4.  Narzędzie które służy do przekonwertowania pliku .dex do jara to: 
-  d2j-jar2dex
- d2j
- dex2jar
- d2j-dex2jar

<details><summary>Zobacz odpowiedź</summary>
ODP. d2j-dex2jar
</details>

5.  Michał wydaję polecenie `apktool d twitter.ipa` i aplikacja nie chce mu się zdekompilować. Dodaje więc slagę `-f` czyli `force` `apktool d twitter.ipa -f` i nadal się nie dekompiluje.  Gdzie Michał popełnił błąd? Odpowiedź uzasadnij. Napisz komendę którą Michał powninien napisać, by poprawnie zdekompilować apllikację. 


<details><summary>Zobacz odpowiedź</summary>
ODP. Michał użył rozszerzenia .ipa, które jest roszerzeniem dla aplikacji z systemem IOS.  Apktool zdekompiluje tylko aplikacje z rozszerzeniem .apk. Michał powinien pobrać apkę przeznaczoną na Androida rozszerzeniem .apk  a następnie wydać polecenie `apktool d twitter.apk`.
</details>

6. Jakie są podstawowe 4 wektory ataków na Andrioda? Omów każdy z nich w jednym zdaniu. 

<details><summary>Zobacz odpowiedź</summary>
ODP. Activities, Services, Broadcat recivers, Content Providers
</details>

7.  Jakie mamy dwie maszyny wirtualne Androida. Która z maszyn jest szybsza i dlaczego? Która z nich  jest obecnie częściej używana?

<details><summary>Zobacz odpowiedź</summary>
ODP. Mamy dwie maszyny Dalvik i ART.  ART jest szybszy ponieważ,  ma mniejsze zuzycie procesora, pamięci oraz baterii telefonu (z powodu AOT)
</details>

8. Która z maszyn wirtualnych na Androida wykorzystuje kompilacje JIT a która AOT?

<details><summary>Zobacz odpowiedź</summary>
Odp. Dalvik - Just in Time. Android Runtime (ART) - Ahead of Time (AOT)
</details>
 
9.   Mamy kilka eventów cyklu życia Activities. Przy jakim cyklu aktivities aplikacja staje się klikalna? 

<details><summary>Zobacz odpowiedź</summary>
ODP. OnResume 
</details>

10. Wymień eventy cyklu życia aplikacji oraz opisz co dzieje sie podczas każdego eventu. 

<details><summary>Zobacz odpowiedź</summary>
ODP. 
Oncreate - aplikacja wstaje i jest niewidoczna. W tym momencie są przypisywane pola do zmiennych, żeby je obsługiwać 
OnStart - aplikacja jest widoczna, ale nie jest klikalna
OnResume - dopiero wtedy aplikacja jest klikalna
OnPause  - kiedy dostaje powiadomienie i zjeżdżam w dół np. górną belkę, ale pod spodem nadal widzę moją aplikację, to wtedy jest ten event 
onStop - w momencie gdy dostaliśmy np. smsa i przenosimy się do pisania wiadomości, wówczas nie widzimy poprzedniej aplikacji 
onDestroy - wówczas gdy zamykamy aplikację.
</details>

11. Partycja /boot to pratycja rozruchowa, która zawiera tylko jądro. Prawda czy Falsz? Odpowiedź uzasadnij.

<details><summary>Zobacz odpowiedź</summary>
ODP. Partycja /boot zawiera jądro oraz RAM disc. 
</details>

12.  Językami programowania ktore obowiązują w Androidzie jest Java i SWIFT. Prawda czy fałsz? 

<details><summary>Zobacz odpowiedź</summary>
ODP. Fałsz. Językami programowania w Androidzie są Java i Kotlin. 
</details>
13. Android Package to jest rozszerzenie skrótu APK. Prawda czy fałsz? 
	
<details><summary>Zobacz odpowiedź</summary>
ODP.  Fałsz, Android Package Kit.
</details>

14. Najważniejszym plikiem konfiguracyjnym w Androidzie jest AndroidManifest.json. Prawda Czy fałsz? 
<details><summary>Zobacz odpowiedź</summary>
Odp.  Fałsz. Nie zgadza się rozszerzenie. Powinno być xml.
</details>

15.  Co muszę zrobić, żeby mój telefon miał opcję zarządzania przez ADB? 

<details><summary>Zobacz odpowiedź</summary>
Odp. 1. Trzeba wlączyć opcje deweloperskie , tzn. kliknąć 7 razy Build Number. 2. Następnie wejść w opcje deweloperskie i kliknąć Develoeper Options i włączamy debugowanie przy pomocy USB.
</details>

16. Czy aplikacje na Androida są łatwe do Reverse Engineeringu? Czy aplikacje na IOS są łatwe do Reverse Engineeringu? Odpowiedź uzasadnij. 
<details><summary>Zobacz odpowiedź</summary>
ODP.  Na Androida - łatwe. Mamy dużo narzędzi, możemy zobaczyć logike aplikacji.  Na IOS jest bardzo trudno, ponieważ nie można łatwo odwrócić języka SWIFT oraz Objective-C do języka czytelnego przez człowieka. 
</details>

17.  Najlepszą metodą Patchowania aplkacji jest usunięcie kodu lub napisanie swojego fragmentu kodu. Prawda czy fałsz? 
<details><summary>Zobacz odpowiedź</summary>
ODP. Prawda. Patchowanie aplikacji można zrobić kilkoma sposobami. Można np. zmienić stałe wartości w kodzie plików .smali. Można również usunąć kod - trudniejsze, ponieważ trzeba zachować pewną strukturę.  Najtrudniejszą opcją patchowania jest jeśli musimy dopisać trochę kodu. 
</details>

18.  Michał wział aplikację, którą uprzednio zainstalował na telefonie, a następnie wykonał następujące kroki: zdekompilował ją, zmienił logikę w pliku .smali, skompilował ją ponownie, podpisał nowo wygenerowanym kluczem, sprawdził zipalignem. Michał probuje zainstalować aplikację ponownie, ale cały czas dostaje komunikat błędu, że nie może. O czym zapomniał Michał? 
<details><summary>Zobacz odpowiedź</summary>
Odp. Michał zapomniał odinstalować  starą aplikację. Zatem nie działa to, ponieważ stara ma inny klucz. Nie można więc nadpisać poprzedniej aplikacji. 
</details>

19.  Czy jest wymagane sprawdzenie zgodności zipalignem po jej przebudowaniu? 
<details><summary>Zobacz odpowiedź</summary>
Odp. Nie jest wymagane, ale jest dobrą praktyką, ponieważ nigdy nie wiemy, czy podczas przebudowywania nie zostało coś zepsute. 
</details>

20. Frida to potężne narzędzie które w sposób dynamiczny wstrzykuje JavaScript do działającego procesu. Prawda czy Fałsz? 
<details><summary>Zobacz odpowiedź</summary>
Odp. Prawda.Frida działa podczas włączonej aplikacji. 
</details>

21. SSL pinning jest mechanizmem chroniącym przed atakami MITM. Prawda czy fałsz? 
<details><summary>Zobacz odpowiedź</summary>
Odp. Prawda. Mechanizm ten weryfikuje, czy certyfikat używany przez użytkownika jest poprawny. Jeśli nie jest, to nie będą wychodzić żadne requesty do serwera. 
</details>

22. Michał używa komendy `adb interfaces` w celu sprawdzenia wszystkich połączonych urządzeń. Polecenie to jednak nie działa. Gdzie Michał popełnił błąd? 

<details><summary>Zobacz odpowiedź</summary>

ODP. Powinien użyć komendy `adb devices`
</details>

23. Do czego służy Mobile Security Framework? 

<details><summary>Zobacz odpowiedź</summary>
Odp. Do analizy statycznej oraz dynamicznej aplikacji mobilnej. 
</details>

24. Czym różni się analiza dynamiczna od statycznej? 

<details><summary>Zobacz odpowiedź</summary>
Odp. Podczas analizy statycznej analizuje się tylko kod aplikacji bez interakcji z aplikacją. Natomiast podczas analizy dynamicznej wchodzimy bezpośrednio w interakcję z aplikacją. 
</details>

25.  Jaki rodzaj analizy aplikacji można dokonać przy pomocy MOBSF? 

<details><summary>Zobacz odpowiedź</summary>
Odp. Analizę statyczną i dynamiczną. 
</details>

26. Michała zatrudniono w nowej firmie. Szef kazał mu skonfigurować śordowisko w tym drozera. Zainstalował więc drozera na komputerze i napisał polecenie 'drozer console connect'. Michał dostaje cały czas odpowiedź Refuse. Co Michał powinien zrobić, by nie uzyskać takiego błędu? 

<details><summary>Zobacz odpowiedź</summary>
Odp. Michał powinien zainstalować jeszcze aplikację dozer-server.apk, następnie trzeba zrobić jeszcze przekierowanie portów.  Następnie uruchamia aplikację drozer na telefonie i w prawym dolnymm rogu kilka 'ON'. Teraz Michał może wykonać polecenie 'drozer console connect'.
</details>

27. Czy drozer służy do atakowania innych aplikacji? 

<details><summary>Zobacz odpowiedź</summary>
Odp. Tak.Drozer jest agentem zainstalowanym na telefonie i z pozycji aplikacji atakuje inne aplikacje. 
</details>

28. Hackintosh, to jest zainstalowana spiracona wersja macOS/ Prawda czy fałsz? 

<details><summary>Zobacz odpowiedź</summary>
Odp.  Fałsz. Hackintosh to system opreacyjny macOS zzainstalowany na innym hardwarze niż produkcji Apple'a. 
</details>

29. W jaki sposób Content Provider dostarcza nam treści? 

<details><summary>Zobacz odpowiedź</summary>
ODP. Content Provider dostarcza treści w postaci linków rozpoczynających się od content:// 
</details>

30. Co musi być spełnione by 4 wektory ataku, a w szczególności activity były podatne na atak? 

<details><summary>Zobacz odpowiedź</summary>
Odp. Dana element (np. activity) musi mieć exported ustawione na true w AndroidManifest.xml 
android:exported="true"
Wyjątkiem jest MainActivity.xml ,który zawsze ma domyślnie ustawioną flagę na true. 
</details>

31.  Jakim narzędziem możemy podpisać aplikację po modyfikacji pliku .smali? 
- apktool
- apksigner
- dex2jar 
- jd-gui 

<details><summary>Zobacz odpowiedź</summary>
Odp. apksigner
</details>

32. Jakim programem odczytamy plik z rozszerzeniem .jar? 

- d2j-dex2jar
- dj-gui
- d2j
- jd-gui

<details><summary>Zobacz odpowiedź</summary>
Odp. jd-gui
</details>





























![[Pasted image 20221121230103.png]]
