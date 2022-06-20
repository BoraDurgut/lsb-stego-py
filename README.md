# lsb-stego-py
 LSB yöntemini kullanarak PNG türü bir görüntüde şifrelenmiş bir mesajı gizlemenize olanak tanır.  Mesaj önce RSA-CBC-256 kullanılarak şifrelenir ve ardından PNG görüntüsünün düşük sıralı bitlerinde gizlenir.

Renkli görüntüler, her piksel için 0-255 piksel değerlerine sahip üç renk kanalına (RGB) sahiptir. Üst aralık 255, 8 bit ikili sayı ile temsil edilebilecek en büyük değerdir. 10001011 gibi 139 ondalık bir değere eşit olan bir ikili sayıda, soldaki ilk rakam en anlamlı bit (MSB) olarak tanımlanır ve sağdaki son rakam doğu anlamlı biti (LSB) olarak tanımlanır. aşağıdaki örnek daha iyi açıklıyor


10001011 = 139 / 00001011 = 1110001011 = 139 / 10001010 = 138
![matlab_code_for_lsb_steganography](https://user-images.githubusercontent.com/70798901/174682276-bf27276b-374f-4dcf-953e-237a9672ab2f.jpg)


Bu projede, görüntü içindeki bir metnin siyah beyaz görüntüsünü kodlamak için kırmızı rengin en az anlamlı bitini alacağım. O pikselin kırmızı değerini elde etmek için görüntüdeki her pikseli tekrarlarım, pikselin değeri çift ise beyaz renkli, çift ise siyah renklidir.


![Encoding-and-decoding-of-a-Cover-image-eso1705atif-126-GB-b-Secret-image-eso1740jpg_Q320](https://user-images.githubusercontent.com/70798901/174682423-ece6aa1c-2073-4de8-a9f1-4166240cd2b7.jpg)





