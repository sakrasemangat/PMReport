# PMReport
PMReport adalah sebuah Ansible Playbook yang bisa digunakan untuk mengambil informasi Linux sistem operasi yang dibutuhkan untuk keperluan pembuatan laporan pemeliharaan sistem operasi

# Disclaimer
Ansible Playbook ini digunakan untuk kebutuhan Internal tim TSS-Integrator PT. Berca Hardayaperkasa, yang digunakan untuk membantu Linux Engineer melakukan pengumpulan data yang akan digunakan untuk pembuatan dokumen laporan maintenance.
Kami tidak bertanggung jawab atas hal-hal yang terjadi akibat dari menjalankan Playbook ini, baik kebocoran data atau informasi mengenai konfigurasi sistem, maupun hilangnya data. Untuk informasi lebih detail mengenai Playbook ini silakan Anda menghubungi penulis melalui email.

# Kebutuhan Konfigurasi
1. Create user student pada control dan managed (target) node.
2. Konfigurasi ssh tanpa password antara control dan managed (target) node, untuk user student.
   
# Cara Menggunakan
1. Untuk menggunakan Ansible Playbook ini, tentunya Anda diharuskan untuk menginstal package Ansible Core ataupun Navigator pada sebuah vm atau server baremetal.
2. Setelah Anda menginstal paket ansible-core atau ansible-navigator, pull repository Ansible playbook ini secara keseluruhan.
3. Setelah Anda pull repository ini ke control node, lakukan perubahan sebagai berikut:
   a. Review file ansible.cfg dan sesuaikan dengan lingkungan control node Anda.
   b. Ubah isi file inventory dan sesuaikan dengan managed (target) node yang ingin Anda kelola.
   c. Jalankan file playbook PMReport.yml dengan menggunakan perintah ansible-playbook atau ansible-navigator.
4. Untuk hasil dari ansible playbook ini, bisa dilihat di dalam direktori /home/student/maintenance_report_date, atau jika Anda ingin mengubah direktori penyimpanan, Anda bisa ubah di file save_dir.yml dan fetch_file.yml pada direktori ../PMReport/tasks.

# Credit
1. Penulis : Sakra Aprila (sakra.aprila@berca.co.id)
2. Supervisi: Arief Furqon
3. Team Support: - Junizar
                 - Reza Septian Putra
