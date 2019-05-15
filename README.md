# SWIG_C
after install perl5 64bit:

perl
install Log:Log4perl
install Config:Auto
install DBI
install MySQL
install DateTime
install MySQl
install DateTime::Format::MySQL
install HTML::Entities
install PDF::API2
install LWP::Simple
install Clone
install Statistics::Basic
install Statistics::Zed
install Inline::Java
force install Inline::Java
force install GD::Image
install PDF::Table
install MIME::Lite
install HTML::Strip
install XML::Dumper
install Email::Valid.pm
install Excel::Writer::XLS
install DateTime::Format::Excel
install HTML::ReportWriter
install Template
install Spreadsheet::SimpleExcel

1.	swig -perl5 example.i

2.	gcc -c -s -O2 -DWIN32 -DWIN64 -DCONSERVATIVE -D__USE_MINGW_ANSI_STDIO -DPERL_TEXTMODE_SCRIPTS -DPERL_IMPLICIT_CONTEXT -DPERL_IMPLICIT_SYS -DUSE_PERLIO -fwrapv -fno-strict-aliasing -mms-bitfields -s -O2   -I C:\STRAWB~1\perl\lib/CORE example.c example_wrap.c

3.	g++ -o example.dll -mdll -s -L"C:\STRAWB~1\perl\lib\CORE" -L"C:\STRAWB~1\c\lib" example.o example_wrap.o   "C:\STRAWB~1\perl\lib\CORE\libperl526.a" -lmoldname -lkernel32 -luser32 -lgdi32 -lwinspool -lcomdlg32 -ladvapi32 -lshell32 -lole32 -loleaut32 -lnetapi32 -luuid -lws2_32 -lmpr -lwinmm -lversion -lodbc32 -lodbccp32 -lcomctl32 -Wl,--enable-auto-image-base

C:\STRAWB~1\perl\lib\CORE\libperl526.a : this file is depends on what perl version you installed

