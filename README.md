# OpenShop POS

🇭🇰 OpenShop Android app for **merchants / shop owners** — receive orders, manage products, run in-store checkout (POS).

> **Brand:** OpenShop → opensystem
> **App type:** Merchant-facing
> **Platform:** Android (Kotlin + Jetpack Compose)
> **Backend:** Firebase (opensystem project)
> **Hardware:** Compatible with barcode scanners + receipt printers (Bluetooth)

## 🎯 Purpose

Merchant experience — two main modes:

### 📋 Online Order Reception
- 🛎️ Receive orders from OpenShop Customer app
- ✅ Accept / reject incoming orders
- 📦 Update order status (preparing → ready for pickup)
- 💬 Chat with customer (in-app)
- 📊 Daily / weekly revenue dashboard

### 🛒 In-Store POS (Point of Sale)
- 🏷️ Barcode scan to add product
- 💵 Multi-payment at counter (cash / Octopus / FPS / Stripe)
- 🧾 Print / send digital receipt
- 📉 Stock decrement on sale
- 🚪 Daily end-of-day closing

## 🏗️ Stack

| Layer | Tech |
|---|---|
| Language | Kotlin 1.9+ |
| UI | Jetpack Compose + Material 3 (POS layout optimized for landscape tablets) |
| Network | Retrofit + OkHttp |
| DB | Firebase Firestore + Room offline cache |
| Hardware | Bluetooth barcode scanners, ESC/POS receipt printers, cash drawer |
| Hardware SDK | Android Bluetooth API + USB-Host |
| KYC | Document scan + Firebase Storage + manual review flow |

## 🚀 Building

```bash
studio . &
./gradlew :app:assembleDebug
```

## 📦 Build Pipeline

Each release → `~/Google Drive/openshop-pos/` → Firebase App Distribution → Google Play Internal.

## 🔗 Related Repos

- `gary3159/openshop-customer` — buyer app
- `gary3159/openshop-admin` — platform admin
- `gary3159/opensystem` — umbrella
