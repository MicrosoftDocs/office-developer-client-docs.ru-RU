---
title: Свойство DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a6b889deb9ccf713c2313b207387be8f6b1681b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868163"
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
