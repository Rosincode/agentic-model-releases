# Agentic Model – Releases

Deze repository publiceert de releasefeed voor installaties van Agentic Model. Er staat geen broncode in.

## Wat staat hier

- **Releasefeed**: een ondertekende `releases.json`, bij de release `feed`. Installaties controleren deze feed
  regelmatig om te zien of er een nieuwe versie is.
- **Container-images**: apart gepubliceerd in de GitHub Container Registry. De feed verwijst ernaar op digest.

## Hoe updates werken

1. Een nieuwe versie wordt gebouwd en de images worden naar de registry gepusht.
2. De versie wordt toegevoegd aan de releasefeed, die wordt ondertekend met de sleutel van de leverancier.
3. Installaties halen de feed op, controleren de handtekening en bieden de update aan hun beheerders aan.
4. De installatie installeert alleen een image dat in een correct ondertekende feed staat, vastgelegd op digest.

Feeds of images van ergens anders worden genegeerd, dus niemand anders kan een installatie een update aanbieden.

## Voor klanten

Normaal hoef je hier niets te doen: je installatie vindt nieuwe versies zelf. Heeft je installatie geen
internettoegang, vraag dan je leverancier om een updatebestand.

## Ondersteuning

Neem voor vragen over je installatie of licentie contact op met je leverancier.
