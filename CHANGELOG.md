# Changelog

Tutte le modifiche rilevanti a questo plugin sono documentate in questo file.

Il formato è basato su [Keep a Changelog](https://keepachangelog.com/it/1.1.0/)
e questo progetto aderisce al [Semantic Versioning](https://semver.org/lang/it/).

## [1.0.0] - 2026-11-05

### Added
- Feed prodotti per **Google Merchant Center** e per il **catalogo Meta** (Facebook e Instagram): un file XML (RSS 2.0 con
  namespace `g:`) per canale, rigenerato dal cron di WordPress (controllo orario) o con `wp threecommerce productfeed generate`.
- URL del feed con token non indovinabile derivato dai salt di WordPress; file in `wp-content/uploads/threecommerce-productfeed/`.
- Un feed per lingua con WPML o Polylang, un feed unico senza plugin multilingua.
- Prezzi con IVA come nel negozio, prezzo scontato (`sale_price`), disponibilità, immagini aggiuntive, marca, GTIN, MPN,
  categoria Google, tipo di prodotto dal percorso di categoria; `identifier_exists = no` per Google quando mancano GTIN e MPN.
- Filtri per tipo di prodotto (semplice, variabile, esterno), categoria, campo/attributo da escludere (es. un flag
  «prossimamente») e disponibilità.
- Prodotti variabili esportati come un solo articolo al prezzo della variazione più economica (le variazioni non sono separate).
- Esclusi i prodotti senza immagine, con prezzo 0, nascosti, protetti da password o non pubblicati.
- Pagina WooCommerce → Product Feed con impostazioni, URL dei feed, data e dimensione dell'ultima generazione e pulsante «Genera ora».
- Compatibilità dichiarata con HPOS e checkout a blocchi. Traduzione it_IT.
