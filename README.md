# CBT980
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 980 is from Vladimir Mironov, via the ibmmainframes.com   *   FILE 980
//*           forum.  This is a zap to Doug Nadel's TASID 5.21      *   FILE 980
//*           load module, to fix problems with displaying the      *   FILE 980
//*           initiators, Option 4.  Since TASID belongs to IBM,    *   FILE 980
//*           because it was written by Doug when he worked there,  *   FILE 980
//*           we cannot publish its load module here.  So first     *   FILE 980
//*           download the load module from URL:                    *   FILE 980
//*                                                                 *   FILE 980
//*    https://www-01.ibm.com/support/docview.wss?uid=swg24009131   *   FILE 980
//*                                                                 *   FILE 980
//*           After you have downloaded the TASID load module,      *   FILE 980
//*           then the accompanying zaps apply, if you have a       *   FILE 980
//*           z/OS 2.2 thru 2.4 system, to fix the "Initiators"     *   FILE 980
//*           display.  If you have z/OS 2.4, then you need the     *   FILE 980
//*           additional zap, member ZAPTAS24.                      *   FILE 980
//*                                                                 *   FILE 980
//*           A third zap, ZAPTASCL, to display the job class       *   FILE 980
//*           for running jobs, was added.  This zap may also       *   FILE 980
//*           be applicable to z/OS 2.1, but see member             *   FILE 980
//*           $$NOTE02 first.                                       *   FILE 980
//*                                                                 *   FILE 980
//*        SUPPORT EMAIL:      sbgolob@cbttape.org                  *   FILE 980
//*                                                                 *   FILE 980
//*    List of zaps to be applied to TASID (in order):              *   FILE 980
//*                                                                 *   FILE 980
//*    ZAPTASID - Must be applied first, to allow the initiator     *   FILE 980
//*               display (option 4) to work for z/OS 2.2 and 2.3.  *   FILE 980
//*                                                                 *   FILE 980
//*    ZAPTAS24 - Zap to be applied AFTER ZAPTASID to allow the     *   FILE 980
//*               initiator display (option 4) to work for z/OS     *   FILE 980
//*               2.4 as well as 2.x.  Prerequisite is ZAPTASID.    *   FILE 980
//*               (x = 2 or 3)                                      *   FILE 980
//*                                                                 *   FILE 980
//*    ZAPTASCL - Zap to allow the initiator display for a running  *   FILE 980
//*               job, to display the Job Class.  This version of   *   FILE 980
//*               TASID pre-dates the 8-character job names, so     *   FILE 980
//*               only the first character of the job name is       *   FILE 980
//*               displayed.                                        *   FILE 980
//*                                                                 *   FILE 980
//*    Further notes:                                               *   FILE 980
//*                                                                 *   FILE 980
//*    ===>   Additional zap (to be applied on top of Vladimir's    *   FILE 980
//*           zap) to fix the initiator display for z/OS 2.4.       *   FILE 980
//*           The additional zap is in member ZAPTAS24.  The        *   FILE 980
//*           additional zap will NOT nullify TASID's effectiveness *   FILE 980
//*           for z/OS 2.2 and 2.3 (see member $$NOTE01 for further *   FILE 980
//*           explanation).                                         *   FILE 980
//*                                                                 *   FILE 980
//*           Also, please remember to apply zap:  ZAPTASCL.        *   FILE 980
//*                                                                 *   FILE 980
//*           BTW, the URL of the ibmmainframes.com posts which     *   FILE 980
//*           are relevant here, is:                                *   FILE 980
//*                                                                 *   FILE 980
//*           http://ibmmainframes.com/about65233.html              *   FILE 980
//*                                                                 *   FILE 980
//*      ==>  Fixed JCL to put the comment before the //SYSIN       *   FILE 980
//*           card.  (SBG)                                          *   FILE 980
//*                                                                 *   FILE 980
//*      ==>  I believe that this note applies best, when you       *   FILE 980
//*           download the version of TASID which includes the      *   FILE 980
//*           compiled panels in the load module, so you don't      *   FILE 980
//*           have a problem or question with also updating the     *   FILE 980
//*           ISPF panels.                                          *   FILE 980
//*                                                                 *   FILE 980
//*           Thanks to Bill Smith for alerting me to this          *   FILE 980
//*           problem, and finding Vladimir's zap.                  *   FILE 980
//*                                                                 *   FILE 980
//*           email:  Bill Smith <sfowjs@sbcglobal.net>             *   FILE 980
//*                                                                 *   FILE 980
```
