---
title: Вызов в Excel из DLL или XLL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- диалоговые окна [excel 2007], вызов excel команды, DLL-библиотеки [Excel 2007] команды вызова Excel, передача аргументов в функции интерфейса API C [Excel 2007], [Excel 2007], вызова с диалоговые окна команды [Excel 2007], доступного из DLL или XLL Excel4 функции [ Функция Excel12 Excel 2007], [Excel 2007], XLCallVer функции аргумент operRes [Excel 2007], [Excel 2007], функции [Excel 2007], доступного из DLL или XLL Excel12v функции [Excel 2007], DLL-только для функции интерфейса API для C [Excel 2007], [Excel 2007], передача аргументы, аргумент [Excel 2007], команды [Excel 2007], вызов при использовании локализованных версий, DLL-только для команды [Excel 2007], международных версий [Excel 2007], вызов функций и счетчика команд, XLL-модулей [Excel 2007], вызов в Excel, функция [4v Excel Excel 2007] xlfn аргумент [Excel 2007], функции [Excel 2007], вызов при использовании локализованных версий
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807197"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Вызов в Excel из DLL или XLL

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel позволяет библиотеки DLL для доступа к встроенными командами Excel, функции листа и функции листа макросов. Эти параметры доступны из DLL-Библиотеку команд и функций, вызываемых из Visual Basic для приложений (VBA) и зарегистрированных XLL команд и функций, вызываемых непосредственно в Excel.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Excel4, Excel4v, Excel12 и Excel12v функции

Приложение Excel позволяет получить доступ к команд и функций через функции обратного вызова [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)и [Excel12v](excel4v-excel12v.md)библиотеки DLL.
  
Функции **Excel4** и **Excel4v** впервые появились в Excel версии 4. Они работают со структурой данных **XLOPER** . Excel 2007 появились две новые функции обратного вызова, **Excel12** и **Excel12v**, которые работают со структурой данных **XLOPER12** . Функции **Excel4** и **Excel4v** экспортируются библиотекой Xlcall32.lib, которое должно быть включено в проекте библиотеки DLL или XLL. В SDK C++ исходный файл Xlcall.cpp, которая должна быть включена в проект, если вы хотите получить доступ к функциональности Excel с помощью структур **XLOPER12** включены **Excel12** и **Excel12v** . 
  
В следующем коде показан прототипов функций для этих функций. Первые три аргумента, совпадают, за исключением того, что второй аргумент указатель **XLOPER** в первой паре и указатель **XLOPER12** второй пару. Соглашение о вызове — **_cdecl** в **Excel4** и **Excel12** , чтобы разрешить списки аргументов переменных. Многоточие представляет указатели значения **Excel4** **XLOPER** и **XLOPER12** значения для **Excel12**. Число указатели равно значение параметра _count_ . 
  
**Все версии Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Начиная с версии Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Для библиотеки DLL иметь возможность вызова **Excel4**, **Excel4v**, **Excel12**или **Excel12v**Excel необходимо передать управление библиотеки DLL. Это означает, что эти обратные вызовы интерфейса API для C могут вызываться только в следующих случаях:
  
- Внутри одной командой XLL, Excel, называется напрямую или с помощью VBA.
    
- Из функцию листа электронной таблицы или макрос XLL, Excel вызываются напрямую или с помощью VBA.
    
Не может вызывать Excel C API в следующих сценариях:
  
- Из событий операционной системы (например, от функции [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) ). 
    
- В фоновом потоке, которые созданы библиотеки DLL.
    
### <a name="return-values"></a>Возвращаемые значения

Все четыре эти функции возвращают целое число, чтобы сообщить вызывающего ли функция или команды успешного вызова. Возвращаемые значения может быть одной из следующих:
  
|**Возвращаемое значение**|**Определенные в Xlcall.h как**|**Описание**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Функция или команда выполнена успешно. Это означает, что выполнение был ошибки. Например, **Excel4** может вернуть **xlretSuccess** при вызове функции **поиска**, несмотря на то, что рассчитано для **#VALUE!** так как текст поиска не найден. Следует проанализировать тип и значение возвращенные **XLOPER и XLOPER12** там, где это возможно.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Команда макроса остановлена пользователем, нажав кнопку **Отмена** или нажав клавишу ESC.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Предоставленный функции или код команды является недопустимым. Эта ошибка может возникнуть при вызывающей функции не имеет разрешения на вызов функции или команды. Например функция листа не может вызывать функции сведений листа макроса или функции, команда.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Число аргументов в вызове не правильный.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Одно или несколько значений **XLOPER** или **XLOPER12** аргумент неправильно сформирован или не появится.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel обнаружено риск, что операция может переполнения стек и, таким образом, не удалось вызвать функцию.  <br/> |
|32  <br/> |**xlretFailed** <br/> |Команда или функция не удалось по причине, не описываемых возвращаемого значения. Операция, которая может потребоваться слишком много памяти, например произойдет сбой с этой ошибкой. Это может произойти при попытке преобразовать ссылки на очень больших массива **xltypeMulti** с помощью функции [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) .  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Операция для извлечения значения не вычисленной ячейки. Чтобы сохранить целостность Пересчет в Excel, функции листа для этого не разрешены. Тем не менее XLL команд и функций, зарегистрированных как функции листа макросов разрешается доступ к значениям, не вычисленной ячейки.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Начиная с версии Excel 2007) Функция листа XLL зарегистрирована как потокобезопасными попытка вызова функции интерфейса API для C, который не является потокобезопасными. Например являющихся потокобезопасными функции не может вызывать функции XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Начиная с Excel 2010) Недопустимый дескриптор асинхронные функции.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Начиная с Excel 2010) Вызов не поддерживается для кластеров.  <br/> |
   
Если функция возвращает одно из значений сбоя в таблице (то есть, он не возвращает **xlretSuccess**), возвращаемое значение **XLOPER** или **XLOPER12** также будет иметь значение **#VALUE!**. В некоторых случаях, проверка может быть достаточно тест успешно, но следует иметь в виду, что звонка можно вернуть оба **xlretSuccess** и **#VALUE!**.
  
Если вызова интерфейса API для C результатов в **xlretUncalced** или **xlretAbort**, DLL или XLL код должен возвращать элемента управления в Excel перед внесением других вызовов интерфейса API для C (кроме вызовы функции [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) для освобождения Excel выделенной памяти ресурсы в **XLOPER** и **XLOPER12** значения). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Команда или функция перечисление аргумент: xlfn

Аргумент _xlfn_ является первый аргумент для обратного вызова функции и 32-разрядное целое число со знаком. Его значение должно быть одно из перечисления команду или функции, определенные в файле заголовка SDK Xlcall.h, как показано в следующем примере. 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

Все списки и макрос лист функции, в диапазоне от 0 (**xlfCount**) до 0x0fff шестнадцатеричные, несмотря на то, что самый высокий назначен номер в Excel 2013 — 547 decimal, 0x0223 шестнадцатеричных (**xlfFloor_precise**).
  
Все функции, команды, в диапазоне от 0x8000 шестнадцатеричных (**xlcBeep**) через 0x8fff шестнадцатеричные, несмотря на то, что с наибольшим числом назначенный в Excel 2013 — это шестнадцатеричный 0x8328 (**xlcHideallInkannots**). Они определены в файле заголовка как `(n | xlCommand)` где `n` — десятичное число, большее или равное 0 и **xlCommand** определяется как 0x8000 шестнадцатеричные. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Вызов, использовать диалоговые окна команды Excel

Некоторые коды команд соответствуют действия в Excel, использующие диалоговых окон. Например, **xlcFileDelete** принимает один аргумент: имя файла или маску. Это может быть вызван с диалоговое окно, чтобы у пользователя есть возможность отменить или изменить операцию удаления. Его можно также вызвать без диалоговом окне в противном случае файл или файлы удаляются без дальнейший взаимодействия, если они существуют и вызывающего абонента есть разрешение. Чтобы позвонить в командах в форму их диалогового окна, перечисление команду должен быть объединен с помощью битовой операции с 0x1000 (**xlPrompt**).
  
В следующем примере кода удаляются файлы в текущем каталоге соответствия my_data маска\*.bak, отображение диалогового окна только в том случае, если аргумент имеет значение true.
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a>Вызов функций и команд при использовании локализованных версий

Можно настроить для отображения функций и имена команд XLM в различных языков в Excel. Некоторые команды C API и функции работают, которые интерпретируются как имена функции или командной строки. Например **xlcFormula** принимает строковый аргумент, предназначенного для находились в указанной ячейке. Для надстройки для работы со всех языковых параметров можно задать имена строки на английском языке и установить бит 0x2000 (**библиотеки xlIntl**) в перечислении команду или функции.
  
В следующем примере кода помещает эквивалент `=SUM(X1:X100)` в ячейку A2 на активном листе. Обратите внимание, что для создания временной внешние ссылки **XLOPER**используется функция Framework, **TempActiveRef**. Формула будет отображаться в A2 на правильном языке определить языковой стандарт (например, `=SOMME(X1:X100)` Если установлен французский язык). 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> Так как в результате вызова **Excel12** не является обязательным, 0 (ноль) может быть передан в качестве аргумента второй, а не адрес **xResult**. Рассматривается более в следующем разделе. 
  
### <a name="dll-only-functions-and-commands"></a>Команды и функции DLL

Excel поддерживает несколько функций, которые доступны только из DLL или XLL. Они определены в файле заголовка как `(n | xlSpecial)` где `n` — десятичное число, большее или равное 0 и `xlSpecial` определяется как 0x4000 шестнадцатеричные. Эти функции в следующей таблице перечислены и описаны в [Справочник по функциям API](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Освобождает ресурсы Excel выделенной памяти.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Возвращает объем свободного пространства в стеке Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Преобразование между типами **XLOPER** и **XLOPER12**  <br/> |
|[функция xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Обеспечивает быстрый метод установки значений ячеек.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Получает имя листа из его внутренний идентификатор.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Получает внутренний идентификатор листа от его имени.  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |Проверяет ли пользователь нажимает кнопку **Отмена** или нажата клавиша ESC.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Получает дескриптор экземпляра Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Получает дескриптор главного окна Microsoft Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Возвращает путь и имя файла библиотеки DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Эта функция устарел и больше не требуется для вызова.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Эта функция устарел и больше не требуется для вызова.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Определяет имя сохраняемого двоичные хранения.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Получает имя постоянное хранилище двоичных данных.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Возвращаемое значение XLOPER и XLOPER12: operRes

Аргумент _operRes_ является второй аргумент процедуры обратного вызова и указатель **XLOPER** (**Excel4** и **Excel4v**) или **XLOPER12** (**Excel12** и **Excel12v**). После успешного вызова в нем возвращаемое значение функции или команды. можно включить **operRes** ноль (указатель NULL), если необходим без возвращаемого значения. Предыдущее содержимое **operRes** , будут перезаписаны, чтобы любой памяти, ранее, на который указывает освобождения перед звонок во избежание утечки памяти. 
  
Если функция или команда не может вызываться (например, если неправильные аргументы), **operRes** задано значение ошибки **#VALUE!**. Команду всегда возвращает **логическое** **значение TRUE,** Если операция будет успешна, или **значение FALSE,** если он не или пользователь отменил ее. 
  
## <a name="number-of-subsequent-arguments-count"></a>Число аргументов последующие: count

Аргумент _count_ — третий аргумент процедуры обратного вызова и 32-разрядное целое число со знаком. Он должен быть задан номер последующие аргументы, начиная с 1. Если функция или команда не принимает аргументы, его необходимо задать нулевое значение. В Microsoft Office Excel 2003 максимальное количество аргументов, которые может выполнять все функции является 30, однако большинство меньше, чем это. Начиная с версии Excel 2007, максимальное количество аргументов, которые может выполнять все функции было увеличено до 255. 
  
С помощью **Excel4** и **Excel12** _счетчик_ — число указатели на **XLOPER** или **XLOPER12** значения, которые передаются. Внимательно очень не для передачи меньше аргументов, чем значение этого _счетчика_ имеет значение. В результате Excel чтение издержек в стеке и выполнении недопустимые значения **XLOPER** или **XLOPER12** , что может привести к сбою приложения. 
  
С помощью **Excel4v** и **Excel12v** _count_ — размер массива указатели на **XLOPER** или **XLOPER12** значения, которое передается в качестве аргумента следующий и последний. Опять же должен быть очень избегать передать меньшего размера массива, чем _количество_ элементов в размер, как это приведет к границ массива переполнения. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Передача аргументов в функции интерфейса API для C

**Excel4** и **Excel12** занять переменной длины списки аргументов, после _count_, которые интерпретируются как указатели на значения **XLOPER** и **XLOPER12** , соответственно. **Excel4v** и **Excel12v** принимает один аргумент, после _count_, то есть указатель на массив указателей **XLOPER** значения в случае **Excel4v**и **XLOPER12** значения в случае **Excel12v**.
  
Формы массива, **Excel4v** и **Excel12v**позволяют аккуратно код вызова интерфейса API для C при число аргументов является переменной. В следующем примере функция, которая принимает размер переменной массива чисел и использует функции листа Excel, с помощью интерфейса API для C, для вычисления суммы, средний, минимальный и максимальный. 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

Замените ссылки значения **XLOPER12** **XLOPER**и **Excel12v** с **Excel4v**, в предыдущем примере кода приведет к функции, которая будет работать со всеми версиями Excel. Эта операция функции Excel **Сумма**, **Среднее**, **MIN**и **MAX** довольно проста, что было бы более эффективно код их C и избежать Подготовка аргументов и вызов в Excel. Тем не менее многие из функций, которые Excel содержит более сложны, выполнение этого подхода полезно в некоторых случаях. 
  
Другой пример работы с **Excel4v** и **Excel12v**раздел [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) . При регистрации функция листа XLL, можно указать строку описания для каждого аргумента, который используется в диалоговом окне **Вставить функцию** . Таким образом число общее аргументов в **xlfRegister** зависит от числа аргументы, которые использует функцию XLL и будут зависеть от одной функции в другую. 
  
Там, где вы всегда вызова функции интерфейса API для C или команды с такое же число аргументов, необходимо избежать дополнительные действия по созданию массив указателей для этих аргументов. В таких случаях проще и более чистый используйте **Excel4** и **Excel12**. Например при регистрации функций и команд XLL, необходимо указать полный путь и имя библиотеки DLL или XLL. Можно получить имя файла в вызове **xlfGetName** и освобождать с помощью вызова **xlFree**, как показано в следующем примере для **Excel4** и **Excel12**.
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

На практике функцию **Excel12v_example**можно построить более эффективно путем создания одного **xltypeMulti** **XLOPER12** аргумент и вызова интерфейса API для C с помощью **Excel12**, как показано в следующем примере.
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> В этом случае возвращаемое значение **Excel12** игнорируется. Код вместо этого проверяется, что возвращенные **XLOPER12** **xltypeNum** для определения, успешно ли вызов. 
  
## <a name="xlcallver"></a>XLCallVer

В дополнение к обратных вызовов **Excel4**, **Excel4v**, **Excel12**и **Excel12v**Excel экспортирует функции **XLCallVer**, который возвращает номер версии интерфейса API для C в настоящее время работает.
  
Прототип функции выглядит следующим образом:
  
 `int pascal XLCallVer(void);`
  
Можно вызвать эту функцию, являющийся потокобезопасными, из XLL команда или функция.
  
В Excel 97 — Excel 2003, **XLCallVer** возвращает 1280 = значения 0x0500 hex = 5 x 256, что указывает Excel версии 5. Начиная с версии Excel 2007, возвращает большего 3072 пикселей = 0x0c00 hex = 12 x 256, аналогично указывает на версию 12.
  
Несмотря на то, что это можно использовать для определения доступности нового C API во время выполнения, можно определять используемой версии Excel с помощью `Excel4(xlfGetWorkspace, &version, 1, &arg)`, где `arg` — это числовой, **XLOPER** значение 2. Функция возвращает строку **XLOPER**версии, который затем может быть преобразован в тип integer. Причина от версии Excel, а не версия интерфейса API для C является различия между Excel 2000, Excel 2002 и Excel 2003, надстройка может также потребоваться обнаружения. Например в точность некоторых статистических функций были внесены изменения.
  
## <a name="see-also"></a>См. также



[Создание XLL-модулей](creating-xlls.md)
  
[Доступ к XLL-коду в Excel](accessing-xll-code-in-excel.md)
  
[���������� �� ������� Excel 2013 XLL SDK API](excel-xll-sdk-api-function-reference.md)
  
[������� ��������� ������ API C Excel4 Excel12](c-api-callback-functions-excel4-excel12.md)
  
[���������� XLL-������� ��� Excel 2013](developing-excel-xlls.md)

