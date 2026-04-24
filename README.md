# Procjena kreditnog rizika – Machine Learning projekt

## Opis projekta
Cilj ovog projekta je razviti model za procjenu kreditnog rizika klijenta koristeći metode strojnog učenja.

Model na temelju financijskih i demografskih podataka predviđa pripada li klijent rizičnoj skupini.

## Podaci
Dataset sadrži podatke o klijentima banke:
- odobreni iznos kredita
- mjesečna primanja
- trenutni dug
- starost klijenta
- radni staž
- kreditna povijest
- obrazovanje
- broj članova kućanstva

Podaci su očišćeni i obrađeni:
- uklonjeni duplikati
- ispravljene pogreške u unosu
- popunjene nedostajuće vrijednosti
- uklonjeni nelogični podaci

## Dataset
Dataset korišten u projektu predstavlja sintetički generirane podatke koji simuliraju profil klijenata u kontekstu procjene kreditnog rizika. Podaci uključuju tipične varijable koje se koriste u financijskom sektoru, poput visine primanja, iznosa duga, radnog staža i kreditne povijesti.
Ciljana varijabla definirana je na temelju kombinacije odabranih atributa, čime se simulira pojednostavljeni model procjene rizičnosti klijenta. Ovakav pristup omogućuje razvoj i testiranje modela strojnog učenja u kontroliranim uvjetima.

## Ciljna varijabla
Ciljna varijabla (Rizik) nije postojala u datasetu, već je definirana na temelju:
- omjera duga i primanja
- kreditne povijesti
- radnog staža

## Model
Za modeliranje je korišten Random Forest algoritam.

Razlog odabira:
- dobro radi s tabličnim podacima
- prepoznaje nelinearne odnose
- daje stabilne rezultate

## Rezultati
Model postiže vrlo dobre rezultate:

- Accuracy: ~0.96
- ROC AUC: ~0.988

Model uspješno razlikuje rizične i nerizične klijente.

## Demo
Model može napraviti predikciju za pojedinog klijenta i dati vjerojatnost pripadnosti rizičnoj skupini.

## Pokretanje projekta

Instalirati potrebne biblioteke:

pip install pandas numpy scikit-learn matplotlib seaborn joblib

Pokrenuti Jupyter Notebook.

## Zaključak
Model pokazuje vrlo dobre rezultate i može se koristiti kao alat za procjenu kreditnog rizika.

U praksi bi se koristio kao podrška odlučivanju, a ne kao jedini kriterij.
