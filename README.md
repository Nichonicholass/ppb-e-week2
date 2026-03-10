# Widgets
**Nicholas | 5025231031**

Aplikasi Flutter sederhana yang mendemonstrasikan penggunaan berbagai widget layout dan state management dasar.

## Deskripsi

Aplikasi ini adalah tutorial dasar Flutter yang menampilkan:
- Layout dengan Row dan Column
- Gambar dari internet
- Icon dengan label
- Counter interaktif dengan StatefulWidget

## Screenshot
Aplikasi ini menampilkan:
1. Gambar random dari Picsum Photos
2. Teks pertanyaan "What image is that"
3. Tiga pilihan kategori dengan icon (Food, Scenery, People)
4. Counter yang bisa ditambah dengan tombol

## Struktur Kode

### 1. MyApp (StatelessWidget)
Widget root aplikasi yang mengatur:
- `MaterialApp` sebagai wrapper utama
- Tema dengan warna ungu (deepPurple)
- Material Design 3
- Homepage mengarah ke `RowColumnPage`

### 2. RowColumnPage (StatelessWidget)
Halaman utama yang mendemonstrasikan layout dengan struktur:
- **AppBar**: Header dengan title "My First App" dan background orange
- **Body**: Column yang berisi beberapa Container dengan berbagai konten

### 3. CounterCard (StatefulWidget)
Widget interaktif yang menerapkan state management:
- Menampilkan counter yang dimulai dari 0
- Tombol dengan icon + untuk menambah counter
- Menggunakan `setState()` untuk update UI

## Widget yang Digunakan

### Layout Widgets
- **MaterialApp**: Root widget untuk aplikasi Material Design
- **Scaffold**: Struktur dasar halaman dengan AppBar dan Body
- **Column**: Menyusun children secara vertikal
- **Row**: Menyusun children secara horizontal
- **Container**: Box untuk styling (margin, padding, color, dll)
- **AspectRatio**: Menjaga rasio aspek widget (1:1 dalam kode ini)
- **Center**: Menempatkan child di tengah

### Display Widgets
- **AppBar**: Bar di bagian atas aplikasi
- **Text**: Menampilkan teks
- **Icon**: Menampilkan icon Material Design
  - `Icons.food_bank` - Icon makanan
  - `Icons.landscape` - Icon pemandangan
  - `Icons.people` - Icon orang
  - `Icons.add` - Icon tambah

### Interactive Widgets
- **IconButton**: Tombol dengan icon yang bisa diklik

### Media & Network Widgets
- **Image.network**: Menampilkan gambar dari URL
  - URL: `https://picsum.photos/200`
  - `fit: BoxFit.cover` - Mengatur cara gambar mengisi ruang

### Responsive Design
- **MediaQuery**: Mendapatkan informasi ukuran layar
  - `MediaQuery.of(context).size.width` - Lebar layar
  - `MediaQuery.of(context).size.height` - Tinggi layar

## Properties Penting

### Alignment & Distribution
- `crossAxisAlignment: CrossAxisAlignment.center` - Alignment horizontal pada Column
- `mainAxisAlignment: MainAxisAlignment.center` - Alignment vertikal pada Column
- `mainAxisAlignment: MainAxisAlignment.spaceEvenly` - Distribusi merata pada Row
- `mainAxisAlignment: MainAxisAlignment.spaceBetween` - Distribusi dengan space di antara

### Spacing
- `margin: EdgeInsets.fromLTRB(20.0, 5.0, 20.0, 10.0)` - Margin (left, top, right, bottom)
- `padding: EdgeInsets.all(20.0)` - Padding sama untuk semua sisi

### Styling
- `color: Colors.lightBlue[100]` - Warna background container
- `TextStyle(fontSize: 16)` - Style untuk text
- `backgroundColor: Colors.orange[200]` - Background color AppBar

## State Management

### StatelessWidget
Widget yang tidak memiliki state yang berubah:
- `MyApp`
- `RowColumnPage`

### StatefulWidget
Widget yang memiliki state yang bisa berubah:
- `CounterCard` - Memiliki `_counter` sebagai state yang di-update dengan `setState()`

### setState()
Method untuk memberitahu Flutter bahwa ada perubahan state dan UI perlu di-rebuild:
```dart
void _incrementCounter() {
  setState(() {
    _counter++; // Update the state.
  });
}
```
