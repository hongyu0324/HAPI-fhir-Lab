# HAPI-fhir-Lab
HAPI FHIR Java SDK教學

基本架構參考 https://github.com/Aidbox/jupyter-course,提供HAPI FHIR Java版本的教學資料。

相關Java設定則是參考HAPI FHIR所提供之hapi-fhirstarters-client-skeleton設定後修改。相關網址：https://github.com/FirelyTeam/fhirstarters/tree/master/java/hapi-fhirstarters-client-skeleton/

主要目的為教學使用，因此採用了互動式的架構。選擇vscode + Jupyter + iJava為開發環境。IJAVA相關訊息可參考：https://github.com/SpencerPark/IJava

- 安裝HAPI FHIR Server + Postgres
  - 使用Docker Compose 
  ```
  docker compose up
  ```
- 安裝VSCode https://code.visualstudio.com/
- 安裝iJava
  ```
  git clone https://github.com/SpencerPark/IJava.git
  cd IJava/
  python install.py --sys-prefix
  ```
- 下載Synthea
  ```
  git clone https://github.com/synthetichealth/synthea.git
  cd synthea
  ./gradlew build check test
  ```
- 產生合成資料(Synthetic Data)，產生10筆病患資料
  ```
  run_synthea -p 10
  ```
- 取得Lab Source Code
