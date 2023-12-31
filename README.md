# HAPI-fhir-Lab
HAPI FHIR Java SDK教學

本實驗課程希望透過互動方式，達到以下目的：

- 了解基本FHIR API與HAPI FHIR Java SDK操作
- 透過一接近"真實案例"方式，讓開發人員可以Step by Step從零出發，建立開發環境。

基本架構參考 https://github.com/Aidbox/jupyter-course, 提供HAPI FHIR Java版本的教學資料。

相關Java設定則是參考HAPI FHIR所提供之hapi-fhirstarters-client-skeleton設定後修改。相關網址：https://github.com/FirelyTeam/fhirstarters/tree/master/java/hapi-fhirstarters-client-skeleton/

主要目的為教學使用，因此採用了互動式的架構。選擇vscode + Jupyter + iJava為開發環境。IJAVA相關訊息可參考：https://github.com/SpencerPark/IJava

測試資料使用 Synthea產生，詳細資料可參考 https://mitre.github.io/fhir-for-research/modules/synthea-overview

執行步驟：
- 取得Lab Source Code
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
- 執行與測試

課程區分為三部分：
- FHIR基礎課程
  - 基本CRUD操作
  - Synthetic資料匯入
  - 合成資料重整與分析(Option)
  - FHIR Search API
  - IPS測試(使用Server operation: $summary)：目前IPS尚在發展階段，並非預設功能。需要將環境變數hapi.fhir.ips_enabled設定為true
  ```
  hapi.fhir.ips_enabled: true
  ```
- 虛擬診所與病患看病流程
- FHIR進階議題
