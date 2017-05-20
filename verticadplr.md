# A dplyr connector for Vertica

Adds Vertica database backend support with the dplyr package


[vertica deployer install R instructions](https://rdrr.io/github/vertica/vertica.dplyr/)

# Installing vertica.dplyr in R

```
ubuntu@ip-172-31-32-142:~$ R

R version 3.2.3 (2015-12-10) -- "Wooden Christmas-Tree"
Copyright (C) 2015 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

  Natural language support but running in an English locale

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

[Previously saved workspace restored]

> install.packages("devtools")
Installing package into ‘/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2’
(as ‘lib’ is unspecified)
--- Please select a CRAN mirror for use in this session ---
HTTPS CRAN mirror 

 1: 0-Cloud [https]                 2: Algeria [https]              
 3: Australia (Canberra) [https]    4: Australia (Melbourne) [https]
 5: Australia (Perth) [https]       6: Austria [https]              
 7: Belgium (Ghent) [https]         8: Brazil (PR) [https]          
 9: Brazil (RJ) [https]            10: Brazil (SP 1) [https]        
11: Bulgaria [https]               12: Canada (MB) [https]          
13: Chile 1 [https]                14: Chile 2 [https]              
15: China (Beijing) [https]        16: China (Hefei) [https]        
17: China (Lanzhou) [https]        18: Colombia (Cali) [https]      
19: Czech Republic [https]         20: Denmark [https]              
21: Estonia [https]                22: France (Lyon 1) [https]      
23: France (Lyon 2) [https]        24: France (Marseille) [https]   
25: France (Montpellier) [https]   26: France (Paris 2) [https]     
27: Germany (Göttingen) [https]    28: Germany (Münster) [https]    
29: Iceland [https]                30: India [https]                
31: Indonesia (Jakarta) [https]    32: Ireland [https]              
33: Italy (Padua) [https]          34: Japan (Tokyo) [https]        
35: Malaysia [https]               36: Mexico (Mexico City) [https] 
37: New Zealand [https]            38: Norway [https]               
39: Philippines [https]            40: Russia (Moscow) [https]      
41: Serbia [https]                 42: Spain (A Coruña) [https]     
43: Spain (Madrid) [https]         44: Sweden [https]               
45: Switzerland [https]            46: Taiwan (Chungli) [https]     
47: Turkey (Denizli) [https]       48: Turkey (Mersin) [https]      
49: UK (Bristol) [https]           50: UK (Cambridge) [https]       
51: UK (London 1) [https]          52: USA (CA 1) [https]           
53: USA (IA) [https]               54: USA (IN) [https]             
55: USA (KS) [https]               56: USA (MI 1) [https]           
57: USA (OR) [https]               58: USA (TN) [https]             
59: USA (TX 1) [https]             60: Vietnam [https]              
61: (HTTP mirrors)                 

Selection: 1
trying URL 'https://cloud.r-project.org/src/contrib/devtools_1.13.1.tar.gz'
Content type 'application/x-gzip' length 486282 bytes (474 KB)
==================================================
downloaded 474 KB

* installing *source* package ‘devtools’ ...
** package ‘devtools’ successfully unpacked and MD5 sums checked
** R
** inst
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (devtools)

The downloaded source packages are in
	‘/tmp/RtmpXExSDu/downloaded_packages’
> library(devtools)
> install_github("vertica/vertica.dplyr")
Downloading GitHub repo vertica/vertica.dplyr@master
from URL https://api.github.com/repos/vertica/vertica.dplyr/zipball/master
Installing vertica.dplyr
trying URL 'https://cloud.r-project.org/src/contrib/assertthat_0.2.0.tar.gz'
Content type 'application/x-gzip' length 11612 bytes (11 KB)
==================================================
downloaded 11 KB

Installing assertthat
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c0511c19a3c9/assertthat'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘assertthat’ ...
** package ‘assertthat’ successfully unpacked and MD5 sums checked
** R
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** testing if installed package can be loaded
* DONE (assertthat)
trying URL 'https://cloud.r-project.org/src/contrib/dplyr_0.5.0.tar.gz'
Content type 'application/x-gzip' length 708476 bytes (691 KB)
==================================================
downloaded 691 KB

Installing dplyr
trying URL 'https://cloud.r-project.org/src/contrib/BH_1.62.0-1.tar.gz'
Content type 'application/x-gzip' length 10181096 bytes (9.7 MB)
==================================================
downloaded 9.7 MB

Installing BH
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c0513abee4ab/BH'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘BH’ ...
** package ‘BH’ successfully unpacked and MD5 sums checked
** inst
** help
*** installing help indices
** building package indices
** testing if installed package can be loaded
* DONE (BH)
trying URL 'https://cloud.r-project.org/src/contrib/DBI_0.6-1.tar.gz'
Content type 'application/x-gzip' length 611344 bytes (597 KB)
==================================================
downloaded 597 KB

Installing DBI
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c0514db026c/DBI'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘DBI’ ...
** package ‘DBI’ successfully unpacked and MD5 sums checked
** R
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (DBI)
trying URL 'https://cloud.r-project.org/src/contrib/lazyeval_0.2.0.tar.gz'
Content type 'application/x-gzip' length 317272 bytes (309 KB)
==================================================
downloaded 309 KB

Installing lazyeval
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c051722c708f/lazyeval'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘lazyeval’ ...
** package ‘lazyeval’ successfully unpacked and MD5 sums checked
** libs
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c expr.c -o expr.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c interp.c -o interp.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c lazy.c -o lazy.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c name.c -o name.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c utils.c -o utils.o
gcc -std=gnu99 -shared -L/usr/lib/R/lib -Wl,-Bsymbolic-functions -Wl,-z,relro -o lazyeval.so expr.o interp.o lazy.o name.o utils.o -L/usr/lib/R/lib -lR
installing to /home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/lazyeval/libs
** R
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (lazyeval)
trying URL 'https://cloud.r-project.org/src/contrib/R6_2.2.1.tar.gz'
Content type 'application/x-gzip' length 325641 bytes (318 KB)
==================================================
downloaded 318 KB

Installing R6
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c051196a629d/R6'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘R6’ ...
** package ‘R6’ successfully unpacked and MD5 sums checked
** R
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (R6)
trying URL 'https://cloud.r-project.org/src/contrib/Rcpp_0.12.10.tar.gz'
Content type 'application/x-gzip' length 2446049 bytes (2.3 MB)
==================================================
downloaded 2.3 MB

Installing Rcpp
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c05151468dd8/Rcpp'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘Rcpp’ ...
** package ‘Rcpp’ successfully unpacked and MD5 sums checked
** libs
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include/     -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c Date.cpp -o Date.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include/     -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c Module.cpp -o Module.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include/     -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c Rcpp_init.cpp -o Rcpp_init.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include/     -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c api.cpp -o api.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include/     -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c attributes.cpp -o attributes.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include/     -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c barrier.cpp -o barrier.o
g++ -shared -L/usr/lib/R/lib -Wl,-Bsymbolic-functions -Wl,-z,relro -o Rcpp.so Date.o Module.o Rcpp_init.o api.o attributes.o barrier.o -L/usr/lib/R/lib -lR
installing to /home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/libs
** R
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (Rcpp)
trying URL 'https://cloud.r-project.org/src/contrib/tibble_1.3.1.tar.gz'
Content type 'application/x-gzip' length 91235 bytes (89 KB)
==================================================
downloaded 89 KB

Installing tibble
trying URL 'https://cloud.r-project.org/src/contrib/rlang_0.1.1.tar.gz'
Content type 'application/x-gzip' length 201419 bytes (196 KB)
==================================================
downloaded 196 KB

Installing rlang
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c0513450dca8/rlang'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘rlang’ ...
** package ‘rlang’ successfully unpacked and MD5 sums checked
** libs
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c attrs.c -o attrs.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c capture.c -o capture.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c eval.c -o eval.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c export.c -o export.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c formula.c -o formula.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c init.c -o init.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c internals.c -o internals.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c lang.c -o lang.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c pairlist.c -o pairlist.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c replace-na.c -o replace-na.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c sexp.c -o sexp.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c splice.c -o splice.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c symbol.c -o symbol.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c unquote.c -o unquote.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG      -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c utils.c -o utils.o
gcc -std=gnu99 -shared -L/usr/lib/R/lib -Wl,-Bsymbolic-functions -Wl,-z,relro -o rlang.so attrs.o capture.o eval.o export.o formula.o init.o internals.o lang.o pairlist.o replace-na.o sexp.o splice.o symbol.o unquote.o utils.o -L/usr/lib/R/lib -lR
installing to /home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/rlang/libs
** R
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (rlang)
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c051764d8f6a/tibble'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘tibble’ ...
** package ‘tibble’ successfully unpacked and MD5 sums checked
** libs
g++ -I/usr/share/R/include -DNDEBUG   -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include"   -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c RcppExports.cpp -o RcppExports.o
gcc -std=gnu99 -I/usr/share/R/include -DNDEBUG   -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include"   -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c init.c -o init.o
g++ -I/usr/share/R/include -DNDEBUG   -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include"   -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c matrixToDataFrame.cpp -o matrixToDataFrame.o
g++ -shared -L/usr/lib/R/lib -Wl,-Bsymbolic-functions -Wl,-z,relro -o tibble.so RcppExports.o init.o matrixToDataFrame.o -L/usr/lib/R/lib -lR
installing to /home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/tibble/libs
** R
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
*** copying figures
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (tibble)
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL '/tmp/RtmpXExSDu/devtools3c051555b84ed/dplyr'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘dplyr’ ...
** package ‘dplyr’ successfully unpacked and MD5 sums checked
** libs
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c RcppExports.cpp -o RcppExports.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c address.cpp -o address.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c api.cpp -o api.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c arrange.cpp -o arrange.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c between.cpp -o between.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c bind.cpp -o bind.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c combine_variables.cpp -o combine_variables.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c distinct.cpp -o distinct.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c dplyr.cpp -o dplyr.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c filter.cpp -o filter.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c group_indices.cpp -o group_indices.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c init.cpp -o init.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c join.cpp -o join.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c nth.cpp -o nth.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c select.cpp -o select.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c strings_addresses.cpp -o strings_addresses.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c summarise.cpp -o summarise.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c test.cpp -o test.o
g++ -I/usr/share/R/include -DNDEBUG -I../inst/include -DCOMPILING_DPLYR  -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/Rcpp/include" -I"/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/BH/include"  -DBOOST_NO_INT64_T -DBOOST_NO_INTEGRAL_INT64_T -DBOOST_NO_LONG_LONG -fpic  -g -O2 -fstack-protector --param=ssp-buffer-size=4 -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2 -g  -c window.cpp -o window.o
g++ -shared -L/usr/lib/R/lib -Wl,-Bsymbolic-functions -Wl,-z,relro -o dplyr.so RcppExports.o address.o api.o arrange.o between.o bind.o combine_variables.o distinct.o dplyr.o filter.o group_indices.o init.o join.o nth.o select.o strings_addresses.o summarise.o test.o window.o -L/usr/lib/R/lib -lR
installing to /home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2/dplyr/libs
** R
** data
*** moving datasets to lazyload DB
** inst
** tests
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (dplyr)
'/usr/lib/R/bin/R' --no-site-file --no-environ --no-save --no-restore --quiet  \
  CMD INSTALL  \
  '/tmp/RtmpXExSDu/devtools3c051406f0819/vertica-vertica.dplyr-ebac291'  \
  --library='/home/ubuntu/R/x86_64-pc-linux-gnu-library/3.2' --install-tests 

* installing *source* package ‘vertica.dplyr’ ...
** R
** preparing package for lazy loading
** help
*** installing help indices
** building package indices
** installing vignettes
** testing if installed package can be loaded
* DONE (vertica.dplyr)
> 
```

# Loading the vertica connection 

```
> library(vertica.dplyr)
Loading required package: assertthat
Loading required package: dplyr

Attaching package: ‘dplyr’

The following objects are masked from ‘package:stats’:

    filter, lag

The following objects are masked from ‘package:base’:

    intersect, setdiff, setequal, union

```

# Connect to HP Vertica using RJDBC
```


> vertica <- src_vertica(dsn = NULL, jdbcpath="/ecrfiles/lib/external/vertica_jdbc.jar","dbase","localhost",5433,"username","password")
Attempting to load package `RJDBC` and its dependencies...
Successfully loaded.

> columns <- c( "varchar","float","float")
> names(columns) <- c("epi_id","prob_use","PAC_cost")
> db_create_table(vertica,"MCOs_PAC_expected",columns)


```

# Leg work

```
> columns <- c( "varchar","float","float")
> names(columns) <- c("epi_id","prob_use","PAC_cost")
> db_create_table(vertica,"MCOs_PAC_expected",columns)

```

# Now the good stuff

```

> orig <- db_load_from_file(vertica, file.name= "/home/ubuntu/MCOs_PAC_expected.csv", "MCOs_PAC_expected", sep = ",") 
> 

```