# LÖSEV Eğitim Uygulaması (Duolingo Benzeri) Proje İhtiyaç ve Gereksinim Dokümanı

## 1. Projeye Neden İhtiyaç Var? (Arka Plan ve Mevcut Durum)
LÖSEV, sadece tedavi sunmadığı gibi aynı zamanda toplumun her kesimini kanser, lösemi, sağlıklı beslenme ve hastalıktan korunma yolları hakkında bilinçlendirmeyi kendine görev edinmiş bir vakıftır. Mevcut operasyonlarında bu bilinçlendirme çalışmaları; okullarda yapılan seminerler, sağlık konferansları, dağıtılan basılı broşürler ve çeşitli yüz yüze saha etkinlikleri ile yürütülmektedir.

## 2. Yaşanan Problemler
LÖSEV yetkilileri ile yapılan eğitim stratejisi görüşmelerinde şu sorunlar tespit edilmiştir:
- **Kalıcılık ve Etkileşim Eksikliği:** Basılı broşürler ve uzun, teknik metinler özellikle çocuklar, gençler ve hatta günümüz hızlı tüketim alışkanlıklarına sahip yetişkinleri tarafından ilgi çekici bulunmamakta, çoğu zaman okunmadan kenara atılmaktadır.
- **Erişim Sınırı:** Fiziksel sunumların ve etkinliklerin ulaştığı kişi sayısı fiziki kapasiteyle sınırlıdır. Herkesin her an cebinden erişip bilgi edinebileceği ölçeklenebilir ve merkezi bir araç eksikliği vardır.
- **Bilgi Kirliliği ile Başa Çıkma Zorluğu:** İnternette asılsız ve moral bozucu sağlık bilgileri çok hızlı yayılırken, LÖSEV'in doğrulanmış bilgilerini geniş kitlelere aynı hızda ve akılda kalıcı şekilde iletecek bir dijital "kalkan" veya köprü bulunmamaktadır.

## 3. Çözüm: Oyunlaştırılmış Eğitim Uygulaması
Toplumun her kesimini kucaklayan, sıkıcı okuma metinleri veya uzun videolar yerine **"Duolingo"** dinamiklerini kullanan interaktif bir eğitim uygulaması. Kullanıcılar oyun oynar gibi quizleri tamamladıkça, seviyeleri (level) atladıkça ve bilgilerini test ettikçe; kanser süreçleri, erken teşhisin önemi ve hastalarla empati kurma konularında kritik bilgileri farkında olmadan, eğlenerek öğrenecekler.

---

## 4. Temel Ürün Beklentileri ve Gereksinimler
Projenin temel amacı eğitim materyallerini bir "oyun/uygulama" akışı içinde sunmaktır.

1. **Oyunlaştırma (Gamification):**
   - Uygulama geliştiricinin hayal gücüne bağlı olarak oyunlaştırma elementleriyle (Seri/streak yapma, puan toplama, animasyonlu ilerleme çubukları vs.) zenginleştirilmelidir. Odak noktası "eğlenceli bir öğrenme deneyimi" yaratmaktır.
2. **Esnek İçerik Yönetimi:**
   - LÖSEV ekibinin kolayca yeni soru, içerik, test ve döküman ekleyebilmesi için platformun bilgi mimarisi modüler olmalıdır (Örn: Ders 101, Ders 102 gibi).

## 🛠 Değerlendirme (Review) Süreci İçin Zorunlu Kurallar (MVP Kısıtlamaları)
Öğrenci veya gönüllü ekiplerin yaptığı bu projelerin incelenebilmesi için bazı süreçlerin sadeleştirilmesi kararlaştırılmıştır:

1. **Basit Kimlik Doğrulama (No OAuth):** Google vb. sosyal giriş entegrasyonlarına gerek yoktur. Basit E-posta/şifre tabanlı kayıt veya "Misafir olarak devam et" mimarisi yeterlidir.
2. **Tarayıcı Desteği (Web-Based App):** Proje mobil hedefli olsa bile, incelenmesi için mutlaka **tarayıcı üzerinde (Web build) tıklanarak test edilebilir** yapıda olmalıdır (Örn: React/Next.js pwa, Flutter Web).
3. **Gerçekçi Hazır Veri (Seed Data):** Uygulama başlatıldığında yöneticilerin sistemi test edebilmesi için sahte kullanıcılar ve örnek kanser/lösemi bilinçlendirme testleri veritabanına hazır oluşturulmuş şekilde gelmelidir. Boş bir sayfa ile karşılaşılmamalıdır.
4. **Tek Komutla Dağıtım:** Geliştiriciler yerel ortam bağımlılıklarından kurtulmak için projeyi tek bir **Docker (`docker-compose up`)** komutu veya `npm run dev` komutu ile tüm bileşenleriyle çalışabilir halde teslim etmelidirler.
