# - R - TUTORIAL
 - https://data-flair.training/blogs/rstudio-tutorial/
 - https://www.tutorialspoint.com/r/r_pie_charts.htm
 
 

# R - Scripts R
- INSTALLED.PACKAGES - VERIFICA SE O PACOTE EXISTE


## COMANDO QUE VERIFICA SE O PACOTE EXISTE, CASO CONTRARIO INSTALA
```
pkgs <- c("RCurl","jsonlite")
for (pkg in pkgs) {
  if (! (pkg %in% rownames(installed.packages()))) { install.packages(pkg) }
  or 
  if (! (pkg %in% (.packages())) { install.packages(pkg) }
}
```
## - COMANDO QUE INSTALA O H2O
install.packages("h2o", type="source", repos=(c("http://h2o-release.s3.amazonaws.com/h2o/latest_stable_R")))


# RMySQL
## CONEXÃO
```
library(RMySQL)

connection <- function(){
  tryCatch({
    conn = dbConnect(MySQL(),db="phdrisk",user="user",password="12345678",host="xxx.xxx.xxx",port=3306)
    return(conn)
  })
}
    
storiesDb <- connection() 

- LISTA AS TABELAS DO BANCO
   dbListTables(storiesDb)
   
- DESCONECTA
  dbDisconnect(storiesDb)
 ```
 ## INSERÇÃO (INSERT)
 ```
 query<- "INSERT INTO teste (campo1,campo2,data) VALUES ('campo1','campo2',NOW())"
rsInsert <- dbSendQuery(storiesDb, query)

query2<- "INSERT INTO teste set campo1='campo1',campo2='campo2',data=NOW()"
rsInsert <- dbSendQuery(storiesDb, query2)
```
## SELEÇÃO (SELECT) 
```
query <- "SELECT * FROM teste";
rs <- dbSendQuery(storiesDb, query)
dbRows <- dbFetch(rs)
```

  seq |id |campo1 |campo2 | data|
  --- |---|-------|-------|-----  
   1  |1  |campo1 |campo2 |2020-12-23
   2  |2  |campo1 |campo2 |2020-12-23



~~~javascript
Esta é uma linha de código em Javascript.
~~~

~~~php
Esta é uma linha de código em PHP.
~~~

~~~html
Esta é uma linha de código em HTML.
~~~
