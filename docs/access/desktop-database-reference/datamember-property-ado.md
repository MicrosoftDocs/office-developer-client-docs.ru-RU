---
title: Свойство DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 410f11af8daf3912dca9dc78a1cb9216ff8f8dd1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719885"
---
# <a name="datamember-property-ado"></a>Свойство DataMember (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает имя элемента данных, который извлекается из объекта ссылается свойство [DataSource](datasource-property-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение. Имя не учитывают регистр.

## <a name="remarks"></a>Замечания

Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных. Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект [набора записей](recordset-object-ado.md) *.*

Свойства **DataSource** и **DataMember** должен использоваться вместе.

Свойство **DataMember** определяет, какие объекта, заданного в свойстве **DataSource** будут представлены как объект **набора записей** . Объект **набора записей** должны быть закрыты, это свойство задано. Ошибка создается в том случае, если свойство **DataMember** не будет установлено перед свойства **источника данных** или имя **DataMember** не распознается объектом, указанных в свойстве **DataSource** .

**Использование**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
