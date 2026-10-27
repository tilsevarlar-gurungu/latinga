# Latinga: Foydalaniş Böyiça Töliq Qöllanma

Latinga özbek lotin alifbosiga ögiruvçi, buyruq satri ilovasidir. Uşbu qöllanmada asosiy imkoniyatlar misollar bilan tuşuntiriladi.

## 1. Imlo Tartiblari

Dastur ikki xil tartibda işlaydi:

| Tartib | Bayroq | Misol (Kirill -> Lotin) |
| :--- | :--- | :--- |
| **Kelgusi** | Fitriy | xalq -> halq, ma'no -> mano |
| **Joriy** | -j, --joriy | shahar -> şahar, oʻrdak -> ördak |


## 2. Atoqli Otlar va Qöşimçalar (-a, --atoqli)

Kelgusi imloda atoqli otlardan keyin keladigan kelişik qöşimçalari tutuq belgisi (') bilan ajratilişi kerak.

```
$ latinga -a "Samarqand,Termiz"
# Kiritma: "Termizga Samarqanddan boramiz."
# Chiqarma: "Termiz'ga Samarqand'dan boramiz."
```

## 3. Matnni Qalqonlaş

Texnik hujjatlar (bitiklar, formulalar) özgarib ketmasligi uçun Latinga bir neça xil himoya usulidan foydalanadi.

### A. Avtomatik Qalqon

Dastur quyidagilarni avtomatik taniydi:

- **LaTeX**: $f'(x) = y$ va \cite{shahar2024} özgarmaydi.
- **HTML**: usttamğalar içidagi matn ögiriladi, lekin tamğaning özi himoyalanadi.
- **Email**: info@latinga.uz kabi manzillar özgarmaydi.
- **XML**: bu format juda egiluvçan bölganligi uçun, çeklangan qöllovga ega.

### B. Umumiy Himoya  ...

Agar matnning biror qismi mutloq özgarmasligini xohlasangiz:

- Kiritma: Yer va Ер.
- Çiqarma: Yer va Yer.

### C. Qolipli Qalqon (-q, --qalqon)

Murakkab qoliplarni özgarişdan qalqonlaş yaʼni özgarmasdan qolişini taʼminlaş uçun işlatiladi:

```
$ latinga matn.txt -q "\*\*Rusça:\*\* ([^\n]+)"
```

## 4. Maxsus Almaştiriş (-m, --almaştir)

Istalgan sözni boşqasi bilan almaştiradi:

```
# Nuqta-vergul (;) bilan bir neçta qoida beriş
$ latinga matn.txt -m "октябрь:oktabr;сентябрь:sentabr"

# Yoki qoidalar yozilgan faylni körsatiş
$ latinga matn.txt -m almashtiruvlar.txt
```

## 5. Sinab köriş

Matndagi tutuq belgisi (joriy tartibda) va eskirgan harf mavjudligini tekşiradi (kelgusi tartibda).
```
$ latinga -t matn.txt
```

Agar xato topilsa, dastur xato satri va ustunini körsatadi hamda xato holati bölgan `exit status 1` bilan tugaydi.
