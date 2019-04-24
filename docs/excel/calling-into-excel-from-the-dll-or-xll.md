---
title: Вызов Excel из библиотеки DLL или XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- диалоговые окна [excel 2007], вызов команд excel, библиотеки DLL [Excel 2007], вызов Excel, передача аргументов функции API C [Excel 2007], команды [Excel 2007], вызов в диалоговых окнах, команды [Excel 2007], предоставление доступа из DLL или XLL, функция Excel4, функция Excel12 [Excel 2007], функция XLCallVer [Excel 2007], аргумент operRes [Excel 2007], [Excel 2007], функции [Excel 2007], доступ из DLL или XLL, функция Excel12v [Excel 2007], функции только для DLL [Excel 2007], API C [Excel 2007], передача аргументов, аргумент счета [Excel 2007], команды [Excel 2007], вызовы в международных версиях, команды только для DLL [Excel 2007], международные версии [Excel 2007], вызовы функций и команд, XLL [Excel 2007], вызовы в Excel, функция 4v Excel [Excel 2007], аргумент xlfn [Excel 2007], функции [Excel 2007], вызовы в международных версиях
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304160"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Вызов Excel из библиотеки DLL или XLL

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel позволяет DLL получить доступ к встроенным командам Excel, функциям листов и функциям листа макросов. Они доступны как из команд и функций DLL, вызываемых из Visual Basic для приложений (VBA), так и из зарегистрированных команд и функций XLL, вызываемых непосредственно в Excel.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Функции Excel4, Excel4v, Excel12 и Excel12v

Excel позволяет DLL получать доступ к командам и функциям через функции обратного вызова [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md) и [Excel12v](excel4v-excel12v.md).
  
Функции **Excel4** и **Excel4v** появились в версии Excel версии 4. Они работают со структурой данных **XLOPER**. В Excel 2007 появились две новые функции обратного вызова, **Excel12** и **Excel12v**, которые работают со структурой данных **XLOPER12**. Функции **Excel4** и **Excel4v** экспортируются библиотекой Xlcall32.lib, которая должна быть включена в проект DLL или XLL. **Excel12** и **Excel12v** включены в исходный файл SDK C++ Xlcall.cpp, который должен быть в проекте, если вам нужен доступ к функциональным возможностям Excel с помощью структур **XLOPER12**. 
  
Приведенный ниже код отображает прототипы для этих четырех функций. Первые три аргумента одинаковы с тем исключением, что второй аргумент является указателем на **XLOPER** в первой паре и указателем на **XLOPER12** во второй. Соглашение о вызовах — **_cdecl** в **Excel4** и **Excel12** для разрешения списков переменных аргументов. Многоточие представляет указатели на значения **XLOPER** для **Excel4** и значения **XLOPER12** для **Excel12**. Количество указателей равно значению параметра _count_. 
  
**Все версии Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Начиная с Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Чтобы DLL могла вызвать **Excel4**, **Excel4v**, **Excel12** или **Excel12v**, приложение Excel должно передать управление библиотеке DLL. Это означает, что обратные вызовы API C возможны только в следующих ситуациях:
  
- Из команды XLL, которую приложение Excel вызвало непосредственно или с помощью VBA.
    
- Из листа XLL функции листа макросов, который приложение Excel вызвало непосредственно или с помощью VBA.
    
Невозможно вызвать API C Excel в следующих ситуациях:
  
- Из события операционной системы (например, из функции [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)). 
    
- Из фонового потока, созданного вашей DLL.
    
### <a name="return-values"></a>Возвращаемые значения

Все эти четыре функции возвращают целочисленное значение, которое уведомляет вызывающего о том, была ли функция или команда вызвана успешно. Могут возвращаться любые значения из указанных ниже.
  
|**Возвращаемое значение**|**Как определено в Xlcall.h**|**Описание**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Функция или команда успешно выполнена. Это не означает, что выполнение прошло без ошибок. Например, **Excel4** может возвратить **xlretSuccess** при вызове функции **FIND** даже при оценке **#VALUE!** из-за того, что найти искомый текст не удалось. Проверьте тип и возвращаемое значение **XLOPER/XLOPER12**, если есть такая возможность.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Макрос команд остановлен пользователем, который нажал кнопку **ОТМЕНА** кнопку или клавишу ESC.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Предоставленная функция или код команды недействительны. Эта ошибка может возникнуть, если у функции вызова нет разрешения для вызова функции или команды. Например, функция листа не может вызвать функцию информации листа макросов или функцию команды.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Число аргументов, передаваемых в вызове, неправильно.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Одно или несколько значений аргумента **XLOPER** или **XLOPER12** не сформировано должным образом или не заполнено.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Приложение Excel обнаружило риск того, что операция могла переполнить стек и не вызвать функцию.  <br/> |
|32  <br/> |**xlretFailed** <br/> |Команда или функция не выполнена по причине, которая не описана одним из других значений возврата. Например, операция, для которой нужно слишком много памяти, может быть не выполнена с такой ошибкой. Это может произойти при попытке преобразовать очень большую ссылку на массив **xltypeMulti** с помощью функции [xlCoerce](xlcoerce.md).  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Операция попыталась получить значение элемента ячейки, вычисление для которой не выполнено. Для сохранения целостности повторного расчета в Excel функциям листов запрещено выполнять такую операцию. Однако командам и функциям XLL, зарегистрированным как функции листа макросов, разрешен доступ к значениям ячеек, вычисление для которых не выполнено.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Начиная с Excel 2007.) Функция листа XLL, зарегистрированная как потокобезопасная, попыталась вызвать не потокобезопасную функцию API C. Например, потокобезопасная функция не может вызвать функцию XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Начиная с Excel 2010.) Асинхронный дескриптор функции недопустим.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Начиная с Excel 2010.) Вызов на кластерах не поддерживается.  <br/> |
   
Если функция возвращает одно из значений сбоя в таблице (иными словами, не возвращает **xlretSuccess**), значение возврата **XLOPER** или **XLOPER12** будет также задано как **#VALUE!**. В некоторых случаях такой проверки может быть достаточно для тестирования успешного выполнения, но следует помнить, что вызов может возвратить **xlretSuccess** и **#VALUE!**.
  
Если вызов API C приносит результат либо **xlretUncalced**, либо **xlretAbort**, код DLL или XLL должен возвратить управление приложению Excel, прежде чем создавать другие вызовы API C (кроме вызовов функции [xlfree ](xlfree.md), чтобы высвободить ресурсы памяти, выделенные приложению Excel, в значениях **XLOPER** и **XLOPER12**). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Аргумент перечисления команды или функции: xlfn

Аргумент _xlfn_ — это первый аргумент для функций обратного вызова, он представляет собой 32-разрядное подписанное целое число. Его значение должно быть одним из перечислений функции или команды, определенным в файле заголовка SDK Xlcall.h, как показано в приведенном ниже примере. 
  
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

Все функции листа и листа макросов находятся в диапазоне шестнадцатеричных чисел от 0 (**xlfCount**) до 0x0fff, хотя максимальное назначенное число в Excel 2013 является десятичным 547, шестнадцатеричным 0x0223 (**xlfFloor_precise**).
  
Все функции команды находятся в диапазоне шестнадцатеричных чисел от 0x8000 (**xlcBeep**) до 0x8fff, хотя максимальное назначенное число в Excel 2013 — шестнадцатеричное 0x8328 (**xlcHideallInkannots**). Они определяются в файле заголовка как `(n | xlCommand)`, где `n` — это десятичное число не меньше 0, а **xlCommand** определено как шестнадцатеричное число 0x8000. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Вызов команд Excel, которые работают с диалоговыми окнами

Некоторые коды команд соответствуют действиям в Excel, в которых используются диалоговые окна. Например, **xlcFileDelete** принимает один аргумент — маску или имя файла. Вызов можно выполнить с помощью диалогового окна, чтобы у пользователя была возможность отменить или изменить операцию удаления. Вызов возможен и без диалогового окна. В этом случае один или более файлов будут удалены без дальнейшего вмешательства при условии, что они существуют, а у вызывающего есть разрешение. Для вызова таких команд в формах диалогового окна перечисление команды должно объединяться с помощью битовой операции OR с 0x1000 (**xlPrompt**).
  
В показанном ниже примере кода удаляются файлы из текущего каталога, соответствующие маске my_data\*.bak, а диалоговое окно отображается, только если аргумент верный.
  
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

### <a name="calling-functions-and-commands-in-international-versions"></a>Вызов функций и команд в международных версиях

Вы можете настроить в Excel вывод на экран имен функций и команд XLM на разных языках. Некоторые команды и функции API C работают со строками, которые будут интерпретироваться как имена функций или команд. Например, **xlcFormula** имеет аргумент строки, который предназначен для размещения в указанной ячейке. Чтобы надстройка работала со всеми языковыми параметрами, можно указать имена строк на английском и задать бит 0x2000 (**xlIntl**) в перечислении функций или команд.
  
В представленном ниже примере кода эквивалент `=SUM(X1:X100)` помещается в ячейку A2 на активном листе. Обратите внимание на то, что он использует функцию Framework **TempActiveRef**, чтобы создать временную внешнюю ссылку **XLOPER**. Формула будет отображаться в ячейке A2 на правильном языке, соответствующем региону (например, `=SOMME(X1:X100)`, если язык французский). 
  
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
> Так как результат вызова в **Excel12** не требуется, нулевое значение (NULL) можно передать как второй аргумент вместо адреса **xResult**. Это обсуждается более подробно в следующем разделе. 
  
### <a name="dll-only-functions-and-commands"></a>Функции и команды только для DLL

Excel поддерживает небольшое количество функций, которые доступны только из DLL или XLL. Они определяются в файле заголовка как `(n | xlSpecial)`, где `n` — это десятичное число не меньше 0, а `xlSpecial` определяется как шестнадцатеричное число 0x4000. Эти функции перечислены в приведенной ниже таблице и задокументированы в [справочнике по функциям API](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Освобождает ресурсы памяти, выделенные для Excel.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Возвращает свободное место в стеке Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Преобразует тип **XLOPER** в **XLOPER12** и наоборот  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Предоставляет быстрый метод для задания значений в ячейках.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Получает имя листа от внутреннего идентификатора.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Получает внутренний идентификатор листа от его имени.  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |Проверяет, нажал ли пользователь кнопку **ОТМЕНА** или клавишу ESC.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Получает дескриптор экземпляра Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Получает дескриптор главного окна Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Получает путь и имя файла DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Эта функция устарела, ее больше не нужно вызывать.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Эта функция устарела, ее больше не нужно вызывать.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Определяет имя постоянного хранилища двоичных данных.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Получает данные имени постоянного хранилища двоичных данных.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Возвращаемое значение XLOPER/XLOPER12: operRes

Аргумент _operRes_ — это второй аргумент для обратных вызовов, который является указателем на **XLOPER** (**Excel4** и **Excel4v**) или **XLOPER12** (**Excel12** и **Excel12v**). После успешного вызова он содержит значение, возвращаемое функцией или командой. В **operRes** можно задать нуль (указатель NULL), если возвращаемое значение не требуется. Предыдущее содержимое **operRes** будет перезаписано, чтобы вся ранее указанная память была освобождена перед вызовом во избежание утечки памяти. 
  
Если не удается вызвать функцию или команду (например, если аргументы неправильные), для **operRes** будет задана ошибка **#VALUE!**. Команда всегда возвращает **логическое** значение **TRUE**, если выполнена успешно, или **FALSE**, если она не выполнена или если пользователь ее отменил. 
  
## <a name="number-of-subsequent-arguments-count"></a>Число последовательных аргументов: count

Аргумент _count_ — это третий аргумент для обратного вызова, он представляет собой 32-разрядное подписанное целое число. Для него должно быть задано число последующих аргументов, начиная с 1. Если функция или команда не принимает аргументы, для него нужно задать ноль. В Microsoft Office Excel 2003 максимальное число аргументов, которое может принять функция, — 30, хотя большинство принимает меньше. Начиная с Excel 2007, максимальное число аргументов, которое может принять функция, увеличилось до 255. 
  
_count_ в **Excel4** и **Excel12** — это количество указателей на передаваемые значения **XLOPER** или **XLOPER12**. Нужно внимательно следить за тем, чтобы не передать меньше аргументов, чем заданное значение _count_. Это приведет к тому, что Excel прочтет стек преждевременно и попытается обработать недопустимые значения **XLOPER** или **XLOPER12**, что может привести к сбою приложения. 
  
_count_ в **Excel4v** и **Excel12v** — это размер массива указателей на значения **XLOPER** или **XLOPER12**, которые передаются как следующий и окончательный аргументы. Здесь также нужно внимательно следить за тем, чтобы не передать меньший массив, чем количество элементов _count_ в размере, так как это приведет к переполнению границ массива. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Передача аргументов функции API C

**Excel4** и **Excel12** принимают списки аргументов переменной длины после _count_, которые интерпретируются как указатели на значения **XLOPER** и **XLOPER12** соответственно. **Excel4v** и **Excel12v** принимают один аргумент после _count_, который является указателем на массив указателей на значения **XLOPER** в случае **Excel4v**, а также на значения **XLOPER12** в случае **Excel12v**.
  
Формы массива **Excel4v** и **Excel12v** позволяют четко прописать в коде вызов API C, когда число аргументов меняется. В примере ниже показана функция, которая принимает массив чисел переменного раздела и использует функции листа Excel через API C, чтобы вычислить сумму, среднее, минимальное и максимальное. 
  
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

Если в предыдущем коде заменить ссылки на значения **XLOPER12** и **Excel12v**, указав **XLOPER** и **Excel4v** соответственно, функция будет работать во всех версиях Excel. Эта операция функций Excel **SUM**, **AVERAGE**, **MIN** и **MAX** достаточно проста, ее код было бы эффективнее написать на C, чтобы избежать чрезмерных затрат на подготовку аргументов и вызовы в Excel. Однако многие функции Excel более сложные, поэтому такой подход полезен в некоторых случаях. 
  
В статье о [xlfRegister](xlfregister-form-1.md) приведен другой пример работы с **Excel4v** и **Excel12v**. При регистрации функции листа XLL можно указать описательную строку для каждого аргумента, который используется в диалоговом окне **Вставить функцию**. Число всех аргументов, переданных в **xlfRegister**, зависит от числа аргументов, которые принимает функция XLL, и меняется от функции к функции. 
  
Если вы всегда вызываете функцию или команду API C с одним и тем же числом аргументов, вам лучше обойтись без дополнительного шага создания массива указателей для этих аргументов. В таких случаях проще и понятнее использование **Excel4** и **Excel12**. Например, при регистрации функций и команд XLL нужно ввести полный путь и имя файла DLL или XLL. Можно получить имя файла в вызове **xlfGetName**, а затем передать его с вызовом в **xlFree**, как показано в приведенном ниже примере, посвященном **Excel4** и ** Excel12**.
  
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

На практике код функции **Excel12v_example** можно более эффективно написать путем создания одного аргумента **xltypeMulti** **XLOPER12** и вызова API C с использованием **Excel12**, как показано в примере ниже.
  
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
> В этом случае возвращаемое значение **Excel12** игнорируется. Вместо этого код проверяет, является ли возвращаемое значение **XLOPER12** **xltypeNum**, чтобы определить, выполнен ли вызов. 
  
## <a name="xlcallver"></a>XLCallVer

Помимо обратных вызовов **Excel4**, **Excel4v**, **Excel12** и **Excel12v**, Excel экспортирует функцию **XLCallVer**, которая возвращает версию API C, выполняемого в настоящий момент.
  
Прототип функции выглядит следующим образом:
  
 `int pascal XLCallVer(void);`
  
Эту потокобезопасную функцию можно вызвать из любой команды или функции XLL.
  
В версиях Excel, начиная с Excel 97 и заканчивая Excel 2003, **XLCallVer** возвращает 1280 = 0x0500 шестн. = 5 x 256, что означает Excel версии 5. Начиная с Excel 2007, функция возвращает 3072 = 0x0c00 шестн. = 12 x 256, что означает версию 12.
  
Хотя ее можно использовать для определения доступности нового API C во время выполнения, иногда лучше определить текущую версию Excel с помощью `Excel4(xlfGetWorkspace, &version, 1, &arg)`, где `arg` является **XLOPER** с заданным числовым значением 2. Функция возвращает строку **XLOPER**, версию, которую можно привести к целому числу. Причина, по которой лучше полагаться на версию Excel, а не версию API C, заключается в том, что есть различия между Excel 2000, Excel 2002 и Excel 2003, которые вашей надстройке может понадобиться определять. Например, изменения точности некоторых статистических функций.
  
## <a name="see-also"></a>Дополнительные ресурсы

- [Создание XLL-файлов](creating-xlls.md)  
- [Доступ к коду XLL в Excel](accessing-xll-code-in-excel.md)  
- [Справочник по функциям API SDK XLL для Excel](excel-xll-sdk-api-function-reference.md)  
- [Функции обратного вызова API C: Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)  
- [Разработка XLL-файлов для Excel](developing-excel-xlls.md)

