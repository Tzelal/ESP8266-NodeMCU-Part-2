# ESP8266-NodeMCU-Part-2
NodeMCU Firmware Update
Mehabalar kolay gelsin.ESP8266 NodeMCU modülünü Arduino IDE ye kurmuş birisinin Firmware update'i nasıl yapması gerektiğini anlatmaya çalışıcam.Öncelikle Part 1 de anlattıklarımı yaptığını farz ediyorum burada anlatıcaklarım 2. adım gibi birşey diyebilirim.Arduino IDE ye gidip Serial portu açtığında eğer NodeMCU modülü çalışıyorsa daha doğrusu komutları almaya hazırsa Serial portta "ready" yazması gerekiyor.Eğer "ready" yazıyorsa modül düzgün çalışıyor demektir ve burada yazdıklarımın hiçbirisini yapmana gerek yok, direkt projene başlayabilirsin.Fakat Serial Portta "ready" yerine okunmayan yazılar varsa o zaman Firmware güncellemesini yapman gerek.

NodeMCU modülü için Firmware Güncellemesi aşağıdaki gibi:

1.Adım

Arduino IDE de tools ların aşağıdaki foto gibi olmasına dikkat et! (Port sende ne gösteriyorsa o :D )


![Arduino IDE Tools](https://user-images.githubusercontent.com/36787074/57237050-091a4080-702f-11e9-93f1-f27412a17ac9.PNG)
