---
title: Свойство Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 7ab090dd6cf0b6e2676cf05907ac77c438f22652
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284822"
---
# <a name="recordsetfilter-property-dao"></a>Свойство Recordset.Filter (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, определяющее записи, включаемые в открытый впоследствии объект **Recordset** (только для рабочих областей Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* .Filter

*выражение*: выражение, возвращающее объект **Recordset**.

## <a name="remarks"></a>Примечания

Параметр или возвращаемое значение является строковым типом данных, содержащим предложение WHERE оператора SQL без зарезервированного слова WHERE.

Используйте свойство **Filter**, чтобы применить фильтр к объекту **Recordset** типа динамический набор, статический набор или однонаправленного типа.

Свойство **Filter** можно использовать для ограничения записей, возвращаемых из существующего объекта, если новый объект **Recordset** открыт на основе существующего объекта **Recordset**.

Используйте формат даты, принятый в США (месяц, день, год), при фильтрации полей, содержащих даты, даже если не используется версия ядра СУБД Microsoft Access для США (в этом случае необходимо вручную создать даты, сцепляя строки. Например: strMonth & "-" & strDay & "-" & strYear). В противном случае данные могут не отфильтроваться нужным образом.

Во многих случаях быстрее будет открыть новый объект **Recordset** с помощью оператора SQL, который включает предложение WHERE.

Если свойству присвоено значение строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия следующего объекта **Recordset**. Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.

## <a name="example"></a>Пример

В примере ниже показано, как использовать свойство Filter для определения записей, которые нужно включить в открываемый впоследствии объект Recordset.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
