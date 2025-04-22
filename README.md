# az204-Cosmos DB test 

## 說明

此專案示範如何使用 Azure Cosmos DB SDK 進行基本的資料庫操作，包括建立資料庫、建立容器、新增資料及查詢資料。

## 使用步驟

1. **設定 Cosmos DB 資訊**  
   開啟 `Program.cs`，找到以下程式碼片段，並將 `EndpointUri` 和 `PrimaryKey` 替換為您 Azure Cosmos DB 的實際值：
   ```csharp
   private static readonly string EndpointUri = "https://___________.documents.azure.com:443/";
   private static readonly string PrimaryKey = "4qZoWiSUj0eoFDkF6Zhiqo________________DbrXcAxg==";
   ```

2. **執行程式**  
   使用 .NET CLI 或 Visual Studio 執行此專案：
   - 若使用 .NET CLI，執行以下指令：
     ```bash
     dotnet run
     ```
   - 若使用 Visual Studio，按下 `F5` 或點擊 `Start` 按鈕。

3. **功能說明**  
   - **建立資料庫與容器**  
     程式會自動建立名為 `az204Database` 的資料庫及名為 `az204Container` 的容器。
   - **新增資料**  
     程式會提示輸入要新增的資料筆數，並使用 `https://api.namefake.com/` 動態產生假資料。
   - **查詢資料**  
     程式會提示輸入查詢關鍵字，並顯示符合條件的資料。

4. **注意事項**  
   - 確保您的 Cosmos DB 帳戶已啟用並可正常連線。
   - 若遇到連線問題，請檢查網路設定及 Cosmos DB 的防火牆規則。

## 程式碼結構

- `Program.cs`  
  包含主要邏輯，包括 Cosmos DB 的初始化、資料庫與容器的建立、新增資料及查詢資料的功能。
- `DataRecord`  
  定義資料結構，包含 `id`、`LastName`、`FirstName`、`Address` 和 `FullName` 等欄位。
