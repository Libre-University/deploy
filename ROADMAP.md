# deploy Yol Haritası

## Faz 0: Geliştirme Ortamı (davet öncesi)

- [ ] `compose.yaml`: PostgreSQL, Keycloak (hazır realm), MinIO, Mailpit, platform-api, platform-web
- [ ] Keycloak realm dışa aktarımı: öğrenci, akademisyen, danışman, idari, yönetici test kullanıcıları
- [ ] `make up` / `make seed` / `make down` komutları
- [ ] Linux, macOS ve Windows (WSL2) için kurulum rehberi
- [ ] CI: Compose yığınının ayağa kalkıp sağlık kontrollerinden geçmesi

## Faz 1: Test ve Üretime Yakın Kurulum

- [ ] Ansible ile tek sunucu kurulumu, TLS (Let's Encrypt veya kurum CA)
- [ ] Prometheus, Grafana panoları, Loki log toplama
- [ ] Gizli bilgilerin yönetimi (ör. SOPS)
- [ ] Veritabanı migration'larının güvenli uygulanması

## Faz 2: Yedekleme ve Geri Dönüş

- [ ] PostgreSQL yedekleme (pgBackRest), MinIO yedekleme
- [ ] Geri dönüş tatbikatı betiği ve belgesi
- [ ] Ders kayıt dönemi için yük testi ortamı

## Faz 3: Canlı Ders Altyapısı

- [ ] Jitsi Meet, JVB, Jibri kurulumu; JWT yapılandırması
- [ ] VOD işleme için FFmpeg işçileri

## Faz 4+

- [ ] Helm chart'ları, yüksek erişilebilirlik (PostgreSQL replikasyon, çoklu JVB)
- [ ] Wazuh ile SIEM entegrasyonu
