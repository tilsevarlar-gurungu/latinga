# Latinga 🇺🇿

Latinga — Rust tilida yozilgan, kengayuvçan va yuqori samaradorlikka ega özbekça kirill-lotin harf ögiruvçisidir. U katta hajmdagi matnlar va texnik hujjatlar (LaTeX, HTML, Markdown) bilan işlaşga möljallangan.

**Diqqat**: Bitik 2026 yil oktabr alifbo islohotlari özgarişlari bilan yangilandi.

## Talaffuzi

Latinga — /loˈtiŋɡa/ yani "lotinga" deb öqiladi. Çunki umid şulki kelajakda Örtoq Turk Alifbosida yozamiz. 😊

## Asosiy Xususiyatlar

- **Aqlli Qalqon**: LaTeX formulalari, HTML tamğalari va Markdown bitik parçalarini avtomatik taniydi va ularni özgartirmaydi.
- **Ikki xil Imlo**: Ham **Joriy** (ş, ç, ö, ğ), ham **Kelgusi** (birlaştirilgan H va X) standartlarini qöllab-quvvatlaydi.
- **Tutuq bilan ajratilgan atoqli otlar**: Kelgusi imloda atoqli otlardan kelişik qöşimçalarini avtomatik ajratadi (masalan: `Toshkentda` -> `Toşkent'da`).
- **Yagona H**: Kelgusi imloda faqat bitta H qoladi va X harfi H bilan almaştiriladi (masalan: `Xato` -> `Hato`).
- **Hujjat turlari**: ilova LaTeX, HTML, XML, Markdown hujjat turlari bilan işlay oladi.

## 🚀 Foydali Boğlamalar

* **Örnatuv:** [Özbekça örnatuv qöllanmasi](https://github.com/tilsevarlar-gurungu/latinga/blob/main/docs/uz/OERNATUV.md).
* **Körgazma:** Ilovani [tilsevarlar-gurungu.github.io/latinga/](https://tilsevarlar-gurungu.github.io/latinga/) jonli veb sahifasida sinab köring.
* [English version of README](https://github.com/tilsevarlar-gurungu/latinga/blob/main/README_EN.md)

## Tezkor Foydalaniş

```
# Faylni tajribaviy kelgusi imloga ögiriş (Kelgusi tartib)
$ latinga matn.txt
```

```
# STDIN orqali amaldagi imloga ögiriş (Joriy tartib)
$ echo "кирилл" | latinga --joriy
```

```
# Matndagi imlo xatolarini tekşiriş
$ latinga -t matn.txt
```
