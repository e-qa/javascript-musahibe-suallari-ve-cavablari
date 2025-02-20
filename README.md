### 1. JavaScript nədir?

**Cavab:** JavaScript, veb səhifələrə interaktivlik əlavə etmək üçün istifadə olunan yüksək səviyyəli, dinamik və obyekt yönlü bir proqramlaşdırma dilidir.

### 2. Javascript-də sinxron və asinxron kod arasındakı fərq nədir?

**Cavab:** Sinxron kod, ardıcıl şəkildə işləyir, yəni hər bir əməliyyat əvvəlkini bitirməyi gözləyir. Asinxron kod isə, bir əməliyyatın tamamlanmasını gözləyərkən digər kodların işləməsinə icazə verir.

### 3. JavaScript-də callback və promise arasındakı fərq nədir?

**Cavab:** callback funksiyalar, digər funksiyalara arqument olaraq ötürülən və digər funksiya tamamlandıqda icra olunan funksiyalardır.
Promislər isə asinxron əməliyyatın tamamlanmasını və ya uğursuzluğunu təmsil edən obyektlərdir və asinxron kodun daha səliqəli şəkildə yazılmasına imkan verir.

### 4. JavaScript-də Promise nədir?

**Cavab:** Promise JavaScript-də asinxron əməliyyatları idarə etmək üçün istifadə olunan bir obyektdir.

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
Ox funksiyalarının daha qısa sintaksisi var və `this` dəyərini avtomatik olaraq daxil olduğu kontekstə bağlayır, regular funksiyalar isə daha uzun sintaksa malikdir və `this` dəyəri funksiyanın necə çağırılmasından asılı olaraq təyin olunur.

### 10. Javascript-də var, let və const arasındakı fərq nədir?

**Cavab:** `var` funksional (function) scope-da təyin olunur, amma `let` və `const` blok (block) scope-da təyin olunur. `var` və `let` dəyişənləri yenidən təyin edilə bilər, amma `const` yenidən təyin edilə bilməz. Bundan əlavə, `const` təyin edildiyi zaman mütləq başlanğıc dəyəri ilə təyin edilməlidir.

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
  console.log(example2.textContent); // Bu yalnız mətn

  example2.textContent = "Yeni mətn məzmunu"; // Yalnız mətn dəyişir
</script>
```

### 15. JavaScript-də fetch funksiyasının məqsədi nədir?

**Cavab:** `fetch` funksiyası HTTP sorğuları etmək və serverdən resursları çəkmək üçün istifadə olunur.

### 16. setTimeout və setInterval arasındakı fərq nədir?

**Cavab:** `setTimeout`, təyin edilmiş bir gecikmədən sonra bir funksiyanı yalnız bir dəfə işlətmək üçün istifadə olunur, `setInterval` funksiyası isə təyin edilmiş interval üzrə funksiyanı təkrarlayaraq işlədir.

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

**Cavab:** `this` açar sözü cari konteksti (mühiti) göstərir, bu qlobal obyekt, funksiya ola bilər.

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

**Cavab:** Həm `map`, həm də `forEach` bir massiv üzərində dövr etmək üçün istifadə olunur, amma `map` transformasiya olunmuş elementlərlə yeni bir massiv qaytarır, `forEach` isə yalnız hər bir element üzərində funksiyanı icra edir.

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

**Cavab:** `eval` funksiyası, cari əhatə dairəsində (scope) JavaScript kodunu ifadə edən bir sətri icra etmək üçün istifadə olunur.

Təhlükəsizlik və performans problemlərinə görə istifadəsi tövsiyə edilmir.

```js
let x = 10;
let y = 20;
let result = eval('x + y'); // 30
console.log(result);
```

### 24. JavaScript-də new açar sözü nədir?

**Cavab:** `new` açar sözü, bir funksiyanı konstruktor kimi çağıraraq yeni bir obyekt yaradır.

### 25. Konstruktor Funksiyalar nədir?

**Cavab:** Konstruktor funksiyalar, obyekt yaratmaq üçün istifadə olunan xüsusi funksiyalardır. Onlar new açar sözü ilə çağırılır və yeni bir obyekt yaradır. Konstruktor funksiyalar, JavaScript-də obyekt yönümlü proqramlaşdırmanın (OOP) əsas hissəsidir. Bu funksiyalar adətən böyük hərflə başlayır (məsələn, Car, Person).

### 26. JavaScript-də primitiv dəyərlər və referans dəyərlər arasındakı fərq nədir?

**Cavab:** Primitiv dəyərlər dəyişməzdir (immutable) və birbaşa stack yaddaşında saxlanılır. Referans dəyərlər isə dəyişəndir (mutable) və heap yaddaşında saxlanılır, yalnız referans (istinad) stack-də olur.

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

**Cavab:** `super` açar sözü, alt sinifdə (subclass) üst sinfin (superclass) konstruktorunu və ya metodlarını çağırmaq üçün istifadə olunur.

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

### 34. Prototype Nədir?

**Cavab:** JavaScript-də prototype, obyektlərin bir-birindən xüsusiyyət və metod miras almasını təmin edən mexanizmdir.

### 35. Map obyekti nədir?

**Cavab:** `Map` obyekti, key-value cütlərini saxlamaq üçün istifadə olunan xüsusi bir data strukturdur. `Object`-dən fərqli olaraq, `Map` key kimi yalnız string deyil, hər hansı bir növ dəyəri (obyekt, funksiya, primitivlər) qəbul edə bilir. Bundan əlavə, Map-də elementlər əlavə edildiyi sıraya görə saxlanılır

```js
const map = new Map();

function myFunction() {
  return 'Hello!';
}

// Map obyektinə açar-dəyərlər əlavə edirik
map.set(myFunction, 'Function Key');
map.set('name', 'John Doe');
map.set(42, 'Number Key');

console.log(map.get('name')); // John Doe
console.log(map.get(myFunction)); // Function Key
console.log(map.get(42)); // Number Key

console.log(map.has('name')); // true
console.log(map.has('age')); // false (çünki 'age' açarı yoxdur)

map.delete(42); // 42 açarını silirik
console.log(map.has(42)); // false
```

### 36. reduce metodu nədir?

**Cavab:** `reduce` metodu, bir massivdəki bütün elementlər üzərində müəyyən bir əməliyyat icra edərək tək bir dəyər qaytarır (məsələn, cəmi, hasil, obyekt yaratmaq və s.).

```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // 10
```

### 37. filter metodu nədir?

**Cavab:** `filter` metodu, müəyyən şərti ödəyən elementlərdən ibarət yeni bir massiv yaratmaq üçün istifadə olunur.

```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter((number) => number % 2 === 0);
console.log(evenNumbers); // Nəticə: [2, 4]
```

### 38. some metodu nədir?

**Cavab:** `some` metodu, massivdə ən azı bir elementin verilmiş şərti ödəyib-ödəmədiyini yoxlamaq üçün istifadə olunur. Əgər şərti ödəyən ən azı bir element tapsa, `true` qaytarır, əks halda `false` qaytarır

```js
const numbers = [1, 3, 5, 7, 8];
const hasEven = numbers.some((num) => num % 2 === 0);
console.log(hasEven); // true (çünki 8 cütdür)
```

### 39.every metodu nədir?

**Cavab:**`every` metodu, bir massivdəki bütün elementlərin verilmiş şərti ödəyib-ödəmədiyini yoxlamaq üçün istifadə olunur.

```js
const numbers = [2, 4, 9, 8];
const allEven = numbers.every((num) => num % 2 === 0);
console.log(allEven); // false (çünki 9 cüt deyil)
```

### 40. splice metodu nədir?

**Cavab:** JavaScript-də `splice` metodu, massivi müəyyən bir indeksdən elementləri əlavə edərək və ya silərək dəyişdirmək üçün istifadə olunur

```js
const numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 1); // İndeks 2-dən 1 elementi silir
console.log(numbers); // Nəticə: [1, 2, 4, 5] (orijinal massiv dəyişdi)
```

### 41. slice metodu nədir?

**Cavab:** `slice` metodu, bir massivdən müəyyən bir hissəni çıxararaq yeni bir massiv qaytarır və orijinal massivi dəyişdirmir.

```js
const numbers = [1, 2, 3, 4, 5];
const slicedArray = numbers.slice(1, 4); // İndeks 1-dən 4-ə qədər (4 daxil deyil) kopyalayır
console.log(slicedArray); // Nəticə: [2, 3, 4]
console.log(numbers); // Orijinal massiv dəyişmir: [1, 2, 3, 4, 5]
```

### 42. unshift metodu nədir?

**Cavab:** `unshift` metodu, massivin əvvəlinə bir və ya bir neçə element əlavə etmək üçün istifadə olunur.

```js
const numbers = [2, 3, 4];
numbers.unshift(1); // Massivin əvvəlinə 1 əlavə edir
console.log(numbers); // Nəticə: [1, 2, 3, 4]
```

### 43. shift metodu nədir?

**Cavab:** `shift` metodu, massivin birinci elementini silir və silinən elementi qaytarır. Bu metod, orijinal massivi dəyişdirir

```js
const numbers = [1, 2, 3, 4];
const removedElement = numbers.shift(); // Birinci elementi (1) silir
console.log(removedElement); // Nəticə: 1
console.log(numbers); // Orijinal massiv: [2, 3, 4]
```

### 44. concat metodu nədir?

**Cavab:** JavaScript-də concat metodu, iki və ya daha çox massivi birləşdirərək yeni bir massiv yaratmaq üçün istifadə olunur. Orijinal massivlər dəyişmir.

```js
const arr1 = [1, 2];
const arr2 = [3, 4];
const combinedArray = arr1.concat(arr2); // arr1 və arr2 birləşdirilir
console.log(combinedArray); // Nəticə: [1, 2, 3, 4]
console.log(arr1); // Orijinal massiv dəyişmir: [1, 2]
console.log(arr2); // Orijinal massiv dəyişmir: [3, 4]
```

### 45. push metodu nədir?

**Cavab:** `push` metodu, massivin sonuna bir və ya bir neçə element əlavə etmək üçün istifadə olunur. Bu metod, orijinal massivi dəyişdirir

```js
const numbers = [1, 2, 3];
numbers.push(4); // Massivin sonuna 4 əlavə edir
console.log(numbers); // Nəticə: [1, 2, 3, 4]
```

### 46. pop metodu nədir?

**Cavab:** `pop` metodu, massivin sonuncu elementini silir və silinən elementi qaytarır. Bu metod, orijinal massivi dəyişdirir.

```js
const numbers = [1, 2, 3, 4];
const removedElement = numbers.pop(); // Sonuncu elementi (4) silir
console.log(removedElement); // Nəticə: 4
console.log(numbers); // Orijinal massiv: [1, 2, 3]
```

### 47. includes metodu nədir?

**Cavab**: `includes` metodu, massivin müəyyən bir dəyəri içində saxlayıb-saxlamadığını yoxlamaq üçün istifadə olunur. Bu metod, boolean (true və ya false) qaytarır.

```js
const numbers = [1, 2, 3, 4];
const hasNumber = numbers.includes(3); // 3-ün massivdə olub-olmadığını yoxlayır
console.log(hasNumber); // Nəticə: true
```

### 48. indexOf metodu nədir?

**Cavab**: `indexOf` metodu, massivdə müəyyən bir dəyərin ilk indeksini tapmaq üçün istifadə olunur. Əgər dəyər massivdə tapılmasa, metod -1 qaytarır.

```js
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(30); // 30-un indeksini tapır
console.log(index); // Nəticə: 2

const notFound = numbers.indexOf(50); // 50 massivdə olmadığı üçün
console.log(notFound); // Nəticə: -1
```

### 49.lastIndexOf metodu nədir?

**Cavab:** `lastIndexOf` metodu, massivdə müəyyən bir dəyərin son indeksini tapmaq üçün istifadə olunur. Əgər dəyər massivdə tapılmasa, metod -1 qaytarır.

```js
const numbers = [10, 20, 30, 20, 40];
const lastIndex = numbers.lastIndexOf(20); // 20-nin son indeksini tapır
console.log(lastIndex); // Nəticə: 3

const notFound = numbers.lastIndexOf(50); // 50 massivdə olmadığı üçün
console.log(notFound); // Nəticə: -1
```

### 50. Array.isArray metodu nədir?

**Cavab:** `Array.isArray` metodu, bir dəyərin massiv olub-olmadığını yoxlamaq üçün istifadə olunur. Bu metod, boolean (true və ya false) qaytarır

```js
const arr = [1, 2, 3];
const isArr = Array.isArray(arr); // arr massiv olub-olmadığını yoxlayır
console.log(isArr); // Nəticə: true

const notArr = 'Bu massiv deyil';
const isNotArr = Array.isArray(notArr); // notArr massiv olub-olmadığını yoxlayır
console.log(isNotArr); // Nəticə: false
```

### 51. Array.from metodu nədir?

**Cavab:** Array.from() metodu, array-like və ya iterable obyektləri (məsələn, arguments və ya stringlər) birbaşa JavaScript massivinə çevirmək üçün istifadə olunur.

```js
const str = 'hello';
const arr = Array.from(str); // ['h', 'e', 'l', 'l', 'o']
```

### 52. Object.freeze metodu nədir?

**Cavab:** `Object.freeze` metodu, bir obyektin dəyişdirilməz (immutable) olmasını təmin edir. Bu metod, obyektin xüsusiyyətlərinin əlavə edilməsini, silinməsini və ya dəyişdirilməsini qadağan edir.

```js
const obj = { name: 'Ali', age: 25 };
Object.freeze(obj); // Obyekt dondurulur

obj.name = 'Veli'; // Dəyişiklik etmək mümkün deyil
console.log(obj); // Nəticə: { name: "Ali", age: 25 }
```

### 53. split metodu nədir?

**Cavab:** `split` metodu, bir stringi müəyyən bir ayırıcı (separator) əsasında alt stringlərə bölərək massivə çevirir.

```js
const str = 'JavaScript,Python,C++';
const arr = str.split(','); // Vergül əsasında bölür
console.log(arr); // Nəticə: ["JavaScript", "Python", "C++"]
```

### 54. Generator funksiyas nədir?

**Cavab:** Generator funksiyası, JavaScript-də dayandırıla bilən və davam etdirilə bilən xüsusi bir funksiya növüdür. Bu funksiyalar, sinxron kodu asinxron kimi idarə etməyə imkan yaradır. Generator funksiyaları `function\*` sintaksisi ilə yazılır və yield ifadəsi ilə dayandırılır.

```js
function* numberGenerator() {
  yield 1;
  yield 2;
  yield 3;
}

const generator = numberGenerator();
console.log(generator.next().value); // Nəticə: 1
console.log(generator.next().value); // Nəticə: 2
console.log(generator.next().value); // Nəticə: 3
```

### 55. instanceof operatoru nədir?

**Cavab:** instanceof operatoru, bir obyektin müəyyən bir konstruktor nümunəsi (instance) olub-olmadığını yoxlamaq üçün istifadə olunur. Bu operator, boolean (true və ya false) qaytarır.

```js
class Car {}
const myCar = new Car();

console.log(myCar instanceof Car); // Nəticə: true
console.log(myCar instanceof Object); // Nəticə: true (hər obyekt Object-dən miras alır)
console.log(myCar instanceof Array); // Nəticə: false
```

### 56. Set obyekti nədir?

**Cavab:** `Set` obyekti, JavaScript-də unikal dəyərləri saxlamaq üçün istifadə olunur. Bu obyekt, eyni dəyəri yalnız bir dəfə saxlayır və dublikatları avtomatik olaraq silir. Set-ə istənilən tipdə dəyərlər əlavə edilə bilər.

```js
const mySet = new Set();

mySet.add(1); // 1 əlavə edir
mySet.add(2); // 2 əlavə edir
mySet.add(2); // 2 yenidən əlavə edilir, lakin unikal olduğu üçün saxlanılmır

console.log(mySet); // Nəticə: Set { 1, 2 }
console.log(mySet.has(1)); // Nəticə: true (1 mövcuddur)
console.log(mySet.size); // Nəticə: 2 (Set-in ölçüsü)
```

### 57. Event loop nədir?

**Cavab:** Event loop JavaScript-də asinxron kodun icrasını idarə edən bir mexanizmdir. Bu mexanizm, əsas thread-in **bloklanmamasını** təmin edir və kodun effektiv şəkildə işləməsini təmin edir. Event loop, call stack, callback queue və microtask queue kimi hissələrdən istifadə edərək asinxron əməliyyatları idarə edir.

1. Call Stack: Sinxron əməliyyatlar burada icra olunur. Hər dəfə funksiya çağırıldıqda, bu funksiya call stack-ə əlavə olunur və icra edildikdən sonra stack-dən çıxarılır.

2. Web APIs: Asinxron əməliyyatlar (məsələn, setTimeout, fetch, DOM hadisələri) burada icra olunur. Web API-lər işə düşərkən nəticəni Call Stack-ə yönləndirmək üçün bir yerdə saxlayır.

3. Microtask Queue: Microtasks (məsələn, Promise callback-ləri və MutationObserver) burada toplanır. Web API-lər tamamlandıqdan sonra bu queue-dən tapşırıqlar Call Stack-ə keçirilməlidir.

4. Callback Queue (Macrotask Queue): Macrotasks (məsələn, setTimeout, setInterval callback-ləri) burada toplanır. Microtasks tamamlandıqdan sonra, Event Loop macrotasks-ları icra edir.

5. Event Loop: Call Stack boşaldıqda, Event Loop əvvəlcə Microtask Queue-dən bütün tapşırıqları (tasks) icra edir, sonra Callback Queue (Macrotask Queue)-dən tapşırıqları götürüb Call Stack-ə əlavə edir.

```js
console.log('Start');

setTimeout(() => {
  console.log('Timeout');
}, 0);

Promise.resolve().then(() => {
  console.log('Promise');
});

console.log('End');
// Start
// End
// Promise
// Timeout
```

### 58. null və undefined dəyərlər arasında fərq nədir?

**Cavab:**
`null` Qəsdən "boş" dəyər. Tipi object.
`undefined` Təyin edilməmiş dəyər. Tipi undefined.

### 59. Higher-order function nədir?

**Cavab:** Higher-order function (yüksək dərəcəli funksiya), ya funksiyaları arqument kimi qəbul edən, ya da funksiya qaytaran funksiyadır. Bu, JavaScript-də funksional proqramlaşdırmanın əsas konseptlərindən biridir.

### 60. Funksiya nədir?

**Cavab:** Funksiya, müəyyən bir işi yerinə yetirən və təkrar istifadə edilə bilən kod blokudur.

### 61. JavaScript engine nədir?

**Cavab:** JavaScript engine, JavaScript kodunu interpret edən və ya kompilyasiya edərək icra edən bir proqramdır. Bu, brauzerlərdə və ya Node.js kimi mühitlərdə JavaScript kodunun işləməsini təmin edir. Hər bir brauzerin öz JavaScript engine-i var.

### 62. Bəzi məşhur JavaScript engineləri hansılardır?

**Cavab:** Nümunələr V8 (Google Chrome tərəfindən istifadə olunur), SpiderMonkey (Firefox tərəfindən istifadə olunur) və JavaScriptCore (Safari tərəfindən istifadə olunur).

### 63. Type coercion nədir?

**Cavab:** Data tipinin avtomatik olaraq başqa bir tipə çevrilməsidir.

```js
console.log('5' + 2); // "52" (string)
console.log('5' == 5); // true (avtomatik çevrilmə)
```

### 64. JavaScript-də hansı data növləri var?

**Cavab:** JavaScript-də data növləri bunlardır: string, number, boolean, null, undefined, object və symbol.

### 65. IIFE (Immediately Invoked Function Expression) nədir?

**Cavab:** IIFE (Immediately Invoked Function Expression), təyin edildiyi kimi dərhal icra olunan funksiyadır.

### 66. Closure nədir?

**Cavab:** Closure, bir funksiyanın xarici funksiyanın dəyişənlərinə daxil olmasıdır.

```js
function outer() {
  let a = 10;
  return function inner() {
    console.log(a);
  };
}

const closure = outer();
closure(); // 10
```

### 67. Framework və Kitabxana arasındakı fərqlər nədir?

**Cavab:** Framework, tam bir tətbiqetmə qurmaq üçün qaydalar, təlimatlar və alətlər təqdim edir, kitabxana isə tətbiqetmə qurmaq üçün istifadə edilə bilən təkrar istifadə olunan funksiyalar və komponentlər kolleksiyası təqdim edir.

### 68. Call stack nədir?

**Cavab:** Call stack, JavaScript-də funksiya çağırışlarını izləyən LIFO (Last In, First Out) data strukturudur. Son daxil olan funksiya ilk icra olunur.

### 69. JavaScript-də call stack necə işləyir?

**Cavab:** Funksiya çağırıldıqda, call stack-in ən üstünə əlavə olunur. Funksiya icra olunub bitdikdə, stack-dən çıxarılır.

### 70. Stack overflow xətası nədir?

**Cavab:** Stack overflow xətası, JavaScript-də call stack-in maksimum ölçüsünü aşdığı zaman baş verir. Bu, adətən sonsuz dövr (infinite loop) və ya düzgün bitməyən rekursiv funksiya səbəbindən yaranır.

### 71. Garbage collector nədir?

**Cavab:** Proqram tərəfindən artıq istifadə edilməyən yaddaşı avtomatik olaraq təmizləyən bir mexanizmdir. Bu, yaddaş sızmalarının qarşısını almaq və yaddaşın səmərəli istifadəsini təmin etmək üçün vacibdir.

### 72. Hoisting nədir?

**Cavab:** Hoisting, JavaScript-də dəyişənlərin və funksiyaların, kod işə düşməzdən əvvəl avtomatik olaraq yuxarıya qaldırılmasıdır.

### 73. JavaScript də event-driven proqramlaşdırma nədir?

**Cavab:** Event-driven proqramlaşdırma, JavaScript-də hadisələrə (click, keypress, load və s.) reaksiya vermə modelidir. Event listener hadisəni izləyir və baş verdikdə bağlı olan funksiyanı işə salır.

```js
document.getElementById('btn').addEventListener('click', function () {
  console.log('Düymə klikləndi!');
});
```

### 74. querySelector və querySelectorAll metodları nədir?

**Cavab:** `querySelector` metodu, göstərilən CSS selektoruna uyğun ilk elementi seçir, `querySelectorAll` metodu isə göstərilən CSS selektoruna uyğun bütün elementləri seçir və NodeList qaytarır.

### 75. removeEventListener metodu nədir?

**Cavab:** removeEventListener metodu, bir elementə əlavə edilmiş hadisə işləyicisini (event handler) silmək üçün istifadə olunur.

### 76. setAttribute metodu nədir?

**Cavab:** `setAttribute` metodu, HTML elementinə müəyyən edilmiş atributun dəyərini təyin etmək üçün istifadə olunur.

```js
const image = document.getElementById('myImage');
image.setAttribute('src', 'new-image.jpg'); // src atributunu təyin et
```

### 77. getAttribute metodu nədir?

**Cavab:** `getAttribute` metodu, bir HTML elementinin müəyyən edilmiş atributunun dəyərini almaq üçün istifadə olunur. Bu metod, elementin atributunun dəyərini qaytarır.

```js
const link = document.getElementById('myLink');

// href atributunun dəyərini al
const hrefValue = link.getAttribute('href');
console.log(hrefValue); // Nəticə: "https://example.com"
```

### 78. DOM nədir?

**Cavab:** DOM (Document Object Model), HTML sənədlərini təmsil edən ağac quruluşudur. JavaScript ilə manipulyasiya edilərək veb səhifənin məzmunu və görünüşü dinamik olaraq dəyişdirilir

### 79. heap nədir?

**Cavab:** Heap, JavaScript-də dinamik olaraq yaradılan obyektlərin və mürəkkəb məlumat strukturlarının saxlandığı yaddaş hissəsidir. Yaddaş avtomatik olaraq ayrılır və garbage collection tərəfindən idarə olunur.

### 80. stack nədir?

**Cavab:** Stack, JavaScript-də funksiya çağırışlarını və lokal dəyişənləri saxlamaq üçün istifadə olunan yaddaş hissəsidir,

### 81. JavaScript-də test niyə vacibdir?

**Cavab:** Test etmək, JavaScript-də kodun düzgün işlədiyini yoxlamaq, bug-ları erkən aşkar etmək və kodun etibarlılığını artırmaq üçün vacibdir.

### 82. JavaScript-də test növləri hansılardır?

**Cavab:** JavaScript-də əsas test növləri bunlardır: unit tests, integration tests, functional tests və end-to-end testlər.

### 83. Unit Testing nədir?

**Cavab:** Ayrı-ayrı funksiyaları və ya modulları təcrid olunmuş şəkildə test etmək. cem(2, 3)-ün 5 qaytarmasını yoxlamaq.

### 84. Integration Testing nədir?

**Cavab:** Müxtəlif modulların bir-biri ilə düzgün işlədiyini yoxlamaq. API və verilənlər bazasının qarşılıqlı əlaqəsini test etmək.

### 85 .Functional Testing nədir?

**Cavab:** Tətbiqin funksionallığını istifadəçi tədbirlərini simulyasiya edərək yoxlamaq.Düymə klik edildikdə mətnin dəyişdiyini yoxlamaq.

### 86 .End-to-End Testing nədir?

**Cavab:**: Tətbiqin bütün axınını (frontend-dən backend-ə qədər) test etmək.İstifadəçi daxil olur və məlumatları görür.
