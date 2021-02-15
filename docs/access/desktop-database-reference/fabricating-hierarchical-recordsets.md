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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293205"
---
# <a name="fabricating-hierarchical-recordsets"></a>Создание иерархических наборов записей


**Область применения**: Access 2013, Office 2013

В следующем примере показано, как сформировать иерархический набор записей без источника данных, используя грамматику формирования данных для определения столбцов для родительских, родительских и родительских и родительских наборов записей.

Чтобы сформировать иерархический набор записей, необходимо указать службу формирования данных Майкрософт для OLE DB (MSDataShape), а также указать значение поставщика данных NONE в параметре строки подключения метода Open объекта [Connection.](connection-object-ado.md) [](open-method-ado-connection.md) Дополнительные сведения см. в [подпукове "Необходимые поставщики для формирования данных".](required-providers-for-data-shaping.md)

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

После того **как набор записей** был сфабрикован, его можно заполнить, обухить или сохранить в файле.

