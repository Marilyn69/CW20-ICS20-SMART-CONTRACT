# CW20-ICS20-SMART-CONTRACT
CW20-ICS20-Smart-Contract
Selamlar Bugün kendimize ait CW20 token oluşturacağız ek olarak CW20-ICS20 Akıllı Sözleşmeleri kullanarak IBC üzerinden transfer yapacağız.
CW20 nedir?
CW20, Kısaca ERC-20 gibi düşünebilirsiniz, CW20 Token oluşturmak için Juno mint kullanıyoruz. Juno mint, Juno üzerinde akıllı sözleşmeler ile kodlama gerektirmeden kendi tokenimizi oluşturduğumuz platformdur.
Nerede işimize yarıyacak?
Şu an Sei Network Atlantic-1 testnetinde ihtiyacımız olacak, size anlatacağım.
İhtiyacımız olan şeyler.
Sei Networkte oluşturduğumuz cüzdan (normal şartlarda herhangi bir keplrda olur, sei görevi yapmak için diyorum)

Juno test tokeni.

Juno test ağı

Sei ağı

En önemlisi tüm floodu okuma becerisi <3

BEN TOKEN OLUŞTURMAYACAĞIM, EN KISA YOLU GÖSTER HOCAM DERSEN FLOODUN SONUNDA.
İlk önce yeni bir keplr cüzandan sei'de ki 12 kelimemizi kullanarak cüzdan oluşturuyoruz.
Daha sonra https://testnets.cosmosrun.info/sei-testnet üzerine gidip sağ üsten cüzdanı bağlamalıyız.
Yukaıda DISCLAIMER: uyarısını önemsemeyin, alta gelip Enable keplr diyerek sei ağını ekleyin.
Keplrda çıkan sei cüzdanınız mainnet. adresler farklı olabilir aynı olursada umursamayın.

![image](https://github.com/user-attachments/assets/ab069514-2cc3-4c26-98e0-dc3dc4d6b0c3)

Daha sonra https://junomint.com/ üzerinden juno test ağını ekleyelim.
![image](https://github.com/user-attachments/assets/c5039f2e-5a96-489f-b677-5483f83c3caa)
Şimdi discorda girip juno test tokeni alalım: https://discord.gg/4HxYGtaQ
Şimdi tokenimizi oluşturalım:
Token Name giriyoruz
Token Symbol giriyoruz
Initial Supply'ın sonuna 1-2 tane sıfır (0) ekliyoruz
Sağ altın biraz üstünden Agreement kısmında tiki onaylıyoruz
Confirm diyoruz.
2 kez cüzdan onayı veriyoruz.
![image](https://github.com/user-attachments/assets/6e5ad2ee-04ae-4dbd-8516-5ede75af63e6)
BU SAYFAYI SAKLAYIN msg KISMINI BURAYA YAZACAĞIZ
Bu arada keplr juno ağında alt kısma bakın tokeniniz gözükecek.

![image](https://github.com/user-attachments/assets/6f671406-d376-4063-bc6d-f385efea1905)

Daha sonra bu sayfaya giriyoruz: Link ve gerekli görevleri sıralıyorum alta.
Yukarıda verdiğim linkten sağ üstten cüzdan bağlıyoruz.
Alt kısımda Write kontrat kısmına tıklıyoruz
Altta verdiğim kodu write kontrat kısmını silip benim kodu giriyoruz.
{
  "allow": {
    "contract": "juno1d3pnlc086evh7d277vak6tpz6gmvw6gr6plwxzf5n2tl9zdtwf7qrdsn44"
  }
}
Daha sonra altta göstedğim görselde ki gibi, kendi kontrat adresimizi kopyalıyoruz.
![image](https://github.com/user-attachments/assets/18d86714-abc1-49e1-a9a0-8bb7260e300c)
Daha sonra kendi oluşturduğumuz tokenin kontrat adresi ile değiştiriyoruz.
Değiştirdikten sonra Execute contrat (mavi buton, altında olur) butonuna tıklıyoruz.
![image](https://github.com/user-attachments/assets/ae9880c3-dfc6-4027-b42a-b5473eaf8d0b)
Şimdi yapacaklarımızı çok basit bir dille anlatacağım 1-2 kez okuyalım lütfen.
Altta ki kodu kopyalayın.
eyJjaGFubmVsIjoiY2hhbm5lbC03OSIsInJlbW90ZV9hZGRyZXNzIjoic2VpMXAwdDZha3M3dGpzdTB5OXNqaHNwNXQ1Z2t1bmtjODlheHg0Mnk3In0=
https://www.utilities-online.info/base64 üzerine gidin.

Altta ki görselde ki gibi sol tarafa yapıştırın

Ortada Decode butonuna tıklayın.

Sağda görselde ki gibi {"channel diye başlayan bir kod çıkacak, o kodun sonunda remote_address ve sei adresi yazar.

O sei testnet adresi ile değiştirin. (çünkü benim adresim o)

Değiştirdikten sonra kopyalayıp sol tarafa yapıştırın.

İlk başta decode demiştik şimdi encode yapıyoruz.

Şimdi size ait bir MSG oluştu, yukarıda paylaştığım komutun benzeri.
![image](https://github.com/user-attachments/assets/373740a9-aa38-4930-9153-c5975ab24045)
Şimdi başta token oluşturmuş ve kendi kontrat adresimize tıkladığımızda Juno Blueprints üzerinde bir site açılmıştı. (görselde ki gibi)
Sırasıyla:

Sağ üstten cüzdanı bağlıyoruz aynı şekilde.
Aşağıya gelip write kontrat diyoruz
![image](https://github.com/user-attachments/assets/d7f21850-77da-4beb-aeec-a89c2afbdce5)

Görselde ki gibi bir mesaj çıkacak, orayı siliyoruz ve görselin altında verdiğim kodu giriyoruz
![image](https://github.com/user-attachments/assets/104ad499-a0ed-4ea1-ac78-915dd7663c90)
{
  "send": {
    "contract": "juno16gckhheyql9f85r9ydmazdccc0pnwxx5xxxrwltygtx3kxjg57ksamkpym",
    "amount": "100000000",
    "msg": "eyJjaGFubmVsIjoiY2hhbm5lbC03OSIsInJlbW90ZV9hZGRyZXNzIjoic2VpMXAwdDZha3M3dGpzdTB5OXNqaHNwNXQ1Z2t1bmtjODlheHg0Mnk3In0="
  }
}
Daha sonra MSG kısmında resimde gösterdiğim gibi tırnak işaretleri içersinde olan (") kodu siliyoruz.
Yukarıda kodu çevirmiştik kendi sei testnet adresimizi girmiştik hatırlarsınız onu kopyalıyoruz.
MSG kısmında sildiğimiz tırnak işaretleri arasına yapıştırıp execute kontrat diyoruz.
Bunu yaptıktan sonra cüzdanınızdan 1 tane kendı oluşturduğunuz token gidecek.
![image](https://github.com/user-attachments/assets/e0279c59-f634-4e02-a059-d746f1152b9b)
Daha sonra bu işlemi tamamladıktan sonra sayfayı yenileyin.
En altta bir TX oluşacak ona tıklıyoruz.
Tıkladıktan sonra açılan sayfada Success yazısını gör
![image](https://github.com/user-attachments/assets/7f685984-ca39-4f74-b347-2993f65c878f)
İşlem sonunda https://sei.explorers.guru/validators giriyoruz ve sırasıyla:
Validatorumuze tıklıyoruz
En altta kendi cüzdanımızı buluyoruz ve tıklıyoruz
Daha sonra böyle bir görselle karşılaşacaksınız, işlem tamam buraya kadar.
![image](https://github.com/user-attachments/assets/13d64a9a-a06e-46e8-b1a5-546cc967d92b)
Daha sonra bunu altta ki paylaşacağım görevler kısmında bu cw20 tokeni kullanarakta ek işlem yapabilirsiniz.
https://github.com/ruesandora/sei-atlantic-1/blob/main/seinami-testnet-mission.md

IBC TRANASFER:
TOKEN OLUŞTURMAK İSTEMEYENLERE KOLAY YOL:
Keplr ayarlardan IBC Transferi açıyoruz.
![image](https://github.com/user-attachments/assets/c23e2c67-4279-4908-a4d7-99bad52bc921)
Juno test ağına gelip en alttan IBC transfer diyoruz:
Sırasıyla:

Select chain
New IBC Transfer Channel
Select channel'dan en altta sei seçiyoruz.
channel ID channel-35 yazıyoruz.
save diyoruz
daha sonra sei testnet cüzdan adresimizi kopylaıyoruz (explorerden alın)
adres kısmına (Recipient) giriyoruz.
Memo boş kalacak
daha sonra token oluşturduysanız tokeninizi veya juno seçiyoruz.
Sırasıyla submit ve approve diyerek 3-5dk geçmesini bekliyoruz.
Görselde ki gibi explorerde gözükecek işlem tamamlanınca: biraz uzun sürebilir
![image](https://github.com/user-attachments/assets/d98b25c8-de56-4667-87eb-5d04201bb5e2)











