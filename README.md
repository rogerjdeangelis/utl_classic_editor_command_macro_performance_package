# utl_classic_editor_command_macro_performance_package
    Aligning sas display manager command macros with SAS function keys, command line and logitech's G502 Hero Mouse
    %let pgm=utl_classic_editor_command_macro_performance_package;
    %let pgm=sas_saspac;

    Aligning sas display manager command macros with SAs function keys, command line and logitech's G502 Hero Mouse
    
    SAS Macros                                                                                                                                                       
    https://github.com/rogerjdeangelis/utl_classic_editor_command_macro_performance_package/blob/main/utl_classic_editor_command_macro_performance_package.sas       
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories/blob/master/utl_classic_editor_command_macro_performance_package.sas  

    I posted a new classic editor performance package on github..

    I purchased a new enhanced mouse with almost 30 programmable actions.
    The mouse is the Logitech G502 Hero.
    Many of the 46 command macros below can be mapped to the mouse.
    All can also be executed from the command line.

    /*                                             _
      ___ ___  _ __ ___  _ __ ___   __ _ _ __   __| |  _ __ ___   __ _  ___ _ __ ___  ___
     / __/ _ \| `_ ` _ \| `_ ` _ \ / _` | `_ \ / _` | | `_ ` _ \ / _` |/ __| `__/ _ \/ __|
    | (_| (_) | | | | | | | | | | | (_| | | | | (_| | | | | | | | (_| | (__| | | (_) \__ \
     \___\___/|_| |_| |_|_| |_| |_|\__,_|_| |_|\__,_| |_| |_| |_|\__,_|\___|_|  \___/|___/
    */


    MACRO       USAGE                         DESCRIPTION

    mish        Usage: mish sex age           Highlight dataset and type mish sex age and for crosstab of missings will appear in output window
    _sv         Usage: pf1 or mmb             Save timestamped version of the program in the c:/ver folder and save program in c:/utl
    sqldesh     Usage: sqldesh                Hilite table and type sqldesh and sql describe output will appear in log
    sasbatch    Usage: sasbatch               Highlight code type sasbatch on command line
    evlh        Usage: evlh                   Hilite expression 2*(3+1) and type evlh and 8 will appear in log
    sumv        Usage: sumv                   Hilite a column of numbers and an proc means will run on the nummbes mean max min ...
    xlrh        Usage: xlrh                   Hilite a table and type xlr and table will open it in excel. No need for pc acces to excel
    sumr        Usage: sumr                   Hilite row of numbers type sumr and the sum will appear in the log and macro variable __sumr
    iota        Usage: iota                   Type iota 10 and 10 rows with 01 02 03 - 10 will be added to the editor
    cuth        Usage: cuth                   Hilite a block of code and type cuth and mutiple spaces will be reduced to single spaces
    parh        Usage: parh                   Hilite a line of code and type parh to test for unbalanced parens
    xit         Usage: xit                    When exiting sas type xit and last program will open next time you start SAS
    cntuh       Usage: cntuh                  Hilite table and count distinct usubjid and number of obs are in pastdmphe buffer *usubjis is hardcoded)
    cliph       Usage: cliph                  Hilite a line of and macro variable _clip will contain the statement
    cnth        Usage: cnth sex age           Hilite table and type cnth age sex and distinct counts of age sex cobinations in paste buffer and output eindow
    avgby       Usage: avgby sex age          Hilite table type avgby sex age for means by sex age also output dataset avgby
    tail        Usage: tail                   Type tail and last 40 obs of last dataset in paste buffer and output window
    tailh       Usage: tail                   Hilite table and type tailh and the last 40 obs will be in output window and in paste buffer
    ls4         Usage: ls4                    Type ls and a list of first 40 obs of last table in output window and paste buffer
    lsh         Usage: lsh                    Type lsh for list and output in paste buffer of hilited table
    lsfh        Usage: lsfh                   Hilight table type lsfh for 40 obs formatted list and output in paste buffer
    lsa         Usage: lsa                    Ttpe lsal to list all obs from the last dataset
    lsah        Usage: lsah                   Type lsah for a list of all obs in output and in paste buffer of hilited table
    doendh      Usage: foendh                 Hilite block of macro code and match do and end will be tested
    lsw         Usage: lsw [dq]]age=14[dq]    Use single and double quotes for chars, 40  filtered for  the _last_ table in pastebuffer and list
    avgh        Usage: avgh                   Hilite table and type avgh for proc means output and table avgh will be created
    frqv        Usage: frqv                   Hilite variable in _last_ table andn proc freq hiltred variable
    cntv        Usage: cntv                   Hilight variable in _last_ table and get count and distinct counts on variable
    unvv        Usage: unv                    Hilite a variable from the _last_ table and proc unvariate will be run on that variable
    unvh        Usage: unvh                   proc univariate on hilited dataset
    rpth        Usage: rpth                   Generate proc report code on hilited dataset. Good template to edit.
    dmp         Usage: dmp                    Type dmp and middle observation of last dataset printed vertically
    dmph        Usage: dmph                   Type dmph middle observation of highlighted dataset printed vertically with type length and sample values
    frq         Usage: frq sex age            Type frq type sex for a crosstab frequency on sex*age for last dataset.akes frq dataset
    frqh        Usage: frqh sex age           Highlight dataset and type frqh sex age and  forfrequency on sex xage. Also frqh dataset.
    debugh      Usage: debugh                 Highlight macro and type debugh to debug the macro (generates final code and runs it)
    con         Usage: con                    Type con and contents of last dataset in outptut
    conh        Usage: conh                   Highlight table and type conh on command line. Contents in output window
    cm          Usage: cm                     Hilite the blank line and subsequent block of code and the code will be commented out
    vu          Usage: vu                     Type vu for viewtable of last dataset created
    vuh         Usage: vuh                    Type vuh for viewtable of highlighted dataset
    xlsh        Usage: xlsh                   Highlight table and type xlsh and the table  will appear in excel uses libname need pc acces
    xplo        Usage: xplo ONEaTWO           Type xplo ONEaTWO and exploded letters will be saved in past buffer. Use lower case for spaces
    unqh        Usage: unqh sex age           Distinct counts. Usubjid must be in the datasets
    keylist     Usage: keylist                Type keylist and a list og your function keys will be in the log
    xpy         Usage: xpy roger              Type xpy roger for program banner with large font https://github.com/rogerjdeangelis/utl_program_banners

    /*__                  _   _               _
     / _|_   _ _ __   ___| |_(_) ___  _ __   | | _____ _   _ ___
    | |_| | | | `_ \ / __| __| |/ _ \| `_ \  | |/ / _ \ | | / __|
    |  _| |_| | | | | (__| |_| | (_) | | | | |   <  __/ |_| \__ \
    |_|  \__,_|_| |_|\___|\__|_|\___/|_| |_| |_|\_\___|\__, |___/
                                                       |___/
    */

    Obs    L1L2

      1    F1 home;_sv;
      2    F2 home;copy cmt;
      3    F3 ~run run;quit;
      4    F4 notesubmit;
      5    F5 cntv
      6    F6 home;
      7    F7 log;file "c:\log\&pgm..log";note z;notesubmit '%utl_logcurchk;';
      8    F8 rfind
      9    F9 rchange
     10    F11 ~ru run;quit;
     11    F12 ;;;;%end;%mend;/*'*/ *);*};*];*/;/*"*/;run;quit;%end;end;run;endcomp;%utlfix;
     12    SHF F1 lsa
     13    SHF F2 con
     14    SHF F6 dmph
     15    SHF F7 avghby
     16    SHF F8 avgh
     17    SHF F9 unv
     18    SHF F10 cntv
     19    SHF F11 lsfa
     20    SHF F12 tail
     21    CTL F1 lsah
     22    CTL F2 conh
     23    CTL F3 sqldesh
     24    CTL F11 lsah
     25    CTL F12 tailh
     26    ALT F1 evlh
     27    ALT F2 xlrh
     28    ALT F3 sasbatch
     29    ALT F11 sumv
     30    ALT F12 tailh
     31    CTL B wattention
     32    CTL D data;retain a b 1;proc tabulate;var a b;table a(n)*f=5.*b(n)*f=5.;run;
     33    CTL E n ? "hil";n=*"P Jone";n gt:"Phil";n le "Eva";sql- eqt gtt ltt get let net
     34    CTL G note g.g
     35    CTL H note h.h
     36    CTL I note i.i
     37    CTL J libname x excel ".xlsx";proc sql;update x;set y=2;where n="John"
     38    CTL K :mcu
     39    CTL L :mcl
     40    CTL M proc format;value $a;proc catalog cat=formats;modify a.formatc(desc='OK');run;
     41    CTL Q options minoperator;%macro t(x=a)/minoperator;%if &x in (a b c) %then
     42    CTL R proc report data=sashelp.class named list wrap;run;quit;
     43    CTL T proc tabulate data=class;class sex age;table age,sex*(n pctn<age>)/rts=8
     44    CTL U ~ Usage:
     45    CTL W ~ x 'tree "c:/temp" /F /A | clip'
     46    CTL Y where name like "B_B" "%B%" "B%B"
     47    RMB log;clear;out;clear;pgm;submit;home;log;z;z;
     48    SHF RMB ls4
     49    CTL RMB lsh
     50    MMB ~as assiigned to F1 (push on scroll wheel
     51    SHF MMB assigned to shf f2 lsa all obs last datasets
     52    CTL MMB assigned to cnt ftl ldah all obs highlighed dataset


     /*
     _ __ ___   ___  _   _ ___  ___   _ __ ___   __ _ _ __  ___
    | `_ ` _ \ / _ \| | | / __|/ _ \ | `_ ` _ \ / _` | `_ \/ __|
    | | | | | | (_) | |_| \__ \  __/ | | | | | | (_| | |_) \__ \
    |_| |_| |_|\___/ \__,_|___/\___| |_| |_| |_|\__,_| .__/|___/
     _                      _                        |_|
    | |_ ___  _ __   __   _(_) _____      __
    | __/ _ \| `_ \  \ \ / / |/ _ \ \ /\ / /
    | || (_) | |_) |  \ V /| |  __/\ V  V /
     \__\___/| .__/    \_/ |_|\___| \_/\_/
             |_|

     I left off desctiptions above the buttons because you
     might want to assign different command macros to the mouse actions

                     _______________________________
                    /                               \
                   /                                 \
                  /   Can use with SHF CTL & ALT      \
                 /                                     \
                |                                       |
                |                            ___        |
                |                           /   \       |
                |                          | RMB | ------- See Below
                |                           \___/       |  Sas allows direct mapping
                |                                       |
                |                                       |
                |                                       |
                |                                       |
                |                                       |
                |    ___                                |
                |   /   \                               |
                |  | F11 |                              |
                |   \___/                               |
                |                                       |
                |           ___       ___      ___      |
                |          /   \     /   \    /   \     |
                |         | F5  |   | F1  |  | F6  |    |
                |          \___/     \___/    \___/     |
                |                                       |
                |    ___                                |
                |   /   \                               |
                |  | F4  |                              |
                |   \___/                               |
                |                     ___               |
                |                    /   \              |
                |                   | F2  |             |
                |                    \___/              |
                 \                                      /
                  \                                    /
                   \                                  /
                    \                                /
                     \______________________________/


         _     _              _
     ___(_) __| | ___  __   _(_) _____      __
    / __| |/ _` |/ _ \ \ \ / / |/ _ \ \ /\ / /
    \__ \ | (_| |  __/  \ V /| |  __/\ V  V /
    |___/_|\__,_|\___|   \_/ |_|\___| \_/\_/


                 _____________
                /             \
               /               \
              /  SIDE VIEW      \
             /                   \
            |                     |
            |    ___              |
            |   /   \             |
            |  | F11 |            |
            |   \___/             -\
            |                     - | Scroll Wheel
            |           ___       - /
            |          /   \      |/
            |         | F5  |     |
            |          \___/      |
            |                     |
            |    ___              |
            |   /   \             |
            |  | F4  |            |
            |   \___/             |
            |                     |
             \                    /
              \                  /
               \                /
                \              /
                 \____________/




       RMB log;clear;out;clear;pgm;submit;home;log;z;z; ==> submit code
       SHF RMB ls4                                          40 obs last datsets
       CTL RMB lsh                                          40 obs hilighted dataset
