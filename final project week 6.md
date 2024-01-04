install.packages("RSQLite")
library("RSQLite")
sql.info <- sqlTypeInfo(conn)
conn.info <- odbcGetInfo(conn)
conn.info["DBMS_Name"]
conn.info["DBMS_Ver"]
conn.info["Driver_ODBC_Ver"] 
sqlSave(Conn, crop_df, "CROP_DATA", append=TRUE, fast=TRUE, rownames=FALSE, colnames=FALSE, verbose=FALSE)
sqlSave(Conn, crop_df, "FARM_PRICES", append=TRUE, fast=TRUE, rownames=FALSE, colnames=FALSE, verbose=FALSE)
sqlSave(Conn, crop_df, "DAILY_FX", append=TRUE, fast=TRUE, rownames=FALSE, colnames=FALSE, verbose=FALSE)
sqlSave(Conn, crop_df, "MONTHLY", append=TRUE, fast=TRUE, rownames=FALSE, colnames=FALSE, verbose=FALSE)