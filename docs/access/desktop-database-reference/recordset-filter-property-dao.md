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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711709"
---
# <a name="recordsetfilter-property-dao"></a>Свойство Recordset.Filter (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, определяющее записей, включенных в последующем открытого объекта **набора записей** (только для рабочих областей Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Фильтр

*выражение* Выражение, возвращающее объект **набора записей** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение имеет тип данных String, содержащий предложение WHERE инструкции SQL без зарезервированные слова WHERE.

Используйте свойство **фильтра** для применения фильтра к динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип.

Свойство **фильтра** для ограничения записей, возвращенных из существующего объекта при открытии нового объекта **набора записей** на основе существующего объекта **набора записей** .

Использовать формат даты США (месяц день года) при фильтрации полей с датами, даже в том случае, если вы не используете США версия ядра базы данных Microsoft Access (в этом случае необходимо собрать дат с объединения строк, например, strMonth & «-» _ aMP_ strDay & «-» & strYear). В противном случае данные могут фильтрация не должным образом.

Во многих случаях это быстрее, чтобы открыть новый объект **набора записей** с помощью инструкции SQL, которая включает в себя предложение WHERE.

Если свойству присвоено значение string, объединяется с не – целое значение и системных параметров укажите десятичных знаков например запятыми (, например strFilter = «PRICE \> "& lngPrice и lngPrice = 125,50), возникает ошибка при попытке Откройте следующий **набор записей**. Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.

## <a name="example"></a>Пример

В следующем примере показано, как использовать свойство фильтр для определения записей, включаемых в последующем открыт записей.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
