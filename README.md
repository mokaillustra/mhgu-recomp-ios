# MHGUiOS Recomp for iOS and iPadOS

<p align="center">
  <img src="https://www.nintendo.com/eu/media/images/10_share_images/games_15/nintendo_switch_4/H2x1_NSwitch_MonsterHunterGenerationsUltimate_image1600w.jpg" alt="Monster Hunter Generations Ultimate banner" width="100%">
</p>

An unofficial iOS/iPadOS port of **MHGUiOS Recomp**, maintained by **Moka Illustra**. This project brings the `gu-native` runtime and iOS platform work together for iPhone and iPad.

Port iOS/iPadOS tidak resmi dari **MHGUiOS Recomp**, dikelola oleh **Moka Illustra**, untuk dimainkan di iPhone dan iPad.

> This is a community project. It is not affiliated with Nintendo or Capcom, and is not an official release from the upstream authors.

## Download / Unduh

Download the stable IPA from the [MHGUiOS Recomp v1.0.0 release](https://github.com/mokaillustra/mhgu-recomp-ios/releases/tag/v1.0.0). IPA stabil tersedia di [rilis MHGUiOS Recomp v1.0.0](https://github.com/mokaillustra/mhgu-recomp-ios/releases/tag/v1.0.0). The IPA contains the app, **not the game data**. GitHub automatically generates source archives for this release from this tag; the archives contain the full folder structure shown in this repository.

## Requirements / Persyaratan

- An iPhone or iPad running iOS/iPadOS 15 or later.  
  iPhone atau iPad dengan iOS/iPadOS 15 atau lebih baru.
- Your own **Monster Hunter Generations Ultimate v1.4.0** game files.  
  File game **Monster Hunter Generations Ultimate v1.4.0** milikmu sendiri.
- Enough free device storage for the game data and app.  
  Ruang penyimpanan yang cukup untuk data game dan aplikasi.
- An iOS app installer that can sign and install IPA files, or [LiveContainer](https://livecontainer.github.io/docs/installation) set up according to its official guide.  
  Aplikasi pemasang iOS yang bisa memasang IPA, atau [LiveContainer](https://livecontainer.github.io/docs/installation) yang sudah disiapkan mengikuti panduan resminya.

## Increased Memory Limit Entilement for Device with 4GB of RAM or Lower

- iRAM https://github.com/NexSideloading/iRAM-Plus
  This is a newer, actively maintained fork of GetMoreRam featuring a cleaner interface and step-by-step setup wizard. In addition to Increased Memory Limit,
  it also lets you toggle Extended Virtual Addressing for heavy emulators

- GetMoreRAM https://github.com/hugeBlack/GetMoreRam
  This is the original open-source utility created by one of LiveContainer's contributors. It performs the same Apple ID entitlement injection, though most users have migrated to iRAM+ for its updated UI.

  Both tools connect to your Apple ID developer profile to patch the memory entitlement onto your sideloaded apps without needing a PC or Mac.

## Installation instructions / Petunjuk instalasi

<details>
<summary>English</summary>

> **Using a free Apple account?** If SideStore's active-app limit is full or you want to save app slots, we recommend installing the official [LiveContainer + SideStore setup](https://livecontainer.github.io/docs/installation) and importing this IPA as a guest app. You can use [iLoader](https://iloader.app/) as the desktop installer; follow the [iLoader steps in the LiveContainer guide](https://livecontainer.github.io/docs/installation/lc_sidestore) and select **LiveContainer+SideStore**. Use the latest iLoader version. Check SideStore's current guide for account limits. LiveContainer is optional with a paid developer account.

### Install as a regular app

1. Download the IPA from the release linked above.
2. Import it into a trusted sideloading app such as [AltStore](https://faq.altstore.io/) or [SideStore](https://docs.sidestore.io/), and install it using that app's instructions.
3. If iOS asks you to trust the signing account or enable Developer Mode, follow the prompts from your installer and iOS Settings.
4. Open **MHGUiOS Recomp** once. This creates its visible folder in the Files app.

Sideloaded apps may need to be refreshed or re-signed by the installer. Refer to the installer's current documentation for those steps.

### Run it with LiveContainer

1. Install and configure the official [LiveContainer](https://livecontainer.github.io/docs/installation) build by following its guide.
2. Open LiveContainer, tap **+**, and import the MHGUiOS Recomp IPA.
3. Launch MHGUiOS Recomp once from LiveContainer.
4. To locate its files, long-press the app in LiveContainer, open **Settings → Container**, then tap **Open Data Folder**. Open that container's `Documents` folder.

LiveContainer keeps app data in its own container. Do not put the game data beside the IPA or inside the app bundle. If the Files app does not show the container folder as expected, use the in-game **Settings → System → Game folder** picker and select the folder that directly contains `exefs/` and `romfs/`.

### Add your game files

Use files from your own legally obtained v1.4.0 game copy. Do not upload game files, keys, or generated game code to this repository or share them with the IPA.

On a regular installation, the default location is **Files → On My iPad/iPhone → MHGUiOS Recomp → `data/`**. Under LiveContainer, place `data/` inside the guest app's `Documents` folder. The expected layout is:

```text
Documents/
└── data/
    ├── exefs/
    │   ├── main
    │   ├── main.npdm
    │   └── sdk/                 (if present in your dump)
    └── romfs/
        └── ...                  (all v1.4.0 RomFS folders and files)
```

The `exefs/` and `romfs/` folders must sit directly inside `data/`. The app checks that `exefs/main` is from v1.4.0 and that RomFS is complete (about 35,531 files). If the app opens its missing-files screen, add the files and tap **Check Files Again**.

You can choose another accessible folder from **Settings → System → Game folder**. Select the folder that directly contains `exefs/` and `romfs/`; the change takes effect the next time the game starts.

</details>

<details>
<summary>Bahasa Indonesia</summary>

> **Menggunakan akun Apple gratis?** Jika batas aplikasi aktif SideStore sudah penuh atau kamu ingin menghemat slot aplikasi, kami menyarankan memasang [LiveContainer + SideStore resmi](https://livecontainer.github.io/docs/installation), lalu mengimpor IPA ini sebagai aplikasi guest. Kamu bisa menggunakan [iLoader](https://iloader.app/) sebagai alat pemasangan dari komputer; ikuti [langkah iLoader di panduan LiveContainer](https://livecontainer.github.io/docs/installation/lc_sidestore) dan pilih **LiveContainer+SideStore**. Gunakan iLoader versi terbaru. Periksa panduan SideStore terbaru untuk batas akun. LiveContainer opsional jika kamu memiliki akun Apple Developer berbayar.

### Memasang sebagai aplikasi biasa

1. Unduh IPA dari rilis di atas.
2. Impor IPA ke aplikasi sideload tepercaya seperti [AltStore](https://faq.altstore.io/) atau [SideStore](https://docs.sidestore.io/), lalu pasang mengikuti petunjuk aplikasi tersebut.
3. Jika iOS meminta untuk memercayai akun penanda tangan atau mengaktifkan Developer Mode, ikuti petunjuk dari aplikasi pemasang dan Pengaturan iOS.
4. Buka **MHGUiOS Recomp** satu kali agar foldernya muncul di aplikasi Files.

Aplikasi sideload mungkin perlu diperbarui masa aktifnya atau ditandatangani ulang melalui aplikasi pemasang. Ikuti dokumentasi terbaru aplikasi yang kamu gunakan.

### Menjalankan dengan LiveContainer

1. Pasang dan siapkan build resmi [LiveContainer](https://livecontainer.github.io/docs/installation) mengikuti panduan resminya.
2. Buka LiveContainer, ketuk **+**, lalu impor IPA MHGUiOS Recomp.
3. Jalankan MHGUiOS Recomp satu kali dari LiveContainer.
4. Untuk menemukan folder datanya, tekan lama kartu aplikasi di LiveContainer, buka **Settings → Container**, lalu ketuk **Open Data Folder**. Buka folder `Documents` milik container itu.

LiveContainer menyimpan data aplikasi di containernya sendiri. Jangan menaruh file game di samping IPA atau di dalam bundle aplikasi. Jika folder container tidak terlihat seperti yang diharapkan di Files, gunakan pemilih **Settings → System → Game folder** di dalam game dan pilih folder yang langsung berisi `exefs/` dan `romfs/`.

### Menambahkan file game

Gunakan file dari salinan game v1.4.0 milikmu sendiri yang diperoleh secara sah. Jangan unggah file game, key, atau kode game hasil kompilasi ke repo ini atau membagikannya bersama IPA.

Pada pemasangan biasa, lokasi default-nya adalah **Files → On My iPad/iPhone → MHGUiOS Recomp → `data/`**. Di LiveContainer, letakkan `data/` di dalam folder `Documents` milik aplikasi guest. Susunan yang diharapkan:

```text
Documents/
└── data/
    ├── exefs/
    │   ├── main
    │   ├── main.npdm
    │   └── sdk/                 (jika ada di dump milikmu)
    └── romfs/
        └── ...                  (semua folder dan file RomFS v1.4.0)
```

Pastikan folder `exefs/` dan `romfs/` berada langsung di dalam `data/`. Aplikasi memeriksa apakah `exefs/main` berasal dari v1.4.0 dan apakah RomFS lengkap (sekitar 35.531 file). Jika muncul layar file belum lengkap, tambahkan file yang diperlukan lalu ketuk **Check Files Again**.

Kamu juga bisa memilih folder lain melalui **Settings → System → Game folder**. Pilih folder yang langsung berisi `exefs/` dan `romfs/`; perubahan berlaku setelah game dimulai ulang.

</details>

## Credits and licenses

This iOS fork preserves credit for the projects and contributors it builds on:

- [MHGURecomp](https://github.com/morerokk/MHGURecomp) — original recompiler and runtime.
- [Khorne's `gu-native`](https://github.com/khorne-hub/gu-native) — source project and mobile runtime work.
- [MHGURecomp-iOS](https://github.com/cerroverb/MHGURecomp-iOS) — iOS build and platform reference, including earlier iOS contributions credited in that project.
- iOS integration and this fork are maintained by **Moka Illustra**.

This combined repository does not have one license that replaces the component licenses. Read [LICENSE](LICENSE), [THIRD_PARTY_NOTICES](THIRD_PARTY_NOTICES), [ios/IOS_BASE_MIT_LICENSE.txt](ios/IOS_BASE_MIT_LICENSE.txt), [ios/PORT_NOTICES.txt](ios/PORT_NOTICES.txt), and upstream license terms before using or redistributing code. Preserve each project's notices and obtain any permissions required by those terms.

## Building / Build

The iOS IPA is built by [the GitHub Actions workflow](.github/workflows/build-ios.yml). A successful app build does not supply game data; each player must provide their own compatible files.

IPA iOS dibuat melalui [workflow GitHub Actions](.github/workflows/build-ios.yml). Build aplikasi tidak menyertakan file game; setiap pemain harus menyediakan file kompatibel miliknya sendiri.
