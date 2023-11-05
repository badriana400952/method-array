method array
• concat() digunakan untuk menggabungkan dua atau lebih array
• entries() cara untuk melihat nomor indeks dan nilainya dalam daftar (array). Jadi, Anda dapat melihat indeks (nomor 
posisi) dan nilainya untuk setiap elemen dalam array
• every() digunakan untuk memeriksa apakah semua elemen dalam array memenuhi suatu kondisi yang ditentukan oleh 
sebuah fungsi.
• Fill() dalam JavaScript digunakan untuk mengganti semua elemen dalam array dengan nilai yang diberikan. Metode ini 
mengubah array asli dan tidak membuat array baru.
• filter() dalam JavaScript digunakan untuk membuat array baru dengan elemen-elemen dari array yang memenuhi kondisi 
tertentu.
• find() dalam JavaScript digunakan untuk menemukan elemen pertama dalam array yang memenuhi kondisi tertentu yang 
diberikan oleh sebuah fungsi
• flat() dalam JavaScript digunakan untuk mengubah array yang bersarang (nested arrays) menjadi array satu dimensi
• Array.from() dalam JavaScript digunakan untuk membuat array baru dari objek yang dapat diiterasi atau array-like object 
(objek yang mirip array),
• includes() adalah metode di JavaScript yang digunakan untuk mengecek apakah suatu nilai tertentu ada dalam sebuah 
array.
• indexOf() dalam JavaScript digunakan untuk mencari posisi (indeks) suatu nilai dalam array. Jika nilai tersebut ditemukan, 
metode ini memberikan indeks dari nilai tersebut dalam array.
• isArray() dalam JavaScript digunakan untuk memeriksa apakah suatu variabel merupakan sebuah array atau bukan.
• join() dalam JavaScript digunakan untuk menggabungkan semua elemen dalam sebuah array ke dalam satu string.
• keys() adalah metode dalam JavaScript yang digunakan untuk mendapatkan indeks dari setiap elemen dalam sebuah array. 
Metode ini menghasilkan iterator yang bisa digunakan untuk mengakses indeks-indeks tersebut.
• map() dalam JavaScript digunakan untuk membuat array baru dengan mengubah setiap elemen dalam array yang ada.
• Array.of() adalah metode dalam JavaScript yang digunakan untuk membuat array baru dengan elemen-elemen yang 
diberikan sebagai argumen.
• pop() adalah metode dalam JavaScript yang digunakan untuk menghapus elemen terakhir dari sebuah array dan 
mengembalikan elemen tersebut.
• push() adalah metode dalam JavaScript yang digunakan untuk menambahkan satu atau lebih elemen ke akhir sebuah array 
dan mengembalikan panjang array yang baru.
• reduce() digunakan untuk menggabungkan semua angka dalam array menjadi satu angka, dengan menggunakan operasi 
matematika yang Anda tentukan.
• reverse() membalikkan urutan angka atau kata dalam array.
• shift() menghapus angka atau kata pertama dari array dan menggeser sisanya ke depan.
• slice() membuat salinan baru dari sebagian angka atau kata dalam array, tanpa mengubah array aslinya.
• some() adalah metode dalam JavaScript yang digunakan untuk memeriksa apakah setidaknya satu elemen dalam array 
memenuhi kondisi tertentu.
• sort() mengurutkan angka atau kata dalam array dari yang terkecil ke yang terbesar (jika angka) atau berdasarkan urutan 
alfabet (jika kata).
• splice() digunakan untuk menghapus, mengganti, atau menambah angka atau kata dalam array.
• toLocaleString() mengubah angka dalam array menjadi bentuk yang sesuai dengan pengaturan lokal (format angka dalam 
bahasa dan angka desimal lokal).
• unshift() menambahkan angka atau kata baru ke awal array, menggeser angka atau kata lain ke posisi selanjutnya.
• values() mengembalikan iterator yang memungkinkan Anda mengakses angka atau kata dalam array satu per satu.
const namaBuah = [
{
id: 1,
name: 'mangga',
price: 20000
}
];
const namaMinuman = [
{
id: 1,
name: 'teh',
price: 40000
}
];
// Metode: concat()
const semuaItem = namaBuah.concat(namaMinuman);
console.log(semuaItem);
// Output: [ { id: 1, name: 'mangga', price: 20000 }, { id: 1, name: 'teh', price: 40000 } ]
// Metode: entries()
const buahEntries = Object.entries(namaBuah[0]);
console.log(buahEntries);
// Output: [ [ 'id', 1 ], [ 'name', 'mangga' ], [ 'price', 20000 ] ]
// Metode: every()
const semuaHargaDiBawah50000 = semuaItem.every(item => item.price < 50000);
console.log(semuaHargaDiBawah50000);
// Output: true (karena semua item memiliki harga di bawah 50000)
// Metode: fill()
const arrayKosong = new Array(3);
arrayKosong.fill('isi');
console.log(arrayKosong);
// Output: [ 'isi', 'isi', 'isi' ]
// Metode: filter()
const itemDenganHargaDiatas30000 = semuaItem.filter(item => item.price > 30000);
console.log(itemDenganHargaDiatas30000);
// Output: [ { id: 1, name: 'teh', price: 40000 } ]
// Metode: find()
const buahDitemukan = semuaItem.find(item => item.name === 'mangga');
console.log(buahDitemukan);
// Output: { id: 1, name: 'mangga', price: 20000 }
// Metode: flat()
const arrayNested = [1, [2, 3], [4, [5]]];
const arrayFlat = arrayNested.flat(2);
console.log(arrayFlat);
// Output: [ 1, 2, 3, 4, 5 ]
// Metode: forEach()
semuaItem.forEach(item => {
console.log(`Nama: ${item.name}, Harga: ${item.price}`);
});
// Output: Nama: mangga, Harga: 20000
// Nama: teh, Harga: 40000
// Metode: from()
const arrayDariNama = Array.from('JavaScript');
console.log(arrayDariNama);
// Output: [ 'J', 'a', 'v', 'a', 'S', 'c', 'r', 'i', 'p', 't' ]
// Metode: includes()
const apakahTehAda = semuaItem.some(item => item.name === 'teh');
console.log(apakahTehAda);
// Output: true (karena 'teh' ada dalam array)
// Metode: indexOf()
const indexMangga = semuaItem.findIndex(item => item.name === 'mangga');
console.log(indexMangga);
// Output: 0 (karena 'mangga' ada di indeks 0 dalam array)
// Metode: isArray()
console.log(Array.isArray(semuaItem));
// Output: true (karena semuaItem adalah array)
// Metode: join()
const namaBuahString = namaBuah.map(item => item.name).join(', ');
console.log(namaBuahString);
// Output: 'mangga' (menggabungkan nama buah menjadi string terpisah oleh koma)
// Metode: keys()
const keysBuah = Object.keys(namaBuah[0]);
console.log(keysBuah);
// Output: [ 'id', 'name', 'price' ] (mengambil kunci-kunci properti objek)
// Metode: map()
const hargaDikaliDua = semuaItem.map(item => ({ ...item, price: item.price * 2 }));
console.log(hargaDikaliDua);
// Output: [ { id: 1, name: 'mangga', price: 40000 }, { id: 1, name: 'teh', price: 80000 } ]
// Metode: of()
const arrayBaru = Array.of(1, 2, 3, 4, 5);
console.log(arrayBaru);
// Output: [ 1, 2, 3, 4, 5 ] (membuat array baru dengan elemen-elemen yang diberikan)
// Metode: pop()
const buahTerakhir = semuaItem.pop();
console.log(buahTerakhir);
// Output: { id: 1, name: 'teh', price: 40000 } (elemen terakhir dihapus dari array)
// Metode: push()
semuaItem.push({ id: 2, name: 'jeruk', price: 30000 });
console.log(semuaItem);
// Output: [ { id: 1, name: 'mangga', price: 20000 }, { id: 2, name: 'teh', price: 40000 }, { 
id: 2, name: 'jeruk', price: 30000 } ] (menambahkan elemen baru ke array)
// Metode: reduce()
const totalHarga = semuaItem.reduce((acc, item) => acc + item.price, 0);
console.log(totalHarga);
// Output: 90000 (menghitung total harga dari semua item)
// Metode: reverse()
const reversedItem = [...semuaItem].reverse();
console.log(reversedItem);
// Output: [ { id: 2, name: 'jeruk', price: 30000 }, { id: 2, name: 'teh', price
const itemPertama = semuaItem.shift();
console.log(itemPertama);
// Output: { id: 1, name: 'mangga', price: 20000 } (elemen pertama dihapus dari array)
const sliceItem = semuaItem.slice(1, 2);
console.log(sliceItem);
// Output: [ { id: 2, name: 'teh', price: 40000 } ] (membuat salinan elemen dari indeks 1 
hingga 1, indeks 2 tidak termasuk)
const adaItemDenganHargaDiatas25000 = semuaItem.some(item => item.price > 25000);
console.log(adaItemDenganHargaDiatas25000);
// Output: true (karena ada item dengan harga di atas 25000 dalam array)
const itemDenganUrutanAlfabet = [...semuaItem].sort((a, b) => a.name.localeCompare(b.name));
console.log(itemDenganUrutanAlfabet);
// Output: [ { id: 2, name: 'jeruk', price: 30000 }, { id: 1, name: 'mangga', price: 20000 }, 
{ id: 2, name: 'teh', price: 40000 } ] (mengurutkan item berdasarkan nama secara alfabetis)
const indexItemTeh = semuaItem.findIndex(item => item.name === 'teh');
semuaItem.splice(indexItemTeh, 1, { id: 2, name: 'susu', price: 35000 });
console.log(semuaItem);
// Output: [ { id: 1, name: 'mangga', price: 20000 }, { id: 2, name: 'susu', price: 35000 }, { 
id: 2, name: 'jeruk', price: 30000 } ] (mengganti item 'teh' dengan 'susu' dalam array)
const arrayToString = semuaItem.toString();
console.log(arrayToString);
// Output: " [object Object],[object Object],[object Object] " (mengubah array menjadi string)
const nilaiItem = Object.values(semuaItem[0]);
console.log(nilaiItem);
// Output: [ 1, 'mangga', 20000 ] (mengambil nilai-nilai properti objek dalam array pertama)
