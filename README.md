# PhishingAI
Bu repository, TensorFlow ve Keras kullanılarak oluşturulmuş bir derin öğrenme modelini içerir. Model, e-posta metinlerini analiz ederek 'Güvenli E-posta' ve 'Phishing E-posta' olarak sınıflandırır. Model eğitimi, tahmini ve gerçek zamanlı kullanıcı girişi ile etkileşim özellikleri sağlanmaktadır.


##Bağımlılıkların İthal Edilmesi ve Google Drive Bağlantısı
Google Drive, veri dosyalarına ve model dosyalarına erişim için bağlanır.
Gerekli kütüphaneler (numpy, pandas, keras, sklearn, joblib, tensorflow) ithal edilir. Bu kütüphaneler, veri işleme, model oluşturma ve eğitim işlemleri için kullanılır.


##Veri Yüklenmesi ve Ön İşleme
Phishing_Email.csv dosyasından e-posta verileri yüklenir.
Eksik değerler boş stringlerle doldurulur.
"Email Type" sütunu sayısal değerlere (0 ve 1) dönüştürülür.


##Veri Hazırlığı ve Tokenizasyon
Metin verileri Tokenizer ile sayısallaştırılır ve ardından sabit uzunlukta dizilere dönüştürülür (pad_sequences kullanılarak).
Eğitim ve test verileri olarak ayrılır.


##Model Tanımı ve Eğitimi
Sequential model, Embedding, SimpleRNN ve Dense katmanları ile oluşturulur.
Model, kategorik çapraz entropi kaybı ve doğruluk metrikleri ile derlenir ve eğitilir.
Model, daha sonra kullanılmak üzere diske kaydedilir.


##Model Değerlendirme
Test veri seti üzerinde modelin performansı değerlendirilir ve kayıp (loss) ile doğruluk (accuracy) değerleri yazdırılır.

##Gerçek Zamanlı Tahmin
Kullanıcıdan sürekli olarak e-posta girişi alınır.
Giriş metni model tarafından değerlendirilir ve e-postanın "Güvenli" veya "Phishing" olup olmadığına dair bir tahminde bulunulur.
Tahminin güvenilirlik derecesi (confidence) hesaplanır ve gösterilir.

##Programın Güvenli Sonlandırılması
Program, kullanıcı Ctrl+C ile kesintiye uğrattığında uygun bir mesaj ile sonlandırılır.



###Bu yazılım, metin sınıflandırma problemlerini çözmek için tipik bir derin öğrenme iş akışı gösterilir ve gerçek dünyada spam veya phishing tespiti gibi uygulamalar için temel teşkil edebilir.






