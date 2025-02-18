### 1. JavaScript nədir?

**Cavab:** JavaScript, veb səhifələrə interaktivlik əlavə etmək üçün istifadə olunan yüksək səviyyəli, dinamik və obyekt yönlü bir proqramlaşdırma dilidir.

### 2. Javascript-də sinxron və asinxron kod arasındakı fərq nədir?

**Cavab:** Sinxron kod, ardıcıl şəkildə işləyir, yəni hər bir əməliyyat əvvəlkini bitirməyi gözləyir. Asinxron kod isə, bir əməliyyatın tamamlanmasını gözləyərkən digər kodların işləməsinə icazə verir.

### 3. JavaScript-də callback və promise arasındakı fərq nədir?

**Cavab:** callback funksiyalar, digər funksiyalara arqument olaraq ötürülən və digər funksiya tamamlandıqda icra olunan funksiyalardır.
Promislər isə asinxron əməliyyatın tamamlanmasını və ya uğursuzluğunu təmsil edən obyektlərdir və asinxron kodun daha səliqəli şəkildə yazılmasına imkan verir.

### 4. JavaScript-də Promise nədir?

**Cavab:** Promise, asinxron əməliyyatın gələcəkdə tamamlanmasını (və ya uğursuzluğunu) təmsil edən bir obyektdir və asinxron kodu daha oxunaqlı şəkildə zəncirləməyə imkan verir.

### 5. JavaScript-də Promise obyektinin üç vəziyyəti hansılardır?

**Cavab:** Promise obyektinin üç vəziyyəti var: Pending, Fulfilled, Rejected.

### 6. JavaScript-də try/catch ifadəsinin məqsədi nədir?

**Cavab:** try/catch ifadəsi, JavaScript-də kodda yaranan səhvləri (xətaları) idarə etmək üçün istifadə olunur.

### 7. JavaScript Promises-də finally metodunun istifadə məqsədi nədir?

**Cavab:** Finally metodu,Promise tamamlandıqdan sonra, nəticə və ya xəta olmasından asılı olmayaraq mütləq icra olunan blokdur

```js
myPromise
  .then((result) => console.log(result))
  .catch((error) => console.error(error))
  .finally(() => console.log('Tamamlandı'));
// Finally hər halda işləyir.
```

### 8. Javascript-də for..in döngəsi ilə for..of döngəsi arasında fərq nədir?

**Cavab:**

`for..in` döngüsü obyektin sadalanan (enumerable) xüsusiyyətlərini gəzmək üçün istifadə olunur.

`for..of` döngüsü isə iterasiya oluna bilən obyektin dəyərləri üzərində gəzmək üçün istifadə olunur.

```js
// for..in: Obyektin açarlarını gəzmək üçün
const obj = { a: 1, b: 2, c: 3 };
for (let key in obj) {
  console.log(key, obj[key]); // a 1, b 2, c 3
}

// for..of: Iterasiya oluna bilən obyektin dəyərlərini gəzmək üçün
const arr = [10, 20, 30];
for (let value of arr) {
  console.log(value); // 10, 20, 30
}
```

### 9. Javascript-də ox funksiyası ilə regular funksiya arasındakı fərq nədir

**Cavab:**
Ox funksiyalarının daha qısa sintaksisi vardır və `this` dəyərini avtomatik olaraq daxil olduğu kontekstə bağlayır, regular funksiyalar isə daha uzun sintaksiyaya malikdir və `this` dəyəri funksiyanın necə çağırılmasından asılı olaraq təyin olunur.

### 10. Javascript-də var, let və const arasındakı fərq nədir?

**Cavab:** var funksional (function) scope-da təyin olunur, amma let və const blok (block) scope-da təyin olunur. var və let dəyişənləri yenidən təyin edilə bilər, amma const yenidən təyin edilə bilməz. Bundan əlavə, const təyin edildiyi zaman mütləq başlanğıc dəyəri ilə təyin edilməlidir.

### 11. Spread operatoru ilə rest parametri arasındakı fərq nədir?

**Cavab:** Spread operator bir array və ya obyektin elementlərini ayrı-ayrı arqumentlərə və ya elementlərə yaymağa imkan verir, rest parameter isə bir neçə arqumenti bir array-də toplamağa imkan verir.

```js
// Spread Operator: Array elementlərini yaymaq
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5]; // [1, 2, 3, 4, 5]
console.log(newArr);

// Rest Parameter: Bir neçə arqumenti array-də toplamaq
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
```

### 12. JavaScript-də async və await açar sözlərinin istifadə məqsədi nədir?

**Cavab:** async və await açar sözləri, asinxron funksiyaları daha oxunaqlı şəkildə yazmağa imkan verir. async funksiyaların asinxron olmasını təmin edir, await isə asinxron əməliyyatların nəticəsini gözləməyə imkan verir. Bu sintaksis arxa planda Promise obyektindən istifadə edir.

### 13. JavaScript-də obyektin shallow və deep kopya arasındakı fərq nədir?

**Cavab:** Shallow copy orijinal obyektin yalnız üst səviyyə (top-level) xüsusiyyətləri ilə yeni bir obyekt yaradır, amma deep copy orijinal obyektin bütün iç içə (nested) xüsusiyyətləri və onların dəyərləri ilə yeni bir obyekt yaradır.

```js
//Shallow Copy
const original = { a: 1, b: { c: 2 } };
const shallowCopy = { ...original };

shallowCopy.b.c = 3; // Orijinal obyekt də dəyişir
console.log(original.b.c); // 3

// Deep Copy
const deepCopy = JSON.parse(JSON.stringify(original));

deepCopy.b.c = 4; // Orijinal obyekt dəyişmir
console.log(original.b.c); // 3
console.log(deepCopy.b.c); // 4
```

### 14. innerHTML və textContent arasındakı fərq nədir?

**Cavab:** innerHTML bir elementin daxilindəki HTML strukturlarını (etiketlər daxil olmaqla) təyin edir və ya qaytarır. textContent isə yalnız mətni (HTML etiketləri olmadan) təyin edir və ya qaytarır.

```js
<div id="example1">
  <p>Bu bir <strong>HTML</strong> mətni</p>
</div>

<div id="example2">
  <p>Bu yalnız mətn mətni</p>
</div>

<script>
  // innerHTML nümunəsi
  const example1 = document.getElementById("example1");
  console.log(example1.innerHTML); // <p>Bu bir <strong>HTML</strong> mətni</p>

  example1.innerHTML = "<p>Yeni <em>HTML</em> mətni</p>"; // HTML məzmunu dəyişir

  // textContent nümunəsi
  const example2 = document.getElementById("example2");
  console.log(example2.textContent); // Bu yalnız mətn mətni

  example2.textContent = "Yeni mətn məzmunu"; // Yalnız mətn dəyişir
</script>
```

### 15. JavaScript-də fetch funksiyasının məqsədi nədir?

**Cavab:** fetch funksiyası HTTP sorğuları etmək və serverdən resursları çəkmək üçün istifadə olunur.

### 16. setTimeout və setInterval arasındakı fərq nədir?

**Cavab:** setTimeout, təyin edilmiş bir gecikmədən sonra bir funksiyanı yalnız bir dəfə işlətmək üçün istifadə olunur, halbuki setInterval funksiyası təyin edilmiş interval üzrə funksiyanı təkrarlayaraq işlədir.

```js
// setTimeout nümunəsi: funksiyanı yalnız bir dəfə gecikmədən sonra işlədir
setTimeout(() => {
  console.log('Bu mesaj 3 saniyədən sonra yalnız bir dəfə göstəriləcək.');
}, 3000);

// setInterval nümunəsi: funksiyanı hər 3 saniyədə bir təkrarlayır
setInterval(() => {
  console.log('Bu mesaj hər 3 saniyədə bir təkrarlanacaq.');
}, 3000);
```

### 17. JavaScript-də this açar sözü nədir?

**Cavab:** this açar sözü cari konteksti (mühiti) göstərir, bu da qlobal obyekt, funksiya və ya obyekt ola bilər.

```js
// Objektdə 'this' obyektə istinad edir
const car = {
  brand: 'Toyota',
  getBrand: function () {
    console.log(this.brand); // 'this' car obyektinə istinad edir
  },
};
car.getBrand(); // Toyota

// Funksiyada 'this' qlobal obyektə istinad edir
function show() {
  console.log(this); // 'this' qlobal obyektə (brauzerlerde 'window') istinad edir
}
show();
```

### 18. JavaScript-də window və document arasındakı fərq nədir?

**Cavab:** `window` brauzer pəncərəsini təmsil edən qlobal obyektdir, `document` isə pəncərədə göstərilən HTML sənədinə istinad edir.

### 19. JavaScript-də map və forEach arasındakı fərq nədir?

**Cavab:** Həm map, həm də forEach bir massiv üzərində dövr etmək üçün istifadə olunur, amma map transformasiya olunmuş elementlərlə yeni bir massiv qaytarır, forEach isə yalnız hər bir element üzərində funksiyanı icra edir.

```js
const arr = [1, 2, 3, 4, 5];

// map: Yeni bir massiv qaytarır
const doubled = arr.map((x) => x * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// forEach: Elementlər üzərində əməliyyat edir, amma heç bir şey qaytarmır
arr.forEach((x) => console.log(x * 2)); // 2, 4, 6, 8, 10
```

### 20. JavaScript-də sintaksis səhvi ilə çalışma zamanı (runtime) səhvi arasındakı fərq nədir?

**Cavab:** Sintaksis səhvi, kod düzgün yazılmadıqda yaranır, run time səhvi isə kod icra olunarkən qarşılaşılan problemlərdən qaynaqlanır.

```js
// Sintaksis Səhvi (Syntax Error)
console.log("Hello World" // Mötərizə bağlanmayıb

// Çalışma Zamanı Səhvi (Runtime Error)
let x = 10;
console.log(x.toUpperCase()); // x bir ədəd olduğu üçün toUpperCase() metodunu çağıra bilməz
```

### 21. JavaScript-də modul nədir?

**Cavab:** Modul, özünü idarə edən bir kod parçasıdır ki, digər kodlara import edilə və istifadə edilə bilər. Bu, böyük kod bazalarını təşkil etmək və modulyarlaşdırmaq üçün kömək edir.

```js
// math.js faylı (Modul)
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}

// app.js faylı (Modulun istifadə edilməsi)
import { add, subtract } from './math.js';

console.log(add(2, 3)); // 5
console.log(subtract(5, 3)); // 2
```

### 22. JavaScript-də JSON.stringify nə üçün istifadə edilir?

**Cavab:** `JSON.stringify` metodu, JavaScript obyektini JSON formatında mətnə çevirmək üçün istifadə olunur.

### 23. JavaScript-də eval funksiyasının nədir?

**Cavab:** eval funksiyası, cari əhatə dairəsində (scope) JavaScript kodunu ifadə edən bir sətri icra etmək üçün istifadə olunur.

Təhlükəsizlik və performans problemlərinə görə istifadəsi tövsiyə edilmir.

```js
let x = 10;
let y = 20;
let result = eval('x + y'); // 30
console.log(result);
```

### 24. JavaScript-də new açar sözü nədir?

**Cavab:** `new` açar sözü bir funksiyanı konstruktor kimi çağıraraq yeni obyekt yaradır. new açar sözü bir funksiyanı konstruktor kimi çağıraraq yeni obyekt yaradır.

### 24. JavaScript-də new açar sözü nədir?

**Cavab:** `new` açar sözü, bir funksiyanı konstruktor kimi çağıraraq yeni bir obyekt yaradır.

### 25. Konstruktor Funksiyalar nədir?

**Cavab:** Konstruktor funksiyalar, obyekt yaratmaq üçün istifadə olunan xüsusi funksiyalardır. Onlar new açar sözü ilə çağırılır və yeni bir obyekt yaradır. Konstruktor funksiyalar, JavaScript-də obyekt yönümlü proqramlaşdırmanın (OOP) əsas hissəsidir. Bu funksiyalar adətən böyük hərflə başlayır (məsələn, Car, Person).

### 26. JavaScript-də primitiv dəyərlər və referans dəyərlər arasındakı fərq nədir?

**Cavab:** Primitiv dəyərlər dəyişməz (immutable) və birbaşa yaddaşda saxlanılır, referans dəyərlər isə dəyişən (mutable) obyektlərdir və yaddaşda referans ilə saxlanılır.

### 27. Object.keys metodu nədir?

**Cavab:** `Object.keys()` metodu bir obyektin yalnız açar (property name) adlarını qaytaran bir massiv yaradır.

```js
const user = { name: 'Ali', age: 25, city: 'Baku' };
console.log(Object.keys(user));
// ["name", "age", "city"]
```

### 28. JavaScript-də JSON.parse metodu nədir?

**Cavab:** `JSON.parse` metodu, JSON formatında olan bir sətri JavaScript obyektinə çevirmək üçün istifadə olunur.

### 29. extends açar sözü nədir?

**Cavab:** `extends` açar sözü, JavaScript-də mövcud olan bir sinifdən alt sinif yaratmaq üçün istifadə olunur. Bu, kodun təkrar istifadəsini və miras (inheritance) mexanizmini təmin edir.

```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name); // Ana sinifin constructor funksiyasını çağırır
    this.breed = breed;
  }

  speak() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog('Max', 'Labrador');
dog.speak(); // "Max barks."
```

### 29. JavaScript-də super açar sözü nədir?

**Cavab:** super açar sözü, alt sinifdə (subclass) üst sinfin (superclass) konstruktorunu və ya metodlarını çağırmaq üçün istifadə olunur.

### 30. JavaScript-də Object.create metodu nədir?

**Cavab:** `Object.create` metodunun məqsədi mövcud bir obyektin prototipini istifadə edərək yeni bir obyekt yaratmağa imkan verir.

```js
const person = {
  greet() {
    console.log(`Salam, mənim adım ${this.name}-dir.`);
  },
};

// person obyektini prototip kimi istifadə edərək yeni obyekt yaratmaq
const eli = Object.create(person);
eli.name = 'Eli';
eli.greet(); // Salam, mənim adım Eli-dir.
```

### 31. JavaScript-də Object.assign metodu nədir?

`Object.assign` metodu, obyektlərin xüsusiyyətlərini birləşdirmək, kopyasını yaratmaq və ya yeni xüsusiyyətlər əlavə etmək üçün istifadə olunur.

```js
const obj1 = { a: 1 };
const obj2 = { b: 2 };
const result = Object.assign({}, obj1, obj2); // { a: 1, b: 2 }
```

### 32. JavaScript-də Object.values ​​metodu nədir?

**Cavab:** `Object.values()` metodu, obyektin dəyərlərini (values) bir massiv olaraq qaytarmaq üçün istifadə olunur.

```js
const obj = { a: 1, b: 2, c: 3 };
const values = Object.values(obj);
console.log(values); // [1, 2, 3]
```

### 33. JavaScript-də Object.entries ​​metodu nədir?

**Cavab:** `Object.entries` metodu, obyektin içindəki key və value cütlərini bir massiv olaraq qaytarmaq üçün istifadə olunur.

```js
const obj = { a: 1, b: 2, c: 3 };
const val = Object.entries(obj);
console.log(val); // [ ['a', 1], ['b', 2], ['c', 3] ]
```

### 34. Prototip Nədir?

**Cavab:** JavaScript-də prototype, obyektlərin bir-birindən xüsusiyyət və metod miras almasını təmin edən mexanizmdir.
