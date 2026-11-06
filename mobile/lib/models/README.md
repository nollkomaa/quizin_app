# Fungsi Folder
Mempresentasikan objek dari backend Laravel

# Aturan
Format JSON mentah tidak bisa langsung di dalam kode Dart Flutter. Oleh karena itu, dibuatlah file model seperti QuizModule.dart. Di dalam file ini, data JSON tersebut diubah menjadi objek berbasis pemrograman berorientasi objek (OOP) di Dart

# Contoh
class QuizModule {
  final int id;
  final int title;
  final String description;

  QuizModule({required this.id, required this.title, required this.description});

  // Fungsi untuk menerjemahkan JSON dari Laravel ke Objek Dart
  factory QuizModule.fromJson(Map<String, dynamic> json) {
    return QuizModule(
      id: json['id'],
      title: json['title'],
      description: json['description'],
    );
  }
}

# Tujuan
Jika ingin menampilkan judul kuis di layar HP, kamu tinggal memanggil kodenya dengan rapi (misalnya quizModule.title) tanpa harus pusing memikirkan format JSON mentahnya lagi.