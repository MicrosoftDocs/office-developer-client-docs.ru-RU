---
title: Создание иерархических наборов записей
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f644f25a04c5573a93aa106884473fed6b45440e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715580"
---
# <a name="fabricating-hierarchical-recordsets"></a>Создание иерархических наборов записей


**Применимо к**: Access 2013, Office 2013

Следующем примере показано, как для создания иерархической записей без источника данных с помощью формирования грамматики определение столбцов для родительских, дочерних и котором **наборов записей**данных.

Для создания иерархической **записей**, необходимо указать служба Microsoft формирования данных для OLE DB (MSDataShape), и можно указать поставщика данных значение NONE в параметрах строки подключения из объект [подключения](connection-object-ado.md) [Open](open-method-ado-connection.md) метод. Для получения дополнительных сведений см [Требуется поставщиков для формирования данных](required-providers-for-data-shaping.md).

```vb
    Dim cn As New ADODB.Connection
    Dim rsCustomers As New ADODB.Recordset
    
    cn.Open "Provider=MSDataShape;Data Provider=NONE;"
     
    strShape = _
    "SHAPE APPEND NEW adInteger AS CustID," & _
                " NEW adChar(25) AS FirstName," & _
                " NEW adChar(25) AS LastName," & _
                " NEW adChar(12) AS SSN," & _
                " NEW adChar(50) AS Address," & _
             " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                            " NEW adInteger AS CustID," & _
                            " NEW adChar(20) AS BodyColor, " & _
                         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                                        " NEW adChar(20) AS Make, " & _
                                        " NEW adChar(20) AS Model," & _
                                        " NEW adChar(4) AS Year) " & _
                            " AS VINS RELATE VIN_NO TO VIN_NO))" & _
                " AS Vehicles RELATE CustID TO CustID) "
     
    rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1
```

После **набора записей** был целью, его можно заполняются, таким образом или сохранено в файле.

