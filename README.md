# Future User

Future User is the end-user desktop client for joining the Future Chain network. This repository contains the user app and the node runtime it needs. It does not include the Future Ecosystem Admin interface or its source.

## Current downloads

- **Windows x64 portable:** `Future-User-1.0.1-win-x64.zip` — SHA-256: `dd317659edd316fe15a3e25d964455b6b6a3dfcc60acb9207e33c005af8cb3be`
- **Source:** `Future-User-1.0.1-source.zip` — SHA-256: `fe036cc91cc3cc7f26546313458fa1459e0f0433c660233309b09919378d9da4`

These files are prepared as GitHub Release assets; the release URLs will be added after the repository is connected and the public release is created.

## Platform support

| Platform | Current status | Notes |
| --- | --- | --- |
| Windows x64 | Built | Portable x64 release is available. |
| Linux x64 | Not built | A real Linux build and runtime validation are required before publishing a download. |
| macOS Intel / Apple silicon | Not built | A real macOS build, signing and runtime validation are required. |
| 2010-era Mac running macOS 12 or earlier | Unsupported by this build | This app uses Electron 45.2.3. Electron 44 and later require macOS 13 Ventura or later. Downgrading the runtime to target older macOS would leave a security-sensitive wallet/node app on an unsupported Chromium runtime. |
| Legacy 32-bit Linux | Unsupported by this build | Current Electron releases are 64-bit only. |

For older computers, a browser-based light client is a separate deliverable. It must be built after the production node exposes a verified mining-work and submission endpoint; this repository does not claim that browser mining is live.

## Build

On Windows x64 with Node.js 24:

```powershell
npm ci --prefix vendor/FutureChain
npm ci --prefix future-user
npm --prefix future-user run dist
```

The current build target is Windows x64 only. Linux and macOS targets must be added and verified on their supported build runners before their artifacts are published.

## Security

- Never commit `.env` files, wallet data, seed phrases, private keys, RPC bearer tokens, or local node data.
- Releases are distributed as separate assets; verify their SHA-256 hashes before use.
- The source contains only the user client and its required chain-node runtime; no Admin.exe UI source is included.

## Dil / Язык / Dil

### Azərbaycan dili
Future User — Future Chain-ə qoşulmaq üçün istifadəçi masaüstü tətbiqidir. Hazırda yoxlanmış yükləmə yalnız Windows x64 üçündür. Linux və macOS faylları real build və sınaqdan sonra əlavə ediləcək. 2010-cu illərin köhnə Mac kompüterləri bu Electron versiyası ilə dəstəklənmir; onlar üçün ayrıca brauzer əsaslı yüngül qoşulma tətbiqi tələb olunur.

### Türkçe
Future User, kullanıcıların Future Chain ağına katılması için masaüstü uygulamasıdır. Şu anda doğrulanmış indirme yalnızca Windows x64 içindir. Linux ve macOS dosyaları gerçek derleme ve test sonrasında eklenecektir. 2010 dönemi eski Mac'ler bu Electron sürümüyle desteklenmez; bu cihazlar için ayrı bir tarayıcı tabanlı hafif bağlantı istemcisi gerekir.

### Русский
Future User — настольное приложение для подключения пользователей к сети Future Chain. Сейчас проверена только версия для Windows x64. Сборки Linux и macOS появятся после реальной сборки и проверки. Старые Mac начала 2010-х не поддерживаются этой версией Electron; для них нужен отдельный облегчённый клиент в браузере.

