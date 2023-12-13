使用Synthea產生Synthetic data
修改 $synthea$\src\main\resources\synthea.properties設定相關產出
- exporter.text.export = true
- exporter.text.per_encounter_export = true 
- exporter.clinical_note.export = true
- exporter.symptoms.text.export = true
可產生FHIR格式以外的資料