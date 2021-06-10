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

Ссылка ADO API описывает функциональность интерфейса программирования приложений ADO (API) с помощью синтаксиса, аналогичного Microsoft Visual Basic. Хотя целевой аудиторией являются все пользователи, программисты ADO используют различные языки, такие **\#** как Visual Basic, Visual C++ (с директивой импорта и без нее) и Visual J++ (с пакетом классов ADO/WFC).

Чтобы обеспечить такое разнообразие, индексы синтаксиса ADO для visual [C++](using-ado-with-microsoft-visual-c.md) предоставляют синтаксис visual C++ с языковым синтаксисом со ссылками на общие описания функциональных возможностей, параметров, исключительных поведений и т. д. в справке API.

ADO реализуется с интерфейсами COM (Component Object Model). Однако для программистов проще работать с COM на определенных языках программирования, чем с другими. Например, почти все сведения об использовании COM обрабатываются неявно для Visual Basic, в то время как программисты Visual C++ должны сами ходить к этим сведениям.

В следующих разделах обобщены сведения о программистах C и C++ с помощью ADO и **\# директивы импорта.** Основное внимание уделяется типам данных, определенным com **(Variant,** **BSTR** и **SafeArray),** а также обработке ошибок \_ (ошибка \_ com).

## <a name="using-the-import-compiler-directive"></a>Использование \# директивы компилятор импорта

Директива **\# по** импорту visual C++ упрощает работу с методами и свойствами ADO. Директива принимает имя файла, содержащего библиотеку типов, например ADO .dll (Msado15.dll), и создает файлы заголовки, содержащие декларации типа, интеллектуальные указатели для интерфейсов и переумежаемые константы. Каждый интерфейс инкапсулируется или завернут в класс.

Для каждой операции в классе (то есть вызова метода или свойства) имеется объявление о вызове операции напрямую (то есть "необработанные" формы операции), а также объявление об вызове необработанных операций и вызове ошибки com, если операция не выполняется успешно. Если операция является свойством, обычно существует директива компиляторов, которая создает альтернативный синтаксис для операции с синтаксисом, как Visual Basic.

Операции, которые получают значение свойства, имеют имена формы**Get***Property*. Операции, которые устанавливают значение свойства, имеют имена формы**Put***Property*. Операции, задав значение свойства с указателем на объект ADO, имеют имена формы**PutRef***Property*.

Вы можете получить или установить свойство с вызовами этих форм:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Использование директив свойств

Директива компиляторов **\_ \_ declspec(property...)** — это языковой расширение C для Microsoft, которое объявляет функцию, используемую в качестве свойства для альтернативного синтаксиса. В результате вы можете установить или получить значения свойства таким образом, как Visual Basic. Например, можно установить и получить свойство таким образом:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Обратите внимание, что вам не нужно кодировать:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Компилятор будет создавать соответствующий вызов **Get***-,* **Put**-или **PutRef***Property* на основе того, какой альтернативный синтаксис объявлен и читается ли свойство или написано.

Директива компилятор **\_ \_ declspec(property...)** может объявлять только **get,** **put**, or **get** and **put** alternative syntax for a function. Операции только для чтения имеют только **объявление получения;** Операции только для записи имеют только объявление **пут;** операции, которые являются одновременно чтением и написанием, имеют как **получать, так** **и ставить** объявления.

С этой директивой можно сделать только две декларации; однако каждое свойство может иметь три свойства: **Get***Property*, **Put***Property* и **PutRef***Property*. В этом случае альтернативный синтаксис имеется только в двух формах свойства.

Например, свойство **Объекта** **Команды ActiveConnection** объявляется с альтернативным синтаксисом для **Get***ActiveConnection* и **PutRef***ActiveConnection.* Синтаксис **PutRef**— это хороший выбор, так как на  практике обычно необходимо поместить  в это свойство открытый объект Connection (то есть указатель объекта Подключения). С другой стороны, объект **Recordset** имеет операции **Get-,** **Put**-и **PutRef***ActiveConnection,* но нет альтернативного синтаксиса.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Коллекции, метод GetItem и свойство Item

ADO определяет несколько коллекций, в том числе **Fields,** **Parameters,** **Properties** и **Errors.** В Visual C++метод **GetItem ***(index)***** возвращает участника коллекции. *Index* — **это вариант,** значение которого — это либо числовой индекс участника в коллекции, либо строка, содержащая имя участника.

Директива компиляторов **\_ \_ declspec(property...)** объявляет свойство **Item** альтернативным синтаксисом для основного метода **GetItem()** каждой коллекции. Альтернативный синтаксис использует квадратные скобки и похож на ссылку массива. В общем, эти две формы выглядят следующим образом:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Например, назначьте значение для поля объекта **Recordset** с именем  ***rs,*** полученное из таблицы авторов базы **данных пабов.** Используйте свойство **Item()** для  доступа к третьему  полю коллекции полей объектов **Recordset** (коллекции индексироваться с нуля; предположим, что третье поле называется ***au \_ fname).*** Затем вызовите **метод Value()** на **объекте Field,** чтобы назначить значение строки.

Это может быть выражено Visual Basic в следующих четырех способах (последние две формы уникальны для Visual Basic, другие языки не имеют эквивалентов):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

Эквивалент visual C++ для первых двух форм выше:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-or- (также показан альтернативный синтаксис для свойства **Value)**

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Типы данных, специфические для COM

Как правило, любой тип Visual Basic, который вы найдете в ссылке ADO API, имеет эквивалент Visual C++. К ним относятся стандартные типы данных, такие как **неподписаный** шар для Visual Basic **byte,** краткое **для** **Integer** и **long** for **Long**. Посмотрите в индексах синтаксиса, чтобы точно узнать, что требуется для операндов данного метода или свойства.

Исключениями из этого правила являются типы данных, специфические для COM: **Variant,** **BSTR** и **SafeArray.**

### <a name="variant"></a>Variant

**Variant —** это структурированный тип данных, содержащий член значения и тип данных. Вариант **может** содержать широкий диапазон других типов данных, включая другой Вариант, BSTR, Boolean, указатель IDispatch или IUnknown, валюту, дату и т. д. COM также предоставляет методы, которые устроит преобразование одного типа данных в другой.

Вариант **\_ \_ t** class инкапсулирует и управляет типом **данных Variant.**

Когда ссылка ADO API говорит, что операнд метода или свойства принимает значение, это обычно означает, что значение передается в **\_ \_ варианте t**.

Это правило явно верно, когда в разделе **Параметры** в разделах ADO API Reference говорится, что operand является **вариантом**. Одним из исключений является то, что в документации явно говорится, что операнд принимает стандартный тип данных, например **Long** или **Byte,** или переуметив. Другим исключением является то, что операнд принимает **строку**.

### <a name="bstr"></a>BSTR

**BSTR** **(B** asic **STR** ing) — структурированный тип данных, содержащий строку символов и длину строки. COM предоставляет методы выделения, управления и **бесплатного BSTR**.

Класс **\_ bstr \_ t** инкапсулирует и управляет типом **данных BSTR.**

Когда ссылка ADO API говорит, что метод или свойство принимает значение **String,** это означает, что значение находится в виде **\_ bstr \_ t**.

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a>\_Литье вариант t и \_ \_ bstr t \_ классов

Часто не требуется явно кодировать вариант **\_ \_ t или** **\_ bstr \_ t** в аргументе для операции. Если в **\_ классе вариант \_ t** или **\_ bstr \_ t** есть конструктор, соответствующий типу данных аргумента, компилятор будет создавать соответствующий вариант **\_ \_ t** или **\_ bstr \_ t**.

Однако если аргумент неоднозначный, то есть тип данных аргумента соответствует более чем одному конструктору, необходимо ввести аргумент с соответствующим типом данных, чтобы вызвать правильного конструктора.

Например, объявление для метода **Recordset::Open:**

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

Аргумент ActiveConnection ссылается на вариант **\_ \_ t,** который можно кодировать как строку подключения или указатель на открытый объект **Подключения.**

Правильный вариант **\_ \_ t** будет построен неявно, если вы передаете строку, например "DSN=pubs;uid=sa;pwd=;", или указатель, например "(IDispatch) \* pConn".

Или вы можете явно кодировать вариант **\_ \_ t,** содержащий указатель, например \_ "variant \_ t((IDispatch) \* pConn, true)". В гипсе (IDispatch) устраняется двусмысленность с помощью другого конструктора, который принимает указатель на \* интерфейс IUnknown.

Важно, хотя и редко упоминалось, что ADO — это интерфейс IDispatch. Всякий раз, когда указатель на объект ADO должен быть передан в качестве **варианта,** этот указатель должен быть отлит в качестве указателя для интерфейса IDispatch.

Последний случай явно кодирует второй аргумент boolean конструктора с его необязательным значением по умолчанию true. В этом аргументе конструктор **Variant** вызывает метод **AddRef**(), который компенсирует автоматический вызов метода **\_ \_ вариантов t::Release**() при завершении вызова метода ADO или свойства.

### <a name="safearray"></a>SafeArray

**SafeArray** — это структурированный тип данных, содержащий массив других типов данных. **SafeArray** называется  безопасным, так как содержит сведения о границах каждого измерения массива и ограничивает доступ к элементам массива в этих границах.

Если в ссылке ADO API говорится, что метод или свойство принимает или возвращает массив, это означает, что метод или свойство принимает или возвращает массив **SafeArray,** а не массив C/C++.

Например, для второго параметра метода **OpenSchema объекта Подключения** требуется массив значений  **Variant.** Эти **значения Variant** должны быть переданы в качестве элементов **SafeArray,** и что **SafeArray** должен быть задат как значение другого **варианта**. Это то, что другой **вариант,** который передается в качестве второго аргумента **OpenSchema**.

В качестве дополнительных примеров первым аргументом метода **Find** является **вариант,** значение которого — одномерный **SafeArray;** каждый из необязательных первого и второго аргументов **AddNew** является одномерным **SafeArray;** и возвращаемая величина метода **GetRows** — это **вариант,** значение которого — двухмерный **SafeArray.**

## <a name="missing-and-default-parameters"></a>Отсутствующие и невыполнение параметров

Visual Basic позволяет пропускать параметры в методах. Например, метод Open  **объекта Recordset** имеет пять параметров, но можно пропустить промежуточные параметры и не использовать параметры trailing. BSTR **или** **Variant** по умолчанию будут заменены в зависимости от типа данных отсутствующих operand.

В C/C++все операнды должны быть указаны. Если необходимо указать отсутствующий параметр, тип данных которого — строка, укажите **\_ bstr \_ t,** содержащий строку null. Если необходимо указать отсутствующий параметр, тип данных которого является **Вариантом,** укажите вариант **\_ \_ t** со значением DISP \_ E \_ PARAMNOTFOUND и типом ошибки \_ VT. Кроме того, укажите эквивалентный вариант **\_ \_ t** **constant, vtMissing,** который поставляется директивой **\# импорта.**

Три метода являются исключениями из обычного использования **vtMissing.** Это методы **выполнения** объектов **Подключения** и **Команды,** а также метод **NextRecordset** объекта **Recordset.** Следующие подписи:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Параметры, *RecordsAffected* и *Parameters*, являются указателями на **вариант**. *Параметры* — это параметр ввода, который  указывает адрес варианта, содержащего один параметр или массив параметров, который изменит выполненную команду. *RecordsAffected* — это выходной параметр, который указывает адрес **варианта,** где возвращается количество строк, затронутых методом.

В методе **Командный** объект **Выполнить** указать, что  параметры не заданы, задав параметры либо к vtMissing (что рекомендуется), либо к указателю null (т. е. NULL или zero \&  (0)). Если *параметры* заданы в указателе null, метод внутренне заменяет эквивалент **vtMissing,** а затем завершает операцию.

Во всех методах указать, что количество затронутых записей не следует возвращать, установив *RecordsAffected* в указатель null. В этом случае указатель null — это не столько отсутствующий параметр, сколько указание на то, что метод должен отменить количество затронутых записей.

Таким образом, для этих трех методов допустимо кодировать что-то, например:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Обработка ошибок

В com большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция. Директива **\# импорта** создает код оболочки вокруг каждого "необработанных" метода или свойства и проверяет возвращаемую HRESULT. Если HRESULT указывает на сбой, код оболочки вызывает ошибку COM, вызывая ошибку com issue errorex() с кодом возврата \_ \_ HRESULT в качестве \_ аргумента. Объекты ошибки COM могут быть пойманы в **блоке try** - **catch.** (Для обеспечения эффективности ловите ссылку на объект **\_ ошибки \_ com.)**

Помните, что это ошибки ADO: они являются результатом сбоя операции ADO. Ошибки, возвращаемые поставщиком, отображаются как **объекты ошибки** в коллекции **Ошибки** **объекта** Подключения.

Директива **\# импорта** создает только процедуры обработки ошибок для методов и свойств, объявленных в ADO .dll. Тем не менее, вы можете воспользоваться этим же механизмом обработки ошибок, написав собственную функцию проверки ошибок макроса или inline. Примеры см. в разделе [Visual C++ Extensions](visual-c-extensions-for-ado.md)или код в следующих разделах.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Visual C++ эквиваленты Visual Basic конвенций

Ниже приводится сводка нескольких конвенций в документации ADO, закодирования в Visual Basic, а также их эквивалентов в Visual C++.

### <a name="declaring-an-ado-object"></a>Объявление объекта ADO

В Visual Basic объектной переменной ADO (в данном случае для объекта **Recordset)** объявляется следующим образом:

```vb 
 
Dim rst As ADODB.Recordset 
```

Пункт "ADODB. Recordset", является progID объекта **Recordset,** как определено в реестре. Новый экземпляр объекта **Record** объявляется следующим образом:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-or-

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

В Visual C++директива **\# импорта** создает интеллектуальные объявления типа указателей для всех объектов ADO. Например, переменная, которая указывает на объект **\_ Recordset,** имеет тип **\_ RecordsetPtr** и объявляется следующим образом:

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

После того как будет вызван метод **CreateInstance,** переменную можно использовать следующим образом:

```cpp 
 
rs->Open(...); 
```

Обратите внимание, что в одном случае оператор "." используется так, как если бы переменная была экземпляром класса (rs. CreateInstance), а в другом случае оператор "- " используется так, как если бы переменная была указателем на интерфейс \> (rs-Open). \>

Одна переменная может использоваться двумя способами, так как оператор "-" перегружен, чтобы позволить экземпляру класса вести себя как указатель \> на интерфейс. Частный член класса переменной экземпляра содержит указатель на интерфейс **\_ Recordset;** оператор "-" возвращает этот указатель, а возвращаемая указатель имеет доступ к участникам объекта \> **\_ Recordset.**

### <a name="coding-a-missing-parameter"></a>Кодирование отсутствующих параметров

#### <a name="string"></a>String

Если вам нужно кодировать отсутствующий операнд **String** в Visual Basic, вы просто опустить operand. Необходимо указать операнд в Visual C++. Код **\_ bstr \_ t** с пустой строкой в качестве значения.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

При необходимости кодировать недостающий операнд **Variant** в Visual Basic, вы просто опустить operand. Необходимо указать все операнды в Visual C++. Код отсутствует **параметр Variant** с вариантом **\_ \_ t,** заданным для специального значения, DISP E \_ \_ PARAMNOTFOUND и типа, VT \_ ERROR. Кроме того, укажите **vtMissing**, эквивалентную заранее определенной константе, предоставленной директивой **\# импорта.**

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-или использование —

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Объявление варианта

В Visual Basic **вариант** объявляется с заявлением **Dim** следующим образом:

```vb 
 
Dim VariableName As Variant 
```

В Visual C++объявите переменную как вариант **\_ \_ типа t**. Ниже показано несколько **\_ схемных \_** объявлений t вариантов.

> [!NOTE]
> Эти объявления просто дают приблизительное представление о том, что вы будете кодировать в собственной программе. Дополнительные сведения см. в примерах ниже и документации Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Использование массивов вариантов

В Visual Basic массивы **Вариантов** можно закодировать с помощью заявления **Dim** или использовать функцию **Array,** как показано в следующем коде примера:

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

В следующем примере Visual C++ показано использование **SafeArray,** используемой с **\_ вариантом \_ t**.

> [!NOTE]
> Следующие заметки соответствуют разделам с комментариями в примере кода.

1. В очередной раз установлена функция inline TESTHR() для использования существующего механизма обработки ошибок.

2. Вам нужен только одномерный массив, поэтому вы можете использовать **SafeArrayCreateVector** вместо общего объявления **SAFEARRAYBOUND** и **функции SafeArrayCreate.** Ниже приводится пример того, как будет выглядеть этот код с помощью **SafeArrayCreate:**
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. Схема, идентифицированная константой, **adSchemaColumns,** связана с четырьмя столбцами ограничений: TABLE \_ CATALOG, \_ TABLE SCHEMA, TABLE \_ NAME и COLUMN \_ NAME. Поэтому создается массив значений **Variant** с четырьмя элементами. Затем задано значение ограничения, соответствующее третьему столбце, TABLE \_ NAME. Возвращенный **набор** записей состоит из нескольких столбцов, подмножество которых — столбцы ограничений. Значения столбцов ограничений для каждой возвращаемой строки должны быть одинаковыми с соответствующими значениями ограничения.

4. Те, кто знаком с **SafeArrays,** могут быть удивлены, что **SafeArrayDestroy**() не вызван перед выходом. На самом деле вызов **SafeArrayDestroy**() в этом случае приведет к исключению времени запуска. Причина в том, что деструктор для vtCriteria будет вызывать **VariantClear**(), когда вариант **\_ \_ t** выходит из области, что освободит **SafeArray**. Вызов **SafeArrayDestroy** без вручную очистки варианта **\_ \_ t** приведет к деструктору, чтобы попытаться очистить недействительный **указатель SafeArray.** Если **бы был вызван SafeArrayDestroy,** код выглядел бы так:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Тем не менее, гораздо проще позволить **\_ \_ варианту t управлять** **SafeArray**.


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

В Visual Basic, имя свойства не может быть квалифицировано, будет ли оно извлечено, назначено или назначено ссылку.

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

В этом примере Visual C++ показано свойство **Get** /  /* *Put PutRef***.*

> [!NOTE]
> Следующие заметки соответствуют разделам с комментариями в примере кода.

1. В этом примере используются две формы отсутствующих аргументов строк: явная константа, **strMissing** и строка, которую компилятор будет использовать для создания временной **\_ bstr \_ t,** которая будет существовать для области метода **Open.**

2. Нет необходимости ставить операнд rs-PutRefActiveConnection (cn) в (IDispatch), так как тип операнда уже \> \* есть (IDispatch). \*
    
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

### <a name="using-getitemx-and-itemx"></a>Использование GetItem (x) и Item \[ x\]

В Visual Basic примере демонстрируется стандартный и альтернативный синтаксис **для Item**().

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

В этом примере Visual C++ **демонстрируется Item**.

> [!NOTE]
> Следующая заметка соответствует разделам с комментариями в примере кода.

1. При доступе к коллекции **с элементом** индекс **2**  должен быть отлит до долгого времени, чтобы был вызван соответствующий конструктор.
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Кастинг указателей объектов ADO с (IDispatch) \*

В следующем примере Visual C++ показано использование (IDispatch) для \* отбраковки указателей объектов ADO.

> [!NOTE]
> Следующие заметки соответствуют разделам с комментариями в примере кода.

1. Укажите объект **open Connection** в явно закодировать **вариант**. Отдай его (IDispatch), чтобы был вызван правильный \* конструктор. Кроме того, явно задан параметр **\_ \_ t** второго варианта к значению true по **умолчанию,** поэтому количество ссылок на объект будет правильным после окончания операции **Recordset::Open.**

2. Выражение (bstr t) — это не литье, а оператор \_ \_  **\_ \_ вариантов t,** который извлекает строку **\_ bstr \_ t** из варианта, возвращенного **значением**. Выражение (char) — это не литье, а оператор \* **\_ bstr \_ t,** который извлекает указатель на инкапсулированную строку в **\_ объекте bstr \_ t.** В этом разделе кода демонстрируются некоторые полезные действия операторов **\_ \_ вариантов t** и **\_ bstr \_ t.**
    
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

