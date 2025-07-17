# World-University-Rankings-Visualization-Plotly

# World University Rankings Analysis

## Proje Açıklaması
Bu projede, Times Higher Education tarafından sağlanan dünya üniversite sıralamalarına ait veri seti kullanılarak çeşitli veri ön işleme ve görselleştirme işlemleri yapılmıştır. Amaç, üniversitelerin farklı kriterler bazında performanslarını incelemek ve ülkeler bazında üniversite dağılımını görselleştirmektir.

## Kullanılan Veri Seti
- **timesData.csv**  
  Dünya genelindeki üniversitelerin yıllara göre sıralama verilerini içerir.  
  Toplam 2603 satır ve 14 sütun bulunmaktadır.  

## Veri Seti Kolonları
- `world_rank`: Dünya sıralaması (sayı veya aralık şeklinde)
- `university_name`: Üniversite adı
- `country`: Ülke adı
- `teaching`: Öğretim skoru
- `international`: Uluslararası skor (object türünde, bazıları yüzde ya da oran olarak ifade edilmiş)
- `research`: Araştırma skoru
- `citations`: Atıf skoru
- `income`: Gelir skoru (object türünde, eksik veya '-' olabilir)
- `total_score`: Toplam puan (object türünde)
- `num_students`: Öğrenci sayısı (eksik değerler var)
- `student_staff_ratio`: Öğrenci-öğretim üyesi oranı (eksik değerler var)
- `international_students`: Uluslararası öğrenci oranı (eksik değerler var)
- `female_male_ratio`: Kadın-erkek oranı (eksik değerler var)
- `year`: Yıl

## Veri Temizleme ve Ön İşleme
- Eksik değer içeren satırlar (`num_students`, `student_staff_ratio`, `international_students`, `female_male_ratio`) `dropna()` ile kaldırıldı.
- `num_students` sütunu sayısal değerlere dönüştürülürken, içindeki binlik ayraçlar (",") kaldırıldı.
- `total_score` sayısal değere çevrildi.
- Bazı sütunlar string formatında olduğu için uygun veri tiplerine dönüştürme işlemleri yapıldı.

## Görselleştirmeler

### 1. 2016 Yılında En Fazla Üniversiteye Sahip 10 Ülke
- Pasta grafiği ile gösterildi.

### 2. Üniversite Sıralaması ve Toplam Puan İlişkisi
- Bubble chart ile dünya sıralaması ve toplam puan ilişkisi, baloncuk büyüklüğü öğrenci sayısı olarak görselleştirildi.

### 3. Ülkelere Göre Uluslararası Öğrenci Oranı
- Box plot ile ülkelerdeki uluslararası öğrenci oranları karşılaştırıldı.

### 4. Toplam Puan Bazında En İyi 10 Üniversite
- Bar chart ile gösterildi.

### 5. Ülkelere Göre Üniversite Sayısı
- Bar chart ile ülkelerin üniversite sayıları karşılaştırıldı.

## Kullanılan Kütüphaneler
- pandas
- numpy
- plotly (plotly.express, plotly.graph_objs)

## Nasıl Çalıştırılır?
1. Veri setini `timesData.csv` olarak indirin ve çalışma dizinine koyun.
2. Gerekli Python kütüphanelerini kurun (pandas, numpy, plotly).
3. Jupyter Notebook veya Python ortamında kodu çalıştırın.
4. Görselleştirmeler interaktif olarak görüntülenecektir.
