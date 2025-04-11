# Beymen Login Sayfası Test Otomasyonu

Bu proje, Beymen login sayfası üzerinde **Python**, **Selenium WebDriver** ve **Unittest** kullanarak test otomasyonu gerçekleştirmeyi amaçlar.

## Kullanılan Teknolojiler

- Python 3.x
- Selenium WebDriver
- Unittest
- Allure Reports

## Proje Yapısı

- **`tests/`**  
  Test senaryolarını içeren dosyalar burada bulunur.

- **`pages/`**  
  Login işlemleri gibi sayfa nesnelerini yöneten sınıflar burada yer alır.

- **`reports/`**  
  Testlerin çalıştırılmasının ardından Allure raporları bu dizine kaydedilir.

- **`conftest.py`**  
  Test öncesi ve sonrası genel konfigürasyon işlemleri yapılır.

## Test Senaryoları

- **Başarılı Giriş Testi**:  
  Doğru kullanıcı adı ve şifre ile giriş yapılır.

- **Başarısız Giriş Testi**:  
  Yanlış kullanıcı adı ve şifre ile giriş yapılmaya çalışılır.

- **Boş Alanlar Testi**:  
  Kullanıcı adı ve şifre alanları boş bırakıldığında hata mesajı doğrulanır.

## Kurulum

Gerekli Python kütüphanelerini yüklemek için:

```bash
pip install selenium allure-pytest



## Testlerin Çalıştırılması

Testleri çalıştırmak için aşağıdaki komutu kullanabilirsiniz:

```bash
python -m unittest discover tests



## Raporlama

Testler çalıştırıldığında, **Allure Report** kullanılabilir. Bu, her testin detaylı bir şekilde kaydını tutarak test sonuçlarının görsel bir rapor halinde sunulmasını sağlar. Raporlama aşağıdaki özelliklere sahiptir:

### Allure Raporu Özellikleri

- **Test Durumu**: Testlerin geçip geçmediği kolayca takip edilebilir. Geçen testler yeşil, kalan testler kırmızı renkte gösterilir.
- **Test Detayları**: Test adımları, her adımın sonucu ve her adımın ayrıntıları raporlanır.
- **Ekran Görüntüleri ve Kayıtlar**: Test sırasında elde edilen hata mesajları, ekran görüntüleri ve diğer kayıtlara yer verilebilir.
- **Zaman Verisi**: Her testin ne kadar sürdüğü, testin ne zaman başladığı ve ne zaman tamamlandığı hakkında bilgiler raporlanır.
- **Adım Adım İzleme**: Testler sırasında gerçekleştirilen her adımın ayrıntıları izlenebilir. Her adımda neler yapıldığını görmek için testin içeriğine girilebilir.
- **Hata Detayları**: Test başarısız olduğunda, hata mesajları ve sebepleri detaylı şekilde raporda yer alır.
  
### Allure Raporu Nasıl Çalışır?

1. Testlerin tamamlanmasının ardından Allure raporları oluşturulabilir.
2. Raporlar HTML formatında bir arayüzde görsel olarak sunulabilir.
3. **Allure Report**'u çalıştırarak test sonuçlarını web tarayıcınızda görüntüleyebilirsiniz.

## Test Raporu Görüntüleme

Test çalıştırıldıktan sonra raporlar oluşturulabilir. Raporu görüntülemek için aşağıdaki adımları izleyebilirsiniz:

### Adım 1: Allure Raporu Oluşturma

Testler tamamlandıktan sonra Allure raporunu oluşturmak için şu komutu çalıştırın:

```bash
allure generate reports/ -o allure-report/
