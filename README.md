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

### 8.Javascript-də for..in döngəsi ilə for..of döngəsi arasında fərq nədir?

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

### 9.Javascript-də ox funksiyası ilə regular funksiya arasındakı fərq nədir

**Cavab:**
Ox funksiyalarının daha qısa sintaksisi vardır və `this` dəyərini avtomatik olaraq daxil olduğu kontekstə bağlayır, regular funksiyalar isə daha uzun sintaksiyaya malikdir və `this` dəyəri funksiyanın necə çağırılmasından asılı olaraq təyin olunur.

### 10.Javascript-də var, let və const arasındakı fərq nədir?

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

### 17.JavaScript-də this açar sözü nədir?

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
