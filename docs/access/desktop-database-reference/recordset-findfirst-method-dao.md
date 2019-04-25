---
title: Метод Recordset.FindFirst (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b2e334dcad84d2a9c3441e76e6552c1cb04f8552
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300534"
---
# <a name="recordsetfindfirst-method-dao"></a>Метод Recordset.FindFirst (DAO)

**Область применения**: Access 2013, Office 2013

Определяет положение первой записи в объекте **Recordset** типа "Динамический набор" или "Статический набор", которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* .FindFirst(***Criteria***)

*выражение*: переменная, представляющая объект **Recordset**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Criteria</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Строка, используемая для поиска записи. Аналогично предложению WHERE в инструкции SQL, но без слова WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если нужно включить все записи в поиск, а не только те, которые удовлетворяют заданному условию, используйте методы **Move**, чтобы переходить между записями. Для поиска записи в объекте **Recordset** табличного типа используется метод **Seek**.

Если запись, соответствующая условиям, не найдена, указатель текущей записи неизвестен, а свойству **NoMatch** присваивается значение **True**. Если набор записей содержит несколько записей, удовлетворяющих условиям, **FindFirst** находит первое вхождение, **FindNext** находит следующее вхождение и т. д.

Каждый метод **Find** начинает поиск из расположения и в направлении, указанных в следующей таблице.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Метод Find</p></th>
<th><p>Начало поиска</p></th>
<th><p>Направление поиска</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Начало набора записей</p></td>
<td><p>Конец набора записей</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Конец набора записей</p></td>
<td><p>Начало набора записей</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Текущая запись</p></td>
<td><p>Конец набора записей</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Текущая запись</p></td>
<td><p>Начало набора записей</p></td>
</tr>
</tbody>
</table>


Однако использование методов **Find** отличается от использования метода **Move**, который просто делает первую, последнюю, следующую или предыдущую запись текущей без указания условия. Операцию Move можно выполнять вслед за операцией Find.

Всегда проверяйте значение свойства **NoMatch**, чтобы определить, выполнена ли операция Find успешно. Если поиск выполнен успешно, свойство **NoMatch** имеет значение **False**. Если поиск завершился безуспешно, свойство **NoMatch** имеет значение **True**, а текущая запись не определена. В этом случае необходимо вернуть указатель текущей записи к допустимой записи.

Использование методов **Find** с наборами записей, которые доступны с помощью ODBC с подключением к ядру СУБД Microsoft Access, может быть неэффективным. Может оказаться, что изменение условий поиска определенной записи выполняется быстрее, особенно при работе с большими наборами записей.

При работе с базами данных ODBC, подключенными к ядру СУБД Microsoft Access, и большими объектами **Recordset** типа "Динамический набор" можно обнаружить, что использование методов **Find** или свойств **Sort** и **Filter** выполняется медленно. Чтобы повысить производительность, используйте запросы SQL с настроенными предложениями ORDER BY или WHERE, запросы параметров или объекты **QueryDef**, возвращающие определенные индексированные записи.

Следует использовать формат даты, применяемый в США (месяц, день, год), при поиске полей, содержащих даты, даже если вы не используете версию ядра СУБД Microsoft Access для США; в противном случае данные могут быть не найдены. Используйте функцию **Format** в Visual Basic для преобразования даты. Например:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Если условие состоит из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (например, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), возникает ошибка при попытке вызова метода. Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.


> [!NOTE]
> - Для оптимальной производительности *условия* должны быть представлены в форме "*поле* = *значение*", где *поле* является индексированным полем в базовой таблице, или "*поле* LIKE *префикс*", где *поле* — это индексированное поле в базовой таблице, а *префикс* — префикс строки поиска (например, "ART*").
> 
> - Как правило, для эквивалентных типов поиска метод **Seek** обеспечивает более высокую производительность, чем метод **Find**. При этом предполагается, что объекты **Recordset** табличного типа могут в одиночку удовлетворить ваши потребности.


## <a name="example"></a>Пример

В приведенном ниже примере показано, как использовать методы FindFirst и FindNext для поиска записи в Recordset.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
