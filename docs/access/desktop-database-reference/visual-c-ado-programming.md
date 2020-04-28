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

Справочник по API ADO описывает функциональные возможности API-интерфейса ADO, используя синтаксис, похожий на Microsoft Visual Basic. Хотя предполагаемая аудитория — это все пользователи, программисты ADO используют различные языки, такие как Visual Basic, Visual C++ (с директивой ** \#Import** и без нее), и Visual J++ (с пакетом классов ADO/WFC).

В соответствии с этим разнообразием [индексы синтаксиса ADO для Visual c++](using-ado-with-microsoft-visual-c.md) предоставляют языковой синтаксис Visual c++ со ссылками на общие описания функций, параметров, исключительных поведений и т. д. в справочнике по API.

ADO реализован с помощью интерфейсов COM (компонентной объектной модели). Однако программисты легче работают с COM на определенных языках программирования, чем другие. Например, почти все детали использования COM неявно обрабатываются для программистов Visual Basic, а программисты Visual C++ должны присутствовать на этих сведениях.

В следующих разделах приведена сводка сведений для программистов C и C++, использующих ADO и директиву ** \#Import** . Он посвящен типам данных, характерным для COM (**Variant**, **BSTR**и **SAFEARRAY**), а также обработке ошибок\_(\_ошибках com).

## <a name="using-the-import-compiler-directive"></a>Использование директивы компилятора \#импорта

Директива компилятора ** \#Import** Visual C++ упрощает работу с методами и свойствами ADO. Директива принимает имя файла, содержащего библиотеку типов, например, ADO. dll (Msado15. dll), и создает файлы заголовков, содержащие объявления typedef, смарт-указатели для интерфейсов и перечислимые константы. Каждый интерфейс инкапсулируется или упаковывается в классе.

Для каждой операции в классе (то есть в методе или вызове свойства) существует объявление для непосредственного вызова операции (то есть "необработанная" форма операции), а также объявление для вызова необработанной операции и генерации ошибки COM, если операция не может быть выполнена успешно. Если операция является свойством, то обычно существует директива компилятора, которая создает альтернативный синтаксис для операции, которая имеет синтаксис, такой как Visual Basic.

Операции, извлекающие значение свойства, имеют имена формы, **Get * * * Property*. Операции, которые задают значение свойства, имеют имена формы, **Put * * * Property*. Операции, которые задают значение свойства с указателем на объект ADO, имеют имена вида **путреф * * **.

Вы можете получить или задать свойство с помощью вызовов следующих форм:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Использование директив свойств

Директива компилятора ** \_деклспек (Property...) — это расширение языка C, зависящее от Майкрософт, которое объявляет функцию, используемую в качестве свойства, альтернативным синтаксисом. \_** В результате можно задать или получить значения свойства, как в Visual Basic. Например, вы можете задать и получить свойство следующим образом:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Обратите внимание, что нет необходимости в коде:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Компилятор создаст соответствующий метод **Get * * *-*, **Put**-или **путреф * * ** в зависимости от объявления альтернативного синтаксиса и того, является ли свойство прочитанным или записанным.

**put** **get** **get** **put** ** \_Директива компилятора деклспек (Property...) может объявлять только альтернативный синтаксис для функции Get, PUT или Get. \_** Только операции чтения имеют только объявление **Get** ; операции только для записи содержат объявление **Put** ; операции, выполняемые как для чтения, так и для записи, имеют объявления **Get** и **Put** .

Эта директива может иметь только два объявления; Однако у каждого свойства могут быть три функции свойств: **Get * * * Property*, **Put * * * Property*и **путреф * * **. В этом случае только две формы свойства имеют альтернативный синтаксис.

Например, свойство **Command** Object **ActiveConnection** объявляется с помощью альтернативного синтаксиса для **Get * * * ActiveConnection* и **путреф * * * ActiveConnection*. **Путреф**-синтаксис является хорошим выбором, так как на практике, как правило, необходимо поместить в это свойство открытый объект **Connection** (то есть, указатель на объект **подключения** ). С другой стороны, объект **Recordset** имеет операции **Get**–, **Put**и **путреф * * * ActiveConnection* , но без альтернативного синтаксиса.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Коллекции, метод GetItem и свойство Item

ADO определяет несколько коллекций, в том числе **поля**, **Параметры**, **Свойства**и **ошибки**. В Visual C++ метод **GetItem (***index***)** Возвращает элемент коллекции. *Index* является **вариантом**, значением которого является числовой индекс элемента в коллекции или строка, содержащая имя члена.

Директива компилятора **Item** ** \_деклспек (Property...) объявляет свойство Item в качестве альтернативного синтаксиса для каждого основного метода GetItem () каждой \_** коллекции. **GetItem()** Альтернативный синтаксис использует квадратные скобки и выглядит примерно так: ссылка на массив. В общем случае две формы выглядят следующим образом:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Например, назначьте значение полю объекта **Recordset** с именем ***RS***, производным от таблицы **authors** базы данных **pubs** . Используйте свойство **Item ()** , чтобы получить доступ к третьему **полю** коллекции **Fields** **Object Collection** (коллекции индексируются из нуля; Предположим, что третье поле называется ***Au\_fname***). Затем вызовите метод **value ()** для объекта **field** , чтобы назначить строковое значение.

Это может быть представлено в Visual Basic следующими четырьмя способами (последние две формы уникальны для Visual Basic; у других языков нет эквивалентов):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

Эквивалент в Visual C++ для первых двух предыдущих форм:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-Кроме того, показан альтернативный синтаксис для свойства **value** .

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Типы данных, зависящие от модели COM

Как правило, любой тип данных Visual Basic, который вы найдете в справочнике по API ADO, имеет эквивалент в Visual C++. **К ним**относятся стандартные типы данных, такие как **неподписанный символ** для **байта**Visual Basic, **Short** для **целого числа**и **Long** . Просмотрите индексы синтаксиса, чтобы точно увидеть, что требуется для операндов данного метода или свойства.

Исключениями из этого правила являются типы данных, характерные для COM: **Variant**, **BSTR**и **SAFEARRAY**.

### <a name="variant"></a>Variant

**Variant** — это структурированный тип данных, который содержит элемент value и элемент типа данных. **Variant** может содержать широкий диапазон других типов данных, в том числе другой Variant, BSTR, Boolean, IDispatch или указатель IUnknown, Currency, Date и т. д. COM также предоставляет методы, упрощающие преобразование одного типа данных в другой.

Класс ** \_Variant\_t** инкапсулирует и управляет типом данных **Variant** .

Если ссылка на API ADO указывает, что в качестве операнда метода или свойства используется значение, обычно это означает, что значение передается в ** \_варианте\_t**.

Это правило явно задано, когда раздел **Parameters** в разделах справочника по API ADO указывает на то, что операнд является **вариантом**. Одним исключением является то, что в документации явно говорится, что операнд принимает стандартный тип данных, например **Long** или **Byte**, или перечисление. Другое исключение — когда операнд принимает **строку**.

### <a name="bstr"></a>СТРОКЕ

Тип данных **BSTR** (B **ASIC)**— это структурированный тип данных, который содержит строку символов и длину строки.**B** COM предоставляет методы для распределения, управления и освобождения **BSTR**.

Класс ** \_BSTR\_t** инкапсулирует и управляет типом данных **BSTR** .

Если ссылка на API ADO указывает на то, что метод или свойство принимает **строковое** значение, это означает, что значение имеет вид ** \_BSTR\_t**.

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a>\_Приведение\_классов Variant \_t\_и BSTR t

Часто нет необходимости явно кодировать ** \_Variant\_t** или ** \_BSTR\_t** в аргументе для операции. Если класс ** \_Variant\_t** или ** \_BSTR\_t** имеет конструктор, который соответствует типу данных аргумента, компилятор создаст соответствующий ** \_Variant\_t** или ** \_\_BSTR t**.

Тем не менее, если аргумент является неоднозначным, то есть тип данных аргумента соответствует более чем одному конструктору, необходимо привести аргумент с соответствующим типом данных для вызова надлежащего конструктора.

Например, объявление для объекта **Recordset:: Open** является следующим:

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

Аргумент ActiveConnection принимает ссылку на ** \_\_вариант t**, который можно закодировать как строку подключения или указатель на открытый объект **Connection** .

Правильный ** \_вариант\_t** будет создан неявно, если вы передаете строку, такую как "DSN = Pubs; UID = SA; pwd =;", или указатель, такой как "(IDispatch \*) пконн".

Или вы можете явно закодировать ** \_объект\_Variant t** , содержащий указатель, такой\_как\_"Variant t ( \*(IDispatch) пконн, true)". Приведение (IDispatch \*) разрешает неоднозначность с другим конструктором, принимающим указатель на интерфейс IUnknown.

Это очень важный, хотя и часто упоминаемый факт, что ADO является интерфейсом IDispatch. Всякий раз, когда указатель на объект ADO должен быть передан как **Variant**, этот указатель должен быть приведен как указатель на интерфейс IDispatch.

В последнем случае явно кодирует второй логический аргумент конструктора с необязательным значением по умолчанию true. Этот аргумент заставляет конструктор **Variant** вызывать метод **AddRef**(), который компенсирует ADO автоматический вызов метода " ** \_\_t:: Release**()" при завершении вызова метода или свойства ADO.

### <a name="safearray"></a>SafeArray

**SAFEARRAY** это структурированный тип данных, который содержит массив других типов данных. **SAFEARRAY** называется *Safe* , так как содержит сведения о границах каждого измерения массива и ограничивает доступ к элементам массива в этих границах.

Если ссылка на API ADO указывает на то, что метод или свойство принимают или возвращают массив, это означает, что метод или свойство принимает или возвращает **SAFEARRAY**, а не собственный массив C/C++.

Например, второму параметру метода **подключения** объекта **OpenSchema** требуется массив значений **Variant** . Эти значения **типа Variant** должны передаваться в виде элементов **SAFEARRAY**, и этот **SAFEARRAY** должен быть установлен в качестве значения другого **варианта**. Это то, что другой **вариант** , передаваемый в качестве второго аргумента **OpenSchema**.

В качестве дальнейших примеров первым аргументом метода **Find** является **Variant** , значение которого является одномерным **массивом SAFEARRAY**; Каждый необязательный первый и второй аргументы **AddNew** является одномерным **массивом SAFEARRAY**; Возвращаемое значение метода **GetRows** — это объект **Variant** , значение которого является двумерным **массивом SAFEARRAY**.

## <a name="missing-and-default-parameters"></a>Отсутствующие параметры и параметры по умолчанию

Visual Basic разрешает отсутствующие параметры в методах. Например, метод **Open** объекта **Recordset** имеет пять параметров, но вы можете пропустить промежуточные параметры и оставить параметры в конце. Значение **BSTR** или **Variant** по умолчанию будет заменено в зависимости от типа данных отсутствующего операнда.

В C/C++ необходимо указать все операнды. Если вы хотите указать отсутствующий параметр, тип данных которого является строкой, укажите строку ** \_BSTR\_t** , содержащую пустую строку. Если вы хотите указать отсутствующий параметр, тип данных которого — **Variant**, укажите ** \_вариант\_t** со значением отображения\_E\_парамнотфаунд и типом ошибки VT\_. Кроме того, можно указать эквивалентную ** \#** **vtMissing** ** \_константу Variant\_t** , втмиссинг, которая предоставляется директивой импорта.

Три метода — это исключения типичного использования **втмиссинг**. Это методы **EXECUTE** для объектов **Connection** и **Command** , а также метод **NextRecordset** объекта **Recordset** . Ниже приведены их подписи:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Параметры, *рекордсаффектед* и *Parameters*— указатели на **Variant**. *Параметр является* входным параметром, который задает адрес **Variant** , содержащий один параметр, или массив параметров, которые будут изменять выполняемую команду. *Рекордсаффектед* — выходной параметр, указывающий адрес **Variant**, в котором возвращается количество строк, затрагиваемых методом.

В методе **EXECUTE** **Object Object** указывает, что никакие параметры не указываются с помощью установки *параметров* для \&втмиссинг (рекомендуется) или для указателя NULL (то есть, **null** или нуль (0)). Если *параметру* присвоено значение null, метод выполняет внутреннее замещение эквивалента **втмиссинг**, а затем завершает операцию.

Во всех методах указывается, что количество затронутых записей не должно возвращаться путем установки для *рекордсаффектед* указателя NULL. В этом случае указатель null не настолько похож на отсутствующий параметр, что означает, что метод должен отбросить количество затронутых записей.

Таким образом, для этих трех методов допустимым кодом может быть нечто подобное:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Обработка ошибок

В COM большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция. Директива ** \#импорта** создает код обертки вокруг каждого "необработанного" метода или свойства и проверяет возвращаемое значение HRESULT. Если HRESULT указывает на ошибку, код оболочки создает ошибку COM, вызывая \_com-\_ошибку\_еррорекс () с возвращаемым кодом возврата HRESULT в качестве аргумента. Объекты ошибок COM можно перехватывать в блоке **try**-**catch** . (Чтобы обеспечить эффективность, перехватите ссылку на объект ** \_Error\_com** .)

Помните, что это ошибки ADO: они возникают при неисправности операции ADO. Ошибки, возвращенные базовым поставщиком, отображаются как объекты **ошибок** в коллекции **ошибок** объекта **подключения** .

Директива ** \#импорта** создает только процедуры обработки ошибок для методов и свойств, объявленных в ADO. dll. Тем не менее, вы можете использовать такой же механизм обработки ошибок, написав собственный макрос или встроенную функцию проверки ошибок. Примеры приведены в разделе, [расширениях Visual C++](visual-c-extensions-for-ado.md)или коде в следующих разделах.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Эквиваленты соглашений Visual Basic в Visual C++

Ниже приведена сводка по нескольким соглашениям в документации по ADO, кодированным в Visual Basic, а также их эквивалентам в Visual C++.

### <a name="declaring-an-ado-object"></a>Объявление объекта ADO

В Visual Basic объектная переменная ADO (в данном случае для объекта **Recordset** ) объявляется следующим образом:

```vb 
 
Dim rst As ADODB.Recordset 
```

Предложение "ADODB. Recordset "— это ProgID объекта **Recordset** , как определено в реестре. Новый экземпляр объекта **Record** объявляется следующим образом:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-также

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

В Visual C++ директива ** \#импорта** создает объявления типов смарт-указателей для всех объектов ADO. Например, переменная, указывающая на объект ** \_Recordset** , имеет тип ** \_рекордсетптр**и объявляется следующим образом:

```cpp 
 
_RecordsetPtr rs; 
```

Переменная, указывающая на новый экземпляр объекта ** \_Recordset** , объявляется следующим образом:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-также

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-также

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

После вызова метода **CreateInstance** переменная может использоваться следующим образом:

```cpp 
 
rs->Open(...); 
```

Обратите внимание, что в одном случае оператор "." используется, как если бы переменная была экземпляром класса (RS. CreateInstance), а в другом случае оператор "-\>" используется так, как если бы переменная была указателем на интерфейс (RS-\>Open).

Одну переменную можно использовать двумя способами, так как оператор "\>-" перегружен, чтобы позволить экземпляру класса вести себя как указатель на интерфейс. Частный член класса переменной экземпляра содержит указатель на интерфейс ** \_Recordset** ; оператор "–\>" возвращает этот указатель; Возвращаемый указатель получает доступ к членам объекта ** \_Recordset** .

### <a name="coding-a-missing-parameter"></a>Написание кода отсутствующего параметра

#### <a name="string"></a>String

Если вам нужно закодировать пропущенный **строковый** операнд в Visual Basic, вы просто опустите операнд. Необходимо указать операнд в Visual C++. Код — ** \_BSTR\_t** , имеющий пустую строку в качестве значения.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

При необходимости кодирования пропущенного операнда **Variant** в Visual Basic вы просто опустите операнд. Необходимо указать все операнды в Visual C++. Код — отсутствует параметр **Variant** со значением ** \_Variant\_t** , равным специальному значению\_,\_отображаемой E парамнотфаунд и Type\_, Error VT. Кроме того, можно указать **втмиссинг**, представляющий собой эквивалентную предварительно определенную константу, предоставляемую директивой ** \#импорта** .

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-или используйте —

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Объявление варианта

В Visual Basic **переменная Variant** объявляется с помощью оператора **Dim** следующим образом:

```vb 
 
Dim VariableName As Variant 
```

В Visual C++ объявите переменную как тип ** \_Variant\_t**. Ниже приведено несколько схематических ** \_объявлений вариантов\_t** .

> [!NOTE]
> Эти объявления просто придают грубое представление о том, что можно сделать с кодом в собственной программе. Дополнительные сведения можно найти в приведенных ниже примерах и документации по Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Использование массивов вариантов

В Visual Basic массивы **Variant** можно закодировать с помощью оператора **Dim** или можно использовать функцию **Array** , как показано в следующем примере кода:

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

В следующем примере на Visual C++ показано использование **SAFEARRAY** , используемого с ** \_вариантом\_t**.

> [!NOTE]
> Следующие примечания соответствуют разделам с комментариями в примере кода.

1. В этом случае встроенная функция ТЕССР () используется для использования существующего механизма обработки ошибок.

2. Необходим только одномерный массив, поэтому вы можете использовать **сафеаррайкреатевектор**вместо объявления общего назначения **Сафеаррайбаунд** и функции **сафеаррайкреате** . Ниже показано, как будет выглядеть код с помощью **сафеаррайкреате**:
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. Схема, определенная с помощью перечислимой константы, **адсчемаколумнс**, связана с четырьмя столбцами ограничений\_: Каталог таблицы\_, таблица,\_имя таблицы и имя\_столбца. Поэтому создается массив значений **Variant** с четырьмя элементами. Затем указывается значение ограничения, соответствующее третьему столбцу, имя\_таблицы. Возвращаемый объект **Recordset** состоит из нескольких столбцов, подмножества которых являются столбцами ограничений. Значения столбцов ограничений для каждой возвращаемой строки должны совпадать со значениями соответствующих ограничений.

4. Хорошо знакомые с **SAFEARRAY** , могут быть удивлены тем, что **сафеаррайдестрой**() не вызывается перед выходом. На самом деле вызов **сафеаррайдестрой**() в этом случае приведет к возникновению исключения времени выполнения. Причина в том, что деструктор для вткритериа будет вызывать **вариантклеар**(), когда ** \_Variant\_t** выходит из области действия, что позволит освободить **SAFEARRAY**. Вызов **сафеаррайдестрой**без ручного очистки ** \_Variant\_t**приведет к тому, что деструктор попытается очистить недопустимый указатель **SAFEARRAY** . При вызове **сафеаррайдестрой** код будет выглядеть следующим образом:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Тем не менее, значительно проще позволить ** \_варианту\_** управлять **SAFEARRAY**.


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

### <a name="using-property-getputputref"></a>Использование свойства get/put/Путреф

В Visual Basic имя свойства не определено при получении, назначении или назначении ссылки.

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

В этом примере в Visual C++ показано свойство **Get**/**Put**/**путреф * * **.

> [!NOTE]
> Следующие примечания соответствуют разделам с комментариями в примере кода.

1. В этом примере используются две формы отсутствующего строкового аргумента: явная константа, **стрмиссинг**и строка, которую компилятор будет использовать для создания временной ** \_строки BSTR\_t** , которая будет существовать для области метода **Open** .

2. Не требуется приведение операнда RS-\>путрефактивеконнектион (CN) к (IDispatch \*), так как тип операнда уже (IDispatch \*).
    
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

### <a name="using-getitemx-and-itemx"></a>Использование метода GetItem (x) и элемента\[x\]

В этом примере Visual Basic показан стандартный и альтернативный синтаксис для **Item**().

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

В этом примере в Visual C++ показано, как **элемент**.

> [!NOTE]
> Следующее примечание соответствует разделу с комментариями в примере кода.

1. Когда доступ к коллекции осуществляется с помощью **элемента**, индекс, **2**, должен быть приведен к типу **Long** , поэтому будет вызван соответствующий конструктор.
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Приведение указателей объектов ADO с \*(IDispatch)

В следующем примере на Visual C++ показано использование ( \*IDispatch) для приведения указателей объектов ADO.

> [!NOTE]
> Следующие примечания соответствуют разделам с комментариями в примере кода.

1. Укажите открытый объект **Connection** в явно заданном коде **Variant**. Приведите его к ( \*IDispatch), чтобы вызвать правильный конструктор. Кроме того, необходимо явным образом задать для второго ** \_параметра Variant\_t** значение по умолчанию **true**, поэтому счетчик ссылок на объекты будет правильным, когда заканчивается операция **Recordset:: Open** .

2. Выражение\_(BSTR\_t) не является приведением, а оператор ** \_Variant\_t** , который извлекает строку ** \_BSTR\_t** из **Variant** , возвращенного по **значению**. Выражение (char\*) не является приведением, но оператор ** \_BSTR\_t** , который извлекает указатель на инкапсулированную строку в объекте ** \_BSTR\_t** . В этом разделе кода показаны некоторые из наиболее эффективных вариантов поведения ** \_операторов\_Variant t** и ** \_BSTR\_t** .
    
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

