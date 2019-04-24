---
title: Необходимые поставщики для формирования данных
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306659"
---
# <a name="required-providers-for-data-shaping"></a>Необходимые поставщики для формирования данных

**Область применения**: Access 2013, Office 2013

Для формирования данных обычно требуются два поставщика. Поставщик услуг, [Служба формирования данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), возможность формирования данных и поставщик данных, например поставщик OLE DB для SQL Server, предоставляет строки данных для заполнения объекта [Recordset](recordset-object-ado.md)в форме.

Имя поставщика услуг (Мсдаташапе) можно указать в качестве значения свойства [поставщика](provider-property-ado.md) объекта [подключения](connection-object-ado.md) или строки подключения "Provider = мсдаташапе;".

Имя поставщика данных можно указать в качестве значения динамического свойства **поставщика данных** , которое добавляется в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** службой формирования данных для OLE DB или зарезервированным словом строки подключения "* *Поставщик данных = * * * поставщик*".

Поставщик данных не нужен, если **набор записей** не заполняется (например, как в созданном **наборе записей** , где столбцы создаются с помощью ключевого слова New). В этом случае укажите "**Data Provider =** None;".

## <a name="example"></a>Пример

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

