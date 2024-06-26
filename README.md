# README.md

## Opis Projektu

Ten projekt jest realizowany w ramach przedmiotu "Podstawy Sztucznej Inteligencji" i ma na celu analizę danych o przestępczości w San Francisco oraz stworzenie modelu predykcyjnego. Projekt jest częścią konkursu na platformie Kaggle.

Link do konkursu: [Kaggle Competition](https://www.kaggle.com/c/sf-crime)

## Struktura Projektu

Projekt składa się z trzech głównych plików:

1. **sf_crime.ipynb**: Ten plik zawiera wizualizację danych, eksplorację danych oraz wstępną analizę.
2. **training_pipeline.ipynb**: Ten plik zawiera preprocessing danych z użyciem różnych pipeline'ów oraz trenowanie modeli predykcyjnych.
3. **evaluation.ipynb**: Ten plik zawiera końcową ewaluację najlepszego modelu, w tym wczytywanie zapisanych modeli i transformatorów z plików `imputer.joblib`, `sincos.joblib`, oraz `pipeline.joblib`.

### Pipeline'y do Przetwarzania Danych

W projekcie zastosowaliśmy trzy różne pipeline'y do przetwarzania danych:

1. **Pipeline z rozdzielonymi datami**: Rozdziela daty na oddzielne kolumny reprezentujące dni, miesiące i godziny.
2. **Pipeline z funkcjami trygonometrycznymi**: Zastosowanie funkcji trygonometrycznych (sinus i cosinus) do przekształcenia dni, miesięcy i godzin.
3. **Pipeline z funkcjami trygonometrycznymi i bucketowaniem**: Połączenie funkcji trygonometrycznych z techniką grupowania (bucketing) współrzędnych geograficznych.

### Uruchamianie Kodu

Aby uruchomić kod na danych, należy pobrać je z linku umieszczonego wyżej oraz umieścić je w folderze `data_sets`.

### Wyniki

Najlepsze wyniki uzyskane w konkursie Kaggle z zastosowaniem różnych pipeline'ów i modeli zostały przedstawione w poniższej tabeli:

| Model           | Pipeline                             | Wynik CV                | Wynik Kaggle          |
|-----------------|--------------------------------------|-------------------------|-----------------------|
| XGBoost         | Bez hiperparametrów                  | 2.29494                 | 2.30348               |
| XGBoost         | Pipeline 1                           | 2.28839                 | 2.30605               |
| XGBoost         | Pipeline 2                           | 2.27688                 | 2.29785               |
| LGBM            | Pipeline 1                           | 2.31692                 | 2.32228               |
