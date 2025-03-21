Metro Ağı Simülasyonu

1. Proje Başlığı ve Kısa Açıklama

Bu proje, bir metro ağı simülatörüdür. Python kullanılarak geliştirilen bu proje, belirli bir metro hattı üzerinde en az aktarmalı rotayı ve en hızlı rotayı bulmayı amaçlar.

Projenin Amaçları:

Kullanıcının belirlediği başlangıç ve hedef istasyonlar arasında en az aktarma yaparak ulaşımı sağlamak.

Kullanıcının belirlediği başlangıç ve hedef istasyonlar arasında en hızlı rota hesaplamak.

Gerçek dünya metro sistemlerine benzer bir yapı sunarak ağ analizlerini mümkün kılmak.

2. Kullanılan Teknolojiler ve Kütüphaneler

Python Kütüphaneleri:

collections: Özellikle deque veri yapısını kullanarak BFS (Genişlik Öncelikli Arama) algoritmasını optimize etmek için kullanılmıştır.

heapq: A* algoritmasının öncelik kuyruğu veri yapısını yönetmek için kullanılmıştır.

typing: Tür belirleyici olarak Dict, List, Tuple gibi veri yapılarını daha okunaklı hale getirmek için kullanılmıştır.

3. Algoritmaların Çalışma Mantığı

BFS Algoritması (En Az Aktarmalı Rota)

BFS (Breadth-First Search), en kısa adım sayısını bulmaya yönelik bir arama algoritmasıdır.

Bu projede en az aktarmalı rota bulmak için kullanılmıştır.

Çalışma Mantığı:

Başlangıç istasyonunu kuyruğa ekler.

Her iterasyonda mevcut istasyonu kontrol eder.

Eğer hedef istasyon bulunursa durur ve sonucu döndürür.

Komşu istasyonları sırayla kuyruğa ekler ve ziyaret edildiğini işaretler.
