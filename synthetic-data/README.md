使用Synthea產生Synthetic data

修改 synthea\src\main\resources\synthea.properties設定相關產出
- exporter.text.export = true
- exporter.text.per_encounter_export = true 
- exporter.clinical_note.export = true
- exporter.symptoms.text.export = true
  
可產生FHIR格式以外的資料，檔案結構如下：

![image](https://github.com/hongyu0324/HAPI-fhir-Lab/assets/5461401/ce3a0e97-7be4-4404-a4fa-aabbe31faa86)
