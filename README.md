Çerezle ilgili başlıklar için düz metin HTTP trafiğini algılar ve ardından bunları bekleyen dinleyicilere enjekte eder.

Birincil dinleyici bunları bir WebSocket sunucusuna gönderir, beraberindeki Chrome / Firefox uzantılarını kullanarak mevcut WebSocket sunucusuna bağlanarak çerezleri tarayıcıya gerçek zamanlı olarak enjekte eder.


<h2>Kurulum</h2>

```
virtualenv venv
source ./venv/bin/activate
python setup.py install
```

<h2>Kullanımı:</h2>

Öncelikle iki tarayıcı uzantısından birini yükleyin:

<li>https://github.com/Tugce41/chrome-extension.git</li>
<li>https://github.com/Tugce41/eklenti-paketi-firefox-extension-cookie-injector.git</li>


Genel kullanım:
80 numaralı bağlantı noktası tcp trafiğini filtreleyen tüm arayüzlerde cookie'i çalıştırın

```
cookiejack -v
```

Çerezleri websocket'e yüklemek için bir pcap dosyası kullanın:

```
cookiejack -v -r path/to/traffic.pcap
```

Çalıştırdıktan sonra tarayıcı uzantısının seçenekler sayfasını ziyaret edin ve ana bilgisayarı ve bağlantı noktasını yapılandırın (varsayılanı localhost:9000'dir) - ardından simgeye tıklayın ve çerezlerin gelişini izleyin.

Çerezler joker karakterli tld ile ayarlanır ve varsayılan olarak oturum çerezleri olarak ayarlanır, dolayısıyla tarayıcıyı kapatmak çerezleri kaldırmanıza olanak tanır.



<h2>Çıkış</h2>

root u sonlandırmak için

```
cookiejack -k
```


