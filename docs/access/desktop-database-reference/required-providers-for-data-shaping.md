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

Для формирования данных обычно требуется два поставщика. Поставщик услуг, служба формирования данных для [OLE DB,](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)поставляет функции формирования данных, а поставщик данных, например поставщик OLE DB для SQL Server, поставляет ряды данных для заполнения сформированного [наборов записей](recordset-object-ado.md).

Имя поставщика услуг (MSDataShape) может быть указано как [](connection-object-ado.md) значение [](provider-property-ado.md) свойства поставщика объектов подключения или ключевое слово строки подключения "Provider=MSDataShape;".

Имя поставщика данных может быть указано как значение динамического свойства поставщика данных,  которое [](properties-collection-ado.md) добавляется в коллекцию свойств объектов подключения службой формирования данных для OLE DB или ключевым словом строки подключения "* Поставщик *данных=***provider".* 

Поставщик данных не требуется, если набор **записей** не заполнен (например,  как в сфабрикованном наборе записей, где столбцы создаются с помощью ключевого слова NEW). В этом случае укажите **"Поставщик данных=** нет;".

## <a name="example"></a>Пример

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

