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

Поля Microsoft Visual C++ для партнеров ADO или привязки полей объекта [Recordset](recordset-object-ado.md) к переменным C/C++. Всякий раз, когда меняется текущая строка связанного **recordset,** все связанные поля в **Наборе** записей копируется в переменные C/C++. При необходимости копируемые данные преобразуются в объявленный тип данных переменной C/C++.

Метод **BindToRecordset** **интерфейса IADORecordBinding** связывает поля с переменными C/C++. Метод **AddNew добавляет** новую строку в связанный **Набор записей.** Метод **Update** заполняет поля в новых строках **Recordset** или обновляет поля в существующих строках со значением переменных C/C++.

Интерфейс **IADORecordBinding** реализуется объектом **Recordset.** Вы не кодировать реализацию самостоятельно.

## <a name="binding-entries"></a>Привязка записей

Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. Определение сопоставления между полем и переменной называется *привязкой.* Макрос обеспечивает привязку записей для числовой, фиксированной длины и переменной длины данных. Записи привязки и переменные C/C++ объявляются в классе, полученном из класса Visual C++ Extensions, **CADORecordBinding.** Класс **CADORecordBinding** определяется внутренними макросами записи привязки.

Внутренний объект ADO создает параметры в этих макросах в структуру **DBBINDING** OLE DB и создает объект OLE DB **Accessor** для управления перемещением и преобразованием данных между полями и переменными. OLE DB определяет данные как состоящие  из трех частей: буфера, в котором хранятся данные; *состояние,* которое указывает, было ли поле успешно сохранено в буфере или как переменная должна быть восстановлена в поле; и *длина* данных. (См. справку *программиста OLE DB,* главу 6: получение и настройку данных для получения дополнительных сведений.)

## <a name="header-file"></a>Файл загона

Включите в приложение следующий файл, чтобы использовать расширения Visual C++ для ADO:

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Поля привязки recordset

**Привязка полей recordset к переменным C/C++**

1.  Создание класса, полученного из **класса CADORecordBinding.**

2.  Укажите обязательные записи и соответствующие переменные C/C++ в полученном классе. Скобка привязки записей **между BEGIN \_ ADO \_ BINDING** и **END \_ ADO \_ BINDING** макрос. Не прекращать макрос запятой или запятой. Соответствующие делимитеры автоматически заданы каждым макросом. Укажите одну привязку для каждого поля, который будет соеди-ться с переменной C/C++. Используйте соответствующий член из семейства макрос **ADO \_ FIXED LENGTH \_ \_ ENTRY,** **ADO \_ NUMERIC \_ ENTRY** или **ADO VARIABLE LENGTH \_ \_ \_ ENTRY.**

3.  В приложении создайте экземпляр класса, полученный из **CADORecordBinding.** Получите **интерфейс IADORecordBinding** из **Recordset.** Затем позвоните **методу BindToRecordset,** чтобы привязать поля **Recordset** к переменным C/C++.

Дополнительные сведения см. в примере Visual [C++ Extensions.](visual-c-extensions-example.md)

## <a name="interface-methods"></a>Методы интерфейса

Интерфейс **IADORecordBinding имеет** три метода: **BindToRecordset,** **AddNew** и **Update.** Единственным аргументом для каждого метода является указатель экземпляра класса, полученного из **CADORecordBinding.** Поэтому методы **AddNew** и **Update** не могут указывать ни один из параметров тезки метода ADO.

**Синтаксис**

Метод **BindToRecordset связывает** поля **Recordset** с переменными C/C++.

`BindToRecordset(CADORecordBinding *binding)` 

Метод **AddNew вызывает** своего тезку, метод ADO [AddNew,](addnew-method-ado.md) чтобы добавить новую строку в **Набор записей.**

`AddNew(CADORecordBinding *binding)` 

Метод **Update** вызывает своего тезку, метод ADO [Update,](update-method-ado.md) для обновления **наборов записей.**

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>Привязка Макрос входа

Макрос привязки для записи определяет связь поля **Recordset** и переменной. Начало и окончание макроса делимитовывает набор обязательных записей.

Семьи макрос предоставляются для данных фиксированной длины, таких как **adDate** или **adBoolean;** числовая информация, например **adTinyInt,** **adInteger** или **adDouble;** и данные переменной длины, такие как **adChar,** **adVarChar** или **adVarBinary.** Все числимые типы, за исключением **adVarNumeric,** также являются типами фиксированной длины. Каждая семья имеет различные наборы параметров, чтобы исключить связывающие сведения, которые не являются интересующими.

Дополнительные сведения см. в справке программиста *OLE DB,* приложении A: Типы данных.

_**Начало обязательных записей**_

**BEGIN \_ ПРИВЯЗКА \_ ADO***(Класс)*

_**Данные фиксированной длины**_

**ADO \_ ЗАПИСЬ \_ \_ ФИКСИРОВАННОЙ ДЛИНЫ***(Ordinal, DataType, Buffer, Status, Modify)*  
**ADO \_ FIXED \_ LENGTH \_ ENTRY2***(Ordinal, DataType, Buffer, Modify)*

_**Числовая информация**_

**ADO \_ NUMERIC \_ ENTRY***(Ordinal, DataType, Buffer, Precision, Scale, Status, Modify)*  
**ADO \_ NUMERIC \_ ENTRY2***(Ordinal, DataType, Buffer, Precision, Scale, Modify)*

_**Данные переменной длины**_

**ADO \_ ЗАПИСЬ \_ VARIABLE \_ LENGTH***(Ordinal, DataType, Buffer, Size, Status, Length, Modify)*  
**ADO \_ VARIABLE \_ LENGTH \_ ENTRY2***(Ordinal, DataType, Buffer, Size, Status, Modify)*  
**ADO \_ VARIABLE \_ LENGTH \_ ENTRY3***(Ordinal, DataType, Buffer, Size, Length, Modify)*  
**ADO \_ VARIABLE \_ LENGTH \_ ENTRY4***(Ordinal, DataType, Buffer, Size, Modify)*

_**Конечные записи привязки**_

**END \_ ПРИВЯЗКА \_ ADO**()

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
<td><p>Класс, в котором определяются записи привязки и переменные C/C++.</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>Эквивалентный тип данных ADO переменной C/C++ (см. <a href="datatypeenum.md">dataTypeEnum</a> для списка допустимых типов данных). При необходимости значение поля <strong>Recordset</strong> будет преобразовано в этот тип данных.</p></td>
</tr>
<tr class="even">
<td><p><em>Буфер</em></p></td>
<td><p>Имя переменной C/C++, в которой будет храниться поле <strong>Recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><em>Размер</em></p></td>
<td><p>Максимальный размер в bytes of <em>Buffer</em>. Если <em>буфер</em> будет содержать строку переменной длины, упустим место для завершаемого нуля.</p></td>
</tr>
<tr class="even">
<td><p><em>Состояние</em></p></td>
<td><p>Имя переменной, которая будет указывать, допустимо ли содержимое <em>буфера</em> и успешно ли было преобразование поля <em>в DataType.</em> Двумя наиболее важными значениями для этой переменной являются <strong>adFldOK,</strong>что означает успешное преобразование; <strong>и adFldNull</strong>, что означает, что значение поля будет ВАРИАНТ типа VT_NULL а не просто пустой. Возможные значения <em>состояния</em> перечислены в следующей таблице &quot; , Значения состояния.&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modify</em></p></td>
<td><p>флаг Boolean; если ЗНАЧЕНИЕ TRUE указывает, что ADO разрешено обновлять соответствующее поле <strong>Recordset</strong> со значением, содержащеся в <em>буфере.</em> Установите параметр Изменения <em></em> Boolean в TRUE, чтобы включить ADO для обновления связанного поля и FALSE, если вы хотите изучить поле, но не изменить его.</p></td>
</tr>
<tr class="even">
<td><p><em>Точность</em></p></td>
<td><p>Количество цифр, которые могут быть представлены в числовом переменном.</p></td>
</tr>
<tr class="odd">
<td><p><em>Scale</em></p></td>
<td><p>Количество десятичных мест в числовом переменной.</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p>Имя переменной из четырех byte, которая будет содержать фактическую длину данных в <em>буфере.</em></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Значения состояния

Значение переменной *Status* указывает, было ли поле успешно скопировано на переменную.

При настройке данных *состояние* может быть назначено **adFldNull,** чтобы указать, что поле **Recordset** должно быть настроено на null.

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
<td><p>Было возвращено значение поля non-null.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldBadAccessor</strong></p></td>
<td><p>1</p></td>
<td><p>Привязка была недействительной.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Значение не может быть преобразовано по другим причинам, кроме несоответствия знака или переполнения данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>3</p></td>
<td><p>При получении поля указывается, что было возвращено значение null. При настройке поля указывается, что поле должно быть настроено на <strong>NULL,</strong> если поле не может кодировать <strong>сам NULL</strong> (например, массив символов или целый ряд).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldTruncated</strong></p></td>
<td><p>4 </p></td>
<td><p>Данные переменной длины или численные цифры были усечены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSignMismatch</strong></p></td>
<td><p>5 </p></td>
<td><p>Значение подписывало, а тип переменных данных не подписывался.</p></td>
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
<td><p>Значение поля не удалось определить — например, в новом, не назначенном поле без значения по умолчанию.</p></td>
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
<td><p>При обновлении недействительный параметр состояния.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>При обновлении использовалось значение по умолчанию.</p></td>
</tr>
</tbody>
</table>

