# Generative-NER-for-Turkish-Healthcare-Reviews-Fine-tuning-Llama-3-for-Nested-Structures

Model linki: https://huggingface.co/mocak2/Turkish-Healthcare-Reviews-Fine-tuning-Llama-3#model-card-for-model-id

Bu proje, Meta Llama-3.1-8B-Instruct modelini kullanarak Türkçe takviye edici gıda (vitamin & supplement) yorumlarından varlık ismi çıkarma (NER) işlemini gerçekleştirmektedir. Model, Unsloth kütüphanesi aracılığıyla QLoRA (Quantized Low-Rank Adaptation) tekniği kullanılarak eğitilmiştir.  Standart NER modellerinin aksine, bu proje Generative NER yaklaşımını benimser ve çıktıları yapılandırılmış XML formatında üretir. Bu sayede iç içe geçmiş (Nested) varlıkları (örneğin bir yan etkinin içinde geçen bir hastalık ismini) başarıyla tespit edebilir.  

 Özellikler 
 
-Generative Approach: Metni sınıflandırmak yerine, etiketlenmiş halini yeniden yazar (Text-to-Text). 
-Nested NER Yeteneği: İç içe geçmiş karmaşık yapıları çözümler (Örn: <ETKI>...<HASTALIK>...</HASTALIK>...</ETKI>).  
-XML Çıktı Formatı: Sonuçları hiyerarşik ve parse edilebilir bir yapıda sunar.  
-Verimli Eğitim: Unsloth ve 4-bit Quantization sayesinde A100/T4 GPU üzerinde düşük bellek kullanımı ile eğitilmiştir.  
-Türkçe Medikal Bağlam: Takviye edici gıda alanındaki argo, yazım yanlışları ve terimlere hakimdir.



Citation

This project utilizes the "Vitamins and Supplements NER and Span Dataset". 
If you use this model or dataset in your research, please cite the original work as requested by the author:

```bibtex
@inproceedings{altinok-2023-diverse,
    title = "A Diverse Set of Freely Available Linguistic Resources for {T}urkish",
    author = "Altinok, Duygu",
    booktitle = "Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.acl-long.768",
    pages = "13739--13750",
    abstract = "This study presents a diverse set of freely available linguistic resources for Turkish natural language processing, including corpora, pretrained models and education material. Although Turkish is spoken by a sizeable population of over 80 million people, Turkish linguistic resources for natural language processing remain scarce. In this study, we provide corpora to allow practitioners to build their own applications and pretrained models that would assist industry researchers in creating quick prototypes. The provided corpora include named entity recognition datasets of diverse genres, including Wikipedia articles and supplement products customer reviews. In addition, crawling e-commerce and movie reviews websites, we compiled several sentiment analysis datasets of different genres. Our linguistic resources for Turkish also include pretrained spaCy language models. To the best of our knowledge, our models are the first spaCy models trained for the Turkish language. Finally, we provide various types of education material, such as video tutorials and code examples, that can support the interested audience on practicing Turkish NLP. The advantages of our linguistic resources are three-fold: they are freely available, they are first of their kind, and they are easy to use in a broad range of implementations. Along with a thorough description of the resource creation process, we also explain the position of our resources in the Turkish NLP world.",
}
