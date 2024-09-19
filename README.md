## Projenin Kaggle linki : https://www.kaggle.com/code/zeynepuysall/carprices-ml
    
# Araç Satış Veri Seti Analizi ve Makine Öğrenimi

Bu proje, araç satış veri seti üzerinde çeşitli veri analizleri ve makine öğrenimi modellemeleri yapmayı amaçladım.

## Veri Seti Hakkında

Veri seti, araç ve araç satışları ile ilgili çeşitli bilgileri içeriyor. Veri setindeki sütunlar:

•	year: Araç model yılı

•	make : Araç yapım yılı

•	model, trim : aracın model ve seri bilgileri

•	body: araç tipi(suv,sedan vb)

•	condition: Araç durumu (örneğin, yeni, kullanılmış)

•	odometer: Araç kilometre bilgisi

•	color : renk bilgisi

•	state: üretim yeri

•	mmr: Araç piyasa değeri

•	sellingprice: Araç satış fiyatı

•	saledate: Satış tarihi

# Adımlar
## Veri Seti Yükleme 
Kod başlangıcında pandas kütüphanesi kullanılarak veri seti yükledim.

## Veri Analizi
İnfo(), head(), describe().T , .isna().sum() gibi fonksiyonlar kullanarak ve veri analizine başladım. Seaborn ve matplotlib kütüphaneleriyle bazı görselleştirmeler yaptım.

•	En Çok Satılan Araç Tipleri: body özelliğine göre en çok satılan 10 araç tipi çubuk grafik ile gösterdim.

•	En Çok Satılan Araç Modelleri: model özelliğine göre en çok satılan 10 araç modeli çubuk grafik ile gösterdim.

•	Korelasyon Analizi: year, condition, odometer, mmr, sellingprice özellikleri arasındaki korelasyonlar ısı haritasıyla görselleştirdim.

## Veri Ön İşleme
•	Gereksiz Sütunlar Kaldırma: Araç satış fiyatı üzerinde etkisinin az olduğunu düşündüğüm vin, state, seller, interior sütunları veri setinden çıkarttım.

•	Eksik Değerlerin Doldurulması: sellingprice özelliği eksik olan az satır bulunuyordu onları cıkarttım ve diğer sütunlardaki  nan satırları sayısal özellikler medyan değeri ile doldurdum.

•	Label Encoding: Makine öğrenimi için satırların sayısal değerlerden oluşması gerekir bu nedenle make, model, trim, transmission, body, color, sale_month sütunlarını label encoding kullanarak sayısal değerlere dönüştürdüm.

•	Bağımlı ve bağımsız değişkenler : Satıs fiyatını bağımlı degısken , geri kalanları ise bağımsız değişken olarak belirledim.

•	Veri setini parçalama: Veri setimi test ve train olarak parçaladım.

## Makine Öğrenimi Modelleri
•	Doğrusal Regresyon: Veri seti üzerinde doğrusal regresyon modelini eğittim ve performansı hesapladım.

•	Karar Ağacı Regresyonu: Karar ağacı kullanılarak bir regresyon modeli oluşturdum ve test verileri ile performansı ölçtüm.

•	k-En Yakın Komşular (kNN): kNN algoritması ile sınıflandırma modeli eğittim ve doğruluğu değerlendirdim.

•	KMeans Kümeleme: Veri seti üzerinde KMeans kümeleme algoritması uyguladım 

•	Cross validation ile daha doğru bir sonuç almayı hedefledim.

## Sonuçlar
•	Her bir modelin performansı (R² skoru, doğruluk skoru vb.) ayrıntılı olarak raporladım.

•	Linear regresyon modeli en yüksek scor alınan model olur ve  MSE, R² skorları hesapladım

Lineer Regresyon ve decision tree de 0.90 larda bir scor alırken kNN ve kMeans algoritmalarında skor 0.02 bandındaydı bunun sebebini anlamadım.

