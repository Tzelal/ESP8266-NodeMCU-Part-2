<h1 align="center">ESP8266-tzelliot-</h1>
<h2 align="center">ESP8266 NodeMCU Firmware Update (...NodeMCU...)</h2>

<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57551143-02623500-7371-11e9-9bb0-59e907150322.JPG" width="650" ></p>

Mehabalar kolay gelsin.ESP8266 NodeMCU modülünü Arduino IDE ye kurmuş birisinin Firmware update'i nasıl yapması gerektiğini anlatmaya çalışıcam.Öncelikle Part 1 de anlattıklarımı yaptığını farz ediyorum burada anlatıcaklarım 2. adım gibi birşey diyebilirim.Arduino IDE ye gidip Serial portu açtığında eğer NodeMCU modülü çalışıyorsa daha doğrusu komutları almaya hazırsa Serial portta "ready" yazması gerekiyor.Eğer "ready" yazıyorsa modül düzgün çalışıyor demektir ve burada yazdıklarımın hiçbirisini yapmana gerek yok, direkt projene başlayabilirsin.Fakat Serial Portta "ready" yerine okunmayan yazılar varsa o zaman Firmware güncellemesini yapman gerek.

NodeMCU modülü için Firmware Güncellemesi aşağıdaki gibi:


<h3 align="center">..............İLK ADIM..................</h3>
<hr size="3" width="%100">

Arduino IDE de tools ların aşağıdaki foto gibi olmasına dikkat et! (Port sende ne gösteriyorsa o :D )



<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57237050-091a4080-702f-11e9-93f1-f27412a17ac9.PNG"width="650" ></p>



<h3 align="center">.............İKİNCİ ADIM...............</h3>
<hr size="3" width="%100">

Şimdi Firmware güncellemesini yapmak için flash tool indirmemiz gerek.Flash tool indirmek için üreticisinin sitesine gitmek gerek o da :

https://www.espressif.com/en/support/download/other-tools

Kullandığın model Espressif'ın olmayabilir, birsürü şirketin modeli var fakat bu flash tool hepsinde geçerli hatta ESP32 içim bile.
İndirmen gereken dosyanın resmi aşağıda...


<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57237629-49c68980-7030-11e9-926a-3bc002f8dc39.PNG"width="650" ></p>


İndirdiğin dosyada Çalıştıracağın program yina aşağıdaki resimde gösteriyorum:


<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57238216-8c3c9600-7031-11e9-9653-64baa7d34314.PNG"width="650" ></p>


Açılan pencerede ESP8266 Download Tool'u seçiyorsun...


<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57238263-a9716480-7031-11e9-82dd-d8a8803a769b.PNG"width="650" ></p>


Karşılaşman gereken sayfa (Uzun zaman önce yaptığım için hatırlamıyorum):


<p align="center"><img src="(https://user-images.githubusercontent.com/36787074/57238808-f0ac2500-7032-11e9-87be-ec1a949adf40.PNG"width="650" ></p>


<h3 align="center">............ÜÇÜNCÜ ADIM..............</h3>
<hr size="3" width="%100">

Bu adımda ESP8266 Download Tool için indirmen gereken dosyaları göstericem.Öncelikle aşağıdaki linke tıklayıp dosyaları indireceğin siteye gitmen gerek.


https://www.espressif.com/en/products/hardware/esp8266ex/resources


Siteye gittikten sonra aşağıdaki resimde belirttiğin dosyayı indirmen gerekecek.

<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57534408-a683b600-7348-11e9-81c0-260c408d33dd.PNG" width="650" ></p>


<h3 align="center">............DÖRDÜNCÜ ADIM..............</h3>
<hr size="3" width="%100">


Son olarak indirdiğin dosyadaki AT BIN'leri ESP8266 Download Tool'a yerleştirmek kalıyor.


<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57540761-1f3d3f00-7356-11e9-88af-d7821650ee70.PNG"width="650" ></p>


:exclamation:NOT:
  Mor çerçevenin içindeki sayfa yukarıdaki kırmızı kutulara tıklayınca çıkıcak.çıkmaması durumunda indirdiğin ESP_AT_Bin_V1.5.1 dosyasını bulup içindeki dosyaları resimde olduğu gibi yerleştirebilirsin...!!!

Tüm dosyaları yerleştirip "START" butonuna tıklayınca Firmware güncellemesi tamamlanmış oluyor.


<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57540891-73e0ba00-7356-11e9-98d2-a128255561e9.PNG"width="550" ></p>


Son olarak Arduino IDE'yi açıp Serial port'a AT yazman gerek.Bundan önce ESP8266 modülünün hazıl olup olmadığını kontrol etmek için serial portta iken ESP8266 modülünün üzerindeki "RSP" (RESET) tuşuna basmanı tavsiye ediyorum.Butona bastığında serial portta "ready" yazacaktır.Serialdeki "ready" yazısını görünce porta bu sefer "AT" yazman gerek.Karşılık olarak olarak aşağıdaki resimde olduğu gibi "ok" cevabı gelicek.



<p align="center"><img src="https://user-images.githubusercontent.com/36787074/57541385-8a3b4580-7357-11e9-9595-085b134b2a3a.PNG"width="550" ></p>

Şuan NodeMCU modülünü kullanmaya hazırsın.Elimden geldiğince buraya yeni projeler eklemeye çalışıcam umarım takipte kalmayı unutma :D .


Farklı modül veya model kullanıyorsan kullandığım ingilice kaynaklar aracılığıyla sadece AT bin'leri değiştirerek güncellemeyi yapabilirsin.


**İngilizce kaynaklar:**

Espressif:https://www.espressif.com/en/products/hardware/esp8266ex/overview

ESP8266 Arduino Core’s documentation:https://arduino-esp8266.readthedocs.io/en/2.5.0/filesystem.html#flash-layout

