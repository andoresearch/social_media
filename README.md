# social_media



import delimited "https://raw.githubusercontent.com/andoresearch/social_media/main/Ehrmann-Wabitsch2022/mmc4.csv", clear case(preserve)

* 文字列を日付型に変換
gen new_date = daily(date, "DMY")
* 日付フォーマットを設定
format new_date %td


tsset new_date


reg ln_tweetsDaily L(-5/3).pressConf tweetECB L(0/20).whatever    EconBulletin  MonPolAccounts speechOtherBoard speechPresident n n2 i.dow i.month dec2* dec31 jan0* easter* good* corpus ascension whitMon may* nov01 oct03, r



