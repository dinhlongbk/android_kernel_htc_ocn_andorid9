#remove YYLTYPE yylloc

git diff                                                
diff --git a/scripts/dtc/dtc-lexer.lex.c_shipped b/scripts/dtc/dtc-lexer.lex.c_shipped
index 2c862bc86..e3663ce1a 100644
--- a/scripts/dtc/dtc-lexer.lex.c_shipped
+++ b/scripts/dtc/dtc-lexer.lex.c_shipped
@@ -631,7 +631,6 @@ char *yytext;
 #include "srcpos.h"
 #include "dtc-parser.tab.h"
 
-YYLTYPE yylloc;
 extern bool treesource_error;
 
 /* CAUTION: this will stop working if we ever use yyless() or yyunput() */



# set env
export GCC_BIN=/home/dinhlongbk/samba/lineage_os/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin
export PATH="$GCC_BIN:$PATH"
export ARCH=arm64
export SUBARCH=arm64
export CROSS_COMPILE=aarch64-linux-android-

# build
make O=out htcperf_defconfig
make -j$(nproc --all) O=out

# build for JAPAN 601HT
make O=out -j$(nproc) PRIVATE_SKU_NAME=JAPAN