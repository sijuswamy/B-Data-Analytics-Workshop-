
# Stage 1: Installing necessary components

## Step 1: Ensure `java 8` is pre installed. If not visit this link <https://www.java.com/en/download/> to download and install `JDK8`.

## Step 2: Go to RStudio and install the library `sparkly` from `CRAN` inside R-environment

```
install.package("sparkly")
```

## Step 3: Install `spark` from `R` using the r-code 

```
spark_install()
```

# Stage 2: Working with `spark` inside RStudio

## Step 1: include the following r-code and run to get connect to `spark`

```
# Load sparklyr
library(sparklyr)

# # install a local version of Spark for development purposes (only once!)
# spark_install()

# set Java home to Java 8 (only working with Java 8 at the moment)
java_path <- normalizePath('C:/Progra~1/Java/jre1.8.0_201')
Sys.setenv(JAVA_HOME=java_path)

# Connect to your Spark cluster
sc <- spark_connect("local")

# Print the version of Spark
spark_version(sc)
```
## Step 4: Work with `spark` handles from `R` as usual.
