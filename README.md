> **Not:** Bu proje, 2025 yılı bahar döneminde Gazi Üniversitesi BMT-110 Bilgisayar Programlama dersi kapsamında geliştirilmiştir.

# Course Registration System

![Status](https://img.shields.io/badge/Status-Completed-success.svg) ![Language](https://img.shields.io/badge/Language-C%23-blue.svg) ![Framework](https://img.shields.io/badge/Framework-.NET_Windows_Forms-purple.svg) ![Database](https://img.shields.io/badge/Database-SQL_Server-lightgrey.svg)

Bu proje, üniversite öğrencilerinin müfredatlarında bulunan derslerin şubelerini saat çakışması ve kontenjan durumlarını gözeterek seçebilmelerini, haftalık ders programlarını oluşturabilmelerini ve bu verilerin güvenli bir şekilde saklanmasını sağlayan bir masaüstü otomasyon sistemidir.

## Temel Özellikler

- **Şube ve Kontenjan Yönetimi:** Öğrencilerin kendilerine sunulan ders şubelerini görüntüleyip kontenjan dahilinde seçim yapabilmesi.
- **Dinamik Çakışma Kontrolü:** Seçilen derslerin gün ve saat bilgilerinin arka planda karşılaştırılarak çakışma durumunda kullanıcıya uyarı verilmesi ve işlemin durdurulması.
- **Otomatik Ders Programı:** Onaylanan ders seçimlerinin haftalık ders programı ızgarasına (grid) otomatik olarak yerleştirilmesi.
- **Kullanıcı Oturum Sistemi:** Öğrenci numarası ve şifre ile güvenli kimlik doğrulama, kullanıcıya özel veri listeleme ve çıkış işlemleri.

## Kullanılan Teknolojiler

- **Programlama Dili:** C# (.NET Framework)
- **Kullanıcı Arayüzü:** Windows Forms (Sekmeli/TabControl mimarisi)
- **Veritabanı:** SQL Server
- **ORM (Nesne-İlişkisel Eşleme):** Entity Framework

## Veritabanı Mimarisi

Sistem, 6 farklı tablodan oluşan tam ilişkisel bir SQL veritabanı üzerine kurulmuştur:

- **Departments:** Akademik bölümlerin listesi.
- **Curricula:** Bölümlere ve yıllara göre özelleşmiş müfredat planları.
- **Courses:** Müfredata bağlı temel ders kodları ve tanımları.
- **CourseSections:** Derslerin gün, saat, kontenjan, sınıf (örn. Lab-5, B-01) ve öğretim görevlisi bazında açılan şubeleri.
- **Students:** Sistemdeki öğrenci kimlik, şifre ve bölüm bilgileri.
- **StudentCourseSelections:** Öğrencilerin seçip onayladığı şubelerin (SectionID ve CourseID) kaydedildiği bağlayıcı tablo[cite: 36].
