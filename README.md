# Oryginalne readme

To jest fork repozytorium. Oryginalne readme znajduje się na stronie cleory. Tutaj umieszczam istotne dla nas informacje.


1. Żeby w ogóle uruchomić to narzędzie, samo repozytorium nie wystarczy. Potrzebny jest binarny (skompilowany?) program - cleora. Na tą chwilę pobieram gotowy program z repozytorium https://github.com/BaseModelAI/cleora/releases . Teraz jestem na windowsie, więc pobrałem cleora-v1.2.3-x86_64-pc-windows-msvc . Gdybym był na innym systemie operacyjnym, wybrałbym inną wersję. Docelowo mam zamiar kompilować kod samodzielnie, ale do tego czasu korzystam z wersji prekompilowanych, tak aby na pewno wszystko zadziałało tak jak powinno.

2. Uruchomienie notebooka 'example_classification'

    i. Pobrałem facebook_large

    ii. utworzyłem w repozytorium katalog datasets/facebook_large

    iii. dodałem katalog datasets do .gitignore

    iv. utworzyłem katalog output/facebook_large

    v. przeniosłem plik binarny cleory do katalogu głównego repozytorium

    vi. dodałem plik binarny do .gitignore

    vii. zmieniłem nazwy plików na zgodne z utworzonym przeze mnie systemem plików (datasets, output i facebook_large)

    viii. zmieniłem w kodzie typy danych na takie, które nie są przestarzałe (np.int -> np.int32)
    
    ix. test
3. Uruchomienie notebooka '