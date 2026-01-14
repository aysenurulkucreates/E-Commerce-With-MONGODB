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
- Eğer APIREST yapıyorsan models bölümüğ açıp içine schemaları oluşturman lazım artık ne geriyorsa, cart, orders, user, product vs gibi.
- Code yazarken async await mantığını sakın unutma.
- # DEFAULT kullanımı çok önemli, şema yapılarında.
- const { password, ...others } = user.\_doc; şifelemeden sonra bunu gşirmen lazım APIRESTTE. Eğer o others (yani kullanıcı bilgileri) paketini göndermezsen; Kullanıcı giriş yapar ama ekran hala boş bakar. React "Tamam girdik de... Kim girdi? Adı ne? Ne göstereyim?" diye kalır.
- JWT eklemen şart, çünkü tarayıcı balık hafızalıdır ve ona giril kimliği vermen lazım, pasaport gibi düiün süresi var.
- $set ile mongodb ye güncellemek için katı kural veriyorsun, sadece yanın ayazdığım şeyi gübcelle diyorsun, yoksa her eşyi kendince yeni bir paket haline getirir. new: true demezsen de güncellediği şeyi sana çıktı olarak vermez ve sen de güncellemedi sanarsın.
- Br de sakın $set. req.boy gibi genel bir şey yazma, değiştirmek istediklerini düzgünce obje halinde var, yoksa çok fena güvenlik açığı.
- Bearer "Bu bir tokendır" diye sisteme haber veren evrensel bir etikettir.
- Kullanıcı (React) -> Route (Adres) -> Middleware (Güvenlikçi) -> Controller (Beyin) -> Database (Depo).

## İNDİRDİĞİM PAKETLER!

- express
- mongoose
- dotenv
- nodemon
- bcrypt
- jsonwebtoken

## HANGİ SORUN ÇIKTI VE NE YAZINCA DÜZELDİ!

- Env dosyamla alakalı bad authentication sorunu çıktı, sebebi de <> şifremde bu işaretlerin olmasından dolayı şifremin yanlış gözükmesiydi, onu silelim bu durumlarda.
