# git
## 手順  
1. main ブランチで main.html を作成してコミットpush  
2. develop ブランチ 
   touch develop.html  
   git add develop.html~git push -u origin develop  
3. feature/challenge ブランチ  
   touch feature-challenge.html  
   git add feature-challenge.html ~git push -u origin feature/challenge  
## しくみ  
　　developではmain.htmlを引き継いでいる　　
　　feature/challengeではdevelop を引き継ぐ  
    mainはなにも引き継いでいない main.html だけ。pull しないと develop.html や challenge.html は main に反映されない  
    push → サーバーにブランチがアップロードされるだけ  
    main に反映させたい場合は main に対して merge（PR）する必要がある  
    結果、main が更新され、pull によってローカルにも反映される
## PRの順序  
1. feature/challenge → develop に PR を作る  
    base（取り込まれ先）＝ develop  compare（取り込む元）＝ feature/challenge  
    タイトル・説明を書いて PR を作成  
    内容を確認後、Merge pull request → Confirm merge 
    git checkout develop  
    git pull  
2.  develop → main に PR を作る  
    GitHub → Pull requests → New pull request  
    base＝ main compare＝ develop  
    内容を確認して PR を作成  
    Merge pull request → Confirm merge  
    git checkout main  
    git pull


