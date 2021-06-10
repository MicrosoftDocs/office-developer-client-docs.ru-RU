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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294494"
---
# <a name="datamember-property-ado"></a>Свойство DataMember (ADO)

**Область применения**: Access 2013, Office 2013

Указывает имя участника данных, который будет извлечен из объекта, на который ссылается свойство [DataSource.](datasource-property-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **String.** Имя не является конфиденциальным.

## <a name="remarks"></a>Примечания

Это свойство используется для создания элементов управления, связанных с данными, с помощью среды данных. Среда данных поддерживает коллекции данных (источников данных), содержащих именуемые объекты *(участники* данных), которые будут представлены в качестве объекта [Recordset.](recordset-object-ado.md) 

Свойства **DataMember** и **DataSource** должны использоваться совместно.

Свойство **DataMember** определяет, какой объект, указанный **свойством DataSource,** будет представлен в качестве объекта **Recordset.** Объект **Recordset** должен быть закрыт до заданной цели. Ошибка создается, если свойство **DataMember** не задано перед свойством **DataSource** или если имя **DataMember** не распознается объектом, указанным в свойстве **DataSource.**

**Использование**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
