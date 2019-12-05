---
title: Совместимость 32- и 64-разрядных версий Office
ms.date: 12/03/2019
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Узнайте о совместимости 32- и 64-разрядных версий Office.
localization_priority: Priority
ms.openlocfilehash: a0accc9c4b0198ab18b999353762a016d52f6b39
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819255"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Совместимость 32- и 64-разрядных версий Office

Узнайте о совместимости 32- и 64-разрядных версий Office.
  
Доступны 32-разрядные и 64-разрядные версии приложений Office. 
  
64-разрядные версии Office позволяют перемещать более крупные объемы данных и обеспечивают дополнительные возможности (например, при работе с большими числами в Microsoft Excel 2010). Если создаете 32-разрядный код, вы можете использовать 64-разрядную версию Office, не внося какие-либо изменения. Если же вы создаете 64-разрядный код, в коде должны использоваться определенные ключевые слова и константы условной компиляции для обратной совместимости кода с более ранней версией Office, а при смешении 32- и 64-разрядного должен выполняться правильный код.
  
Visual Basic для приложений 7.0 (VBA 7) выпущен в виде 64-разрядных версий для Office и работает как с 32-, так и с 64-разрядными приложениями. Изменения, приведенные в этой статье, применимы только к 64-разрядным версиям Office. 32-разрядные версии Microsoft Office позволяют использовать решения, встроенные в предыдущие версии Office, без дальнейших изменений.
  
> [!NOTE]
> По умолчанию при установке 64-разрядной версии Office также устанавливается 32-разрядная версия. Во время установки выберите непосредственно 64-разрядную версию Microsoft Office. 
  
Для работы с 64-разрядной версией в VBA 7 необходимо обновить существующие операторы Windows API (операторы **Declare**). Кроме того, необходимо обновить адресные указатели и отобразить дескрипторы окон в пользовательских типах, которые используются этими операторами. Эти вопросы, а также проблемы совместимости между 32-разрядной и 64-разрядной версиями и предлагаемые решения обсуждаются более подробно далее. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Сравнение 32- и 64-разрядных систем
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Приложения, созданные с использованием 64-разрядных версий Office, могут ссылаться на адресные пространства большего объема, чем приложения, созданные в 32-разрядных версиях. Это значит, что вы можете использовать для данных больший объем физической памяти, чем раньше, и в результате снизить потребление ресурсов на перемещение данных в физическую память и из нее.
  
Помимо ссылок на определенные места (известных как указатели) в физической памяти, вы также можете использовать адреса для обращения к идентификаторам окна отображения (известным как дескрипторы). Размер (в байтах) указателя или дескриптора зависит от того, какая система используется (32- или 64-разрядная). 
  
Чтобы запустить существующие решения вместе с 64-разрядными версиями Office, учитывайте следующее:
  
- Собственные 64-разрядные процессы в Office не могут загружать 32-разрядные двоичные файлы. Это происходит при использовании существующих элементов Microsoft ActiveX и надстроек.
    
- Ранее в VBA не было типа данных указателя, поэтому для хранения указателей и дескрипторов приходилось использовать 32-разрядные переменные. Теперь при использовании операторов **Declare** эти переменные усекают 64-разрядные значения, возвращаемые при вызовах API. 
    
## <a name="vba-7-code-base"></a>База кода VBA 7
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 заменяет базу кода VBA в Office 2007 и более ранних версиях. VBA 7 доступен в 32- и 64-разрядных версиях Office. Он предоставляет две константы условной компиляции: 
  
- **VBA7** помогает обеспечить обратную совместимость вашего кода, проверяя, какую версию VBA использует ваше приложение — VBA 7 или более раннюю. 
    
- **Win64** проверяет разрядность кода (32- или 64-разрядный код). 
    
За некоторыми исключениями макросы, которые работают в документе в 32-разрядной версии приложения, также будут работать в 64-разрядной версии.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Совместимость элементов ActiveX и надстроек COM
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Существующие 32-разрядные элементы ActiveX несовместимы с 64-разрядными версиями Office. Для элементов ActiveX и объектов COM:
  
- Если есть исходный код, создайте 64-разрядную версию самостоятельно.
- Если исходного кода нет, обратитесь к поставщику за обновленной версией.
    
Собственные 64-разрядные процессы в Office не могут загружать 32-разрядные двоичные файлы. Сюда входят общие элементы управления **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) и элементы управления **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Эти элементы управления были установлены 32-разрядными версиями Office, выпущенными до Office 2010. При переносе кода в 64-разрядные версии Office вам потребуется найти альтернативные варианты для существующих решений VBA, использующих эти элементы управления. 
  
## <a name="api-compatibility"></a>Совместимость API
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

Сочетая VBA и библиотеки типов, вы получаете множество функций для создания приложений Office. Однако иногда бывает необходимо взаимодействовать с операционной системой компьютера и другими компонентами напрямую (например, при управлении памятью или процессами, при работе с элементами пользовательского интерфейса, такими как окна и элементы управления, или при внесении изменений в реестр Windows). В этих ситуациях лучше всего использовать одну из внешних функций, встроенных в DLL-файлы. Это можно сделать в VBA, вызвав API с помощью операторов **Declare**. 
  
> [!NOTE]
> Корпорация Майкрософт предоставляет файл Win32API.txt, содержащий 1500 операторов Declare, и инструмент для копирования требуемого оператора **Declare** в ваш код. Однако эти операторы предназначены для 32-разрядных систем и должны быть преобразованы в 64-разрядные. Это можно сделать, используя информацию, приведенную далее в этой статье. Существующие операторы **Declare** не будут компилироваться в 64-разрядной версии VBA до тех пор, пока они не будут помечены с помощью атрибута **PtrSafe** как безопасные для 64-разрядных систем. Вы можете найти примеры этого типа конверсии на веб-сайте Яна Карела Питерса, являющегося MVP по продуктам Excel, по адресу [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp). [Руководство пользователя для инспектора совместимости кода Office](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) — полезный инструмент для проверки синтаксиса API оператора **Declare** на наличие атрибута **PtrSafe**, если это необходимо, и соответствующего возвращаемого типа. 
  
Операторы **Declare** похожи на один из приведенных ниже примеров в зависимости от того, вызывается ли подпрограмма (без возвращаемого значения) или функция (с возвращаемым значением). 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

Функция **SubName** или **FunctionName** заменяется фактическим именем процедуры в файле DLL и представляет собой имя, которое используется при вызове этой процедуры из кода VBA. Для имени процедуры можно также указать аргумент **AliasName**. Имя DLL-файла, содержащего вызываемую процедуру, следует за ключевым словом **Lib**. И, наконец, список аргументов содержит параметры и типы данных, которые должны быть переданы в процедуру. 
  
Приведенный ниже оператор **Declare** открывает *подраздел* реестра Windows и заменяет его значение. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

Запись Windows.h (дескриптор окна) для функции **RegOpenKeyA** выглядит следующим образом: 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

В Visual C и Microsoft Visual C++ предыдущий пример правильно компилируется как для 32-разрядных, так и для 64-разрядных версий. Это объясняется тем, что HKEY определен как указатель, размер которого показывает размер памяти платформы, на которой компилируется код.
  
В предыдущих версиях VBA не было определенного типа данных указателя, поэтому использовался тип **Long**. А поскольку тип данных **Long** всегда является 32-разрядным, код прерывается при работе в системе с 64-разрядной памятью, так как 32-разрядные данные могут быть усечены или перезаписаны поверх других адресов памяти. Любая из этих ситуаций может привести к непредсказуемому поведению или сбою системы. 
  
Для решения этой проблемы VBA содержит истинный тип данных *указателя*: **LongPtr**. Новый тип данных позволяет написать исходный оператор **Declare** правильно: 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Этот тип данных и новый атрибут **PtrSafe** позволяют использовать этот оператор **Declare** как в 32-разрядных, так и в 64-разрядных системах. Атрибут **PtrSafe** указывает компилятору VBA, что оператор **Declare** предусмотрен для 64-разрядной версии Office. При использовании оператора **Declare** в 64-разрядной системе без этого атрибута возникнет ошибка компиляции. Атрибут **PtrSafe** необязателен в 32-разрядной версии Office. Это позволяет существующим операторам **Declare** работать так, как и обычно. 
  
В приведенной ниже таблице описаны новые квалификатор и тип данных, а также другой тип данных, два оператора преобразования и три функции.
  
|Тип|Item|Описание|
|:-----|:-----|:-----|
|Квалификатор  <br/> |**PtrSafe** <br/> |Указывает, что оператор **Declare** совместим с 64-разрядными версиями. Этот атрибут обязателен в 64-разрядных системах.<br/> |
|Тип данных  <br/> |**LongPtr** <br/> |Переменный тип данных, равный 4 байтам в 32-разрядных версиях и 8 байтам в 64-разрядных версиях Microsoft Office. Это рекомендуемый способ объявления указателя или дескриптора в новом, а также устаревшем коде, который должен работать в 64-разрядной версии Office. Он поддерживается только в 32- и 64-разрядной среде выполнения VBA 7. Обратите внимание, что вы можете назначать ему числовые значения, но не числовые типы.  <br/> |
|Тип данных  <br/> |**LongLong** <br/> |Это 8-байтовый тип данных, который доступен только в 64-разрядных версиях Microsoft Office. Вы можете назначать числовые значения, но не числовые типы (чтобы избежать усечения).  <br/> |
|Оператор преобразования  <br/> |**CLngPtr** <br/> |Преобразует простое выражение в тип данных **LongPtr**.  <br/> |
|Оператор преобразования  <br/> |**CLngLng** <br/> |Преобразует простое выражение в тип данных **LongLong**.  <br/> |
|Функция  <br/> |**VarPtr** <br/> |Преобразователь переменной. Возвращает тип данных **LongPtr** в 64-разрядных версиях и тип данных **Long** в 32-разрядных версиях (4 байта).<br/> |
|Функция  <br/> |**ObjPtr** <br/> |Преобразователь объекта. Возвращает тип данных **LongPtr** в 64-разрядных версиях и тип данных **Long** в 32-разрядных версиях (4 байта).<br/> |
|Функция  <br/> |**StrPtr** <br/> |Преобразователь строки. Возвращает тип данных **LongPtr** в 64-разрядных версиях и тип данных **Long** в 32-разрядных версиях (4 байта).<br/> |
   
В приведенном ниже примере показано, как использовать некоторые из этих элементов в операторе **Declare**. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Обратите внимание, что операторы **Declare** без атрибута **PtrSafe** не совместимы с 64-разрядной версией Office. 
  
Существует две константы условной компиляции: **VBA7** и **Win64**. Чтобы предотвратить использование 64-разрядного кода в более ранней версии Office и тем самым обеспечить обратную совместимость с предыдущими версиями Microsoft Office, используйте константу **VBA7** (наиболее распространенный случай). Для кода с отличающимися друг от друга 32- и 64-разрядными версиями (например, для вызова математического API, который применяет тип данных **LongLong** в 64-разрядной версии и тип данных **Long** в 32-разрядной версии) используйте константу **Win64**. В следующем коде показан пример использования этих двух констант. 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

Подводя итог, если вы пишете 64-разрядный код и планируете использовать его в предыдущих версиях Office, рекомендуется использовать константу условной компиляции **VBA7**. Но если вы пишете в Office 32-разрядный код, он будет работать так же, как и в предыдущих версиях Office (без использования константы компиляции). Чтобы гарантировать использование 32-разрядных операторов для 32-разрядных версий и 64-разрядных операторов для 64-разрядных версий, лучше всего применять константу условной компиляции **Win64**. 
  
## <a name="using-conditional-compilation-attributes"></a>Использование атрибутов условной компиляции
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

В следующем примере показан требующий обновления код на языке VBA, написанный для 32-разрядных версий. В устаревшем коде обратите внимание на типы данных, которые обновлены для использования ** LongPtr **, так как ссылаются на дескрипторы или указатели. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Код на языке VBA, написанный для 32-разрядных версий
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Код на языке VBA, написанный для 64-разрядных версий
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a>

## <a name="frequently-asked-questions"></a>Вопросы и ответы

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>В каком случае мне следует использовать 64-разрядную версию Office?
  
Это зависит в большей степени от того, какое ведущее приложение (Excel, Word и т. д.) вы используете. Например, Excel в 64-разрядной версии Microsoft Office может обрабатывать листы большего размера.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>Могу ли я установить параллельно 64- и 32-разрядную версии Office?
  
Нет.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>В каком случае необходимо преобразовывать параметры типа Long в тип LongPtr?
  
Вам необходимо заглянуть в документацию по Windows API на сайте Microsoft Developers Network и найти функцию, которую вы хотите вызвать. Дескрипторы и указатели должны быть преобразованы в **LongPtr**. Например, в документации для функции [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) есть такая сигнатура: 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Ниже приведено определение параметров.
  
|Параметр|Описание|
|:-----|:-----|
|hKey [in]  <br/> |*Дескриптор* для открытого раздела реестра.  <br/> |
|lpSubKey [in, необязательный]  <br/> |Имя открытого подраздела реестра.  <br/> |
|ulOptions  <br/> |Этот параметр зарезервирован и должен равняться нулю.  <br/> |
|samDesired [in]  <br/> |Маска, указывающая желаемые права для доступа к разделу.  <br/> |
|phkResult [out]  <br/> |*Указатель* на переменную, которая получает дескриптор для открытого раздела.  <br/> |
   
В [Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support) оператор **Declare** определен следующим образом: 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>Нужно ли мне преобразовывать указатели и дескрипторы в структурах?
  
Да. См. тип **MSG** в Win32API_PtrSafe.txt: 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>В каких случая необходимо использовать функции strptr, varpt и objptr?
  
Эти функции необходимо использовать для извлечения указателей на строки, переменные и объекты соответственно. В 64-разрядной версии Office эти функции будут возвращать 64-разрядный тип данных **LongPtr**, который может быть передан в операторы **Declare**. Использование этих функций осталось таким же, как в предыдущих версиях VBA. Разница лишь в том, что теперь они возвращают тип данных **LongPtr**.
  
## <a name="see-also"></a>См. также
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Структура оператора Declare](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))
