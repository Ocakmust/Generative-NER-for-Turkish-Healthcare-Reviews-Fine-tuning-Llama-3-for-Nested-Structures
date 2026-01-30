# Generative-NER-for-Turkish-Healthcare-Reviews-Fine-tuning-Llama-3-for-Nested-Structures

Bu proje, Meta Llama-3.1-8B-Instruct modelini kullanarak Türkçe takviye edici gıda (vitamin & supplement) yorumlarından varlık ismi çıkarma (NER) işlemini gerçekleştirmektedir. Model, Unsloth kütüphanesi aracılığıyla QLoRA (Quantized Low-Rank Adaptation) tekniği kullanılarak eğitilmiştir.  Standart NER modellerinin aksine, bu proje Generative NER yaklaşımını benimser ve çıktıları yapılandırılmış XML formatında üretir. Bu sayede iç içe geçmiş (Nested) varlıkları (örneğin bir yan etkinin içinde geçen bir hastalık ismini) başarıyla tespit edebilir.  

 Özellikler 
 
-Generative Approach: Metni sınıflandırmak yerine, etiketlenmiş halini yeniden yazar (Text-to-Text). 
-Nested NER Yeteneği: İç içe geçmiş karmaşık yapıları çözümler (Örn: <ETKI>...<HASTALIK>...</HASTALIK>...</ETKI>).  
-XML Çıktı Formatı: Sonuçları hiyerarşik ve parse edilebilir bir yapıda sunar.  
-Verimli Eğitim: Unsloth ve 4-bit Quantization sayesinde A100/T4 GPU üzerinde düşük bellek kullanımı ile eğitilmiştir.  
-Türkçe Medikal Bağlam: Takviye edici gıda alanındaki argo, yazım yanlışları ve terimlere hakimdir.
