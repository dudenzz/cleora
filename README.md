# Oryginalne readme

To jest fork repozytorium. Oryginalne readme znajduje się na stronie cleory. Tutaj umieszczam istotne dla nas informacje.


1. Żeby w ogóle uruchomić to narzędzie, samo repozytorium nie wystarczy. Potrzebny jest binarny (skompilowany?) program - cleora. Na tą chwilę pobieram gotowy program z repozytorium https://github.com/BaseModelAI/cleora/releases . Teraz jestem na windowsie, więc pobrałem cleora-v1.2.3-x86_64-pc-windows-msvc . Gdybym był na innym systemie operacyjnym, wybrałbym inną wersję. Docelowo mam zamiar kompilować kod samodzielnie, ale do tego czasu korzystam z wersji prekompilowanych, tak aby na pewno wszystko zadziałało tak jak powinno.

2. Uruchomienie notebooka 'example_classification'

    i. Pobrałem facebook_large

    ii. Utworzyłem w repozytorium katalog datasets/facebook_large

    iii. Dodałem katalog datasets do .gitignore

    iv. Utworzyłem katalog output/facebook_large

    v. Przeniosłem plik binarny cleory do katalogu głównego repozytorium

    vi. Dodałem plik binarny do .gitignore

    vii. Zmieniłem nazwy plików na zgodne z utworzonym przeze mnie systemem plików (datasets, output i facebook_large)

    viii. Zmieniłem w kodzie typy danych na takie, które nie są przestarzałe (np.int -> np.int32)

    ix. Zmieniłem w kodzie funkcję loss, na nieprzestarzałą wersję (log -> log_loss)
    
    x. uruchomiłem wszystkie komórki w notebooku. Ostatnia prezentuje wynik klasyfikacji.

      100%|██████████| 20/20 [00:19<00:00,  1.04it/s]
      algo: output/facebook_large/emb__cluster_id__StarNode.out epochs: 20, micro f1: 0.8816933638443936, macro f1:0.8730898589082499

      100%|██████████| 20/20 [00:17<00:00,  1.13it/s]
      algo: output/facebook_large/emb__CliqueNode__CliqueNode.out epochs: 20, micro f1: 0.8867276887871853, macro f1:0.8784493199093816


3. Uruchomienie notebooka '