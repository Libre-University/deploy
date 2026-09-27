# deploy

LibreUniversity kurulum ve operasyon dosyaları: self-hosted öncelikli ([ADR-0003](https://github.com/Libre-University/docs/blob/main/docs/adr/0003-self-hosted-first.md)).

## Ortamlar

| Ortam | Araç | Amaç |
| --- | --- | --- |
| Geliştirme | Docker/Podman Compose | Tek komutla tüm yığın |
| Test / demo | Compose + Ansible | Üretime yakın tek sunucu |
| Üretim | Helm (Kubernetes) veya Ansible | Yüksek erişilebilir kurulum |

## Yığın

PostgreSQL, Redis/Valkey, Keycloak, MinIO, platform-api, Celery işçileri, platform-web, ters vekil sunucu (Caddy/Nginx), Mailpit (geliştirme), Prometheus, Grafana, Loki; Faz 3'te Jitsi (Meet, JVB, Jibri).

## Fazlara Göre İşler

| Faz | Bu repoda yapılacaklar |
| --- | --- |
| Faz 0 | Docker Compose geliştirme ortamı, hazır Keycloak realm'i, `make` komutları, kurulum rehberi, CI |
| Faz 1 | Ansible ile üretime yakın tek sunucu, TLS, Prometheus/Grafana/Loki, gizli bilgi yönetimi |
| Faz 2 | PostgreSQL ve MinIO yedekleme, geri dönüş tatbikatı, yük testi ortamı |
| Faz 3 | Jitsi Meet, JVB, Jibri kurulumu, VOD işleme |
| Faz 4+ | Helm chart'ları, yüksek erişilebilirlik, Wazuh SIEM |

Ayrıntılı ve işaretlenebilir liste: [ROADMAP.md](ROADMAP.md). Fazlar [ana yol haritası](https://github.com/Libre-University/docs/blob/main/ROADMAP.md) ile hizalıdır. Açık işler için `phase:*` etiketlerine bakın.

## Katkı

Katkı rehberi, davranış kuralları ve güvenlik politikası organizasyon genelinde [`.github`](https://github.com/Libre-University/.github) reposundadır. Mimari kararlar [`docs`](https://github.com/Libre-University/docs) reposundaki ADR'lerle alınır.

## Lisans

Bu proje [GNU Affero Genel Kamu Lisansı v3.0 veya sonrası](LICENSE) (AGPL-3.0-or-later) ile lisanslanmıştır. Ağ üzerinden hizmet olarak sunulan değiştirilmiş sürümlerin kaynak kodu da kullanıcılarla paylaşılmalıdır ([ADR-0002](https://github.com/Libre-University/docs/blob/main/docs/adr/0002-prefer-agpl-3-or-later-license.md)).
