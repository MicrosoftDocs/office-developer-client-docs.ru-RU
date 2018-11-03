---
title: Fabricating иерархические наборы записей
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 302ca12b96317cdb203b2091c2b2da916188175a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943964"
---
# <a name="fabricating-hierarchical-recordsets"></a><span data-ttu-id="c2eeb-102">Fabricating иерархические наборы записей</span><span class="sxs-lookup"><span data-stu-id="c2eeb-102">Fabricating hierarchical Recordsets</span></span>


<span data-ttu-id="c2eeb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2eeb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2eeb-104">Следующем примере показано, как для создания иерархической записей без источника данных с помощью формирования грамматики определение столбцов для родительских, дочерних и котором **наборов записей**данных.</span><span class="sxs-lookup"><span data-stu-id="c2eeb-104">The following example shows how to fabricate a hierarchical Recordset without an underlying data source by using the data shaping grammar to define columns for parent, child, and grandchild **Recordsets**.</span></span>

<span data-ttu-id="c2eeb-105">Для создания иерархической **записей**, необходимо указать служба Microsoft формирования данных для OLE DB (MSDataShape), и можно указать поставщика данных значение NONE в параметрах строки подключения из объект [подключения](connection-object-ado.md) [Open](open-method-ado-connection.md) метод.</span><span class="sxs-lookup"><span data-stu-id="c2eeb-105">To fabricate a hierarchical **Recordset**, you must specify the Microsoft Data Shaping Service for OLE DB (MSDataShape), and you may specify a Data Provider value of NONE in the connection string parameter of the [Connection](connection-object-ado.md) object's [Open](open-method-ado-connection.md) method.</span></span> <span data-ttu-id="c2eeb-106">Для получения дополнительных сведений см [Требуется поставщиков для формирования данных](required-providers-for-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="c2eeb-106">For more information, see [Required Providers for Data Shaping](required-providers-for-data-shaping.md).</span></span>

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

<span data-ttu-id="c2eeb-107">После **набора записей** был целью, его можно заполняются, таким образом или сохранено в файле.</span><span class="sxs-lookup"><span data-stu-id="c2eeb-107">After the **Recordset** has been fabricated, it can be populated, manipulated, or persisted to a file.</span></span>

