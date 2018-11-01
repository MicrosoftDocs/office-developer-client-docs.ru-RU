---
title: Свойство DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eebd4e485c358ed141e6bcb5dc84c82d41fd88ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870151"
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
