使用Synthea產生Synthetic data

修改 synthea\src\main\resources\synthea.properties設定相關產出
- exporter.fhir.use_us_core_ig = false (不使用US Core IG)
- exporter.text.export = true
- exporter.text.per_encounter_export = true 
- exporter.clinical_note.export = true
- exporter.symptoms.text.export = true
```
 .\run_synthea -p 10
```
可產生FHIR格式以外的資料，檔案結構如下：

![image](https://github.com/hongyu0324/HAPI-fhir-Lab/assets/5461401/44a202f8-484f-478c-b740-88e799466f32)

