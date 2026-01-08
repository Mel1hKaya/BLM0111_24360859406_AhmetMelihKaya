# 🚀 Uzay Simülasyonu: Çoklu Gezegen Fizik Deneyleri

Bu proje, güneş sistemindeki 8 farklı gezegenin yerçekimi ivmelerini kullanarak çeşitli fizik deneylerini simüle eden C dilinde yazılmış bir konsol uygulamasıdır. Bursa Teknik Üniversitesi Bilgisayar Mühendisliği çalışmaları kapsamında geliştirilen bu uygulama; pointer aritmetiği, modüler fonksiyon yapısı ve temel fizik formüllerini bir araya getirir.

## 🛠️ Özellikler

Uygulama, kullanıcıdan alınan girdilerle aşağıdaki 9 farklı deneyi simüle etmektedir:

1.  **Serbest Düşme:** Belirli bir sürede cismin her gezegende kat edeceği mesafeyi ($h = \frac{1}{2}gt^2$) hesaplar.
2.  **Yukarı Atış:** Verilen bir ilk hızla fırlatılan cismin ulaşabileceği maksimum yüksekliği ($h_{max} = \frac{v_0^2}{2g}$) bulur.
3.  **Ağırlık Hesaplama:** Bir kütlenin farklı gezegenlerdeki ağırlığını ($G = m \cdot g$) hesaplar.
4.  **Potansiyel Enerji:** Belirli bir yükseklikteki cismin sahip olduğu enerjiyi ($E_p = m \cdot g \cdot h$) ölçer.
5.  **Hidrostatik Basınç:** Sıvı içindeki bir derinlikte oluşan basıncı ($P = \rho \cdot g \cdot h$) hesaplar.
6.  **Arşimet Kaldırma Kuvveti:** Sıvı içindeki cisme etki eden kaldırma kuvvetini ($F_k = \rho \cdot g \cdot V_{batan}$) bulur.
7.  **Basit Sarkaç:** Sarkacın gezegenlere göre salınım periyodunu ($T = 2\pi \sqrt{\frac{L}{g}}$) hesaplar.
8.  **İp Gerilmesi:** Asılı bir kütlenin oluşturduğu statik gerilmeyi hesaplar.
9.  **Asansör Deneyi:** Hareketli bir referans sistemindeki etkin ağırlığı (eylemsizlik etkisiyle) hesaplar.

## 🪐 Yerçekimi Verileri

Program içerisinde kullanılan yerçekimi ivmeleri ($m/s^2$):
* **Merkür:** 3.70
* **Venüs:** 8.87
* **Dünya:** 9.81
* **Mars:** 3.71
* **Jüpiter:** 24.79
* **Satürn:** 10.44
* **Uranüs:** 8.69
* **Neptün:** 11.15

## 💻 Teknik Detaylar

* **Pointer Kullanımı:** Gezegen ivmelerine erişim için pointer aritmetiği (`*(g_dizi + i)`) tercih edilmiştir.
* **Hata Yönetimi:** Kullanıcıdan gelen negatif değerler ternary operatörler kullanılarak mutlak değere dönüştürülür.
* **Modülerlik:** Her deney, main fonksiyonundan bağımsız, tekrar kullanılabilir fonksiyonlar olarak tanımlanmıştır.

## 🚀 Başlangıç

### Gereksinimler
* GCC veya herhangi bir standart C derleyicisi.

### Derleme ve Çalıştırma
1. Terminalinizi açın.
2. Kodun bulunduğu dizine gidin.
3. Aşağıdaki komutla derleyin:
   ```bash
   gcc main.c -o uzay_simulasyonu -lm

