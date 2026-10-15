<div align="center">

# ComfyUI
**The most powerful and modular AI engine for content creation.**


[![Website][website-shield]][website-url]
[![Dynamic JSON Badge][discord-shield]][discord-url]
[![Twitter][twitter-shield]][twitter-url]
[![Matrix][matrix-shield]][matrix-url]
<br>
[![][github-release-shield]][github-release-link]
[![][github-release-date-shield]][github-release-link]
[![][github-downloads-shield]][github-downloads-link]
[![][github-downloads-latest-shield]][github-downloads-link]

[matrix-shield]: https://img.shields.io/badge/Matrix-000000?style=flat&logo=matrix&logoColor=white
[matrix-url]: https://app.element.io/#/room/%23comfyui_space%3Amatrix.org
[website-shield]: https://img.shields.io/badge/ComfyOrg-4285F4?style=flat
[website-url]: https://www.comfy.org/
<!-- Workaround to display total user from https://github.com/badges/shields/issues/4500#issuecomment-2060079995 -->
[discord-shield]: https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2Fcomfyorg%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&logo=discord&logoColor=white&label=Discord&color=green&suffix=%20total
[discord-url]: https://discord.com/invite/comfyorg
[twitter-shield]: https://img.shields.io/twitter/follow/ComfyUI
[twitter-url]: https://x.com/ComfyUI

[github-release-shield]: https://img.shields.io/github/v/release/comfyanonymous/ComfyUI?style=flat&sort=semver
[github-release-link]: https://github.com/comfyanonymous/ComfyUI/releases
[github-release-date-shield]: https://img.shields.io/github/release-date/comfyanonymous/ComfyUI?style=flat
[github-downloads-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/total?style=flat
[github-downloads-latest-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/latest/total?style=flat&label=downloads%40latest
[github-downloads-link]: https://github.com/comfyanonymous/ComfyUI/releases

<img width="1590" height="795" alt="ComfyUI Screenshot" src="https://github.com/user-attachments/assets/36e065e0-bfae-4456-8c7f-8369d5ea48a2" />
<br>
</div>
ComfyUI, her modele, her parametreye ve her çıktıya hükmetmek isteyen görsel profesyoneller için geliştirilmiş yapay zeka üretim motorudur. Güçlü ve modüler düğüm grafiği (node graph) arayüzü, yaratıcıların görsel, video, 3D model, ses ve çok daha fazlasını üretmesini sağlar...
- ComfyUI, en yeni açık kaynaklı son teknoloji modelleri yerel olarak (native) destekler.
- Yerel tüketici donanımlarına odaklanan, dünyadaki açık ara en optimize difüzyon modeli çıkarım (inference) motorudur.
- Son teknoloji asenkron ağırlık akışı (weight streaming) teknolojimiz sayesinde, en büyük açık kaynaklı modelleri bile 4GB vram + 8GB ram gibi düşük donanımlarda nispeten hızlı bir şekilde (GPU işlem gücünüzü doyurarak) çalıştırabilir.
- [Partner düğümleri](https://docs.comfy.org/tutorials/partner-nodes/overview#partner-nodes), Nano Banana, Seedance, Hunyuan3D vb. en iyi kapalı kaynaklı modellere erişim sağlar.
- Windows, Linux ve macOS üzerinde; [masaüstü uygulamamız](https://www.comfy.org/download), [portable kurulumumuz](#installing) ile yerel olarak ya da [bulut](https://www.comfy.org/cloud) üzerinden kullanılabilir.
- En karmaşık iş akışları bile App Mode sayesinde basit bir arayüz üzerinden kullanıma sunulabilir.
- API uç noktalarımız sayesinde üretim hatlarına (production pipeline) sorunsuz bir şekilde entegre olur.

## Başlarken

### Yerel

#### [Masaüstü Uygulaması](https://www.comfy.org/download)
- Başlamanın en kolay yolu.
- Windows ve macOS için mevcut.

#### [Manuel Kurulum](#manual-install-windows-linux)
Tüm işletim sistemlerini ve GPU türlerini (NVIDIA, AMD, Intel, Apple Silicon, Ascend) destekler.

### Bulut

#### [Comfy Cloud](https://www.comfy.org/cloud)
- Yerel donanımı karşılayamayanlar için resmi ücretli bulut sürümümüz.

## Örnekler
ComfyUI'ın neler yapabildiğini [yeni şablon iş akışları](https://comfy.org/workflows) veya eski [örnek iş akışları](https://comfyanonymous.github.io/ComfyUI_examples/) ile görebilirsiniz.

## Özellikler
- Görsel, video, ses, 3D ve metin iş akışlarını kod yazmadan oluşturmak ve yeniden kullanmak için görsel bir düğüm grafiği.
- Yeniden kullanılabilir alt grafikler (subgraph), iş akışı şablonları, App Mode ve iş akışlarını uygulamalara entegre etmek için yerel bir API.
- Asenkron kuyruklama, kısmi grafik yeniden çalıştırma, akıllı VRAM ve RAM yönetimi, model boşaltma (offloading) ve nicemlenmiş (quantized) model desteği ile verimli yerel çalıştırma.
- Geniş yerel model desteği. Bu liste örnek niteliğindedir; bakımı yapılan, kullanıma hazır şablonlar için [iş akışı kütüphanesine](https://comfy.org/workflows/) göz atın.
  - [Görsel üretimi](https://comfy.org/workflows/tag/text-to-image/): Stable Diffusion 1.5, SDXL, SD3.5, Flux.1, Flux.2, Qwen Image, Z-Image, Hunyuan Image 2.1, HiDream, Lumina Image 2.0, Chroma, Anima, LongCat Image, Ideogram 4, Krea 2, MageFlow, Microsoft Lens, PixelDiT, Kandinsky 5 ve Ernie Image.
  - [Görsel düzenleme](https://comfy.org/workflows/tag/image-edit/): Flux Kontext, Flux.2 Klein, Qwen Image Edit, HiDream E1.1 ve O1, OmniGen2, Boogu, JoyImage Edit, MageFlow Edit ve LongCat Image Edit.
  - [Video üretimi](https://comfy.org/workflows/tag/video-generation/): Wan 2.1 ve 2.2, LTX-Video 2 ve 2.3, HunyuanVideo 1.5, Kandinsky 5 Video, CogVideoX, Cosmos Predict2, Bernini-R, SCAIL 2 ve Mochi.
  - [Ses ve video üretimi](https://comfy.org/workflows/): MiniMax H3 ve LTX-AV.
  - [Ses üretimi](https://comfy.org/workflows/tag/text-to-audio/): ACE-Step 1.5, Stable Audio 3, MiniMax Music 3 ve Yue 2.
  - [3D ve görü (vision)](https://comfy.org/workflows/): Hunyuan3D 2.1, TripoSplat, SeedVR2, SUPIR, Depth Anything 3, MoGe, SAM 3 ve 3.1, RT-DETRv4 ve BiRefNet.
  - [Metin üretimi](https://comfy.org/workflows/tag/text-generation/): Gemma 3 ve 4, Qwen3, Qwen3.5 ve Qwen3-VL (çok modlu girdiler dahil).
- Tam checkpoint'leri ya da ayrı difüzyon modellerini, VAE'leri, metin kodlayıcıları (text encoder), LoRA'ları, ControlNet'leri, adaptörleri ve upscaler'ları desteklenen model formatlarından yükleyin.
- Inpainting, outpainting, referans koşullandırma (reference conditioning), maskeler ve kompozitleme, model birleştirme, upscale, kare interpolasyonu, segmentasyon, derinlik tahmini ve medya işleme için yerleşik araçlar.
- İş akışlarını JSON olarak kaydedin ve yükleyin ya da desteklenen üretilmiş medyalardan eksiksiz iş akışlarını ve seed'leri geri getirin.
- Tamamen çevrimdışı çalışır: siz istemedikçe çekirdek (core) hiçbir şey indirmez. İsteğe bağlı ücretli [Comfy API düğümlerini](https://docs.comfy.org/tutorials/api-nodes/overview) devre dışı bırakmak ve tüm yerleşik işlevlerin çevrimdışı kalmasını sağlamak için `--offline`, yalnızca API düğümlerini devre dışı bırakmak için `--disable-partner-nodes` kullanın.
- ComfyUI'ı özel düğümlerle (custom nodes) genişletin
- Ek model konumlarını [`extra_model_paths.yaml`](extra_model_paths.yaml.example) ile yapılandırın.
- Yüksek bit derinliğine sahip görsellerin ve videoların kaydedilmesi ve yüklenmesi desteği: 16 bit PNG görseller, 32 bit EXR, 10 bit AVIF ve daha fazlası desteklenir.
- Çeşitli formatlarda HDR video ve görsellerin kaydedilmesi ve yüklenmesi desteği.


## Sürüm Süreci

ComfyUI, pazartesi gününü hedefleyen haftalık bir sürüm döngüsünü takip eder; ancak model sürümleri veya kod tabanındaki büyük değişiklikler nedeniyle bu sıklıkla değişir. Birbiriyle bağlantılı üç depo vardır:

1. **[ComfyUI Core](https://github.com/comfyanonymous/ComfyUI)**
   - Yaklaşık 2 haftada bir yeni bir ana kararlı sürüm (ör. v0.7.0) yayınlar.
   - v0.4.0'dan itibaren, mevcut kararlı sürüme geri taşınan (backport) düzeltmeler için yama (patch) sürümleri kullanılacaktır.
   - Minör sürümler, master dalından (branch) çıkan sürümler için kullanılacaktır.
   - Geri taşımanın mantıklı olmadığı durumlarda, master dalındaki sürümler için yine de yama sürümleri kullanılabilir.
   - Kararlı sürüm etiketlerinin dışındaki commit'ler çok kararsız olabilir ve birçok özel düğümü bozabilir.
   - Masaüstü sürümünün temelini oluşturur

2. **[Comfy Desktop](https://github.com/Comfy-Org/Comfy-Desktop)**
   - En son kararlı core sürümünü kullanarak yeni bir sürüm derler

3. **[ComfyUI Frontend](https://github.com/Comfy-Org/ComfyUI_frontend)**
   - Her 2+ haftada bir frontend güncellemeleri core deposuna birleştirilir
   - Yaklaşan core sürümü için özellikler dondurulur
   - Bir sonraki sürüm döngüsü için geliştirme devam eder

## Kısayollar

| Tuş Kombinasyonu                   | Açıklama                                                                                                           |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `Ctrl` + `Enter`                      | Mevcut grafiği üretim için kuyruğa ekler                                                                           |
| `Ctrl` + `Shift` + `Enter`              | Mevcut grafiği üretim için kuyruğun en başına ekler                                                                |
| `Ctrl` + `Alt` + `Enter`                | Mevcut üretimi iptal eder                                                                                          |
| `Ctrl` + `Z`/`Ctrl` + `Y`                 | Geri al/Yinele                                                                                                     |
| `Ctrl` + `S`                          | İş akışını kaydet                                                                                                  |
| `Ctrl` + `O`                          | İş akışını yükle                                                                                                   |
| `Ctrl` + `A`                          | Tüm düğümleri seç                                                                                                  |
| `Alt `+ `C`                           | Seçili düğümleri daralt/genişlet                                                                                   |
| `Ctrl` + `M`                          | Seçili düğümleri sessize al/sesini aç (mute/unmute)                                                                |
| `Ctrl` + `B`                           | Seçili düğümleri atla (bypass) (düğüm grafikten kaldırılmış ve kablolar üzerinden yeniden bağlanmış gibi davranır) |
| `Delete`/`Backspace`                   | Seçili düğümleri sil                                                                                               |
| `Ctrl` + `Backspace`                   | Mevcut grafiği sil                                                                                                 |
| `Space`                              | Basılı tutup imleci hareket ettirerek tuvali (canvas) kaydırır                                                     |
| `Ctrl`/`Shift` + `Click`                 | Tıklanan düğümü seçime ekler                                                                                       |
| `Ctrl` + `C`/`Ctrl` + `V`                  | Seçili düğümleri kopyala ve yapıştır (seçili olmayan düğümlerin çıkışlarıyla bağlantıları korunmaz)               |
| `Ctrl` + `C`/`Ctrl` + `Shift` + `V`          | Seçili düğümleri kopyala ve yapıştır (seçili olmayan düğümlerin çıkışlarından yapıştırılan düğümlerin girişlerine bağlantılar korunur) |
| `Shift` + `Drag`                       | Seçili birden fazla düğümü aynı anda taşır                                                                         |
| `Ctrl` + `D`                           | Varsayılan grafiği yükler                                                                                          |
| `Alt` + `+`                          | Tuvali yakınlaştırır                                                                                               |
| `Alt` + `-`                          | Tuvali uzaklaştırır                                                                                                |
| `Ctrl` + `Shift` + LMB + Dikey sürükleme | Tuvali yakınlaştırır/uzaklaştırır                                                                              |
| `P`                                  | Seçili düğümleri sabitler/sabitlemeyi kaldırır                                                                     |
| `Ctrl` + `G`                           | Seçili düğümleri gruplar                                                                                           |
| `Q`                                 | Kuyruğun görünürlüğünü açar/kapatır                                                                                |
| `H`                                  | Geçmişin görünürlüğünü açar/kapatır                                                                                |
| `R`                                  | Grafiği yeniler                                                                                                    |
| `F`                                  | Menüyü gösterir/gizler                                                                                             |
| `.`                                  | Görünümü seçime sığdırır (hiçbir şey seçili değilse tüm grafiğe)                                                   |
| Çift Tıklama LMB                   | Düğüm hızlı arama paletini açar                                                                                    |
| `Shift` + Drag                       | Birden fazla kabloyu aynı anda taşır                                                                               |
| `Ctrl` + `Alt` + LMB                   | Tıklanan yuvadaki (slot) tüm kabloların bağlantısını keser                                                         |

macOS kullanıcıları için `Ctrl` yerine `Cmd` da kullanılabilir

<a id="installing"></a>
# Kurulum

## Windows ve Mac

[Masaüstü uygulamasını](https://comfy.org/download) kullanmanızı şiddetle öneririz:

### [İndirme Bağlantısı](https://comfy.org/download)

Masaüstü uygulaması, yeni kullanıcılar için ComfyUI'ı kullanmanın en kolay ve en iyi yoludur.

## Windows Portable

Windows için, Nvidia GPU'larda ya da yalnızca CPU üzerinde çalışması gereken taşınabilir (portable) bağımsız bir sürüm vardır. Normal kullanıcılar için önerilmez. Normal kullanıcılar yukarıdaki masaüstü uygulamasını kullanmalıdır.

[Doğrudan indirme bağlantısı (nvidia)](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_nvidia.7z)

Yalnızca indirin, [7-Zip](https://7-zip.org) ile veya yeni Windows sürümlerinde Windows gezgini ile çıkarın ve çalıştırın. Küçük modeller için normalde yalnızca checkpoint'leri (devasa ckpt/safetensors dosyaları) şu klasöre koymanız yeterlidir: ComfyUI\models\checkpoints ancak daha büyük modellerin çoğu birden fazla dosyadan oluşur. Hangi alt klasöre koymanız gerektiğini öğrenmek için talimatları takip ettiğinizden emin olun: ComfyUI\models\

Çıkarmakta sorun yaşıyorsanız dosyaya sağ tıklayın -> özellikler -> engellemeyi kaldır (unblock)

Yukarıdaki portable sürüm şu anda python 3.13 ve pytorch cuda 13.0 ile birlikte gelir. Başlamazsa Nvidia sürücülerinizi güncelleyin.

#### Tüm Resmi Portable İndirmeleri:

[AMD GPU'lar için Portable](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_amd.7z)

[Intel GPU'lar için Portable](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_intel.7z)

[Nvidia GPU'lar için Portable](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_nvidia.7z) (20 serisi ve üzerini destekler).

[pytorch cuda 12.6 ve python 3.12 ile Nvidia GPU'lar için Portable](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_nvidia_cu126.7z) (Nvidia 10 serisi ve daha eski GPU'ları destekler, YENİ 20 SERİSİ VE ÜZERİ GPU'LARDA BUNU KULLANMAYIN).

#### Modelleri başka bir arayüz ile ComfyUI arasında nasıl paylaşırım?

Modeller için arama yollarını ayarlamak üzere [yapılandırma dosyasına](extra_model_paths.yaml.example) bakın. Windows bağımsız sürümünde bu dosyayı ComfyUI dizininde bulabilirsiniz. Bu dosyayı extra_model_paths.yaml olarak yeniden adlandırın ve en sevdiğiniz metin düzenleyiciyle düzenleyin.


## [comfy-cli](https://docs.comfy.org/comfy-cli/getting-started)

ComfyUI'ı comfy-cli ile kurabilir ve başlatabilirsiniz:
```bash
pip install comfy-cli
comfy install
```

<a id="manual-install-windows-linux"></a>
## Manuel Kurulum (Windows, Linux)

Python 3.14 çalışır ancak bazı özel düğümlerde sorunlar olabilir. Free threaded (GIL'siz) varyantı çalışır ancak bazı bağımlılıklar GIL'i etkinleştireceği için tam olarak desteklenmez.

Python 3.13 çok iyi desteklenir. 3.13'te bazı özel düğüm bağımlılıklarıyla sorun yaşarsanız 3.12'yi deneyebilirsiniz.

torch 2.7 asgari düzeyde desteklenir, ancak daha yeni bir sürüm kullanmanız şiddetle tavsiye edilir. Nvidia 20 serisi ve üzerinde pytorch'un cu130 veya üzeri bir sürümünü kullanmak zorunludur. Bazı özellikler ve optimizasyonlar yalnızca daha yeni sürümlerde çalışabilir. Genel olarak, 2 haftadan yeni olmadığı sürece, en son cuda sürümüyle birlikte pytorch'un en son ana sürümünü kullanmanızı öneririz. Pytorch sürümünüz 6 aydan eskiyse lütfen güncelleyin.

### Talimatlar:

Bu depoyu git ile klonlayın.

SD checkpoint'lerinizi (devasa ckpt/safetensors dosyaları) şu klasöre koyun: models/checkpoints

VAE'nizi şu klasöre koyun: models/vae


### AMD GPU'lar (Linux)

AMD kullanıcıları, kurulu değilse rocm ve pytorch'u pip ile kurabilir; kararlı sürümü kurmak için komut şudur:

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm7.2```

Bazı performans iyileştirmeleri içerebilecek ROCm 7.2'li nightly sürümünü kurmak için komut şudur:

```pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/rocm7.2```


### AMD GPU'lar (Windows, ROCm 10.0)

AMD'nin [çoklu mimari PyTorch paketlerini](https://rocm.docs.amd.com/projects/ai-ecosystem/en/latest/frameworks/pytorch/install.html) kullanın. `device-*` ekstraları, GPU'nuzun çekirdeklerini (kernel) ve eşleşen ROCm çalışma zamanını otomatik olarak kurar; ayrıca bir HIP SDK kurulumuna gerek yoktur.

Windows 11, güncel bir [AMD grafik sürücüsü](https://www.amd.com/en/support/download/drivers.html) ve 64 bit Python 3.13 kullanın.

Aşağıdaki kurulum komutu, desteklenen tüm GPU'lar için çekirdekleri kurmak üzere `device-all` kullanır. İndirme boyutunu ve disk kullanımını azaltmak için isteğe bağlı olarak `device-all` ifadesinin **her iki** geçtiği yeri de GPU'nuzun hedefiyle değiştirebilirsiniz:

| GPU | Device extra |
| --- | --- |
| RX 9070 / XT, Radeon AI PRO R9700 | `device-gfx1201` |
| RX 9060 / XT | `device-gfx1200` |
| RX 7900 XT / XTX | `device-gfx1100` |
| RX 7700 XT / 7800 XT | `device-gfx1101` |
| RX 7600 / XT | `device-gfx1102` |
| Ryzen AI Max / Max+ (Strix Halo) | `device-gfx1151` |

**Not:** Bu tablo yalnızca örnekleri listeler. Tabloda yer almayan bir GPU yine de desteklenebilir: desteklenen mimariler arasında RDNA 2, RDNA 3, RDNA 3.5 ve RDNA 4 bulunur. Desteklenen tüm hedefler için çekirdekleri kurmak üzere `device-all` ifadesini koruyun. Diğer modeller için AMD'nin [GPU hedef tablosuna](https://github.com/ROCm/TheRock/blob/main/RELEASES.md#gfx-target-lookup-table) ve [ROCm uyumluluk matrisine](https://rocm.docs.amd.com/en/docs-10.0.0/compatibility/compatibility-matrix.html) bakın.

**ROCm 10.0.0 ile PyTorch 2.13:**

```bat
pip install --index-url https://stable.repo.amd.com/rocm/whl-next/ "torch[device-all]==2.13.0+rocm10.0.0" "torchvision[device-all]==0.28.0+rocm10.0.0" "torchaudio==2.11.0.2+rocm10.0.0"
```

### Intel GPU'lar (Windows ve Linux)

Intel Arc GPU kullanıcıları, pip kullanarak torch.xpu destekli yerel PyTorch'u kurabilir. Daha fazla bilgiye [buradan](https://pytorch.org/docs/main/notes/get_start_xpu.html) ulaşabilirsiniz

1. PyTorch xpu'yu kurmak için şu komutu kullanın:

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/xpu```

Bazı performans iyileştirmeleri içerebilecek Pytorch xpu nightly sürümünü kurmak için komut şudur:

```pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/xpu```

### NVIDIA

Nvidia kullanıcıları kararlı pytorch'u şu komutla kurmalıdır:

```pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu130```

Bunun yerine pytorch nightly sürümünü kurmak için komut şudur; performans iyileştirmeleri içerebilir.

```pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu132```

#### Sorun Giderme

"Torch not compiled with CUDA enabled" hatasını alırsanız torch'u şu komutla kaldırın:

```pip uninstall torch```

Ve yukarıdaki komutla yeniden kurun.

<a id="dependencies"></a>
### Bağımlılıklar

Terminalinizi ComfyUI klasörünün içinde açarak bağımlılıkları kurun:

```pip install -r requirements.txt```

Bundan sonra her şey kurulmuş olmalı ve ComfyUI'ı çalıştırmaya geçebilirsiniz.

### Diğerleri:

#### Apple Mac silicon

ComfyUI'ı, yeni sayılabilecek herhangi bir macOS sürümü ile Apple Mac silicon'a (M1, M2, M3 veya M4) kurabilirsiniz.

1. Pytorch nightly'yi kurun. Talimatlar için [Accelerated PyTorch training on Mac](https://developer.apple.com/metal/pytorch/) Apple Developer rehberini okuyun (en son pytorch nightly sürümünü kurduğunuzdan emin olun).
1. Windows ve Linux için olan [ComfyUI manuel kurulum](#manual-install-windows-linux) talimatlarını izleyin.
1. ComfyUI [bağımlılıklarını](#dependencies) kurun. Başka bir Stable Diffusion arayüzünüz varsa [bağımlılıkları yeniden kullanabilirsiniz](#i-already-have-another-ui-for-stable-diffusion-installed-do-i-really-have-to-install-all-of-these-dependencies).
1. ComfyUI'ı `python main.py` komutunu çalıştırarak başlatın

> **Not**: [ComfyUI manuel kurulum](#manual-install-windows-linux) bölümünde anlatıldığı gibi, modellerinizi, VAE'lerinizi, LoRA'larınızı vb. ilgili Comfy klasörlerine eklemeyi unutmayın.

#### Ascend NPU'lar

Ascend Extension for PyTorch (torch_npu) ile uyumlu modeller içindir. Başlamak için, ortamınızın [kurulum](https://ascend.github.io/docs/sources/ascend/quick_install.html) sayfasında belirtilen ön koşulları karşıladığından emin olun. İşte platformunuza ve kurulum yönteminize göre hazırlanmış adım adım bir rehber:

1. Gerekirse, torch-npu Kurulum sayfasında belirtilen Linux için önerilen veya daha yeni çekirdek (kernel) sürümünü kurarak başlayın.
2. Sürücü, firmware ve CANN içeren Ascend Basekit'i, platformunuza özel talimatları izleyerek kurun.
3. Ardından, [Kurulum](https://ascend.github.io/docs/sources/pytorch/install.html#pytorch) sayfasındaki platforma özel talimatlara uyarak torch-npu için gerekli paketleri kurun.
4. Son olarak, Linux için [ComfyUI manuel kurulum](#manual-install-windows-linux) rehberine uyun. Tüm bileşenler kurulduktan sonra ComfyUI'ı daha önce anlatıldığı gibi çalıştırabilirsiniz.

#### Cambricon MLU'lar

Cambricon Extension for PyTorch (torch_mlu) ile uyumlu modeller içindir. İşte platformunuza ve kurulum yönteminize göre hazırlanmış adım adım bir rehber:

1. Cambricon CNToolkit'i, platforma özel talimatları izleyerek kurun: [Kurulum](https://www.cambricon.com/docs/sdk_1.15.0/cntoolkit_3.7.2/cntoolkit_install_3.7.2/index.html)
2. Ardından PyTorch'u (torch_mlu) şu talimatları izleyerek kurun: [Kurulum](https://www.cambricon.com/docs/sdk_1.15.0/cambricon_pytorch_1.17.0/user_guide_1.9/index.html)
3. ComfyUI'ı `python main.py` komutunu çalıştırarak başlatın

#### Iluvatar Corex

Iluvatar Extension for PyTorch ile uyumlu modeller içindir. İşte platformunuza ve kurulum yönteminize göre hazırlanmış adım adım bir rehber:

1. Iluvatar Corex Toolkit'i, platforma özel talimatları izleyerek kurun: [Kurulum](https://support.iluvatar.com/#/DocumentCentre?id=1&nameCenter=2&productId=520117912052801536)
2. ComfyUI'ı `python main.py` komutunu çalıştırarak başlatın


## [ComfyUI-Manager](https://github.com/Comfy-Org/ComfyUI-Manager/tree/manager-v4)

**ComfyUI-Manager**, ComfyUI için özel düğümleri kolayca kurmanızı, güncellemenizi ve yönetmenizi sağlayan bir eklentidir.

### Kurulum (Setup)

1. Manager bağımlılıklarını kurun:
   ```bash
   pip install -r manager_requirements.txt
   ```

2. ComfyUI'ı çalıştırırken `--enable-manager` bayrağı ile manager'ı etkinleştirin:
   ```bash
   python main.py --enable-manager
   ```

### Komut Satırı Seçenekleri

| Bayrak | Açıklama |
|------|-------------|
| `--enable-manager` | ComfyUI-Manager'ı etkinleştirir |
| `--enable-manager-legacy-ui` | Yeni arayüz yerine eski manager arayüzünü kullanır (`--enable-manager`'ı da kapsar) |
| `--disable-manager-ui` | Güvenlik kontrolleri ve zamanlanmış kurulum tamamlama gibi arka plan özelliklerini koruyarak manager arayüzünü ve uç noktalarını devre dışı bırakır (`--enable-manager` gerektirir) |


# Çalıştırma

```python main.py```

### ROCm tarafından resmi olarak desteklenmeyen AMD kartlar için

Sorun yaşarsanız şu komutla çalıştırmayı deneyin:

6700, 6600 ve belki diğer RDNA2 veya daha eski kartlar için: ```HSA_OVERRIDE_GFX_VERSION=10.3.0 python main.py```

AMD 7600 ve belki diğer RDNA3 kartlar için: ```HSA_OVERRIDE_GFX_VERSION=11.0.0 python main.py```

### AMD ROCm İpuçları

İşleri hızlandırabilecek `PYTORCH_TUNABLEOP_ENABLED=1` ortam değişkenini ayarlamayı deneyebilirsiniz; bunun bedeli çok yavaş bir ilk çalıştırmadır.

# Notlar

Yalnızca tüm doğru girdilere sahip bir çıktısı olan grafik parçaları çalıştırılır.

Yalnızca bir çalıştırmadan diğerine değişen grafik parçaları çalıştırılır; aynı grafiği iki kez gönderirseniz yalnızca ilki çalıştırılır. Grafiğin son kısmını değiştirirseniz yalnızca değiştirdiğiniz kısım ve ona bağlı olan kısım çalıştırılır.

Üretilmiş bir png'yi web sayfasına sürükleyip bırakmak veya yüklemek, onu oluşturmak için kullanılan seed'ler dahil tüm iş akışını size verir.

Bir kelimenin ya da ifadenin vurgusunu değiştirmek için () kullanabilirsiniz, örneğin: (good code:1.2) veya (bad code:0.8). () için varsayılan vurgu 1.1'dir. Gerçek isteminizde () karakterlerini kullanmak için bunları \\( veya \\) şeklinde kaçırın (escape).

Dinamik/joker (wildcard) istemler için {day|night} kullanabilirsiniz. Bu sözdizimiyle "{wild|card|test}", istemi her kuyruğa eklediğinizde frontend tarafından rastgele "wild", "card" veya "test" ile değiştirilir. Gerçek isteminizde {} karakterlerini kullanmak için bunları şöyle kaçırın: \\{ veya \\}.

Dinamik istemler ayrıca C tarzı yorumları da destekler, örneğin `// comment` veya `/* comment */`.

Bir textual inversion kavramını/embedding'ini metin isteminde kullanmak için, onu models/embeddings dizinine koyun ve CLIPTextEncode düğümünde şu şekilde kullanın (.pt uzantısını atlayabilirsiniz):

```embedding:embedding_filename.pt```


## Yüksek kaliteli önizlemeler nasıl gösterilir?

Önizlemeleri etkinleştirmek için ```--preview-method auto``` kullanın.

Varsayılan kurulum, düşük çözünürlüklü hızlı bir latent önizleme yöntemiyle gelir. [TAESD](https://github.com/madebyollin/taesd) ile daha yüksek kaliteli önizlemeleri etkinleştirmek için [taesd_decoder.pth, taesdxl_decoder.pth, taesd3_decoder.pth ve taef1_decoder.pth](https://github.com/madebyollin/taesd/) dosyalarını indirin ve `models/vae_approx` klasörüne koyun. Kurulduktan sonra ComfyUI'ı yeniden başlatın ve yüksek kaliteli önizlemeleri etkinleştirmek için `--preview-method taesd` ile çalıştırın.

## TLS/SSL nasıl kullanılır?
Şu komutu çalıştırarak kendinden imzalı bir sertifika (paylaşımlı/üretim ortamları için uygun değildir) ve anahtar oluşturun: `openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 3650 -nodes -subj "/C=XX/ST=StateName/L=CityName/O=CompanyName/OU=CompanySectionName/CN=CommonNameOrHostname"`

TLS/SSL'i etkinleştirmek için `--tls-keyfile key.pem --tls-certfile cert.pem` kullanın; uygulamaya artık `http://...` yerine `https://...` ile erişilebilir olacaktır.

> Not: Windows kullanıcıları, yukarıdaki örnek komutu çalıştırmak için [alexisrolland/docker-openssl](https://github.com/alexisrolland/docker-openssl) veya [3. parti ikili dağıtımlardan](https://wiki.openssl.org/index.php/Binaries) birini kullanabilir.
<br/><br/>Bir konteyner kullanıyorsanız, `-v` ile bağlanan birimin (volume mount) göreli bir yol olabileceğini unutmayın; yani `... -v ".\:/openssl-certs" ...` komut isteminizin veya powershell terminalinizin geçerli dizininde anahtar ve sertifika dosyalarını oluşturur.

## Destek ve geliştirici kanalı

[Discord](https://comfy.org/discord): #help veya #feedback kanallarını deneyin.

[Matrix alanı: #comfyui_space:matrix.org](https://app.element.io/#/room/%23comfyui_space%3Amatrix.org) (discord gibi ama açık kaynaklı).

Ayrıca bakın: [https://www.comfy.org/](https://www.comfy.org/)

> _psst — işe alım yapıyoruz!_ ComfyUI'ı birlikte geliştirelim: [comfy.org/careers](https://www.comfy.org/careers)

## Frontend Geliştirme

15 Ağustos 2024 itibarıyla yeni bir frontend'e geçiş yaptık; artık ayrı bir depoda barındırılıyor: [ComfyUI Frontend](https://github.com/Comfy-Org/ComfyUI_frontend). Derlenmiş JS dosyaları (TS/Vue'dan) [pypi](https://pypi.org/project/comfyui-frontend-package) üzerinde yayınlanır ve ComfyUI'a bir bağımlılık olarak kurulur.

### Sorun Bildirme ve Özellik Talep Etme

Frontend ile ilgili her türlü hata, sorun veya özellik talebi için lütfen [ComfyUI Frontend deposunu](https://github.com/Comfy-Org/ComfyUI_frontend) kullanın. Bu, frontend'e özgü konuları daha verimli yönetmemize ve ele almamıza yardımcı olur.

### En Son Frontend'i Kullanma

Yeni frontend artık ComfyUI için varsayılandır. Ancak lütfen şunlara dikkat edin:

1. Ana ComfyUI deposundaki frontend iki haftada bir güncellenir.
2. Günlük sürümler ayrı frontend deposunda mevcuttur.

En güncel frontend sürümünü kullanmak için:

1. En son günlük sürüm için ComfyUI'ı şu komut satırı argümanıyla başlatın:

   ```
   --front-end-version Comfy-Org/ComfyUI_frontend@latest
   ```

2. Belirli bir sürüm için `latest` yerine istediğiniz sürüm numarasını yazın:

   ```
   --front-end-version Comfy-Org/ComfyUI_frontend@1.2.2
   ```

Bu yaklaşım, kararlı iki haftalık sürüm ile en yeni günlük güncellemeler arasında ya da test amacıyla belirli sürümler arasında kolayca geçiş yapmanızı sağlar.

# SSS

### Bunun için hangi GPU'yu almalıyım?

[Bazı öneriler için bu sayfaya bakın](https://github.com/comfyanonymous/ComfyUI/wiki/Which-GPU-should-I-buy-for-ComfyUI)


[See this page for some recommendations](https://github.com/comfyanonymous/ComfyUI/wiki/Which-GPU-should-I-buy-for-ComfyUI)
