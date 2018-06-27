---
title: xlfRegister (формы 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- функция xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4fb4e8656b4f27105a30764cdda020849a07645e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807357"
---
# <a name="xlfregister-form-1"></a>xlfRegister (формы 1)

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel. Это значение равно вызову **регистрации** из таблицы Excel XLM макрос. 
  
можно вызвать **xlfRegister** в двух вариантах: 
  
- xlfRegister (формы 1): регистрирует одной команды или функции.
    
- [xlfRegister (формы 2)](xlfregister-form-2.md): загружает и активирует надстройке XLL.
    
Вызывает в виде 1, эта функция выполняет команду или функции DLL в Excel, задается его использований 1 и возвращает его идентификатор регистрации, которую можно использовать для вызова функции более поздней версии с помощью [xlUDF](xludf.md) или функцию **xlfCall** . КОД регистрации также используется для отмены регистрации функции, с помощью [xlfUnregister (формы 1)](xlfunregister-form-1.md). Если функция был зарегистрирован, вызов **xlfRegister** еще раз увеличивает счетчик его использования. 
  
Эту форму функции также определяет скрытые имя которого является аргумента функции текст, _pxFunctionText_и которая вычисляет код регистрации функции или команды. Если функция отмены регистрации, удалите это имя, с помощью [xlfSetName](xlfsetname.md). Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, int iCount,
    LPXLOPER12 pxModuleText,   LPXLOPER12 pxProcedure,
    LPXLOPER12 pxTypeText,     LPXLOPER12 pxFunctionText,
    LPXLOPER12 pxArgumentText, LPXLOPER12 pxMacroType,
    LPXLOPER12 pxCategory,     LPXLOPER12 pxShortcutText,
    LPXLOPER12 pxHelpTopic,    LPXLOPER12 pxFunctionHelp,
    LPXLOPER12 pxArgumentHelp1, LPXLOPER12 pxArgumentHelp2,
        ...);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
Имя DLL, которая содержит функцию. Это можно получить путем вызова функции XLL-только для [xlGetName](xlgetname.md) , если функция регистрации также в настоящий момент DLL. 
  
_pxProcedure_ (**xltypeStr** или **xltypeNum**)
  
Если строка, имя функции для вызова как оно отображается в коде DLL. Если номер, порядковый номер экспорта число вызываемой функции. Для ясности всегда используйте форму строки.
  
_pxTypeText_ (**xltypeStr**)
  
Необязательный атрибут типа string, указывающее типы аргументов, функции и типа возвращаемого значения функции. Для получения дополнительных сведений см. Этот аргумент можно опустить, для изолированной DLL (XLL), который включает в себя [функции xlAutoRegister](xlautoregister-xlautoregister12.md) или **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** поддерживается только в Excel 2007. 
  
Если **xlfRegister** вызывается с помощью этого аргумента отсутствует, Excel вызывает **xlAutoRegister** или **xlAutoRegister12**, если существует в указанной библиотеке DLL, необходимо правильно Зарегистрируйте функцию, предоставляя эти сведения.
  
_pxFunctionText_ (**xltypeStr**)
  
Имя функции, как оно будет отображаться в Мастер функций. Этот аргумент является необязательным; Если он указан, функция недоступны в Мастер функций и может быть вызван только с помощью функции **звонков** с помощью кода регистрации функции из таблицы макросов XLM. Таким образом для использования обычного рабочего листа, должен обрабатывать этот аргумент при необходимости. 
  
_pxArgumentText_ (**xltypeStr**)
  
Необязательный текстовая строка, описывающая аргументы для функции. Пользователь видит это в Мастер функций. Если он указан, Excel создает базовой описания из _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** или **xltypeInt**)
  
Необязательный аргумент, указывающий тип записи XLL точка. Значение по умолчанию, если он указан, равно 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _значение pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Может быть вызван из листа  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Может быть вызван из листа макросов  <br/> |Да  <br/> |Да  <br/> |Да  <br/> |
|Может быть вызван из определения определенное имя  <br/> |Да  <br/> |Да  <br/> |Да  <br/> |
|Может быть вызван из выражение условного форматирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Из списка в мастере функции для функции листа  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Из списка в мастере функции для функции листа макросов  <br/> |Нет  <br/> |Да  <br/> |Да  <br/> |
   
На практике следует использовать 1 для функции листа, 1 для эквивалентный функции листа макросов (зарегистрировали в качестве типа **#**), которому нужно позвонить с рабочего листа и 2 для команды. 
  
> [!NOTE]
> Команды XLL скрыты и не отображаются в диалоговых окнах для выполнения макросов, несмотря на то, что их имена можно вводить в любом месте правильное имя команды является обязательным. 
  
_pxCategory_ (**xltypeStr** или **xltypeNum**)
  
Необязательный аргумент, который позволяет указать категорию, новые функции или команды, должна принадлежать к. Мастер функций делит функции по типу (категории). Можно указать имя категории или порядковый номер, где номер позиции категории в Мастер функций. Дополнительные сведения см в разделе «категория». Если он опущен, используется значение категории пользовательских.
  
_pxShortcutText_ (**xltypeStr**)
  
Строка одного символа, с учетом регистра, указывает ключ элемента управления, назначенных для этой команды. Например «A» назначает эта команда CTRL + SHIFT + A. Этот аргумент является необязательной и используется для только команд.
  
_pxHelpTopic_ (**xltypeStr**)
  
Ссылки на файл справки (CHM-файла или просмотр) для отображения при нажатии пользователем кнопки Справка (при отображении пользовательской функции). Может быть в формате `filepath!HelpContextID` или `http://address/path_to_file_in_site!0`. Обе части до и после «!» являются обязательными.  *HelpContextID* не должно содержать одинарные кавычки и будут преобразованы в Excel 4 байтов, в виде десятичного знака целое число. При использовании формы URL-адрес, Excel открывает файл справки, который указывает ссылка. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Необязательный атрибут типа string, описывающий пользовательской функции, при этом в Мастер функций.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Необязательно. Первое строк, которые описывают пользовательские аргументы функции при выборе функции в Мастер функций. В Excel 2003 и более ранних версиях **xlfRegister** может принимать, не более 30 аргументы таким образом, можно обеспечить справки для первого 20 только аргументов функции. Начиная с версии Excel 2007, **xlfRegister** может занять до 255 аргументов, таким образом, можно обеспечить справки до 245 параметров функции. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Если регистрация прошла успешно, эта функция возвращает идентификатор регистрации функции (**xltypeNum**), которую можно использовать в вызовах **xlUDF** и **xlfUnregister** в библиотеке DLL или с помощью **ВЫЗОВА** и **Отменить РЕГИСТРАЦИЮ** в таблице макросов XLM. В противном случае возвращает #VALUE! Ошибка. 
  
## <a name="remarks"></a>Замечания

### <a name="data-types"></a>Типы данных

Аргумент _pxTypeText_ указывает тип данных возвращаемого значения и типы данных всех аргументов, функция DLL или код ресурс. Первым символом _pxTypeText_ указывает тип данных возвращаемого значения. Оставшиеся знаки показывают типы данных всех аргументов. Например функция DLL, которая возвращает число с плавающей запятой и принимает целое число и число с плавающей запятой в качестве аргументов требуются «Списка ЛИТЕРАТУРЫ» для аргумента _pxTypeText_ . 
  
Типы данных и структуры, используемые Excel для обмена данными с XLL-модулей приведен в следующих таблицах.
  
В первой таблице перечислены типы, поддерживаемые во всех версиях Excel.
  
|**��� ������**|**������������ �� ��������**|**������������ �� ������ (���������)**|**�����������**|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |Short [int] (0 = false или 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |ASCII byte, идентифицирующий  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Строка байтов инвентаризации ASCII  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||16-разрядный WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16-разрядное целое число со знаком  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32-разрядное целое число со знаком  <br/> |
|FP  <br/> ||K  <br/> |Структура массива с плавающей запятой  <br/> |
|Array  <br/> ||O  <br/> |Передаются три аргумента:<br/>-короткое целое число\*<br/>-короткое целое число\*<br/>-Дважды]  <br/> |
|XLOPER  <br/> ||P  <br/> |Значения типа переменной листа и массивов  <br/> |
|||R  <br/> |Значения, массивы и ссылки на диапазон  <br/> |
   
В Excel 2007, которые были представлены следующие типы данных для поддержки больших таблиц и длинные Юникод строки.
  
|**��� ������**|**������������ �� ��������**|**������������ �� ������ (���������)**|**�����������**|
|:-----|:-----|:-----|:-----|
|короткий неподписанных\*  <br/> ||C%, F%  <br/> |Строка Юникода Юникода символом NULL  <br/> |
|короткий неподписанных\*  <br/> ||D%, G%  <br/> |Строка Юникода инвентаризации Юникода  <br/> |
|FP12  <br/> ||K%  <br/> |Структура массива с плавающей запятой размером сетки  <br/> |
|Array  <br/> ||O%  <br/> |Передаются три аргумента:<br/>-подпись int \* / RW\*<br/>-подпись int \* / Столбца\*<br/>-Дважды]  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Значения типа переменной листа и массивов  <br/> |
|||U  <br/> |Значения, массивы и ссылки на диапазон  <br/> |
   
Начиная с версии Excel 2010 следующие данные были представлены типов:
  
|**Тип данных**|**������������ �� ��������**|**������������ �� ������ (���������)**|**�����������**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X   <br/> |Асинхронный дескриптор используется для отслеживания ожидающие асинхронные функции в Excel и XLL. Наличие тип параметра в тип string также определяет функцию как асинхронный. Дополнительные сведения о асинхронные функции [Asynchronous_User-Defined](asynchronous-user-defined-functions.md)см.  <br/> |
   
���� ����� **F**, **F%**, **G** � **G%** ������������ ��� ����������, ���������� �� �����. 
  
При работе с типами данных, отображаемых в предыдущей таблице, необходимо учитывать следующее:
  
- Объявления для языка C предполагается, что компилятор использует удваивается 8 байтов, 2-байтовое коротких целых и 4 — для длинных целых по умолчанию.
    
- Все функции в DLL-библиотеки и ресурсы, код вызываются с помощью **__stdcall** соглашение о вызове. 
    
- Любая функция, которая возвращает тип данных с помощью ссылки, то есть, который возвращает указатель на что-то, безопасно может вернуть указатель null. Microsoft Excel интерпретирует указатель null как #NUM! Ошибка.
    
## <a name="additional-data-type-information"></a>Дополнительные данные

В этом разделе содержатся подробные сведения о **E**, **F**, **F %**, **G**, **G %**, **K**, **O**, **P**, **Q**, **R**и типы данных **U** и другие сведения о _pxTypeText _аргумент. 
  
### <a name="e-data-type"></a>Тип данных E

Предполагается, что библиотеки DLL, с помощью типа данных E передавать указатели чисел с плавающей запятой в стеке. Это может вызвать проблемы с некоторые языки (например, C++ Borland), согласно прогнозу, номер будет передан в стеке эмулятора сопроцессора. Обходным путем является передать указатель на номер в стеке сопроцессора. Следующем примере показано, как из Borland C++ возвращает значение типа double.
  
```cpp
typedef double * lpDbl;
extern "C" lpDbl __stdcall AddDbl(double D1,
    double D2, WORD npDbl)
{
    lpDbl Result;
    Result = (lpDbl)MK_FP(_SS, npDbl);
    *Result = D1 + D2;
    return (Result);
}
```

### <a name="f-f-g-and-g-data-types"></a>F, F %, G и G % типов данных

**F**, **F %**, **G**и **G %** типы данных функция позволяет изменять на буфер строки, выделенный Microsoft Excel. Если код типа возвращаемого значения — это один из этих типов, Excel игнорирует значение, возвращаемое функцией. Вместо этого Excel выполняется поиск списка аргументов функции для первый соответствующий тип данных (**F**, **F %**, **G**или **G %**) и затем рассматривает текущее содержимое выделенного буфера строки как возвращаемое значение. Все версии Excel выделите 256 байт для **F** и **G** строки ASCII и начиная с версии Excel 2007 65 536 байт распределяются, достаточно для 32 768 знаков Юникод, **F %** и **G %** строк в кодировке Юникод. Помните, что буферы должны включать count (типы **G** и **G %**) или нулем знак (типы **F** и **F %**), чтобы значения длины ключа фактические строки максимально: 255 до 32 767. Строк в кодировке Юникод и аргументы типа **F %** и **G %** , доступны только с помощью интерфейса API для C в Excel. 
  
### <a name="k-and-k-data-types"></a>K и типы данных K %

Типы данных **K** и **K %** Используйте указатели на переменную высоту FP и FP12 структур соответственно. Эти структуры определяются в XLLCALL. З. FP12 структуры и аргументы типа **K %** , поддерживаются только начиная с версии Excel 2007. 
  
### <a name="o-and-o-data-types"></a>O и типы данных O %

Типы данных **O** и **O %** может использоваться только для аргументов, не возвращает значений, несмотря на то, что возвращаемые значения my изменение аргумент типа **O** или **O %** на месте. Каждый передает три элемента: указатель на число строк в массиве, указатель на число столбцов в массиве и указатель на двухмерный массив чисел с плавающей запятой. 
  
Чтобы изменить массив, переданный по O или O тип % данных на месте, можно использовать «> O» или «> O %» в качестве аргумента _pxTypeText_ . Дополнительные сведения об изменении массив обратитесь к разделу «Изменение в месте: функции, объявленные как Void» в этом разделе. 
  
Тип данных **O** был создан для прямой совместимости с библиотеками Fortran, которые передают аргументы по ссылке. 
  
**O %** поддерживается начиная с версии Excel 2007 и обеспечивает большое число строк, поддерживаемые в Excel. 
  
### <a name="p-and-q-data-types"></a>Типы данных P и Q

При аргументы функции DLL регистрируются как с удалением типа **P** XLOPERs или введите **Q** XLOPER12s, Excel преобразует ссылки на одну ячейку для простого значения и ссылки на множество ячеек для массивов при подготовке этих аргументов. Другими словами, типы **P** и **Q** будут всегда попадают в функцию как один из следующих типов: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**или **xltypeNil **, но не **xltypeRef** или **xltypeSRef** так, как они всегда, отменяются. **XLOPER12**s и аргументы типа **Q** , поддерживаются только начиная с версии Excel 2007. 
  
Если типы **xltypeMissing** или **xltypeNil** используется для возврата значения, они рассматриваются в Excel как числовое нулю. **xltypeMissing** передается при вызове аргумент опущен. **xltypeNil** передается, когда при вызове ссылку на пустую ячейку. Диапазон ячеек, преобразованный в **xltypeMulti** для передачи в качестве типа **P** или **Q**, все пустые ячейки в диапазоне преобразуются в элементы массива **xltypeNil** . Недостающие элементы в массиве литерала аналогичным образом передаются как элементы **xltypeNil** . 
  
### <a name="volatile-functions-and-recalculation"></a>Переменные функции и пересчет

В таблицу можно сделать DLL функция или программный ресурс переменные, таким образом, чтобы он пересчитывает каждый раз, когда пересчитывается лист. Для этого добавьте восклицательный знак (!) после последнего кода аргумент в аргументе _pxTypeText_ . 
  
> [!NOTE]
> По умолчанию, функции, которые тип **R** XLOPERs или введите **U** XLOPER12s и, зарегистрированные в качестве макроса листа эквивалентами (тип **#**; далее в разделе) обрабатываются как переменные в Excel. 
  
### <a name="functions-declared-as-void"></a>Функции, объявленные как void

Существует два условия, которые могут вызывать при объявлении функции, что возврат void. В обоих случаях функция возвращает результат любым другим способом.
  
#### <a name="modifying-in-place"></a>Изменение на месте

Отдельная цифра _n_ можно использовать для кода тип возвращаемого значения в _pxTypeText_, где _n_ — число в диапазоне от 1 до 9. Это заставляет Excel, чтобы сделать значение переменной в расположении, на который указывает аргумент _n_th в _pxTypeText_ как возвращаемое значение. Это также известные как изменение на месте. Аргумент _n_th должен быть проход по ссылке тип данных (C, D, E, F, F %, G, G %, K, K %, L, M, N, O, O %, P, Q, R или U). Функция DLL или код ресурс также должен быть объявлен с **void** ключевое слово на языках C/C++ (или ключевое слово **процедуру** на Pascal). 
  
Например функции DLL, которая принимает строку символом null и два указателя на целые числа как аргументы можно изменить строку на месте. Используйте «1FMM» в качестве аргумента _pxTypeText_ и объявления функции как void. 
  
Предыдущие версии Excel используется **\>** в начале _pxTypeText_ для обозначения, что функция была объявлена как void и что первый аргумент было изменено на месте — не было возможности для изменения любого аргумента, кроме первого. **\>** Эквивалентен _n_ = 1 в текущей версии Excel и это **\>** в функциях, синхронные поддерживается только для обратной совместимости. 
  
#### <a name="asynchronous-functions"></a>Асинхронные функции

Асинхронные функции, идентификаторами с помощью параметра типа X в **pxTypeText**не возвращает результат из вызова начальное функции. Вместо этого необходимо объявить асинхронные функции как void и более поздних версий надстройки возвращает результат посредством обратного вызова. Асинхронные функции должны быть зарегистрированы с помощью **\>** в начале **pxTypeText**. В асинхронные функции **\>** обозначает, что функции объявленные как void, но не указывает, что первый аргумент изменяется на месте. Дополнительные сведения о асинхронные функции [Asynchronous_User-Defined](asynchronous-user-defined-functions.md)см. 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Регистрация функции листа как эквиваленты листа макросов (обработка невычисляемая ячейки)

Размещение **#** символов после последнего параметра код в _pxTypeText_ предоставляет функцию вызывающего разрешения, как функции на листе макросов. Это, как показано ниже: 
  
- Функции можно извлечь значений ячеек, которые еще не вычислялись в этом цикле пересчета.
    
- Функция вызовом функции XLM сведения (класса 2), к примеру, **xlfGetCell**.
    
- Если не решетки (#): оценке результатов не вычисленной ячейки в ошибку **xlretUncalced** и текущей функции снова вызывается после вычисления ячейки; вызов функции сведения любого XLM отличный от **xlfCaller** приводит к ошибке **xlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Регистрация функции листа в качестве потоками

Начиная с версии Excel 2007, Excel могут выполнять пересчет многопоточные рабочей книги. Это означает, что его можно назначить разные экземпляров функции потоками параллельных потоков для повторного вычисления. Начиная с версии Excel 2007, большая часть встроенных функций являются потокобезопасными. Начиная с версии Excel 2007, Excel также позволяет XLL-модулей для регистрации функции листа как потоками. Чтобы сделать это, включают **$** символ после последнего параметра кода в _pxTypeText_. 
  
> [!NOTE]
> Только функции могут быть объявлены являющихся потокобезопасными. Excel не учитывает макрос листа эквивалентный функции являющихся потокобезопасными, чтобы не удается добавить оба **#** и **$** символов в аргументе _pxTypeText_ . 
  
Если функция была зарегистрирована как потоками, следует убедиться, что ведет себя образом потоками, несмотря на то, что Excel отклоняет вызовы небезопасных потока с помощью интерфейса API для C. Например если функция потоками пытается вызвать **xlfGetCell**, вызова завершается с ошибкой **xlretNotThreadSafe** . 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Регистрация функции листа в качестве безопасных кластера

Начиная с версии Excel 2010, Excel можно разгрузки вызовы функций к поставщику назначенного compute cluster. Для получения дополнительных сведений см [Безопасные для кластера функции](cluster-safe-functions.md). Все функции листа XLL зарегистрирована как безопасный кластера принять участие в разгрузки при наличии кластера. Зарегистрированные кластера безопасных функций, включая **&amp;** символ после последнего параметра кода в аргументе _pxTypeText_ . 
  
Если функция была зарегистрирована как безопасный кластера, следует убедиться, что ведет себя в кластере безопасным способом. Для получения дополнительных сведений см [Безопасные для кластера функции](cluster-safe-functions.md).
  
> [!NOTE]
> Только функции листа может быть объявлен как безопасный кластера. Excel не учитывает макрос листа эквивалентный функции безопасности кластера, чтобы не удается добавить оба **#** и **&amp;** символов в аргументе _pxTypeText_ . Функции листа может быть объявлен как безопасный кластера и являющихся потокобезопасными. В этом случае Excel позволит эти функции, чтобы принять участие в многопоточные вычисления при отключении разгрузки кластера. 
  
### <a name="category-names"></a>Имя категории

Чтобы определить, какие категории, которую требуется поместить вашей XLL функции в придерживайтесь следующих принципов.
  
- Если функция делает то, что можно сделать пользователя как часть надстройки пользовательского интерфейса, следует помещать функцию в категории **команд** . 
    
- Если функция возвращает сведения о состоянии надстройки и другие полезные сведения, следует помещать функцию в **сведения о** категории. 
    
- Надстройка никогда не указывать функции или команды для категории **Пользовательских** . Эта категория предназначена для исключительное право на использование конечных пользователей. 
    
Категория указана с помощью параметра _pxCategory_ в **xlfRegister**. Это может быть число или текст, который соответствует одной из категорий жестко стандартный или текст новой категории, указанного идентификатором библиотеки DLL. Если данный текст еще не существует, Excel создает новую категорию с таким именем.
  
В следующей таблице перечислены стандартные категории, которые отображаются при просмотре **Вставить функцию** диалогового окна в лист. 
  
|**Число**|**Text**|
|:-----|:-----|
|1  <br/> |Финансовые  <br/> |
|2  <br/> |Дата &amp; времени  <br/> |
|3  <br/> |Математические &amp; активация  <br/> |
|4  <br/> |Text  <br/> |
|5  <br/> |Логические операции  <br/> |
|6  <br/> |Поиск &amp; Справочник  <br/> |
|7  <br/> |База данных  <br/> |
|8  <br/> |Статистические  <br/> |
|9  <br/> |Сведения  <br/> |
|14  <br/> |Определенные пользователем  <br/> |
||Инженерные работы (начиная с версии Excel 2007)  <br/> |
||Куба (начиная с версии Excel 2007)  <br/> |
   
Кроме того эти категории доступны при просмотре **Вставить функцию** диалогового окна в лист макросов. 
  
|**Число**|**Text**|
|:-----|:-----|
|10  <br/> |�������  <br/> |
|11  <br/> |DDE или внешний  <br/> |
|12  <br/> |Настройка  <br/> |
|13  <br/> |Элемент управления макросов  <br/> |
   
### <a name="example"></a>Пример

Просмотр кода для функции **xlAutoOpen** в `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>См. также

- [РЕГИСТРАТОР.ИД](xlfregisterid.md)
- [ОТМЕНА РЕГИСТРАЦИИ](xlfunregister-form-1.md)
- [Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)
