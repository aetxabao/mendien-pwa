# Mendi entrenamendua — PWA estatikoa

Web-aplikazio progresiboa (PWA) mendira bideratutako prestakuntza fisikoko errutina orokorra kudeatzeko. 

## VS Code programan exekutatu 

1. Ireki karpeta hau VS Code-n.
2. Terminal batean egikaritu `python3 -m http.server 8000` (Windowsen ere `py -m http.server 8000`).
3. Ireki http://localhost:8000. **Ez ireki** `index.html` fitxategia `file://` moduan: JSONen kargak eta service workerrak web zerbitzari bat behar dute.


## Edukiak editatu

- `data/plan.json`: saioak, ariketak, serieak, errepikapenak, atsedenaldiak, oharrak, bilaketa-terminoak YouTuben.
- `styles.css`: diseinua, tipografia eta koloreak.
- `app.js`: nabigazio-logika, erregistroa, inportazioa eta esportazioa.
- `assets/*.svg`: mugimenduen irudi eskematikoak (konexiorik gabeko babes bisuala).
- Ariketen miniaturak YouTube-ri estekatzen zaizkio `i.ytimg.com` URL finkoen bitartez, ez dira automarikoki eguneratzen.
- `Ezarpenak eta datuak` atalean, `Ariketak editatu` ireki dezakezu ariketak pertsonalizatzeko.

Ariketa bakoitzak `id` bakarra eta egonkorra behar du. Identifikatzaile bat aldatzen baduzu, aurreko oharrak jada ez dira ariketa horrekin lotuko.


## GitHub Pagesen argitaratzeko

1. **Biltegi berria** sortu, ez da beharrezkoa beste proiektu bat kopiatzea edo klonatzea.
2. Igo karpeta honetako fitxategiak `main` adarrera.
3. GitHuben, sar zaitez Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.
4. Ireki `https://ERABILTZAILEA.github.io/REPOSITORIO/`mugikorran.
5. Android: nabigatzailearen menua → Aplikazioa instalatu / Hasierako pantailara gehitu. iOS Safari: Partekatu → Hasierako pantailara gehitu.

GitHub Pages zerbitzu publikoa da: ez igo jarraipen-backup-ak, ezta datu pertsonalak edo osasun-datuak ere. Jarraipena gailuan gordetzen da, `localStorage` bidez, sinkronizatu gabe. Segurtasun-kopiak egin aldian behin.

## Konexiorik gabe eta eguneratzea

Oinarrizko baliabideak online lehen bisitaren ondoren biltegiratzen dira. YouTubeko bideoek konexioa behar dute.

Baliabideak edo plana aldatzean, `CACHE` identifikatzailea eguneratzen du `sw.js` en (`mendi-entrenamendua-v2`, etab.) eta argitaratzen du. `data/plan.json` lehenengo saretik eguneratzen saiatzen da; konexiorik ez badago, kopia lokala erabiltzen da.

## Irismena

Biltegiaren edukia orokorra da eta **ez du informazio pertsonalik edo baldintza medikorik gordetzen**. Pertsona bakoitzak bere beharretara egokitu behar ditu jarduerak eta kargak, orientazio profesionalarekin, hala dagokionean.
