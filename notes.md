# BAŞLANGIÇTA YAPMAM GEREKENLER!

- Öncelikle ya app.js indireceksin ya da index.js, bunları tyscripte çecirmek lazım tabi bunu da unutma.
- Sonra npm init yapman gerek ki, paket oluşsun, ayrıca githuba bağlanmak için de git init yazman gerek.
- Sonra lazım olan paketkleri indirmen gerek.
- .gitignore açarak karşıya nodemodullerin gidip yer kaplamasını önlersin ve şifrelerinin gitmeaini de önlersin, .env paketi de şifreler için, unutma.
- Scripts kısmına start komutu eklemeyi unutma, kısa oluyor çalıştırırken.
- Sonrasında indirdiğin paketleri ana klasöre tanımlaman gerek.
- require("dotenv").config(); bunu mutlka ana klasöre eklemen lazım ve connect le birlikte process.env de yazman gerek ki şifren sistem tarafından anlaşıbilsin.
- Dosyaları görevlere ayırman gerek, routes, controller olarak. rotesta get, post,put delete şlemleri yaparsın ve bunalrı ana dosyana tanıtırsın, mutlaka export etemn gerek yoksa ana dosyan okuyamaz. 'app.use()' şeklinde okut, öncesinde import etmeyi unutma.
- Tarayıcıya "Bana ver" diyorsan -> GET
- Tarayıcıya "Al bunu veritabanına koy" diyorsan -> POST

## İNDİRDİĞİM PAKETLER!

- express
- mongoose
- dotenv
- nodemon

## HANGİ SORUN ÇIKTI VE NE YAZINCA DÜZELDİ!

- Env dosyamla alakalı bad authentication sorunu çıktı, sebebi de <> şifremde bu işaretlerin olmasından dolayı şifremin yanlış gözükmesiydi, onu silelim bu durumlarda.
