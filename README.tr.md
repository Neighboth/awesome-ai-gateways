<div align="center">

  <p>
    <a href="./README.md">English</a> | 
    <b>Türkçe</b>
  </p>

  <a href="https://github.com/sindresorhus/awesome">
    <img width="260" src="https://raw.githubusercontent.com/sindresorhus/awesome/main/media/logo.png" alt="Awesome Logo">
  </a>

  <h1>Harika Self-Hosted AI Gateway'leri</h1>

  <p>
    Üretim ortamındaki yapay zeka uygulamaları için kendi sunucunuzda barındırabileceğiniz (self-hosted) en iyi LLM gateway'leri, API yönlendiricileri, yük dengeleyiciler ve yedekleme (fallback) sistemlerinin derlenmiş listesi.
  </p>

  <p>
    <a href="https://github.com/sindresorhus/awesome">
      <img src="https://raw.githubusercontent.com/sindresorhus/awesome/refs/heads/main/media/badge.svg" alt="Awesome Rozeti">
    </a>
  </p>

</div>

---

Birden fazla yapay zeka modelini yönetmek, istek limitlerini (rate limits) aşmamak, maliyetleri optimize etmek ve yüksek erişilebilirlik sağlamak, güçlü bir self-hosted yönlendirme altyapısı gerektirir. Bu liste; uygulamanız ile yapay zeka sağlayıcıları (OpenAI, Anthropic, Google Gemini, DeepSeek, Groq, yerel modeller vb.) arasında durmak üzere tasarlanmış açık kaynaklı çözümleri toplar.

---

## İçindekiler

- [Self-Hosted Gateway'ler](#self-hosted-gatewayler)
- [Temel Özellik Karşılaştırması](#temel-özellik-karşılaştırması)
- [Katkıda Bulunma](#katkıda-bulunma)

---

## Self-Hosted Gateway'ler

Vekil sunucu (proxy), jeton (token) yönetimi, istek sınırlama ve otomatik yedek modele geçiş sağlayan temel açık kaynaklı projeler.

| Proje | Dil | Demo | Ticari Modül / Billing | Akıllı Fallback | Yük Dengeleme | Dinamik Model Eşleme | Açıklama |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **[better-new-api](https://github.com/Neighboth/better-new-api)** ![Önerilen](https://img.shields.io/badge/-Önerilen-brightgreen) ![Beta](https://img.shields.io/badge/-Beta-blue) | Go | [Demo](https://pixrouter.com) | ✅ | ✅ | ✅ | ✅ | New-API'nin aktif hata düzeltmeleri, performans iyileştirmeleri ve geliştirilmiş kanal kararlılığı sunan cilalanmış forku. |
| **[New API](https://github.com/QuantumNous/new-api)** | Go | - | ✅ | ✅ | ✅ | ✅ | Ticari satış operasyonları ve kurumsal token yönetimi için geliştirilmiş One-API forku. |
| **[LiteLLM](https://github.com/BerriAI/litellm)** | Python | - | ❌ | ✅ | ✅ | ✅ | Sanal anahtar yönetimi ve bütçe takibi ile 100'den fazla LLM API'sini OpenAI formatında çağırın. |
| **[One-API](https://github.com/songquanpeng/one-api)** | Go | - | ✅ | ✅ | ✅ | ✅ | Birden fazla sağlayıcıyı tek bir uç noktada toplayan OpenAI API yönetim ve yönlendirme platformu. |
| **[9router](https://github.com/decolua/9router)** | TypeScript | - | ❌ | ✅ | ✅ | ✅ | Anahtar dağıtımı sunan açık kaynaklı, birleşik yapay zeka API gateway ve model yönlendiricisi. |
| **[LMRouter](https://github.com/LMRouter/lmrouter)** | Go | - | ❌ | ✅ | ✅ | ✅ | Düşük gecikmeli çalışmaya odaklanmış, yüksek performanslı ve hafif LLM yönlendirme vekil sunucusu. |
| **[Bifrost](https://github.com/maximhq/bifrost)** | Go | - | ❌ | ✅ | ✅ | ✅ | Birleşik OpenAI uyumlu API, çoklu sağlayıcı yönlendirmesi, otomatik hata telafisi, yük dengeleme ve yönetişim kontrolleri sunan yüksek performanslı, açık kaynaklı AI gateway. |
| **[Portkey Gateway](https://github.com/Portkey-AI/gateway)** | TypeScript | - | ❌ | ✅ | ✅ | ✅ | Tek bir API, yeniden denemeler ve semantik önbellek ile 250'den fazla LLM'e yönlendirme yapan hızlı AI Gateway. |
| **[RouteLLM](https://github.com/lm-sys/RouteLLM)** | Python | - | ❌ | ✅ | ❌ | ✅ | İstek karmaşıklığına ve maliyet optimizasyonuna göre LLM'leri dinamik olarak yönlendiren altyapı. |

---

## Temel Özellik Karşılaştırması

Üretim ortamınız için bir self-hosted AI gateway seçerken veya değerlendirirken şu temel yetenekleri göz önünde bulundurun:

* **Akıllı Fallback & Yeniden Deneme (Retry):** Bir istek zaman aşımına uğradığında, rate limit'e (429) takıldığında veya 5xx sunucu hatası verdiğinde otomatik olarak yedek modellere veya sağlayıcılara geçiş yapar.
* **Sistem Komutu ve Parametre Değiştirme:** İstekleri anında düzenleyin (ör. özel yedekleme başlıkları veya varsayılan system prompt'ları enjekte edin).
* **Yük Dengeleme (Load Balancing):** Trafiği Round Robin, Ağırlıklı veya Gecikme Tabanlı stratejiler kullanarak birden fazla API anahtarına veya sunucu uç noktasına dağıtın.
* **Token ve Maliyet Yönetimi:** Kullanıcı, token veya kanal başına harcamaları bakiye/yükleme entegrasyonlarıyla gerçek zamanlı olarak takip edin.
* **Dinamik Model Eşleme (Dynamic Mapping):** Özel model takma adlarını (ör. `gpt-4o-custom`) şeffaf bir şekilde belirli sağlayıcı uç noktalarına eşleyin.

---

## Katkıda Bulunma

Katkılarınızı bekliyoruz! Lütfen bir Pull Request göndermeden önce kuralları okuyun:

1. Çift kayıt oluşturmamak için mevcut projeleri arayın.
2. Proje bağlantılarının aktif ve doğrudan self-hosted AI yönlendirme/gateway alanıyla ilgili olduğundan emin olun.
3. Yukarıdaki tablo biçimlendirmesine uyun ve açıklamaları kısa, nesnel tutun.

---

*Açık kaynak topluluğu tarafından ❤️ ile sürdürülmektedir.*
