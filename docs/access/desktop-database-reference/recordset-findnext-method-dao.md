---
title: Метод Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300639"
---
# <a name="recordsetfindnext-method-dao"></a>Метод Recordset.FindNext (DAO)

**Область применения**: Access 2013, Office 2013

Определяет положение следующей записи в объекте **[Recordset](recordset-object-dao.md)** типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*expression* .FindNext(***Criteria***)

*expression*: переменная, представляющая объект **Recordset**.

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

Если в поиск нужно включить все записи, а не только те, которые удовлетворяют заданному условию, используйте методы **Move**, чтобы переходить между записями. Для поиска записи в объекте **Recordset** табличного типа используется метод **Seek**.

Если соответствующая условиям запись не найдена, то указатель текущей записи неизвестен, а свойству **NoMatch** присваивается значение **True**. Если набор записей содержит несколько записей, удовлетворяющих условиям, **FindFirst** находит первое вхождение, **FindNext** находит следующее вхождение и т. д.

В приведенной ниже таблице показано, с какого расположения и в каком направлении выполняют поиск разные методы **Find**.

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


Однако использование методов **Find** отличается от использования метода **Move**, который просто делает первую, последнюю, следующую или предыдущую запись текущей без указания условия. После операции Find можно выполнить операцию Move.

Всегда проверяйте значение свойства **NoMatch**, чтобы определить, успешно ли выполнена операция Find. Если поиск выполнен успешно, свойство **NoMatch** принимает значение **False**. Если поиск не дал результатов, то свойство **NoMatch** принимает значение **True**, а текущая запись не определяется. В этом случае необходимо вернуть указатель текущей записи к допустимой записи.

Использование методов **Find** с наборами записей, доступ к которым осуществляется через ODBC с подключением к ядру СУБД Microsoft Access, может быть неэффективным. Может оказаться, что изменение условий поиска определенной записи выполняется быстрее, особенно при работе с большими наборами записей.

В рабочей области ODBCDirect методы **Find** и **Seek** недоступны для объектов **Recordset** любых типов, так как выполнение методов **Find** и **Seek** через подключение ODBC по сети не очень эффективно. Вместо этого следует составить запрос (то есть использовать аргумент source метода **OpenRecordset**) с соответствующим предложением WHERE, благодаря которому будут возвращаться только записи, отвечающие условиям, которые в ином случае использовались бы в методе **Find** или **Seek**.

При работе с базами данных ODBC, подключенными к ядру СУБД Microsoft Access, и большими объектами типа "Динамический набор" может оказаться, что методы **Find** или свойства **Sort** и **Filter** работают медленно. Чтобы повысить производительность, используйте SQL-запросы с настроенными предложениями ORDER BY или WHERE, запросы параметров или объекты **QueryDef**, возвращающие определенные индексированные записи.

При поиске полей, содержащих даты, следует использовать формат даты, применяемый в США (месяц, день, год), даже если вы не используете версию ядра СУБД Microsoft Access для США. В противном случае данные могут быть не найдены. Используйте функцию **Format** в Visual Basic для преобразования даты. Пример:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Если условие состоит из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например запятую (примеры: strSQL = "PRICE \> " & lngPrice и lngPrice = 125,50), то при попытке вызова метода возникнет ошибка. Это связано с тем, что при объединении число будет преобразовано в строку при помощи используемого по умолчанию в вашей системе десятичного символа, а Microsoft Access SQL поддерживает только десятичные символы, используемые в США.

> [!NOTE]
> - Для оптимальной производительности *условия* должны быть представлены в форме "*поле* = *значение*" (где *поле* — это индексированное поле в базовой таблице) или "*поле* LIKE *префикс*", где *поле* — это индексированное поле в базовой таблице, а *префикс* — префикс строки поиска (например, "ART*").
> 
> - Как правило, для эквивалентных типов поиска метод **Seek** обеспечивает более высокую производительность, чем метод **Find**. При этом предполагается, что для ваших потребностей будет достаточно объектов **Recordset** табличного типа.


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
