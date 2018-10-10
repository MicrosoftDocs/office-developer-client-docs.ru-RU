---
title: Required Providers for Data Shaping
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41b8c7b34aa8a0da7a360dbdca5b396bb9f2b4b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482892"
---
# <a name="required-providers-for-data-shaping"></a>Required Providers for Data Shaping


**Применимо к**: Access 2013 | Office 2013

Формирование данных обычно требуется двух поставщиков. Поставщик услуг [Служба формирования данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)предоставляет функциональные возможности формирования данных и поставщика данных, таких как поставщик OLE DB для SQL Server предоставляет строк данных для заполнения формы [набора записей](recordset-object-ado.md).

Имя поставщика услуг (MSDataShape) можно указать в качестве значения свойства [подключения](connection-object-ado.md) объект [поставщика](provider-property-ado.md) или ключевое слово строки подключения «поставщик MSDataShape; =».

Имя поставщика данных можно указать в качестве значения свойства динамического **Поставщика данных** , которое добавляется объект **подключения** коллекции [свойств](properties-collection-ado.md) службой формирования данных для OLE DB или ключевое слово строки подключения «* *Поставщик данных = *** поставщика*«.

Поставщик данных не является обязательным, если не содержит **записей** (например, как и создано **записей** место, где столбцы создаются с помощью нового ключевого слова). В этом случае указать "**Поставщик данных =** none;».

## <a name="example"></a>Пример

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

