<div align="center">

  <a href="https://github.com/sindresorhus/awesome">
    <img width="260" src="https://raw.githubusercontent.com/sindresorhus/awesome/main/media/logo.png" alt="Awesome Logo">
  </a>

  <h1>Harika Self-Hosted Yapay Zeka Ağ Geçitleri (AI Gateways)</h1>

  <p>
    Üretim ortamındaki yapay zeka uygulamaları için kendi sunucunuzda barındırabileceğiniz (self-hosted) LLM ağ geçitleri, API yönlendiricileri, yük dengeleyiciler, yedekleme (fallback) sistemleri ve proxy motorlarının derlenmiş listesi.
  </p>

  <p>
    <a href="https://github.com/sindresorhus/awesome">
      <img src="https://raw.githubusercontent.com/sindresorhus/awesome/refs/heads/main/media/badge.svg" alt="Awesome Rozeti">
    </a>
    <a href="https://github.com/Neighboth/awesome-ai-gateways/stargazers">
      <img src="https://img.shields.io/github/stars/Neighboth/awesome-ai-gateways?style=flat-square&color=blue" alt="Yıldızlar">
    </a>
    <a href="https://github.com/Neighboth/awesome-ai-gateways/network/members">
      <img src="https://img.shields.io/github/forks/Neighboth/awesome-ai-gateways?style=flat-square&color=blue" alt="Forklar">
    </a>
    <a href="https://github.com/Neighboth/awesome-ai-gateways/commits/main">
      <img src="https://img.shields.io/github/last-commit/Neighboth/awesome-ai-gateways?style=flat-square&color=green" alt="Son Taahhüt">
    </a>
    <a href="https://github.com/Neighboth/awesome-ai-gateways/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/Neighboth/awesome-ai-gateways?style=flat-square&color=orange" alt="Lisans">
    </a>
  </p>

</div>

---

Birden fazla yapay zeka modelini yönetmek, istek limitlerini (rate limit) ele almak, maliyetleri optimize etmek ve yüksek erişilebilirlik sağlamak; güvenilir, self-hosted bir yönlendirme altyapısı gerektirir. Bu liste, uygulamanız ile yapay zeka sağlayıcıları (OpenAI, Anthropic, Google Gemini, DeepSeek, Groq, yerel modeller vb.) arasında duracak şekilde tasarlanmış açık kaynaklı ve kendi sunucunuzda çalıştırılabilir çözümleri bir araya getirir.

---

## İçindekiler

- [Self-Hosted Ağ Geçitleri](#self-hosted-ağ-geçitleri)
- [Temel Özellikler Matrisi](#temel-özellikler-matrisi)
- [Katkıda Bulunma](#katkıda-bulunma)

---

## Self-Hosted Ağ Geçitleri

Proxy, jeton (token) yönetimi, istek limitleme ve model yedekleme özellikleri sunan temel açık kaynaklı ve self-hosted projeler.

| Proje | Dil | Demo | Ticari / Faturalandırma | Akıllı Yedekleme | Yük Dengeleme | Dinamik Haritalama | Açıklama |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **[better-new-api](https://github.com/Neighboth/better-new-api)** ![Önerilen](https://img.shields.io/badge/-%C3%96nerilen-brightgreen) ![Beta](https://img.shields.io/badge/-Beta-blue) | Go | [Demo](https://pixrouter.com) | ✅ | ✅ | ✅ | ✅ | Aktif hata düzeltmeleri, performans iyileştirmeleri ve genişletilmiş kanal kararlılığı sunan gelişmiş New-API çatallaması (fork). |
| **[New API](https://github.com/QuantumNous/new-api)** ![Kararlı](https://img.shields.io/badge/-Kararl%C4%B1-red) | Go | - | ✅ | ✅ | ✅ | ✅ | Ticari/satış operasyonları ve kurumsal jeton yönetimi için geliştirilmiş One-API çatallaması. |
| **[LiteLLM](https://github.com/BerriAI/litellm)** | Python | - | ❌ | ✅ | ✅ | ✅ | Sanal anahtar yönetimi ve bütçe takibi ile OpenAI formatında 100'den fazla LLM API'sini çağırın. |
| **[One-API](https://github.com/songquanpeng/one-api)** | Go | - | ✅ | ✅ | ✅ | ✅ | Birden fazla sağlayıcıyı tek bir uç noktada toplamak için OpenAI API yönetim ve yönlendirme platformu. |
| **[Bifrost](https://github.com/maximhq/bifrost)** | Go | - | ❌ | ✅ | ✅ | ✅ | Birleşik OpenAI uyumlu API, çoklu sağlayıcı yönlendirmesi, otomatik hata telafisi, yük dengeleme ve yönetişim kontrolleri sunan yüksek performanslı açık kaynaklı AI ağ geçidi. |
| **[Helicone](https://github.com/Helicone/helicone)** | TypeScript | - | ✅ | ✅ | ✅ | ✅ | Akıllı yönlendirme, yedekleme ve istem (prompt) yönetimi sunan açık kaynaklı LLM gözlemlenebilirlik platformu ve AI ağ geçidi. |
| **[Higress](https://github.com/higress-group/higress)** | C++ / Go | - | ❌ | ✅ | ✅ | ✅ | Wasm eklenti desteği, yük dengeleme ve MCP sunucu barındırma özelliklerine sahip bulut tabanlı, Envoy tabanlı AI API ağ geçidi. |
| **[Kong AI Gateway](https://github.com/Kong/kong)** | Lua / Go | - | ✅ | ✅ | ✅ | ✅ | Çoklu LLM yönlendirmesi, istem dönüştürme ve istek limitleme için AI eklentileriyle genişletilmiş kurumsal API ağ geçidi. |
| **[Portkey Gateway](https://github.com/Portkey-AI/gateway)** | TypeScript | - | ❌ | ✅ | ✅ | ✅ | Tek API, yeniden deneme ve anlamsal önbellekleme (semantic caching) ile 250'den fazla LLM'e yönlendirme sağlayan hızlı AI ağ geçidi. |
| **[Aperture](https://github.com/fluxninja/aperture)** | Go | - | ❌ | ✅ | ✅ | ✅ | LLM iş yükleri için yüksek performanslı dağıtık istek limitleme, önbellekleme ve eşzamanlılık kontrolü proxy'si. |
| **[VoidLLM](https://github.com/voidmind-io/voidllm)** | Go | - | ❌ | ✅ | ✅ | ✅ | Çoklu sağlayıcı yönlendirmesi, yük dengeleme ve jeton kotaları içeren gizlilik odaklı, sıfır bilgi (zero-knowledge) LLM proxy'si. |
| **[9router](https://github.com/decolua/9router)** | TypeScript | - | ❌ | ✅ | ✅ | ✅ | Anahtar dağıtımı sunan açık kaynaklı birleşik AI API ağ geçidi ve model yönlendiricisi. |
| **[LMRouter](https://github.com/LMRouter/lmrouter)** | Go | - | ❌ | ✅ | ✅ | ✅ | Düşük kaynak kullanımına odaklanmış yüksek performanslı, hafif LLM yönlendirme proxy'si. |
| **[RouteLLM](https://github.com/lm-sys/RouteLLM)** | Python | - | ❌ | ✅ | ❌ | ✅ | İstem karmaşıklığına ve maliyet optimizasyonuna göre LLM'leri dinamik olarak sunan ve yönlendiren bir çatı. |

---

## Temel Özellikler Matrisi

Üretim ortamları için self-hosted bir yapay zeka ağ geçidi değerlendirirken veya seçerken şu temel yetenekleri göz önünde bulundurun:

* **Akıllı Yedekleme ve Yeniden Deneme (Smart Fallback & Retry):** İstek zaman aşımına uğradığında, oran limitlerine (429) takıldığında veya 5xx sunucu hatalarıyla karşılaşıldığında yedek modellere veya sağlayıcılara otomatik geçiş yapar.
* **Sistem İstemi ve Parametre Yeniden Yazma (System Prompt & Parameter Rewriting):** İstekleri anında değiştirir (örneğin özel yedekleme başlıkları veya varsayılan sistem istemleri ekler).
* **Yük Dengeleme (Load Balancing):** Trafiği Round Robin, Ağırlıklı veya Gecikme Tabanlı stratejiler kullanarak birden fazla API anahtarına veya ana uç noktaya dağıtır.
* **Jeton ve Maliyet Yönetimi (Token & Cost Management):** Gerçek zamanlı faturalandırma ve bakiye yükleme entegrasyonlarıyla kullanıcı, jeton veya kanal bazında harcamaları takip eder.
* **Dinamik Model Haritalama (Dynamic Model Mapping):** Özel model takma adlarını (ör. `gpt-4o-custom`) şeffaf bir şekilde sağlayıcı uç noktalarına haritalar.

---

## Katkıda Bulunma

Katkılarınızı bekliyoruz! Lütfen bir değişiklik isteği (PR) göndermeden önce yönergeleri okuyun:

1. Çift kayıt oluşturmamak için mevcut girdileri arayın.
2. Proje bağlantılarının aktif olduğundan ve doğrudan self-hosted AI yönlendirme/ağ geçitleri ile ilgili olduğundan emin olun.
3. Yukarıdaki tablo biçimlendirmesine uyun; açıklamaları kısa, olgusal ve tarafsız tutun.

---

*Açık kaynak topluluğu tarafından ❤️ ile sürdürülmektedir.*