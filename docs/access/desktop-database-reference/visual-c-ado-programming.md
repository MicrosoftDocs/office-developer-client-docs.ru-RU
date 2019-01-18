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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721292"
---
# <a name="visual-c-ado-programming"></a>Программирование для ADO на Visual C++

**Применимо к**: Access 2013, Office 2013

Справочник по API ADO описывается функциональных возможностей ADO программный интерфейс (API) с помощью синтаксис, подобный в Microsoft Visual Basic. То, что Предполагаемая аудитория всех пользователей, ADO с любым опытом использования различных языков, например Visual Basic, Visual C++ (с и без ** \#импорта** директива) и Visual J ++ (с пакетом класс ADO/WFC).

Чтобы обеспечить этот плотности, [ADO для Visual C++ синтаксис индексов](using-ado-with-microsoft-visual-c.md) предоставляют синтаксис конкретного языка Visual C++ с помощью ссылки на общие описания функциональных возможностей, параметры, исключительных поведения и т. д в справочник по API.

ADO реализуется с помощью интерфейсов COM (объектная модель компонента). Тем не менее проще для программистов для работы с COM на некоторых языках программирования, чем другие. Например почти все дополнительные сведения об использовании COM осуществляется неявно для программистов Visual Basic программистов Visual C++ должны принять участие в этих сведений о себе.

В следующих разделах приведены подробные сведения для программистов C и C++ с помощью ADO и ** \#импорта** директивы. В данном документе описываются типы данных, относящимся к COM (**Variant**, **BSTR**и **SafeArray**) и обработка ошибок (\_com\_ошибка).

## <a name="using-the-import-compiler-directive"></a>С помощью \#импорта директива компилятора

** \#Импорта** директивы компилятора Visual C++ упрощает работу с ADO методы и свойства. Директива принимает имя файла, содержащего библиотеку типов, таких как ADO библиотеки DLL (Msado15.dll) и создает файлы заголовков, содержащие объявления typedef, смарт-указатели интерфейсов и перечисляемые константы. Каждого интерфейса инкапсулированную или заключены в классе.

Для каждой операции в классе (то есть, метод или свойство звонок) отсутствует объявление, чтобы вызвать операцию непосредственно (то есть, «необработанные» форма операции) и объявление, чтобы вызвать операцию необработанные и создавать COM-ошибки, если не удается выполнить операцию для выполнения succ essfully. Если операция является свойством, есть обычно директива компилятора, который создает альтернативный синтаксис для операции, которая имеет синтаксис, аналогичный Visual Basic.

Операции, которые извлекают значение свойства имеют имена формы, **получения *** свойство*. Операции, задайте значение свойства имеют имена формы, **поместить *** свойство*. Операции, задайте значение свойства с помощью указателя на объект ADO имеют имена формы, **PutRef *** свойство*.

Можно получить или задать свойство со звонками из следующих форм:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Свойство директивы using

** \_ \_Declspec(property...)** директивы компилятора является расширением языка C зависящие от корпорации Майкрософт, которая объявляет функцию, используемую как свойство иметь альтернативный синтаксис. В результате можно задать или получить значения свойства в виде делается в Visual Basic. К примеру можно задать и получить свойство таким образом:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Обратите внимание на то, что нет необходимости кода:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Компилятор будет создавать соответствующий **Get ***-*, **поместите**-, или **PutRef *** свойство* звонок на основе объявлен какие альтернативный синтаксис и ли сейчас свойство чтения или записи.

** \_ \_Declspec(property...)** директивы компилятора можно объявить только **Получение**, **поместить**или **get** и **put** альтернативный синтаксис для функции. Только для чтения operations иметь только объявление **получения** ; операции только для записи только у объявление **поместить** ; операции, которые являются чтение и запись иметь как **get** и **put** объявлений.

Только два объявления, которые можно получить с этой директивы; Тем не менее, каждое свойство может иметь три функции свойств: **получения *** свойство*, **поместить *** свойство*, и **PutRef *** свойство*. В этом случае только две формы свойства имеют альтернативный синтаксис.

Например, объект **команды** свойства **ActiveConnection** объявлен с альтернативный синтаксис **получения *** ActiveConnection* и **PutRef *** ActiveConnection*. **PutRef**- синтаксис является хорошим выбором, поскольку на практике обычно требуется поместить объект **подключения** open (указатель объекта **подключения** ), это свойство. С другой стороны, имеет объекта **набора записей** **Get**-, **поместите**- и **PutRef *** ActiveConnection* операций, но не альтернативный синтаксис.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Коллекции, метод GetItem и свойство Item

ADO определяет несколько семейств сайтов, включая **поля**, **Параметры**, **свойств**и **ошибки**. В Visual C++ метод **GetItem (***индекс***)** возвращает элемент коллекции. *Индекс* находится **Variant**, значение которого равно числовой индекс элемента в коллекции или строка, содержащая имя элемента.

** \_ \_Declspec(property...)** директивы компилятора объявляет свойство **Item** как альтернативный синтаксис для каждого семейства сайтов фундаментальные метод **GetItem() для удаленного элемента** . Альтернативный синтаксис использует квадратные скобки и выглядит ссылкой на массив. В общем случае две формы иметь следующий вид:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Например присвоить значение поля объекта **набора записей** , с именем ***rs***, полученных из таблицы **авторов** базы данных **pubs** . Используйте свойство **Item()** для доступа к третьего **поля** объекта **набора записей** коллекции **полей** (семейств сайтов, индексируются с нуля; возможно, с именем третьего поля ***au\_отображающее общие сведения***). Затем вызовите метод **Value()** для объекта **поля** для присвоения строкового значения.

Это может быть выражено в Visual Basic следующие четыре способа (последние два формы являются уникальными для Visual Basic, другие языки, которые не имеют эквиваленты):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

— Это эквивалент в Visual C++ выше первые две формы:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-или -(альтернативный синтаксис для свойства **значение** также отображается)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Типы данных COM

В общем случае любой тип данных Visual Basic, поиск в справке API ADO имеет эквивалентом Visual C++. К ним относятся типов стандартных данных, таких как **неподписанные символов** для Visual Basic **Byte**, **короткий** для **целого числа**и **много** **времени**. Просмотрите индексов синтаксис, чтобы увидеть именно то, что требуется для операндов данный метод или свойство.

Исключения для этого правила — это типы данных, относящиеся к COM: **Variant**, **BSTR**и **SafeArray**.

### <a name="variant"></a>Variant

**Variant** — это тип структурированных данных, который содержит элемент значение и член типа данных. **Variant** может содержать большое число других типов данных, включая другого типа Variant, BSTR, логическое значение, IDispatch или IUnknown указатель, валюты, даты и т. д. COM также предоставляет методы, которые позволяют легко преобразования одного типа данных в другой.

** \_Variant\_t** класс инкапсулирует и управляет тип данных **Variant** .

Справочник по API ADO сказано, метод или свойство операнд принимает значение, обычно означает значение передается в ** \_variant\_t**.

Это правило не явным образом значение true, если в разделе **Параметры** в разделах Справочник по API ADO говорит операнд **Variant**. Одно исключение — при документации явно сказано, что операнд принимает тип стандартных данных, таких как **длинный** или **байтов**или перечисление. Операнд принимает **строку**при еще одно исключение.

### <a name="bstr"></a>BSTR

**BSTR** (**B**asic **STR**ing) — это тип структурированных данных, который содержит строку символов и длина строки. COM предоставляет методы для выделения, работы с и без **BSTR**.

** \_Bstr\_t** класс инкапсулирует и управляет тип данных **BSTR** .

Справочник по API ADO сказано, метод или свойство принимает значение типа **String** , означает значение задается в виде ** \_bstr\_t**.

#### <a name="casting-variantt-and-bstrt-classes"></a>Приведение \_variant\_t и \_bstr\_классы t

Часто не требуется явно кода ** \_variant\_t** или ** \_bstr\_t** в аргумент для операции. Если ** \_variant\_t** или ** \_bstr\_t** класс содержит конструктор, который соответствует типу данных аргумента, а затем компилятор будет создавать соответствующий ** \_variant\_t** или ** \_ BSTR\_t**.

Тем не менее если аргумент является неоднозначным, то есть, тип данных аргумента соответствует более одного конструктора, необходимо привести аргумент с соответствующий тип данных для вызова конструктора правильное.

Например объявление для метода **Recordset::Open** является:

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

Аргумент ActiveConnection принимает ссылку на ** \_variant\_t**, которой может кода как строка подключения или указатель на открытый объект **подключения** .

Правильный ** \_variant\_t** будут созданы неявно, если передачи строки, например, «уведомления о Доставке = pubs; uid = sa; pwd =;», или указатель, такие как "(IDispatch \*) pConn».

Или может явно кода ** \_variant\_t** содержащий указатель, таких как "\_variant\_t ((IDispatch \*) pConn true)». Приведение (IDispatch \*), разрешает неопределенность с другой конструктор, который принимает указатель на интерфейс IUnknown.

Очень важно, хотя редко упомянутые факт, ADO интерфейс IDispatch. Каждый раз, когда указатель на объект ADO должен передаваться в качестве **типа Variant**, этот указатель должны быть приведены как указатель на интерфейс IDispatch.

Последний случай явно кодов второй аргумент boolean конструктора с его дополнительный параметр, по умолчанию значение true. Этот аргумент вызывает конструктор **типа Variant** , чтобы вызвать метод **AddRef**(), который компенсация ADO автоматически вызов ** \_variant\_t::Release**() метод при завершении вызова метод или свойство ADO.

### <a name="safearray"></a>SafeArray

**SafeArray** — это тип структурированных данных, который содержит массив из других типов данных. **SafeArray** называется *безопасных* , так как он содержит сведения о границы каждого измерения массива и ограничения доступа к элементам массива в этих границах.

Справочник по API ADO сказано, метод или свойство принимает или возвращает массив, это означает, что метод или свойство принимает или возвращает **SafeArray**, не собственный массив C/C++.

Например второго параметра объект **подключения** **OpenSchema** метод требует массив значений **Variant** . Эти значения **Variant** передается как элементы **SafeArray**и этого **SafeArray** должно быть задано как значение другого **типа Variant**. Это, другие **Variant** , которое передается в качестве аргумента второй **OpenSchema**.

В качестве примеров первый аргумент метода **поиска** является **Variant** , значение которого равно одномерный **массив SafeArray**; Каждый дополнительный первый и второй аргументы **AddNew** является одномерный **массив SafeArray**; а возвращаемое значение метода **получения строк** — **Variant** , значение которого равно двухмерных **SafeArray**.

## <a name="missing-and-default-parameters"></a>Параметры по умолчанию и отсутствует

Visual Basic позволяет отсутствуют параметры в методах. К примеру метод **Open** объекта **набора записей** имеет пять параметров, но можно пропустить промежуточных параметров и не указывайте конечные параметры. В зависимости от типа операнд будет заменен по умолчанию **BSTR** или **Variant** .

В C/C++ необходимо указать все операндов. Если вы хотите указать отсутствующий параметр типом данных — это строка, укажите ** \_bstr\_t** содержащий пустую строку. Если вы хотите отсутствующий параметр указан тип данных которого является значение **типа Variant**, укажите ** \_variant\_t** со значением Отображать\_E\_PARAMNOTFOUND тип VT и\_ошибка. Кроме того, укажите эквивалент ** \_variant\_t** константа, **vtMissing**, которая хранится в телефонном ** \#импорта** директивы.

Три метода, исключения для типичного использования **vtMissing**. Это методов **Execute** объектов **подключения** и **команды** и метод **NextRecordset** объекта **набора записей** . Ниже приведены их подписей.

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Используются параметры, *Параметры*и *RecordsAffected* указатели на **Variant**. *Параметры* — это входного параметра, который определяет адрес **Variant** один параметр, содержащий или массив параметров, которые будет изменять выполняемой команды. *RecordsAffected* — это выходной параметр, который указывает адрес **Variant**, где возвращается количество строк с помощью метода.

В объекте **команд** метода **Execute** указывает, что не указаны параметры путем установки *параметров* на любой \&vtMissing (что рекомендуется) или значение null, указатель (то есть, **значение NULL** или нуль (0)). Если *Параметры* указателя null, метод внутренне заменяет эквивалент **vtMissing**и затем завершает операцию.

Все методы указывает, что количество записей не должны возвращаться путем установки для параметра *RecordsAffected* указатель null. В этом случае указатель null не так отсутствующий параметр как это свидетельствует о том, что метод необходимо отменить количество записей.

Таким образом для этих трех методов является допустимым написать код таких как:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Обработка ошибок

В модели COM большинство операций возврата HRESULT кода возврата, которое указывает, будет ли функция успешно завершена. ** \#Импорта** директива создает код программы-оболочки вокруг каждого «необработанные» метод или свойство и проверяет возвращаемое значение HRESULT. Если значение HRESULT указывает на ошибку, кода программы-оболочки для вызывает ошибку COM путем вызова \_com\_проблему\_errorex() со значением HRESULT возвращают код в качестве аргумента. Ошибка COM-объектов может быть зафиксировано в **Попробуйте**-блок**catch** . (Ради повышения эффективности перехватывающей ссылку на ** \_com\_ошибка** объект.)

Помните, что это ADO ошибки: они являются результатом сбоя операции ADO. Ошибок, возвращаемых основного поставщика отображаются в виде объектов **ошибок** в объект **подключения** семейства **Errors** .

** \#Импорта** директива создает только ошибки процедур обработки для методов и свойств, объявленных в ADO DLL-файл. Тем не менее вы можете воспользоваться преимуществами эта же ошибка механизм обработки, создав собственный макрос или встроенной функции проверки ошибок. Просмотрите раздел, [Расширений Visual C++](visual-c-extensions-for-ado.md)или код в следующих разделах приведены примеры.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Visual C++ эквиваленты соглашения по Visual Basic

Ниже приводится сводка по несколько условные обозначения в документации по ADO, закодированный в Visual Basic, а также их эквивалентами в Visual C++.

### <a name="declaring-an-ado-object"></a>Объявление объекта ADO

В Visual Basic ADO объектной переменной (в данном случае для объекта **набора записей** ) объявляется следующим образом:

```vb 
 
Dim rst As ADODB.Recordset 
```

Предложение «ADODB. Записей» — это программный идентификатор объекта **набора записей** , как определено в реестре. Новый экземпляр объекта **записи** объявляется следующим образом:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-или -

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

В Visual C++ ** \#импорта** директива создает смарт-тип указателя объявления для всех объектов ADO. Например, переменную, которая указывает на ** \_записей** — это объект типа ** \_RecordsetPtr**и объявляется следующим образом:

```cpp 
 
_RecordsetPtr rs; 
```

Переменная, указывающий на новый экземпляр объекта ** \_записей** объект объявляется следующим образом:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-или -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-или -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

После вызова метода **CreateInstance** переменной можно использовать следующим образом:

```cpp 
 
rs->Open(...); 
```

Обратите внимание, что в одном случае «.» используется оператор, как если бы переменная экземпляра класса (rs. CreateInstance) и в другом случае «-\>"оператор используется, как если бы переменная указатель на интерфейс (rs -\>Open).

По одной переменной можно использовать двумя способами, так как «-\>"оператор перегрузить чтобы экземпляр класса для обрабатываются как указатель на интерфейс. Закрытый класс элемент переменной экземпляра содержит указатель на ** \_записей** интерфейса; «-\>"оператор возвращает этот указатель; и возвращенный указатель обращается к членов ** \_записей** объекта.

### <a name="coding-a-missing-parameter"></a>Создание кода отсутствующий параметр

#### <a name="string"></a>Строка

При необходимости кода операнд **строки** в Visual Basic, просто опустить операнд. Необходимо указать операнд в Visual C++. Код ** \_bstr\_t** , которая имеет пустую строку как значение.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

При необходимости кода операнд **Variant** в Visual Basic, просто опустить операнд. Необходимо указать все операнды в Visual C++. Код отсутствующий параметр **типа Variant** с ** \_variant\_t** специальные значение Отображать\_E\_PARAMNOTFOUND и тип, VT\_ошибка. Кроме того, укажите **vtMissing**, который является эквивалент предопределенные константы в телефонном ** \#импорта** директивы.

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-или воспользуйтесь-

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Объявление типа variant

В Visual Basic **Variant** объявлен с помощью оператора **Dim** следующим образом:

```vb 
 
Dim VariableName As Variant 
```

В Visual C++ объявлении переменной в качестве типа ** \_variant\_t**. Несколько схема ** \_variant\_t** ниже показаны объявления.

> [!NOTE]
> Эти объявления просто присвойте приблизительное представление об бы кода в собственную программу. Для получения дополнительных сведений см. в приведенных ниже примерах и документации по Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Использование массивов вариантов

В Visual Basic массивов **вариантов** можно закодировать с помощью оператора **Dim** , или можно использовать функцию **массива** , как показано в следующем примере кода:

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

В следующем примере Visual C++ демонстрируется использование **SafeArray** используется с ** \_variant\_t**.

> [!NOTE]
> Следующие замечания соответствуют закомментированного разделов в примере кода.

1. Еще раз чтобы воспользоваться преимуществами существующего механизм обработки ошибок определяется встроенная функция TESTHR().

2. Одномерный массив, требуется только в том случае, поэтому **SafeArrayCreateVector**, можно использовать вместо объявления **SAFEARRAYBOUND** общего назначения и функции **SafeArrayCreate** . Ниже приведен код будет выглядеть как с помощью **SafeArrayCreate**.
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. Схемы, определяемую средством константа перечисления **adSchemaColumns**связан с четыре столбца ограничение: таблица\_КАТАЛОГА, в ТАБЛИЦЕ\_СХЕМЫ, таблица\_имя и столбец\_имя. Таким образом создается массив значений **Variant** с четырьмя элементами. Выберите ограничение по значению, соответствующий третьего столбца в ТАБЛИЦЕ\_имя, указано. **Набор записей** , который возвращается состоит из нескольких столбцов, подмножество из которых представляет столбцы ограничений. Значения столбцов ограничения для каждой строки набора должно совпадать с соответствующие значения ограничения.

4. Те, которые знакомы с **объекты SAFEARRAY** может получать уведомления, что ( **SafeArrayDestroy**) не вызывается до завершения. На самом деле вызов ( **SafeArrayDestroy**) в этом случае вызовет исключение во время выполнения. Причина в том, что деструктор vtCriteria выполняется звонок ( **VariantClear**) при ** \_variant\_t** выходит за область, в которой будет освободить **SafeArray**. Вызов **SafeArrayDestroy**без вручную очистка ** \_variant\_t**, вызовет деструктор для снимите недопустимый указатель **SafeArray** . Если вызов **SafeArrayDestroy** , код будет выглядеть следующим образом:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Тем не менее, гораздо проще let ** \_variant\_t** управление **SafeArray**.


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

### <a name="using-property-getputputref"></a>С помощью свойства Get и Put/PutRef

В Visual Basic имя свойства не дополняется ли его получить, назначенных или назначенных ссылку.

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

В этом примере Visual C++ демонстрируется **Начало**/**поместить**/**PutRef *** свойство*.

> [!NOTE]
> Следующие замечания соответствуют закомментированного разделов в примере кода.

1. В этом примере используется два вида отсутствует строковый аргумент: явные константа, **strMissing**и строку, компилятор будет использовать для создания временного ** \_bstr\_t** , которая будет присутствовать для области метода **Open** .

2. Нет необходимости привести операнд rs -\>PutRefActiveConnection(cn) для (IDispatch \*), так как тип операнда уже (IDispatch \*).
    
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

### <a name="using-getitemx-and-itemx"></a>С помощью GetItem(x) и элемента\[x\]

В этом примере Visual Basic демонстрируется стандартный и альтернативный синтаксис ( **элемент**).

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

В этом примере Visual C++ **элемента**.

> [!NOTE]
> Следующее примечание соответствует комментариев для разделов в примере кода.

1. При доступе к коллекции с помощью **элемента**, индекса, **2**, необходимо привести к **времени** , вызывается соответствующий конструктор.
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Приведение указатели объект ADO с (IDispatch \*)

В следующем примере Visual C++ демонстрируется использование (IDispatch \*) для приведения указателей объектов ADO.

> [!NOTE]
> Следующие замечания соответствуют закомментированного разделов в примере кода.

1. Укажите open объекта **подключения** в явным образом закодированный **Variant**. Привести его с (IDispatch \*), будет вызываться надлежащий конструктор. Также, необходимо явно задать второй ** \_variant\_t** параметр со значением по умолчанию **значение true**, поэтому счетчик ссылок объекта будет правильный после завершения операции **Recordset::Open** .

2. Выражение (\_bstr\_t), не является приведения, но ** \_variant\_t** оператор, который извлекает ** \_bstr\_t** строку из **типа Variant** , возвращенное **значение**. Выражение (символ\*), не является приведения, но ** \_bstr\_t** оператор, который извлекает указатель инкапсулированное строку в ** \_bstr\_t** объекта. В этом разделе кода показаны некоторые полезные поведения ** \_variant\_t** и ** \_bstr\_t** операторы.
    
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

