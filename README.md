這是一支從mssql 下select query 後可以把 column name+ table轉成csv的程式

套件:pyodbc,pandas

過程中遇到困難

1.中文encoding問題
  >>>原本我使用pymssql，但在轉中文時，即使我把python encoding 以及 讀取資料庫的預設編碼都設置utf-8，轉出來還是會有亂碼
  >>>solution:把套件改成pyodbc，因為此套件為microsoft釋出的，底層中文轉譯編碼才會與sql-server同步
  
2.insert,update資料失敗(未解決)
  >>>目前還在尋找原因
