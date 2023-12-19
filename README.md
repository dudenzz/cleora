# Oryginalne readme

To jest fork repozytorium. Oryginalne readme znajduje się na stronie cleory. Tutaj umieszczam istotne dla nas informacje.


1. Żeby w ogóle uruchomić to narzędzie, samo repozytorium nie wystarczy. Potrzebny jest binarny (skompilowany?) program - cleora. Na tą chwilę pobieram gotowy program z repozytorium https://github.com/BaseModelAI/cleora/releases . Teraz jestem na windowsie, więc pobrałem cleora-v1.2.3-x86_64-pc-windows-msvc . Gdybym był na innym systemie operacyjnym, wybrałbym inną wersję. Docelowo mam zamiar kompilować kod samodzielnie, ale do tego czasu korzystam z wersji prekompilowanych, tak aby na pewno wszystko zadziałało tak jak powinno.

2. Uruchomienie notebooka 'example_classification'

    i. Pobrałem facebook_large

    ii. Utworzyłem w repozytorium katalog datasets/facebook_large

    iii. Dodałem katalog datasets do .gitignore

    iv. Utworzyłem katalog output/facebook_large

    v. Przeniosłem plik binarny cleory do katalogu głównego repozytorium

    vi. Dodałem plik binarny do .gitignore, oraz zmieniłem jego nazwę w kodzie

    vii. Zmieniłem nazwy plików na zgodne z utworzonym przeze mnie systemem plików (datasets, output i facebook_large)

    viii. Zmieniłem w kodzie typy danych na takie, które nie są przestarzałe (np.int -> np.int32)

    ix. Zmieniłem w kodzie funkcję loss, na nieprzestarzałą wersję (log -> log_loss)
    
    x. uruchomiłem wszystkie komórki w notebooku. Ostatnia prezentuje wynik klasyfikacji.

      100%|██████████| 20/20 [00:19<00:00,  1.04it/s]
      algo: output/facebook_large/emb__cluster_id__StarNode.out epochs: 20, micro f1: 0.8816933638443936, macro f1:0.8730898589082499

      100%|██████████| 20/20 [00:17<00:00,  1.13it/s]
      algo: output/facebook_large/emb__CliqueNode__CliqueNode.out epochs: 20, micro f1: 0.8867276887871853, macro f1:0.8784493199093816


3. Uruchomienie notebooka 'example_link_prediction'. Podjęte kroki są analogiczne w stosunku do poprzedniego notebooka (w kodzie trzeba zmienić strukturę plików i katalogów; np.int -> np.int32; oraz zmienić nazwę pliku binarnego). Tak prezentuje się wynik:

100%|██████████| 535/535 [00:17<00:00, 30.05it/s]
100%|██████████| 535/535 [00:20<00:00, 25.81it/s]
mrr  0.07459434689397301  hr@10  0.22
mrr  0.07055648800503342  hr@10  0.215
mrr  0.06886324062766128  hr@10  0.21
mrr  0.07224367475183043  hr@10  0.21
mrr  0.07321340012345748  hr@10  0.204
mrr  0.07244010685365321  hr@10  0.19666666666666666
mrr  0.07150541270597703  hr@10  0.19714285714285715
mrr  0.07056938845930436  hr@10  0.19875
mrr  0.06963597265826221  hr@10  0.19444444444444445
mrr  0.06900495220162918  hr@10  0.198
algo: output/facebook_large/emb__cluster_id__StarNode.out epochs: 2 lr: 0.0001, mrr: 0.06900495220162918, hr@10: 0.198
100%|██████████| 535/535 [00:19<00:00, 27.54it/s]
100%|██████████| 535/535 [00:21<00:00, 25.38it/s]
mrr  0.06602019476829273  hr@10  0.2
mrr  0.05717456929652858  hr@10  0.165
mrr  0.06248289699816748  hr@10  0.18666666666666668
mrr  0.06594249215546175  hr@10  0.185
mrr  0.06684644784920664  hr@10  0.182
mrr  0.0695754531562925  hr@10  0.185
mrr  0.06733528585959776  hr@10  0.18714285714285714
mrr  0.06842146045727965  hr@10  0.18625
mrr  0.06637753294614365  hr@10  0.18333333333333332
mrr  0.06469972685462926  hr@10  0.181
algo: output/facebook_large/emb__CliqueNode__CliqueNode.out epochs: 2 lr: 0.0001, mrr: 0.06469972685462926, hr@10: 0.181