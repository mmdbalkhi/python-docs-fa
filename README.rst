ترجمه مستندات پایتون — fa
============================================

.. image:: https://travis-ci.org/python/python-docs-fa.svg?branch=3.10
  :target: https://travis-ci.org/python/python-docs-fa

مشارکت در ترجمه
-------------------------------

چگونه مشارکت کنیم؟
~~~~~~~~~~~~~~~~~

برای مشارکت در ترجمه تنها کافی است که  `یک ایشو در گیت‌هاب <https://github.com/mmdbalkhi/python-docs-fa/issues>`_ ایجاد کنید.

مشارکت با استفاده از گیت هاب
~~~~~~~~~~~~~~~~~~~~~~~~~

پیش‌نیاز ها:

- یک `حساب کاربری گیت‌هاب <https://github.com/join>`_.
- ``git`` `نصب شده داشته باشید <https://help.github.com/articles/set-up-git/>`_ (برای ویندوز, این را ببینید
  https://gitforwindows.org/).
- یک ادیتور فایل ``.po`` (اگر هنوز گزینه ای را انتخاب نکرده اید، میتوانید از `poedit <https://poedit.net/>`_ استفاده کنید).


بیاین شروع کنیم:

شما به یک فورک از  `python-docs-fa
<https://github.com/mmdbalkhi/python-docs-fa>`_ نیاز دارید. بر روی دکمه ``Fork``
کلیک کنید. این یک کپی از کل پروژه را در حساب کاربری گیت‌هاب شما ایجاد میکند. 
اینجا جایی است که شما میتوانید در آن تغییر ایجاد کنید.

گام به گام:

.. code-block:: bash

    # کلون کردن فورک شما با توسط ssh (نام کاربری خودتان را با Username جایگزین کنید):
    git clone git@github.com:Username/python-docs-fa.git

    # به دایرکتوری کلون شده بروید:
    cd python-docs-fa/

    # مخزن اصلی را توسط HTTPS اضافه کنید(رمز عبوری از شما نخواهد پرسید):
    git remote add upstream https://github.com/mmdbalkhi/python-docs-fa.git

تمام ترجمه ها باید در آخرین نسخه انجام شوند.
ما هرگز بر روی قدیمی ترین نسخه، به عنوان مثال، آخرین نسخه پایتون ترجمه نمی کنیم
پایتون 3.9 است، ما نمی خواهیم مستقیماً در نسخه 3.5 پایتون ترجمه کنیم.
در صورت نیاز، ترجمه‌ها بر روی قدیمی‌ترین نسخه‌ها توسط سازمان پشتیبانی می‌شوند.
`تیم مستندسازی <https://www.python.org/dev/peps/pep-8015/#documentation-team>`_.

اکنون برای شروع یک جلسه کاری آماده هستید، هر بار که کار جدیدی را شروع می کنید، از اینجا شروع کنید:

.. code-block:: bash

    # برای کار، به یک شاخه بر اساس شاخه به‌روز (جدیدا fetch شده) نیاز داریم
    # شاخه upstream/3.10، فرض کنید روی "glossary" کار می کنیم تا نام گذاری کنیم
    # شاخه "glossary":
    git fetch upstream
    git checkout -b glossary upstream/3.7

    # اکنون می توانید روی فایل کار کنید.(معمولا از poedit استفاده میشود)
    poedit directory/file.po

    # وقتی همه چیز واضح است (خطاهای نحوی از Sphinx، رندر html،
    # معناشناسی، تایپوگرافی)،
    # می توانید کار خود را با یک پیام صریح زیبا کامیت کنید:
    git commit -a -m "Working on glossary."

    # سپس تغییرات خود را به کلون github خود پوش کنید،
    # چون شاخه های زودگذر هستند، اجازه دهید git را برای ردیابی همه آنها پیکربندی نکنیم،
    # "origin HEAD" یک نحو "ویژه" برای گفتن "Push on origin" است،
    # در شاخه ای با همان نام محلی،"
    # خوب است زیرا دقیقاً همان چیزی است که ما می خواهیم:
    git push origin HEAD

    # دستور قبلی یک پیوند برای باز کردن پول ریکوئست در github برای شما چاپ می کند.
    # اگر آن را از دست دادید، فقط به آن بروید
    # https://github.com/mmdbalkhi/python-docs-fa/ و یک "pull requests and compare" خوب
    # دکمه باید بعد از چند ثانیه ظاهر شود و به شما بگوید می‌توانید pull reqyests ایجاد کنید.

    # اکنون شخصی در حال بررسی تغییرات شما است و شما می خواهید آنها را اصلاح کنید
    # یافته ها، به شاخه خود بازگردید
    # (در صورتی که کار دیگری را در شاخه دیگری شروع کرده باشید):
    git checkout glossary
    # مشکلات را برطرف و سپس دوباره کامیت کنید:
    git commit -a -m "glossary: small fixes."
    git push origin HEAD

ممکن است متوجه شده باشید که این مشابه یک مثلث است و یک راس آن گم شده است:

- شما در حال fetch کردن از upstream (مخزن عمومی عمومی در github) هستید
- شما در حال پوش کردن به origin هستید (کلون شما در github)

بنابراین بله، این کار کسی است که آخرین راس را از شما اضافه کند
منشاء عمومی upstream برای "بستن حلقه"، این نقش است
که pr های افراد را پس از تصحیح ادغام میکند.

همچنین ممکن است متوجه شده باشید که هرگز در یک شاخه نسخه تعهد نکرده اید
( ``3.6``, ``3.7`` , ...)، فقط از آنها بیرون بکشید، آنها را فقط خواندنی در نظر بگیرید
از مشکلات جلوگیری خواهید کرد 


چه چیزی را ترجمه کنیم
~~~~~~~~~~~~~~~~~~

شما می توانید با کارهای آسانی مانند مرور ورودی های fuzzy برای کمک شروع کنید
به روز نگه داشتن مستندات (آنها را با استفاده از "make fuzzy" پیدا کنید).

همچنین می توانید مدخل های ترجمه شده قبلی را تصحیح کنید و در نهایت
ترجمه‌نشده‌ها را ترجمه کنید (آنها را با استفاده از «make todo» پیدا کنید).

- محتوای ``:ref:...`` و ``:term:...`` را ترجمه نکنید
- کلمات انگلیسی را، اگر مجبور به استفاده از آنها هستید، با حروف *مورب* قرار دهید توسط ستاره ها).
- اگر عنوان پیوند را ترجمه می کنید، لطفاً پیوند را نیز ترجمه کنید (معمولاً اگر ویکی پدیا باشد و مقاله ترجمه داشته باشد). اگر هیچ ترجمه ای از هدف وجود ندارد، آن را ترجمه نکنید

از کجا کمک بگیریم
~~~~~~~~~~~~~~~~~
میتوانید در بخش `بحث و گفت‌وگو گیت‌هاب <https://github.com/mmdbalkhi/python-docs-fa/discussions>`_ سوالات خود را بپرسید.


منابع ترجمه
---------------------


واژه نامه
--------

برای ثبات در ترجمه‌های ما، در اینجا چند گزاره و یادآوری برای اصطلاحات مکرر که باید ترجمه کنید، وجود دارد، در صورت مخالفت، از باز کردن موضوع دریغ نکنید.

برای اینکه به راحتی بفهمید که چگونه یک اصطلاح قبلاً در اسناد ما ترجمه شده است، می توانید از آن استفاده کنید
`find_in_po.py <https://gist.github.com/JulienPalard/c430ac23446da2081060ab17bf006ac1>`_.

========================== =============================================================================================================
 اصطلاح                       ترجمه پیشنهادی
========================== =============================================================================================================
-like
abstract data type          `دیتا تایپ های انتزاعی <https://docs.python.org/3/library/collections.html#collections.abc.MutableMapping>`_
argument                    *argument* `<https://docs.python.org/3/glossary.html#term-argument>`_
backslash                   *backslash(\\)*
bound                       محدوده
bug                         باگ
built-in                    `توکار/داخلی <https://docs.python.org/3/library/functions.html>`_
call stack                  *call stack*
debugging                   اشکال زدایی
deep copy                   `deep copy <https://docs.python.org/3/library/copy.html#copy.deepcopy>`_
double-quote                *double-quote(")*
e.g.                        به عنوان مثال
garbage collector           زباله جمع کن
identifier                  `identifier <https://docs.python.org/3/reference/lexical_analysis.html#identifiers>`_
immutable                   تغییرناپذیر
installer                   نصاب
interpreter                 مترجم
library                     کتابخانه
list comprehension          *list comprehension*
little-endian, big-endian   `اصطلاح ریاضیاتی <https://en.wikipedia.org/wiki/Endianness>`_
mutable                     تغییر پذیر
namespace                   *namespace*
parameter                   پارامتر                    
prompt                      *prompt*
raise                       *raise*
regular expression          *regular expression*
return                      برگشت
simple quote                *simple quote(')*
socket                      *socket*
statement                   `statement <https://docs.python.org/3/reference/simple_stmts.html>`_
subprocess                  *subprocess*
thread                      `رشته‌های تردد <https://docs.python.org/3/library/threading.html>`_
underscore                  *underscore(_)*
expression                  عبارت   

========================== =============================================================================================================


git diff ها را ساده کنید.
------------------

Git diff ها اغلب مملو از تغییرات بی‌فایده شماره خط هستند، مانند:

.. code-block:: diff

    -#: ../Doc/library/signal.rst:406
    +#: ../Doc/library/signal.rst:408

برای اینکه به git بگویید اطلاعات مفیدی نیستند، می‌توانید پس از اطمینان از اینکه ``~/.local/bin/`` در ``PATH`` شما قرار دارد، موارد زیر را انجام دهید.

.. code-block:: bash

    cat <<EOF > ~/.local/bin/podiff
    #!/bin/sh
    grep -v '^#:' "\$1"
    EOF

    chmod a+x ~/.local/bin/podiff

    git config diff.podiff.textconv podiff


نگهداری
-----------

همه این قطعه‌ها از ریشه یک کلون ``python-docs-fa`` اجرا می‌شوند، و برخی انتظار دارند یک کلون به‌روز CPython را در نزدیکی آن پیدا کنند.

مانند:

.. code-block:: bash

  ~/
  ├── python-docs-fa/
  └── cpython/

برای کلون کردن CPython می توانید از موارد زیر استفاده کنید:

.. code-block:: bash

  git clone --depth 1 --no-single-branch https://github.com/python/cpython.git

این از دانلود کل تاریخچه جلوگیری می کند (برای ساخت اسناد مفید نیست) اما همچنان همه شاخه ها را فتچ می کند.

فایل های pot را از CPython ادغام کنید
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  make merge


رشته های fuzzy را پیدا کنید
~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  make fuzzy


یک بیلد برای آزمایشی به صورت محلی بسازید
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  make build
