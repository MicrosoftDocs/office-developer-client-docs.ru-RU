---
title: Использование расширений Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312063"
---
# <a name="using-visual-c-extensions"></a>Использование расширений Visual C++


**Область применения**: Access 2013, Office 2013

## <a name="the-iadorecordbinding-interface"></a>Интерфейс IADORecordBinding

Расширения Microsoft Visual C++ для ADO связывают поля объекта [Recordset](recordset-object-ado.md) с переменными C/C++. При внесении изменений в текущую строку привязанного наборов **записей** все связанные поля в наборе **записей** копируется в переменные C/C++. При необходимости скопированные данные преобразуются в объявленный тип данных переменной C/C++.

Метод **BindToRecordset** интерфейса **IADORecordBinding** привязывает поля к переменным C/C++. Метод **AddNew** добавляет новую строку в привязанный **набор записей.** Метод **Update** заполняет поля в новых строках наборов **записей** или обновляет поля в существующих строках значением переменных C/C++.

Интерфейс **IADORecordBinding** реализуется **объектом Recordset.** Вы не кодировать реализацию самостоятельно.

## <a name="binding-entries"></a>Привязка записей

Поля карты Visual C++ для ADO объекта [Recordset](recordset-object-ado.md) с переменными C/C++. Определение сопоставления между полем и переменной называется *записью привязки.* Макрос предоставляет записи привязки для числовой, фиксированной длины и переменной длины данных. Записи привязки и переменные C/C++ объявляются в классе, производном от класса Visual C++ **Extensions, CADORecordBinding.** Класс **CADORecordBinding** определяется внутренним образом макросами записи привязки.

ADO внутренне соповедет параметры в этих макросах со структурой **DBBINDING** OLE DB и создает объект OLE DB **Accessor** для управления перемещением и преобразованием данных между полями и переменными. OLE DB определяет данные как состоящие из трех частей: *буфера,* в котором хранятся данные; *состояние,* которое указывает, было ли поле успешно сохранено в буфере или как переменная должна быть восстановлена в поле; и *длина* данных. (Дополнительные сведения см. в справочнике программиста *по OLE DB*, глава 6. Получение и настройка данных.)

## <a name="header-file"></a>Файл загона

Включите в приложение следующий файл, чтобы использовать расширения Visual C++ для ADO:

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Поля наборов записей привязки

**Привязка полей recordset к переменным C/C++**

1.  Создайте класс, производный от **класса CADORecordBinding.**

2.  Укажите записи привязки и соответствующие переменные C/C++ в производного класса. Прикрепить записи привязки между **МАКРОСАМИ BEGIN \_ ADO \_ BINDING** и **END \_ ADO \_ BINDING.** Не прерывать макрос запятой или запятой. Соответствующие селитари автоматически заданы каждым макросом. Укажите одну запись привязки для каждого поля, соедино с переменной C/C++. Используйте соответствующий член из семейства макроса **ADO \_ FIXED LENGTH \_ \_ ENTRY,** **ADO \_ NUMERIC \_ ENTRY** или **ADO VARIABLE LENGTH \_ \_ \_ ENTRY.**

3.  В приложении создайте экземпляр класса, производный от **CADORecordBinding.** Получите интерфейс **IADORecordBinding** из **recordset.** Затем вызовите метод **BindToRecordset,** чтобы привязать поля **Recordset** к переменным C/C++.

Дополнительные сведения см. в примере расширений [Visual C++.](visual-c-extensions-example.md)

## <a name="interface-methods"></a>Методы интерфейса

Интерфейс **IADORecordBinding** имеет три метода: **BindToRecordset,** **AddNew** и **Update.** Единственным аргументом для каждого метода является указатель на экземпляр класса, производный от **CADORecordBinding.** Поэтому методы **AddNew** и **Update** не могут указывать параметры имен методов ADO.

**Синтаксис**

Метод **BindToRecordset** связывает поля **Recordset** с переменными C/C++.

`BindToRecordset(CADORecordBinding *binding)` 

Метод **AddNew** вызывает именовую строку, метод ADO [AddNew,](addnew-method-ado.md) чтобы добавить новую строку в **recordset.**

`AddNew(CADORecordBinding *binding)` 

Метод **Update** вызывает имя , метод ADO [Update,](update-method-ado.md) для обновления **recordset**.

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>Макрос записи привязки

Макрос записи привязки определяет связь поля **Recordset** и переменной. В начале и конце макроса набор записей привязки размесков.

Семейства макроса предоставляются для данных фиксированной длины, таких как **adDate** или **adBoolean;** числовая информация, например **adTinyInt,** **adInteger** или **adDouble;** и данные переменной длины, такие как **adChar,** **adVarChar** или **adVarBinary.** Все числимые типы, кроме **adVarNumeric,** также являются типами фиксированной длины. Каждое семейство имеет разные наборы параметров, поэтому можно исключить не интересующие вас сведения о привязке.

Дополнительные сведения см. в справочнике программиста *OLE DB,* приложении А. Типы данных.

_**Начало записей привязки**_

**BEGIN \_ ADO \_ BINDING**(*Class)*

_**Данные фиксированной длины**_

**ADO \_ FIXED \_ LENGTH \_ ENTRY**(*Ordinal, DataType, Buffer, Status, Modify)*  
**ADO \_ FIXED \_ LENGTH \_ ENTRY2**(*Ordinal, DataType, Buffer, Modify)*

_**Числовая информация**_

**ADO \_ NUMERIC \_ ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify)*  
**ADO \_ NUMERIC \_ ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify)*

_**Данные переменной длины**_

**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ЗАПИСИ**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify)*  
**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify)*  
**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify)*  
**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify)*

_**Конечные записи привязки**_

**END \_ ADO \_ BINDING**()

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Class</em></p></td>
<td><p>Класс, в котором определены записи привязки и переменные C/C++.</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>Порядковая цифра, отсчитывая от одного поля <strong>Recordset,</strong> соответствующего переменной C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>Эквивалентный тип данных ADO переменной C/C++ (список допустимых типов данных см. в <a href="datatypeenum.md">dataTypeEnum).</a> Значение поля <strong>Recordset</strong> при необходимости будет преобразовано в этот тип данных.</p></td>
</tr>
<tr class="even">
<td><p><em>Буфер</em></p></td>
<td><p>Имя переменной C/C++, в которой будет храниться поле <strong>Recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><em>Размер</em></p></td>
<td><p>Максимальный размер буфера в <em>ветвях.</em> Если <em>буфер</em> будет содержать строку переменной длины, опустоните ноль.</p></td>
</tr>
<tr class="even">
<td><p><em>Состояние</em></p></td>
<td><p>Имя переменной, которая указывает, допустимо <em></em> ли содержимое буфера, и успешно ли преобразование поля <em>в DataType.</em> Два наиболее важных значения для этой переменной <strong>adFldOK</strong>, что означает успешное преобразование; и <strong>adFldNull</strong>, что означает, что значение поля будет вариантом типа VT_NULL а не просто пустым. Возможные значения для <em>состояния</em> перечислены в следующей таблице, &quot; "Значения состояния".&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modify</em></p></td>
<td><p>Boolean flag; Если задается значение TRUE, ADO разрешается обновлять соответствующее поле <strong>Recordset</strong> со значением в <em>буфере.</em> Задайте для параметра Boolean <em>modify</em> true, чтобы включить ADO для обновления привязанного поля, и FALSE, если вы хотите изучить поле, но не изменять его.</p></td>
</tr>
<tr class="even">
<td><p><em>Точность</em></p></td>
<td><p>Число цифр, которые могут быть представлены в числовой переменной.</p></td>
</tr>
<tr class="odd">
<td><p><em>Масштабирование</em></p></td>
<td><p>Количество десятичных цифр в числовом переменных.</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p>Имя четырех byte переменной, которая будет содержать фактическую длину данных в <em>буфере.</em></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Значения состояния

Значение переменной *Status* указывает, было ли поле успешно скопировано в переменную.

При настройке данных *для параметра Status* может быть установлено состояние **adFldNull,** чтобы указать, что для поля **Recordset** должно быть установлено null.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Возвращено ненулевом значение поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldBadAccessor</strong></p></td>
<td><p>1 </p></td>
<td><p>Привязка недействительна.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldCantConvertValue</strong></p></td>
<td><p>2 </p></td>
<td><p>Значение не может быть преобразовано по другим причинам, кроме несоответствия подписи или переполнения данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>3 </p></td>
<td><p>При получении поля указывает, что возвращено значение null. При настройке поля указывает, что для поля необходимо установить <strong>NULL,</strong> если это поле не может закодировать само <strong>NULL</strong> (например, массив символов или целый ряд).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldTruncated</strong></p></td>
<td><p>4 </p></td>
<td><p>Данные переменной длины или цифры были усечены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSignMismatch</strong></p></td>
<td><p>5 </p></td>
<td><p>Значение подписано, а тип данных переменной — нет.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldDataOverFlow</strong></p></td>
<td><p>6 </p></td>
<td><p>Значение больше, чем может храниться в переменном типе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldCantCreate</strong></p></td>
<td><p>7 </p></td>
<td><p>Неизвестный тип столбца и поле уже открыты.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnavailable</strong></p></td>
<td><p>8 </p></td>
<td><p>Не удалось определить значение поля, например в новом ненаписаном поле без значения по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldPermissionDenied</strong></p></td>
<td><p>9 </p></td>
<td><p>При обновлении нет разрешения на написание данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIntegrityViolation</strong></p></td>
<td><p>10 </p></td>
<td><p>При обновлении значение поля нарушает целостность столбцов.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>При обновлении значение поля нарушает схему столбца.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldBadStatus</strong></p></td>
<td><p>12 </p></td>
<td><p>При обновлении недопустимый параметр состояния.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldDefault</strong></p></td>
<td><p>13 </p></td>
<td><p>При обновлении использовалось значение по умолчанию.</p></td>
</tr>
</tbody>
</table>

