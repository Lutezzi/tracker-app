# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.
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
    git clone https://github.com/kullaniciadiniz/calorie-tracker-app.git
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