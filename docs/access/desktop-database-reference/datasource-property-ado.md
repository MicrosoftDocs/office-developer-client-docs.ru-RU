---
title: Свойство DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700033"
---
# <a name="datasource-property-ado"></a>Свойство DataSource (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает объект, который содержит данные в виде объекта [набора записей](recordset-object-ado.md) .

## <a name="remarks"></a>Замечания

Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных. Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект **набора записей** *.*

Свойства **DataSource** и [DataMember](datamember-property-ado.md) должен использоваться вместе.

Объект, на который необходимо реализовать интерфейс **IDataSource** и должна содержать интерфейс **IRowset** .

**Использование**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
