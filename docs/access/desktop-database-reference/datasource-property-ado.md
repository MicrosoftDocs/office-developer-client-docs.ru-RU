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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294472"
---
# <a name="datasource-property-ado"></a>Свойство DataSource (ADO)


**Область применения**: Access 2013, Office 2013

Указывает объект, содержащий данные, которые должны быть представлены в виде объекта [Recordset](recordset-object-ado.md) .

## <a name="remarks"></a>Примечания

Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных. Среда данных поддерживает коллекции данных (источников данных), содержащие именованные объекты (*элементы данных*), которые будут представлены как объект **Recordset** *.*

Свойства [DataMember](datamember-property-ado.md) и **DataSource** должны использоваться совместно.

Объект, на который указывает ссылка, должен реализовать интерфейс **IDataSource** и должен содержать интерфейс **IRowset** .

**Usage**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
