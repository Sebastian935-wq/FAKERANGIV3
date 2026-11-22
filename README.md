# FAKE RANGI ANARCHIA.GG — v1.3 (Fabric 1.21.4)

Projekt źródłowy do samodzielnej kompilacji na GitHub Actions (`.github/workflows/main.yml`). Wymaga Javy 21 i Fabric API.

## Instrukcja
1. Rozpakuj ZIP. Wgraj **zawartość**, a nie sam ZIP, do katalogu głównego repozytorium GitHub; zachowaj `src/`.
2. Wejdź w Actions -> Build Fake Rangi 1.21.4 i pobierz artifact.
3. Wgraj właściwy JAR (nie `-sources.jar`) do `mods` i usuń starszy JAR moda.
4. Testuj najpierw na osobnej instalacji Fabric 1.21.4 z Fabric API, bez dodatkowych modów.

## Funkcje
- `Z`: GUI z zakładkami RANGA EKWIPUNEK oraz USTAWIENIA.
- Voucher VIP / SVIP / GVIP: **lewy klik** bierze lokalny voucher do widoku hotbara. Wymagana dokładnie 1 sztuka dowolnego prawdziwego przedmiotu w aktywnej ręce.
- **Prawy klik** podczas rozgrywki lub na wybrany voucher w GUI aktywuje lokalną rangę. Voucher znika z widoku; prawdziwy przedmiot nie jest usuwany.
- `COFNIJ / PRZYWROC` usuwa lokalny voucher i wyłącza fake rangę. Żaden prawdziwy ekwipunek nie jest zmieniany, więc nie ma czego odzyskiwać z serwera.
- Napisy w TAB, HUD i nad głową mają wyłącznie charakter lokalny.
- Tekstury voucherów są już w zasobach moda — osobny TXT nie jest potrzebny.
- Ustawienia: `config/fake-rangi-anarchia.properties`.

## Ograniczenia
- Voucher jest rysowany jako **nakładka na slot hotbara**, a nie prawdziwy model 3D w ręce. Inni gracze widzą prawdziwy przedmiot.
- Kliknięcie PPM nie przechwytuje ani nie blokuje normalnego użycia przedmiotu na serwerze. Testuj z bezpiecznym przedmiotem, np. kamieniem; nie trzymaj mikstur, perł ani innych przedmiotów aktywowanych PPM.
- Nie można przywrócić ekwipunku utraconego wskutek zwykłych akcji serwerowych. Mod nie usuwa ani nie przywraca prawdziwych przedmiotów.
- Projekt nie został przetestowany w działającym Minecraft 1.21.4. Szczególnie sprawdź kompatybilność mixina nametag; jeśli wystąpi crash, wyślij `latest.log`.
