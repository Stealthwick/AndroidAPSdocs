ברוכים הבאים לתיעוד של AndroidAPS
***************************************

.. image:: images/modules-female.png
  :alt: Components

AndroidAPS is an open source app for people living with insulin-dependent diabetes that acts as an artificial pancreas system (APS) on Google Android smartphones. The main components are different openAPS software algorithms which aim to do what a living pancreas does: keeping blood sugar levels within healthy limits by using automated insulin dosing (AID). Additionally, you need at least a supported and FDA/CE approved insulin pump and continuous glucose meter. 

The app does NOT use self-learning artificial intelligence. Instead, the calculations of AndroidAPS are based on the individual dosage algorithm and carbohydrate intake the user manually puts into their treatments profile, but they are verified by the system for safety reasons. 

The app is not provided in Google Play - you have to build it from source code by yourself for legal reasons.

How to read the documentation?
==============================

We have provided this subsection of the documentation especially for those who are new to concept of Do-It-Yourself-APS (Artificial-Pancreas-Systems) in order to best show how to get acquainted with the information we consider to be the most important, especially in terms of understanding the reasons behind the "limits" set in place when you are first beginning your AAPS journey. These safety limits have been developed over many years by observations of the inadvertent mistakes that new users are most likely to make when first learning to set up, build, and then successfully loop with AndroidAPS - as most often those mistakes occur simply because the user was so excited to get started using the system that they may have forgotten to sit down and dedicate the time needed to understand the information within this documentation thoroughly. We have all been there!

Certainly the approach, "read everything" has merit and is certainly true. However, it is not uncommon for newcomers to quickly become overwhelmed by the sheer volume and variety of new information that they are expected to understand all at once! So these next few subsections are meant to lay out the most important foundations of the knowledge necessary to successfully run your own chosen setup with as few hiccups as is possible. New users can refer back to this guide when they run into aspects of the system they are not yet familiar with; and to remind themselves where to go within the Documentation in order to locate more in-depth information, as needed. It is also important to lay out the capabilities of AndroidAPS in an up-front manner, as sometimes it can be disappointing to discover in the middle of reading the documentation that certain necessary tools are currently not available for use (due to constraints on which types of insulin pumps or CGMs are available in some countries vs. other countries etc.) or simply offers less/different functionality than first assumed. Finally, it is important to acknowledge that many experience-related aspects inside this documentation only become pertinent as you begin to use AAPS in real-time. Just as it is nearly impossible to learn to play a sport perfectly just by reading about the rules, it takes a combination of first learning the foundations of the rules for safely operating AAPS and then committing the time learning how best to apply those rules as you navigate through the steps of looping with AndroidAPS.

The `Getting started <Getting-Started/Safety-first.html>`_ subsection is a must read to understand the general concept of what an artificial pancreas system is designed to do; and is especially pertinent for users of AndroidAPS.

The subsection `What do I need? <Module/module.html>`_ specifies the CGMs (Continuous Glucose Monitors) and insulin pumps which are are available for use with AndroidAPS. This subsection is important to understand so that your AndroidAPS system can be assembled and built correctly the first time around and will function well in real world situations.

The subsection `Where to go for help? <Where-To-Go-For-Help/Connect-with-other-users.html>`_ should help direct you to the best places to go to find help depending upon your levels of experience with AAPS. This is very important so that you don't feel left out, especially at the beginning, and so that you can get in touch with others as quickly as possible, clarify questions and solve the usual pitfalls as quickly as possible. Experience shows that a lot of people are already using AndroidAPS successfully, but everyone has a question at some point that they couldn't solve on their own. The nice thing is, however, that due to the large number of users, the response times to questions are usually very quick, typically only a few hours. Don’t worry about requesting help, as there is no such thing as a dumb question! We encourage users of any/all levels of experience to ask as many questions as they feel is necessary to help get them up and running safely. Just try it out please.

In the subsection `Glossary <Getting-Started/Glossary.html>`_ we have compiled a list of the acronyms (or short-term names) used throughout AAPS. For example, where to go to find out what the terms ISF or TT, stand for in in the more common (longer) terms.

For parents who want to build AndroidAPS for their children, we recommend the subsection `AndroidAPS for children <Children/Children.html>`_ , as there you will find more advanced information specifically tailored for learning the extra steps necessary in order to remotely control your child's AndroidAPS app as well as a more comprehensive safety profile as compared to adults. You need to be able to support your children and understand the all the advanced concepts that AndroidAPS offers to help you succeed.

Now that you have a solid understanding of the concepts that AndroidAPS uses, know where to go for the the necessary tools to build your APS and are familiar with where to get help in case of an emergency, it is the right time to start building the app! The subsection `How to install AndroidAPS? <Installing-AndroidAPS/Building-APK.html>`_ shows you this in detail. Since the requirements are very different from anything you might have set up in the past, we recommend that you really follow the instructions, step-by-step the first few times you build the app, so that you have a stronger sense of how the app building process is supposed to behave when all directions are followed exactly. Please remember to take your time. Later this will go very quickly when you build the app again for a new version. That way you will have a greater chance of noticing when something doesn't going as planned before too many steps are out of line. It is important to save the your keystore file (.jks file used to sign your app) in a safe place, so that you can always use that exact same keystore file and password each and every time you are asked to create a new updated version of AndroidAPS, as this file is what makes sure that each new version of the app "remembers" all the information that you have provided to it in previous versions of the app and thus ensure that the updates will go as smoothly as possible. On average, you can assume that there will be one new version and 2-3 required updates per year. This number is based on experience and may change in the future. But we do want to at least give you a general guideline on what to expect. When you are more experienced at building updated AndroidAPS app versions all the steps that are required in building an updated app will only take 15-30 minutes, on average. However, in the beginning there can be a rather steep learning curve as these steps are not always considered intuitive by new users! So do not get frustrated if you find that it takes half a day or a whole day with some help from the community before you are finally finished with the update process. If you find that you are getting very frustrated just take a short break, and oftentimes; after a stroll around the block or two...you'll find that you are better able to approach the problem again. We have also compiled a list of questions and answers to most of the typical errors that are likely to occur the first few updates located within the FAQs section; as well as within "How to install AndroidAPS?" that provides additional information in the subsection "Troubleshooting".

The subsection `Component Setup <Configuration/BG-Source.html>`_ explains how to properly integrate each of the various different separate component parts into AndroidAPS, as well as how to set them up to work as seamlessly as possible together. All components are listed under the separate sections: CGM/FGM, xDrip Settings, Pumps, Phones, Nightscout setup, and Smartwatches. The sensor (BG) values and control of the insulin pump are particularly important information to understand. The subsection `Configuration <Configuration/BG-Source.html>`_ describes the best pump configurations to use in AndroidAPS.

This is followed by a particularly important subsection `AndroidAPS Usage <Getting-Started/Screenshots.html>`_, in which you are slowly introduced to the full usage of what AndroidAPS has to offer via a safe and carefully calibrated step-by-step gradual process designed to make sure that you/your child are thoroughly familiar and comfortable navigating all the different levels and menu configurations before graduating on the next phase, each commonly referred to as the next Objective, until you are have enough experience to begin using the more advanced options available within the app. These Objectives are specially designed in such a way that will gradually unlock more possibilities of AndroidAPS and switch from Open Loop to Closed Loop.

After that there is a subsection `General Hints <Usage/Timezone-traveling.html>`_ with e.g. information on how to deal with the crossing of time zones as well as knowing what to do during the Spring Forward - Fall Back daylight saving time changes which will occur twice a year while using AndroidAPS.

There is a subsection for the `clinicians <Resources/clinician-guide-to-AndroidAPS.html>`_ who have expressed interest in open source artificial pancreas technology such as AndroidAPS, or for patients who want to share such information with their clinicians.

Finally, in the subsection `How to help? <make-a-PR.html>`_ we would like to provide you with information so that you are able to suggest small or larger changes to the documentation yourself and work together with us on the documentation. We further need support for `translation of the documentation <translations.html>`_ By the way, it also very helpful for everyone if you could provide links to the corresponding documentation (or screenshots of where the links are located within the Documentation if you are not familiar with how to send a link) when answering questions from other users. That way the correct information can easily be located again should other users also be trying to find answers to the same types of questions in the future.


.. הערה::
   Please don't be shy, we need support in creating the documentation. A pull request is relatively simple to create. You can't break anything. There are release procedures. If you just want to talk in the beginning to see how you can help, give us a shout on Discord or Facebook. In this day and age, a telco is quickly arranged and we can discuss how you can best get involved and how we can show you the first steps.

לפרטים נוספים, קראו הלאה כאן.

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: שינוי השפה

   שינוי השפה <./changelanguage.rst>

.. _מתחילים:

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: מתחילים

   בטיחות מעל הכול <./Getting-Started/Safety-first.rst>
   מהי מערכת לולאה סגורה <./Getting-Started/ClosedLoop.rst>
   מהי מערכת לולאה סגורה ב-AndroidAPS? <./Getting-Started/WhatisAndroidAPS.rst>  
   מבחר המשאבות <./Getting-Started/Pump-Choices.md>
   עדכונים ושינויים בתיעוד <./Getting-Started/WikiUpdate.rst>

.. _מה אני צריך\ה:

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: מה אני צריך\ה? 

   מודול <./Module/module.rst>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: איך להתקין את AndroidAPS

   בניית קובץ ה-APK <./Installing-AndroidAPS/Building-APK.md>
   עדכון לגרסה חדשה או לענף חדש <./Installing-AndroidAPS/Update-to-new-version.md>
   טיפים ובדיקות לאחר עדכון ל-AAPS 3.0<./Installing-AndroidAPS/update3_0.md>
   טיפים ובדיקות לאחר עדכון ל-AAPS 2.7<./Installing-AndroidAPS/update2_7.rst>
   התקנת Git <./Installing-AndroidAPS/git-install.rst>
   פתרון בעיות באנדרואיד סטודיו <../Installing-AndroidAPS/troubleshooting_androidstudio.html>
   הערות פרסום <./Installing-AndroidAPS/Releasenotes.rst>
   ענף הפיתוח <./Installing-AndroidAPS/Dev_branch.md>

.. _הגדרות-הרכיבים:

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: הגדרת הרכיבים

   חיישני סוכר <./Configuration/BG-Source.rst>
   הגדרות xDrip <./Configuration/xdrip.md>
   משאבות <./Hardware/pumps.rst>
   טלפונים <./Hardware/Phoneconfig.rst>
   הגדרת Nightscout <./Installing-AndroidAPS/Nightscout.md>
   שעון חכם <./Hardware/Smartwatch.rst>

.. _תצורה:

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: תצורה

   בונה התצורה <./Configuration/Config-Builder.md>
   העדפות <./Configuration/Preferences.rst>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: שימוש ב-AndroidAPS

   מסכי AndroidAPS <./Getting-Started/Screenshots.md>
   משימות <./Usage/Objectives.rst>
   תכונות OpenAPS <./Usage/Open-APS-features.md>   
   חישוב פחמימות פעילות (COB) <./Usage/COB-calculation.rst>
   זיהוי רגישות <./Configuration/Sensitivity-detection-and-COB.md>
   החלפת פרופיל <./Usage/Profiles.md>
   ערכי מטרה זמניים <./Usage/temptarget.md>   
   פחמימות ממושכות <./Usage/Extended-Carbs.rst>
   אוטומציה <./Usage/Automation.rst>
   פורטל הטיפולים (הופסק) <./Usage/CPbefore26.rst>
   Open Humans Uploader <./Configuration/OpenHumans.rst>
   אוטומציה עם יישומי צד שלישי <./Usage/automationwithapp.md>
   Android auto <./Usage/Android-auto.md>  

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: הנחיות כלליות 

   מעבר בין אזורי זמן עם משאבות <./Usage/Timezone-traveling.md>
   גישה לקבצי הרשומות <./Usage/Accessing-logfiles.md>
   עצות לשימוש בסיסי ב-Accu-Chek Combo <./Usage/Accu-Chek-Combo-Tips-for-Basic-usage.md> 
   יבוא\ייצוא הגדרות <./Usage/ExportImportSettings.rst>
   מצב הנדסה ב-xDrip <./Usage/Enabling-Engineering-Mode-in-xDrip.md>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: ילדים ו-AndroidAPS

   ניטור מרחוק <./Children/Children.rst>
   פקודות SMS <./Children/SMS-Commands.rst>
   עוזר הפרופילים <./Configuration/profilehelper.rst>
   
.. toctree::
   :maxdepth: 1
   :glob:
   :caption: פתרון בעיות

   פתרון בעיות <./Usage/troubleshooting.rst>
   פתרון בעיות בקליינט נייטסקאוט <./Usage/Troubleshooting-NSClient.md>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: שאלות נפוצות

   שאלות נפוצות <./Getting-Started/FAQ.md>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: מילון מונחים

   מילון מונחים <./Getting-Started/Glossary.md>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: לאן לגשת לקבלת עזרה 

   חומרים שימושיים לקריאה לפני שמתחילים <./Where-To-Go-For-Help/Background-reading.md>
   לאן לגשת לקבלת עזרה <./Where-To-Go-For-Help/Connect-with-other-users.md>
   עדכונים ושינויים בתיעוד <./Getting-Started/WikiUpdate.rst>

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: לקלינאים

   לקלינאים <./Resources/clinician-guide-to-AndroidAPS>


.. toctree::
   :maxdepth: 1
   :glob:
   :caption: איך לסייע

   איך לסייע <./Getting-Started/How-can-I-help.md>
   כיצד לתרגם את היישום ואת התיעוד <./translations.md>
   כיצד לערוך את התיעוד <./make-a-PR>


.. הערה:: 
	**כתב ויתור ואזהרה**

	* כל המידע, המחשבה והקוד המתוארים כאן מיועדים למטרות מידע וחינוכיות בלבד.
 Nightscout לא עושה כרגע ניסיון לתאימות לפרטיות HIPAA. 
 השימוש ב-Nightscout וב-AndroidAPS הוא על אחריותכם בלבד, ואל תשתמשו במידע או בקוד כדי לקבל החלטות רפואיות.

	* השימוש בקוד מ-github.com הוא ללא אחריות או תמיכה רשמית מכל סוג שהוא. אנא עיינו ברישיון של מאגר זה לפרטים.


	* כל שמות המוצרים והחברות, הסימנים המסחריים, סימני השירות, הסימנים המסחריים הרשומים וסימני השירות הרשומים הם רכושם של בעליהם בהתאמה. 
 השימוש בהם הוא למטרות מידע ואינו מרמז על כל זיקה או אישור על ידם. 


	שימו לב - לפרויקט זה אין קשר ואינו מאושר על ידי: `SOOIL <http://www.sooil.com/eng/>`_, `Dexcom <https://www.dexcom.com/>`_, `Accu-Chek, Roche Diabetes Care <https://www.accu-chek.com/>`_, `Insulet <https://www.insulet.com/>`_ או `Medtronic <https:// www.medtronic.com/>`_
