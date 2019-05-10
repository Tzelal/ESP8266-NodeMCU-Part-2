# ESP8266-NodeMCU-Part-2
NodeMCU Firmware Update
Mehabalar kolay gelsin.ESP8266 NodeMCU modülünü Arduino IDE ye kurmuş birisinin Firmware update'i nasıl yapması gerektiğini anlatmaya çalışıcam.Öncelikle Part 1 de anlattıklarımı yaptığını farz ediyorum burada anlatıcaklarım 2. adım gibi birşey diyebilirim.Arduino IDE ye gidip Serial portu açtığında eğer NodeMCU modülü çalışıyorsa daha doğrusu komutları almaya hazırsa Serial portta "ready" yazması gerekiyor.Eğer "ready" yazıyorsa modül düzgün çalışıyor demektir ve burada yazdıklarımın hiçbirisini yapmana gerek yok, direkt projene başlayabilirsin.Fakat Serial Portta "ready" yerine okunmayan yazılar varsa o zaman Firmware güncellemesini yapman gerek.

NodeMCU modülü için Firmware Güncellemesi aşağıdaki gibi:

1.Adım

Arduino IDE de tools ların aşağıdaki foto gibi olmasına dikkat et! (Port sende ne gösteriyorsa o :D )


![Arduino IDE Tools](https://user-images.githubusercontent.com/36787074/57237050-091a4080-702f-11e9-93f1-f27412a17ac9.PNG)

2.Adım

Şimdi Firmware güncellemesini yapmak için flash tool indirmemiz gerek.Flash tool indirmek için üreticisinin sitesine gitmek gerek o da :

https://www.espressif.com/en/support/download/other-tools

Kullandığın model Espressif'ın olmayabilir, birsürü şirketin modeli var fakat bu flash tool hepsinde geçerli hatta ESP32 içim bile.
İndirmen gereken dosyanın resmi aşağıda...

![Espressif Webpage](https://user-images.githubusercontent.com/36787074/57237629-49c68980-7030-11e9-926a-3bc002f8dc39.PNG)

İndirdiğin dosyada Çalıştıracağın program yina aşağıdaki resimde gösteriyorum:

![Flash Download Tool](https://user-images.githubusercontent.com/36787074/57238216-8c3c9600-7031-11e9-9653-64baa7d34314.PNG)

Açılan pencerede ESP8266 Download Tool'u seçiyorsun...

![Flash Tool ESP8266](https://user-images.githubusercontent.com/36787074/57238263-a9716480-7031-11e9-82dd-d8a8803a769b.PNG)

Karşılaşman gereken sayfa (Uzun zaman önce yaptığım için hatırlamıyorum):


![ESP8266 Download Tool](https://user-images.githubusercontent.com/36787074/57238808-f0ac2500-7032-11e9-87be-ec1a949adf40.PNG)

3.Adım
Bu adımda ESP8266 Download Tool için indirmen gereken dosyaları göstericem.Öncelikle aşağıdaki linke tıklayıp dosyaları indireceğin siteye gitmen gerek.

https://www.espressif.com/en/products/hardware/esp8266ex/resources

Siteye gittikten sonra aşağıdaki resimde belirttiğin dosyayı indirmen gerekecek.

![AT Bin V1 5 1 Screenshot](https://user-images.githubusercontent.com/36787074/57534408-a683b600-7348-11e9-81c0-260c408d33dd.PNG)

4.Adım

Son olarak indirdiğin dosyadaki AT BIN'leri ESP8266 Download Tool'a yerleştirmek kalıyor.

![AT Bin yükleme işlemi](https://user-images.githubusercontent.com/36787074/57535752-80134a00-734b-11e9-8248-0b65e182cd21.PNG)


NOT:
!!! Mor çerçevenin içindeki sayfa yukarıdaki kırmızı kutulara tıklayınca çıkıcak.çıkmaması durumunda indirdiğin ESP_AT_Bin_V1.5.1 dosyasını bulup içindeki dosyaları resimde olduğu gibi yerleştirebilirsin...!!!
