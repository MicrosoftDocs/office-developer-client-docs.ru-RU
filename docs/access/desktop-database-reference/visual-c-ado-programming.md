---
title: Программирование для ADO на Visual C++
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302774"
---
# <a name="visual-c-ado-programming"></a>Программирование для ADO на Visual C++

**Область применения**: Access 2013, Office 2013

The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic. Хотя предполагаемая аудитория — все пользователи, программисты ADO используют различные языки, такие **\#** как Visual Basic, Visual C++ (с директивой импорта и без нее) и Visual J++ (с пакетом класса ADO/WFC).

Чтобы учесть такое разнообразие, синтаксис ADO для [Visual C++](using-ado-with-microsoft-visual-c.md) предоставляет синтаксис для языка Visual C++ со ссылками на общие описания функций, параметров, исключительных поведений и т. д. в справочнике по API.

ADO реализуется с помощью интерфейсов COM (объектной модели компонентов). Однако программистам проще работать с COM на определенных языках программирования, чем с другими. Например, почти все сведения об использовании COM обрабатываются неявно для Visual Basic программистов, тогда как программисты Visual C++ должны сами обращаться к этим сведениям.

В следующих разделах приводится краткое руководство для программистов C и C++, использующих ADO и **\# директиву импорта.** В ней основное внимание уделяется типам данных, характерным для COM (**Variant,** **BSTR** и **SafeArray),** а также обработке ошибок \_ (ошибка \_ com).

## <a name="using-the-import-compiler-directive"></a>Использование \# директивы компилятор импорта

Директива **\# компиляторов** Импорта Visual C++ упрощает работу с методами и свойствами ADO. Директива принимает имя файла, содержащего библиотеку типов, например ADO DLL (Msado15.dll), и создает файлы заголовок, содержащие объявления typedef, интеллектуальные указатели для интерфейсов и нумерированные константы. Каждый интерфейс инкапсулируется или оболочка в класс.

Для каждой операции в классе (то есть вызова метода или свойства) имеется объявление для прямого вызова операции (то есть "необработанные" формы операции) и объявление для вызова необработанных операций и вызова ошибки COM, если операция не удается выполнить успешно. Если операция является свойством, обычно существует директива компиляторов, которая создает альтернативный синтаксис для операции с синтаксис, например Visual Basic.

Операции, которые получают значение свойства, имеют имена формы, **Get***Property*. Операции, которые устанавливают значение свойства, имеют имена формы, **Put***Property*. Операции, которые устанавливают значение свойства с указателем на объект ADO, имеют имена формы, **PutRef***Property*.

Вы можете получить или настроить свойство с помощью вызовов этих форм:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Использование директив свойств

Директива **\_ \_ компиляторов declspec(property...)** — это расширение языка C корпорации Майкрософт, которое объявляет функцию, используемую в качестве свойства для использования альтернативного синтаксиса. В результате вы можете установить или получить значения свойства так же, как Visual Basic. Например, можно настроить и получить свойство таким образом:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Обратите внимание, что вам не нужно кодировать:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Компилятор создает соответствующий вызов **Get***-*, **Put**-, or **PutRef***Property* в зависимости от объявленного альтернативного синтаксиса и того, считывало ли свойство или оно было записано.

Директива **\_ \_ компиляторов declspec(property...)** может объявлять только **get,** **put,** or **get** and **put** alternative syntax for a function. Операции только для чтения имеют только объявление **получения;** Операции только для записи имеют только объявление **put;** операции как для чтения, так и для записи имеют объявления **get** и **put.**

С этой директивой можно сделать только два объявления; Однако каждое свойство может иметь три функции свойств: **Get***Property*, **Put***Property* и **PutRef***Property*. В этом случае альтернативный синтаксис имеется только в двух формах свойства.

Например, свойство **ActiveConnection** объекта **Command** объявляется с альтернативным синтаксисом для **Get***ActiveConnection* и **PutRef***ActiveConnection.* Синтаксис **PutRef**— хороший выбор, так как на практике в это свойство обычно нужно поместить открытый объект **Connection** (то есть указатель объекта **Connection).** С другой стороны, объект **Recordset** имеет операции **Get-,** **Put**-и **PutRef***ActiveConnection,* но без альтернативного синтаксиса.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Коллекции, метод GetItem и свойство Item

ADO определяет несколько коллекций, в том числе **Fields,** **Parameters,** **Properties** и **Errors.** В Visual C++ метод **GetItem(index)** возвращает член коллекции. *Индекс* — **это variant,** значение которого — это либо числовой индекс члена коллекции, либо строка, содержащая имя члена.

Директива компиляторов **\_ \_ declspec(property...)** объявляет свойство **Item** в качестве альтернативного синтаксиса для основного метода **GetItem()** каждой коллекции. Альтернативный синтаксис использует квадратные скобки и выглядит аналогично ссылке на массив. Как правило, две формы выглядят следующим образом:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Например, назначьте значение полю объекта **Recordset** с именем ***rs,*** производного от таблицы авторов базы **данных pubs.**  Используйте свойство **Item()** для  доступа к третьему  полю коллекции Полей объекта **Recordset** (коллекции индексются с нуля; предполагается, что третье поле называется ***au \_ fname).*** Затем вызовите **метод Value()** объекта **Field,** чтобы назначить строку.

Это может быть выражено Visual Basic следующими четырьмя способами (последние две формы уникальны для Visual Basic; другие языки не имеют эквивалентов):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

Эквивалент в Visual C++ для первых двух вышеперечисленной формы:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-or- (также показан альтернативный синтаксис для свойства **Value)**

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Типы данных, специфики для COM

Как правило, любой Visual Basic данных, который вы найдете в справочнике по ADO API, имеет эквивалент Visual C++. К ним относятся стандартные типы данных, такие как неподписаный символ для Visual Basic **Byte,** **short** for **Integer** и **long** for **Long.**  Посмотрите в индексах синтаксиса, чтобы узнать, что именно требуется для операнд данного метода или свойства.

Исключениями из этого правила являются типы данных, специфические для COM: **Variant,** **BSTR** и **SafeArray.**

### <a name="variant"></a>Variant

Variant **—** это структурированный тип данных, содержащий член значения и тип данных. Variant  может содержать широкий диапазон других типов данных, включая другой указатель Variant, BSTR, Boolean, IDispatch или IUnknown, валюту, дату и т. д. COM также предоставляет методы, которые делают преобразование одного типа данных в другой.

Класс **\_ variant \_ t** инкапсулирует тип данных **Variant** и управляет им.

Когда ссылка ADO API сообщает, что метод или операнд свойства принимает значение, обычно это означает, что значение передается в **\_ \_ варианте t**.

Это правило явным образом  действует, если в разделе "Параметры" в разделах справочника по ADO API говорится, что операнд является **вариантом.** Одним из исключений является, когда в документации явно говорится, что операнд принимает стандартный тип данных, например **Long** или **Byte,** или enumeration. Еще одно исключение — когда операнд принимает **строку.**

### <a name="bstr"></a>BSTR

**BSTR** (**B** asic **STR** ing) — это структурированный тип данных, содержащий строку символов и длину строки. COM предоставляет методы для выделения, управления и бесплатного **BSTR**.

Класс **\_ bstr \_ t** инкапсулирует тип данных **BSTR** и управляет им.

Если ссылка ADO API сообщает, что  метод или свойство принимает строку, это означает, что значение имеет форму **\_ bstr \_ t**.

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a>Классы \_ variant \_ t и \_ bstr \_ t casting

Часто нет необходимости явно кодировать вариант **\_ \_ t** или **\_ bstr \_ t** в аргументе для операции. Если класс **\_ variant \_ t** или **\_ bstr \_ t** имеет конструктор, соответствующий типу данных аргумента, компилятор создает соответствующий вариант **\_ \_ t** или **\_ bstr \_ t**.

Однако если аргумент неоднозначн, то есть тип данных аргумента соответствует более чем одному конструктору, необходимо привести аргумент с соответствующим типом данных, чтобы вызвать правильный конструктор.

Например, для метода **Recordset::Open** используется объявление:

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

Аргумент ActiveConnection принимает ссылку на вариант **\_ \_ t,** который можно закодировать как строку подключения или указатель на открытый **объект Connection.**

Правильный вариант **\_ \_ t** будет построен неявно, если передать строку, например "DSN=pubs;uid=sa;pwd=;", или указатель, например "(IDispatch \* ) pConn".

Или вы можете явно закодировать вариант, **\_ \_ не** содержащий указатель, например \_ "variant \_ t((IDispatch \* ) pConn, true)". При этом (IDispatch) неоднозначность устраняется с помощью другого конструктора, который принимает указатель на интерфейс \* IUnknown.

Хотя этот факт редко упоминается, важно, чтобы ADO был интерфейсом IDispatch. Каждый раз, когда указатель на объект ADO должен передаваться в качестве **варианта,** этот указатель должен быть приведя в качестве указателя к интерфейсу IDispatch.

Последний случай явно кодирует второй boolean аргумент конструктора с необязательным значением по умолчанию, значением true. Этот аргумент вызывает метод **AddRef**() **конструктора Variant,** который автоматически вызывает метод variant **\_ \_ t::Release**() при вызове метода ADO или свойства.

### <a name="safearray"></a>SafeArray

**SafeArray** — это структурированный тип данных, содержащий массив других типов данных. **SafeArray** называется  безопасным, так как он содержит сведения об границах каждого измерения массива и ограничивает доступ к элементам массива в этих границах.

Если ссылка ADO API сообщает, что метод или свойство принимает или возвращает массив, это означает, что метод или свойство принимает или возвращает **SafeArray,** а не массив C/C++.

Например, второй параметр метода **OpenSchema** объекта **Connection** требует массив значений **Variant.** Эти **значения Variant** должны быть переданы в качестве элементов **SafeArray,** и что **SafeArray** должен быть установлен в качестве значения другого **варианта**. Это другой **вариант,** который передается в качестве второго аргумента **OpenSchema.**

В качестве дополнительных примеров первым аргументом метода **Find** является **Variant,** значением которого является одномерное **значение SafeArray;** каждый необязательный первый и второй аргумент **AddNew** является одномерным **SafeArray;** и возвращаемая величина метода **GetRows** — **это Variant,** значение которого является двумерным **safeArray.**

## <a name="missing-and-default-parameters"></a>Отсутствующие параметры и параметры по умолчанию

Visual Basic параметры в методах. Например, метод **Recordset** object **Open** имеет пять параметров, но вы можете пропустить промежуточные параметры и не использовать последние параметры. BSTR или **Variant** **по** умолчанию будут заменены в зависимости от типа данных отсутствующих операндов.

В C/C++ должны быть указаны все операнды. Если необходимо указать отсутствующий параметр, тип данных которого является строкой, укажите **\_ строку bstr \_ t,** содержащую нулевую строку. Если необходимо указать отсутствующий параметр, тип данных которого — **Variant,** укажите вариант **\_ \_ t** со значением DISP E PARAMNOTFOUND и типом \_ \_ ошибки \_ VT. Кроме того, укажите эквивалентную константу **\_ variant \_ t,** **vtMissing,** которая предоставляется директивой **\# импорта.**

Три метода являются исключениями из обычного использования **vtMissing.** Это методы **Execute** объектов **Connection** и **Command** и **метод NextRecordset** объекта **Recordset.** Их подписи:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Параметры *RecordsAffected* и *Parameters*— это указатели на **variant.** *Параметры* — это входной параметр, который указывает адрес **Variant,** содержащий один параметр или массив параметров, который будет изменять команду, которая выполняется. *RecordsAffected* — это выходной параметр, который указывает адрес **variant,** где возвращается количество строк, затронутых методом.

В **методе Execute** объекта **Command** указать, что  параметры не заданы, задав для параметров значение \& vtMissing (рекомендуется) или нулевой указатель (то есть **NULL** или ноль (0)). Если *параметры заданы* как указатель null, метод внутренне заменяет эквивалент **vtMissing,** а затем завершает операцию.

Во всех методах следует указать, что количество затронутых записей не должно возвращаться путем установки параметра *RecordsAffected* для указателя null. В этом случае null-указатель — это не столько отсутствующий параметр, сколько указание на то, что метод должен отменить количество затронутых записей.

Таким образом, для этих трех методов допустимо закодировать что-то, например:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Обработка ошибок

В COM большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция. Директива **\# импорта** создает код-оболочку для каждого "необработанных" метода или свойства и проверяет возвращенный HRESULT. Если HRESULT указывает на сбой, код-оболочка вызывает ошибку COM, вызывая \_ com \_ issue errorex() с кодом возврата HRESULT в качестве \_ аргумента. Объекты ошибки COM могут быть перехвачены в **блоке try** - **catch.** (Для повышения эффективности перехватить ссылку на объект **\_ ошибки \_ com.)**

Помните, что это ошибки ADO: они являются результатом сбоя операции ADO. Ошибки, возвращенные поставщиком, отображаются как **объекты Error** в коллекции **Errors** объекта **Connection.**

Директива **\# импорта** создает только процедуры обработки ошибок для методов и свойств, объявленных в DLL ADO. Тем не менее, вы можете воспользоваться этим же механизмом обработки ошибок, написав собственный макрос проверки ошибок или функцию. Примеры см. в разделе [,Visual C++ Extensions](visual-c-extensions-for-ado.md)или коде в следующих разделах.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Visual C++ equivalents of Visual Basic conventions

Ниже приводится сводка по нескольким соглашениям в документации ADO, закодирование в Visual Basic, а также их эквиваленты в Visual C++.

### <a name="declaring-an-ado-object"></a>Объявление объекта ADO

В Visual Basic объектной переменной ADO (в данном случае для объекта **Recordset)** объявляется следующим образом:

```vb 
 
Dim rst As ADODB.Recordset 
```

Предложение "ADODB. Recordset" — это progID объекта **Recordset,** как определено в реестре. Новый экземпляр объекта **Record** объявляется следующим образом:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-or-

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

В Visual C++ директива **\# импорта** создает объявления типа интеллектуального указателя для всех объектов ADO. Например, переменная, которая указывает на объект **\_ Recordset,** имеет тип **\_ RecordsetPtr** и объявляется следующим образом:

```cpp 
 
_RecordsetPtr rs; 
```

Переменная, которая указывает на новый экземпляр объекта **\_ Recordset,** объявляется следующим образом:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-or-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-or-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

После того как будет вызван **метод CreateInstance,** переменную можно использовать следующим образом:

```cpp 
 
rs->Open(...); 
```

Обратите внимание, что в одном случае оператор "." используется так, как если бы переменная была экземпляром класса (rs). CreateInstance), а в другом случае оператор "- " используется, как если бы переменная была указателем на \> интерфейс (rs-Open). \>

Одну переменную можно использовать двумя способами, так как оператор "-" перегружен, чтобы позволить экземпляру класса вести себя как указатель \> на интерфейс. Частный член класса переменной экземпляра содержит указатель на интерфейс **\_ recordset;** оператор "-" возвращает этот указатель, а возвращенный указатель возвращает доступ к членам объекта \> **\_ Recordset.**

### <a name="coding-a-missing-parameter"></a>Написание кода отсутствующих параметров

#### <a name="string"></a>String

Если вам нужно закодировать отсутствующий операнд строки в Visual Basic, просто опустить операнд.  Операнд необходимо указать в Visual C++. Код **\_ bstr \_ t с** пустой строкой в качестве значения.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

Если вам нужно закодировать отсутствующий операнд **Variant** в Visual Basic, просто опустить операнд. Необходимо указать все операнды в Visual C++. Задайте код для **\_ \_** отсутствующих параметров **Variant,** для варианта не заданы специальные значения DISP \_ E \_ PARAMNOTFOUND и type, VT \_ ERROR. Кроме того, укажите **vtMissing**— эквивалентную предопределенную константу, предоставленную директивой **\# импорта.**

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-или использовать —

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Объявление варианта

В Visual Basic **variant** объявляется с помощью заявления **Dim** следующим образом:

```vb 
 
Dim VariableName As Variant 
```

В Visual C++ объявите переменную как тип **\_ variant \_ t**. Ниже показано несколько **\_ схемных \_ вариантов t** объявлений.

> [!NOTE]
> Эти объявления просто дают приблизительное представление о том, что бы вы напрограмме в собственной программе. Дополнительные сведения см. в примерах ниже и документации по Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Использование массивов вариантов

В Visual Basic массивы **Variant** можно закодировать с помощью заявления **Dim** или использовать функцию **Array,** как показано в следующем примере кода:

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

В следующем примере Visual C++ демонстрируется использование **SafeArray,** используемой с **\_ вариантом \_ t**.

> [!NOTE]
> Следующие примечания соответствуют закомментным разделам в примере кода.

1. Опять же, в рамках функции TESTHR() определена возможность использования существующего механизма обработки ошибок.

2. Вам нужен только одномерный массив, поэтому вместо объявления **SAFEARRAYBOUND** общего назначения и функции **SafeArrayCreate** можно использовать **SafeArrayCreate.** Вот как будет выглядеть этот код с помощью **SafeArrayCreate:**
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. Схема, обнаруженная по нумероватой константы **adSchemaColumns,** связана с четырьмя столбцами ограничений: TABLE \_ CATALOG, TABLE \_ SCHEMA, TABLE \_ NAME и COLUMN \_ NAME. Поэтому создается массив значений **Variant** с четырьмя элементами. Затем указывается значение ограничения, соответствующее третьему столбце , TABLE \_ NAME. **Возвращаемая группа** записей состоит из нескольких столбцов, подмножество которых является столбцом ограничения. Значения столбцов ограничений для каждой возвращаемой строки должны быть одинаковыми с соответствующими значениями ограничений.

4. Те, кто знаком **с SafeArrays,** могут быть удивлены тому, что **SafeArrayDestroy**() не вызван перед выходом. Вызов **SafeArrayDestroy**() в данном случае приведет к исключению во время запуска. Причина заключается в том, что деструктор для vtCriteria будет вызывать **VariantClear**(), когда вариант **\_ \_ t** выходит за пределы области, что освободит **SafeArray**. Вызов **SafeArrayDestroy** без очистки варианта **\_ \_ t** вручную приведет к тому, что деструктор попытается очистить недопустимый **указатель SafeArray.** Если **бы был вызван SafeArrayDestroy,** код выглядел бы так:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Однако гораздо проще позволить варианту **\_ \_** не управлять **SafeArray.**


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a>Использование свойства Get/Put/PutRef

В Visual Basic имя свойства не квалифицироваться по извлечению, назначению или назначению ссылки.

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

В этом примере Visual C++ демонстрируется / **свойство Get Put** /* *PutRef***Property.*

> [!NOTE]
> Следующие примечания соответствуют закомментным разделам в примере кода.

1. В этом примере используются две формы отсутствующих аргументов строки: явная константа, **strMissing** и строка, которую компилятор будет использовать для создания временной **\_ строки \_ t,** которая будет существовать для области метода **Open.**

2. Нет необходимости привести операнд \> rs-PutRefActiveConnection(cn) к (IDispatch), так как тип операнда уже \* есть (IDispatch). \*
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a>Использование GetItem(x) и Item \[ x\]

В Visual Basic примере демонстрируется стандартный и альтернативный синтаксис **для элемента**().

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

В этом примере Visual C++ **демонстрируется item.**

> [!NOTE]
> Следующее примечание соответствует закомментным разделам в примере кода.

1. При доступе к коллекции с помощью **Item** индекс **2** должен быть приводиться к длинному, чтобы был вызван соответствующий конструктор. 
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Casting ADO object pointers with (IDispatch) \*

В следующем примере Visual C++ демонстрируется использование (IDispatch) для \* придаия указателям объектов ADO.

> [!NOTE]
> Следующие примечания соответствуют закомментным разделам в примере кода.

1. Укажите открытый **объект Connection** в явно кодовом **варианте.** Привязим его с помощью (IDispatch), чтобы был вызван правильный \* конструктор. Кроме того, явно установите для второго параметра **\_ variant \_ t** значение по умолчанию **true,** поэтому количество ссылок на объект будет правильным после окончания операции **Recordset::Open.**

2. Выражение ( bstr t) не является оператором cast, а оператором \_ variant \_ **\_ \_ t,** который извлекает **\_ строку bstr \_ t** из **варианта,** возвращаемого **значением**. Выражение (char) не является оператором cast, а \* **\_ оператором bstr \_ t,** который извлекает указатель на инкапсулированную строку в **\_ объекте bstr \_ t.** В этом разделе кода демонстрируются некоторые полезные поведения операторов **\_ variant \_ t** и **\_ bstr \_ t.**
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

