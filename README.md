# Çevrimiçi Ödeme Dolandırıcılığı Tespiti: Random Forest ve Regresyon Analizi

[Fraud Detection]([[images/fraud_detection.png](https://images.squarespace-cdn.com/content/v1/5d242dd8a10ed400017e7a33/1582505122015-PXLJEO8XGS7U06D2YCL7/CreditCardFraudDetection.png?format=2500w)](https://images.squarespace-cdn.com/content/v1/5d242dd8a10ed400017e7a33/1582505122015-PXLJEO8XGS7U06D2YCL7/CreditCardFraudDetection.png))

## Proje Açıklaması

Bu proje, çevrimiçi ödeme dolandırıcılığını tespit etmek için geliştirilen bir makine öğrenimi modelini içermektedir. Çevrimiçi ödemeler, hem bireysel kullanıcılar hem de işletmeler için önemli bir risk taşımaktadır. Dolandırıcılık faaliyetlerinin artmasıyla birlikte, etkili tespit yöntemlerinin geliştirilmesi kritik hale gelmiştir. Bu çalışma, dolandırıcılık tespitine yönelik olarak Random Forest ve regresyon analizi algoritmalarının entegrasyonunu hedeflemektedir.

## Kullanılan Teknolojiler
- Python
- Scikit-Learn
- Pandas
- Matplotlib

## Kullanılan Algoritmalar

### Gözetimli Öğrenme Nedir?

Gözetimli öğrenme, modelin etiketli verilerle eğitilmesi sürecini ifade eder. Bu yöntemde, model, giriş verileri ile birlikte doğru çıkış verilerini kullanarak öğrenir. Model, eğitim sırasında öğrendiği bilgileri, daha önce görmediği veriler üzerinde tahmin yapmak için kullanır. Gözetimli öğrenme, özellikle sınıflandırma ve regresyon problemlerinde yaygın olarak kullanılmaktadır.

### Regresyon Analizi

Regresyon analizi, bir bağımlı değişken ile bir veya daha fazla bağımsız değişken arasındaki ilişkiyi modellemek için kullanılan istatistiksel bir yöntemdir. Bu yöntem, dolandırıcılık tespiti bağlamında, dolandırıcılığı etkileyen faktörlerin belirlenmesine yardımcı olur. Örneğin, işlem tutarı, işlem türü gibi değişkenler dolandırıcılığı etkileyen önemli faktörler olabilir. Regresyon analizi, bu değişkenlerin dolandırıcılık durumu üzerindeki etkisini nicel olarak değerlendirmeye imkan tanır.

### Random Forest Algoritması

Random Forest, birçok karar ağacının birleşiminden oluşan bir topluluk (ensemble) öğrenme yöntemidir. Her bir karar ağacı, eğitim verilerinin rastgele bir alt kümesi üzerinde eğitilir. Bu, modelin daha dayanıklı ve genelleştirilmiş sonuçlar üretmesini sağlar. Random Forest, sınıflandırma ve regresyon görevlerinde yüksek doğruluk oranları sunar ve aşırı uyum (overfitting) riskini azaltır. Bu çalışma kapsamında, dolandırıcılık tespitinde Random Forest algoritmasının kullanılması, etkili bir model oluşturmayı hedefler.

## Proje Adımları

1. **Veri Setinin Yüklenmesi**: 
   - Çevrimiçi ödeme dolandırıcılığına dair veriler, CSV formatında bir dosyadan yüklenir. Veri seti, işlem özelliklerini ve dolandırıcılık etiketlerini içerir.

2. **Veri Ön İşleme**:
   - Eksik değerlerin ve aykırı değerlerin yönetimi yapılır.
   - Gereksiz özellikler (örn. kullanıcı kimlikleri) veri setinden çıkarılır.
   - Kategorik veriler sayısal verilere dönüştürülür (örneğin, işlem türü).

3. **Veri Setinin Bölünmesi**:
   - Veri seti, eğitim ve test setlerine ayrılır. Eğitim seti modelin eğitimi için kullanılırken, test seti modelin performansını değerlendirmek için kullanılır.

4. **Özellik Ölçeklendirme**:
   - Modelin daha iyi öğrenmesi için, özelliklerin standartlaştırılması amacıyla ölçeklendirme (StandardScaler) uygulanır.

5. **Modelin Eğitilmesi**:
   - Random Forest algoritması kullanılarak model eğitilir. Eğitim sürecinde, model verileri analiz eder ve dolandırıcılığı tespit etmeye yönelik öğrenme sürecini gerçekleştirir.

6. **Tahmin ve Değerlendirme**:
   - Test verileri üzerinde tahminler yapılır.
   - Modelin performansı, doğruluk, karışıklık matrisi ve sınıflandırma raporu gibi metriklerle değerlendirilir.

7. **Görselleştirme**:
   - Modelin sonuçları, grafikler ve görselleştirmeler ile sunulur. Gerçek etiketler ile tahmin edilen etiketler arasındaki ilişkiyi görselleştirmek için dağılım grafikleri ve karışıklık matrisleri kullanılır.

## Gelecek Çalışmalar

Gelecek hedefler arasında, Random Forest ve regresyon analizi algoritmalarını birleştirerek bir meta model oluşturmak yer almaktadır. Bu meta model, her iki yöntemin avantajlarını bir araya getirerek dolandırıcılık tespitinde daha iyi sonuçlar elde etmeyi amaçlayacaktır. Ayrıca, modelin performansını artırmak için farklı parametre ayarları ve özellik mühendisliği (feature engineering) teknikleri kullanılabilir.

## Uygulama Senaryoları

- **Finansal Kurumlar**: Bankalar ve ödeme sistemleri, dolandırıcılık tespit sistemlerini geliştirerek müşterilerini koruma altına alabilir.
- **E-Ticaret**: E-ticaret platformları, dolandırıcılık riskini azaltmak için bu tür modelleri kullanabilir.
- **Sigorta Şirketleri**: Sigorta şirketleri, dolandırıcılığı tespit etmek için bu tür analitik çözümleri uygulayabilir.

## Sonuç

Bu proje, çevrimiçi ödeme sistemlerinin güvenliğini artırmak amacıyla önemli bir adım teşkil etmektedir. Kullanılan yöntemler ve elde edilen bulgular, dolandırıcılığı önlemeye yönelik stratejilerin geliştirilmesine katkı sağlayabilir. Elde edilen sonuçlar, finansal sistemlerin güvenliğini artırmak ve kullanıcıların korunmasına yönelik etkili çözümler geliştirmek için değerlendirilecektir.

## Katkıda Bulunma

Bu projeye katkıda bulunmak isterseniz, lütfen bir pull request oluşturun veya sorunlarınızı belirtmek için bir issue açın. Her türlü katkı ve geri bildirim değerlidir!

## Lisans

Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.

## İletişim Bilgileri

Sorularınız veya işbirlikleri için benimle iletişime geçebilirsiniz:

- E-posta: [handekilinc3510@gmail.com]
- GitHub: [handekilinc](https://github.com/handekilinc)
