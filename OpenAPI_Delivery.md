# OpenAPI Tasarımı Ödevi Teslim Raporu

## 👤 Öğrenci Bilgileri
- **Ad Soyad**: Ertunga Yusuf Ocak
- **Öğrenci Numarası**: 170422028


---

## 📂 OpenAPI YAML Dosyası

- **openapi.yaml** dosyası, projeye dahil edilmiştir.
- Swagger Editor ile test edilip doğrulama yapılmıştır.

### 🔗 GitHub Repo Linki
https://github.com/ErtungaYusuf/openapi-design


---

## 📝 API Açıklaması

API’de üç temel varlık yer almaktadır:
- 'books'
- 'students'
- 'loans'


Her varlık için CRUD işlemleri sağlanmıştır:
- 'GET', 'POST', 'PUT', 'DELETE' endpoint'leri kitaplar ve öğrenciler için
- 'POST /loans` ve 'PATCH /loans/{id}/return' ile kitap ödünç alma ve iade işlemleri


Yapıda kullanılan başlıca bölümler:
- 'components/schemas': Tüm veri modelleri tanımlandı. UUID, email, date gibi formatlar belirtildi.
- 'parameters': 'page', 'size', 'id' gibi query ve path parametreleri kullanıldı.
- 'responses`: 200, 201, 400, 404 ve 500 HTTP durum kodları kullanıldı.
- 'example`: `POST /books` endpoint’inde örnek veri eklendi.
- 'GET /books' endpoint’inde sayfalama ('page','size') desteklenmektedir.


---

## 🧪 Test Notları

Swagger Editor üzerinde başarıyla test edilmiştir:

- 'GET /books' çağrısında kitapların listesi döner.
- 'POST /students' ile yeni öğrenci eklenebilir.
- 'PATCH /loans/{id}/return' ile kitap iade edilir.
- Hatalı veri gönderildiğinde '400 Bad Request' dönmektedir.


---

## 📌 Ek Açıklamalar

- API, OpenAPI 3.0.3 standardına uygundur.
- Swagger Editor üzerinde validasyon hatası bulunmamaktadır.
- İsteğe bağlı kullanım içimn 'bearerAuth' ile güvenlik şeması tanımlanmıştır.
