# Latinga va WebAssembly (WASM)

Latingaʼni veb-ilovalar yoki Node.js muhitiga yuqori tezlikdagi kutubxona sifatida qöşiş mumkin. ```Latinga``` obyekti orqali luğatlarni bir marta xotiraga yuklab, ulardan samarali foydalaniş imkoniyati mavjud.

## Örnatiş
Avval ```wasm-pack``` yordamida loyihani yiğing:
```bash
wasm-pack build --features wasm
```

## Foydalaniş Namunalari

### 1. Brauzerda (ES Modules)
```javascript
import init, { Latinga } from './pkg/latinga.js';

async function run() {
    await init();

    // Router obyektini yaratiş (Bir marta bajariladi)
    // false = Kelgusi imlo, true = Joriy imlo
    const latinga = new Latinga(false);

    // Maxsus qoidalar qöşiş
    latinga.almashuvchilarni_yukla("Apple:Epl;Google:Gugl");
    latinga.atoqlilarni_yukla("Toshkent,Samarqand");
    latinga.qalqonlarni_yukla("\\{.*?\\}"); // Jingalak qavslarni himoyalaş

    // Ögiriş (Juda tez bajariladi)
    const natija = latinga.ogir("Toshkentga bordik.");
    console.log(natija); // Toşkent'ga bordik.
}
```

### 2. Node.js muhitida
Node.js uçun yiğilgan paketdan quyidagiça foydalaniladi:

```javascript
const { Latinga } = require('./pkg/latinga.js');

const latinga = new Latinga(true);
console.log(latinga.oegir("Ўзбекистон"));
```

## Texnik Tavsiya
```Latinga``` yaratilganda içki luğatlar xotiraga yuklanadi. Şu sababli, bitta latinga'dan butun dastur davomida foydalaniş tavsiya etiladi.
