# Calorie Tracker App (NutriFlow) 🍏

**Calorie Tracker App**, **React Native (Expo)** ve **TypeScript** ile geliştirilmiş modern, yapay zeka destekli bir beslenme takip uygulamasıdır. Kullanıcıların günlük kalori alımını takip etmesine, makro besinleri (protein, karbonhidrat, yağ) izlemesine ve sadece fotoğraf çekerek yemekleri analiz etmesine yardımcı olur.

## ✨ Özellikler

- **📸 AI Yemek Tarayıcısı**: Kameranızla yemeğin fotoğrafını çekin, yapay zeka anında analiz etsin.
  - *Mevcut Durum:* API maliyeti oluşturmaması için şu anda "Gelişmiş Simülasyon Modu" (gerçekçi veri simülasyonu) ile çalışmaktadır.
  - *Hazır:* Google Gemini veya OpenAI Vision API entegrasyonuna uygun yapıdadır.
- **📊 İnteraktif Gösterge Paneli (Dashboard)**:
  - Anlık Kalori, Protein, Karbonhidrat ve Yağ takibi.
  - Görsel ilerleme çubukları ve günlük özetler.
- **📅 Takvim Geçmişi**: Beslenme alışkanlıklarınızı geriye dönük inceleyebileceğiniz detaylı takvim görünümü.
- **🥪 Yemek Detayları**: Tükettiğiniz yemeklerin içindeki malzemeleri ve besin değerlerini detaylıca görüntüleyin.
- **👤 Kişiselleştirilmiş Profil**:
  - Boy, kilo, yaş ve aktivite seviyenize göre otomatik **BMR (Bazal Metabolizma Hızı)** ve **TDEE (Günlük Enerji İhtiyacı)** hesaplaması.
  - Kilo verme, koruma veya kas yapma hedeflerine göre özelleştirme.
- **🎨 Modern Arayüz (UI/UX)**:
  - Akıcı animasyonlar ve şık tasarım.
  - **Karanlık Mod (Dark Mode)** ve **Aydınlık Mod (Light Mode)** desteği (Sistemle senkronize).
- **💾 Çevrimdışı Kayıt**: Tüm verileriniz (yemekler, hedefler, ayarlar) cihazınızın hafızasında **AsyncStorage** ile güvenle saklanır.

## 🛠️ Kullanılan Teknolojiler

- **Framework**: [Expo](https://expo.dev/) (React Native)
- **Dil**: [TypeScript](https://www.typescriptlang.org/)
- **Navigasyon**: [Expo Router](https://docs.expo.dev/router/introduction/) (Dosya tabanlı yönlendirme)
- **Durum Yönetimi (State Management)**: React Context API
- **Depolama**: AsyncStorage
- **İkonlar**: Expo Symbols / Ionicons

## 🚀 Kurulum ve Başlangıç

### Gereksinimler

- Bilgisayarınızda [Node.js](https://nodejs.org/) kurulu olmalıdır.
- Telefonunuzda **Expo Go** uygulaması veya bilgisayarınızda bir Android/iOS Emülatörü bulunmalıdır.

### Adımlar

1.  **Projeyi Klonlayın**
    ```bash
    git clone https://github.com/kullaniciadiniz/tracker-app.git
    cd nutriflow-tracker
    ```

2.  **Paketleri Yükleyin**
    ```bash
    npm install
    ```

3.  **Uygulamayı Başlatın**
    ```bash
    npx expo start
    ```

4.  **Cihazda/Emülatörde Çalıştırın**
    - **Fiziksel Cihaz:** Terminalde çıkan QR kodu **Expo Go** uygulaması ile okutun.
    - **Emülatör:** iOS simülatörü için `i`, Android emülatörü için `a` tuşuna basın.

## 🤖 Yapay Zeka Ayarları (Bilgi)

Uygulama, geliştirme aşamasında API ücreti çıkmaması için varsayılan olarak **Simülasyon Modu**'nda çalışır.

Gerçek yapay zeka analizini (örneğin Google Gemini) aktif etmek isterseniz:
1.  `services/FoodAnalysisService.ts` dosyasını açın.
2.  `MOCK_MODE` (veya benzeri kontrol bayrağını) `false` yapın.
3.  Kendi API anahtarınızı `.env` dosyasına ekleyin.
