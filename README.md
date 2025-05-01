# Modular Systems Sandbox – Unreal Engine 5.5

*Read this in other languages: [English](#modular-systems-sandbox-unreal-engine-55-english), [Turkish](#modular-systems-sandbox-unreal-engine-55-türkçe)*

## Modular Systems Sandbox – Unreal Engine 5.5 (English)

This sandbox project is a **technical integration testbed** showcasing a suite of custom Unreal Engine systems, all developed with a focus on **modularity**, **performance**, and **production-readiness**. It is not a game, but a **live, interactive environment** where each plugin can be tested and profiled independently.

### Features

- **Enhanced Tick System**: Multithreaded, cache-aware tick batching for components like AI, physics, and movement — enabling spatial and priority-based optimization.
- **Object Recycler**: High-performance actor pooling system that minimizes GC impact and spawn/despawn costs — useful for projectiles, effects, and NPCs.
- **Dismemberment Framework**: Runtime character dismemberment with physics simulation, bone hiding, and custom logic triggers (pre/post events, item drop).
- **Attribute Component System**: Modular gameplay attributes (health, mana, stamina, etc.) with data-driven config, regeneration, threshold delegates, and save/load support.

### Installation

1. **Launch the project in Unreal Engine 5.5+.**
2. In the **Content Browser**, navigate to:
   `Content/Maps/` → `MS_Sandbox_Example`
3. Open the `MS_Sandbox_Example` map and press **Play**.

### Usage

Once in the map, you can:
- Toggle systems using the **in-game UI**
- Interact with test actors (spawn enemies, deal damage, fire projectiles)
- Observe runtime logs and performance metrics for each system

### Project Structure

The project follows a standard structure with plugins and content separated:

```
/Plugins/
  ├── EnhancedTickSystem/
  ├── ObjectRecycler/
  ├── Dismemberment/
  ├── AttributeSystem/
  └── RuntimeVertexPaint/

/Content/
  ├── Maps/
  ├── DemoActors/
  ├── UI/
  └── FX/
```

Each plugin located under `/Plugins/` is included as a **Git submodule** for easy reuse across projects. You can update or decouple them from this sandbox without altering their source. The `/Content/` directory contains example maps, actors, UI elements, and effects specific to this sandbox environment.

### Performance Recommendations

- Use the in-game profiler to monitor performance impacts of each system
- Toggle systems individually to isolate performance characteristics
- The sandbox is optimized for development profiling rather than shipping performance
- Consider your target platform requirements when deciding which systems to implement

### Note

This sandbox is designed as a development tool and technical demonstration. While the individual plugins are production-ready, the sandbox itself is meant for testing and not intended to be shipped as a final product.

### License

All code and content in this project is provided under the [MIT License](LICENSE).
Use freely in commercial or personal Unreal Engine projects.

### Technical Details

#### System Integration

Each system is designed with minimal dependencies on other systems, allowing them to be used independently. However, they are also built with integration points to enhance each other when used together.

#### Performance Profiling

The sandbox includes built-in performance monitoring tools to help evaluate the impact of each system under various conditions and load scenarios.

#### Platforms

All systems have been tested on Windows, Mac, and consoles (where applicable). Mobile performance may vary and specific optimizations may be required.

#### Plugin Design

The plugins follow Unreal Engine's recommended architecture patterns and can be enabled/disabled at runtime through the project settings.

---

## Modular Systems Sandbox – Unreal Engine 5.5 (Türkçe)

Bu sandbox projesi, **modülerlik**, **performans** ve **üretime hazırlık** odaklı geliştirilen özel Unreal Engine sistemlerini sergileyen bir **teknik entegrasyon test ortamıdır**. Bu bir oyun değil, her eklentinin bağımsız olarak test edilip profillenebileceği **canlı, interaktif bir ortamdır**.

### Özellikler

- **Enhanced Tick System**: Çok iş parçacıklı (multithreaded), önbellek bilinçli tick gruplandırması sunan, AI, fizik ve hareket bileşenleri için — mekansal ve öncelik tabanlı optimizasyon sağlar.
- **Object Recycler**: GC etkisini ve spawn/despawn maliyetlerini en aza indiren yüksek performanslı actor havuzlama sistemi — mermi, efekt ve NPC'ler için kullanışlıdır.
- **Dismemberment Framework**: Fizik simülasyonu, kemik gizleme ve özel mantık tetikleyicileri (ön/son olaylar, eşya düşürme) içeren çalışma zamanı karakter parçalama sistemi.
- **Attribute Component System**: Veri odaklı yapılandırma, rejenerasyon, eşik delegeleri ve kaydetme/yükleme desteği ile modüler gameplay özellikleri (sağlık, mana, dayanıklılık, vb.).

### Kurulum

1. **Unreal Engine 5.5+ içinde projeyi başlatın.**
2. **Content Browser** içinde şu yola gidin:
   `Content/Maps/` → `MS_Sandbox_Example`
3. `MS_Sandbox_Example` haritasını açın ve **Play** tuşuna basın.

### Kullanım

Haritaya girdikten sonra şunları yapabilirsiniz:
- **Oyun içi UI** kullanarak sistemleri açıp kapatabilirsiniz
- Test aktörleri ile etkileşime geçebilirsiniz (düşman spawn etme, hasar verme, mermi atma)
- Her sistem için çalışma zamanı loglarını ve performans metriklerini gözlemleyebilirsiniz

### Proje Yapısı

Proje, plugin'ler ve içerik ayrı tutulacak şekilde standart bir yapı izler:

```
/Plugins/
  ├── EnhancedTickSystem/
  ├── ObjectRecycler/
  ├── Dismemberment/
  ├── AttributeSystem/
  └── RuntimeVertexPaint/

/Content/
  ├── Maps/
  ├── DemoActors/
  ├── UI/
  └── FX/
```

`/Plugins/` altında bulunan her plugin, projeler arasında kolay yeniden kullanım için **Git submodule** olarak eklenmiştir. Bunları, kaynaklarını değiştirmeden bu sandbox'tan güncelleyebilir veya ayırabilirsiniz. `/Content/` dizini bu sandbox ortamına özel örnek haritaları, aktörleri, UI elemanlarını ve efektleri içerir.

### Performans Önerileri

- Her sistemin performans etkisini izlemek için oyun içi profiler'ı kullanın
- Performans özelliklerini izole etmek için sistemleri tek tek açıp kapatın
- Sandbox, yayın performansından ziyade geliştirme profili için optimize edilmiştir
- Hangi sistemleri uygulamaya karar verirken hedef platform gereksinimlerinizi göz önünde bulundurun

### Not

Bu sandbox, bir geliştirme aracı ve teknik gösteri olarak tasarlanmıştır. Tek tek eklentiler üretime hazır olsa da, sandbox'ın kendisi test amaçlıdır ve nihai bir ürün olarak yayınlanması amaçlanmamıştır.

### Lisans

Bu projedeki tüm kod ve içerik [MIT License](LICENSE) altında sağlanmaktadır.
Ticari veya kişisel Unreal Engine projelerinde serbestçe kullanabilirsiniz.

### Teknik Detaylar

#### Sistem Entegrasyonu

Her sistem, bağımsız olarak kullanılabilmeleri için diğer sistemlere olan bağımlılıkları en aza indirecek şekilde tasarlanmıştır. Bununla birlikte, birlikte kullanıldıklarında birbirlerini geliştirmek için entegrasyon noktaları ile inşa edilmişlerdir.

#### Performans Profili

Sandbox, her sistemin çeşitli koşullarda ve yük senaryolarında etkisini değerlendirmeye yardımcı olmak için yerleşik performans izleme araçları içerir.

#### Platformlar

Tüm sistemler Windows, Mac ve konsollar (uygun olduğu durumlarda) üzerinde test edilmiştir. Mobil performans değişebilir ve belirli optimizasyonlar gerekebilir.

#### Plugin Tasarımı

Eklentiler, Unreal Engine'in önerilen mimari modellerini takip eder ve proje ayarları aracılığıyla çalışma zamanında etkinleştirilebilir/devre dışı bırakılabilir.
