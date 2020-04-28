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

Указывает имя элемента данных, который будет получен из объекта, на который ссылается свойство [DataSource](datasource-property-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение. Имя не задается с учетом регистра.

## <a name="remarks"></a>Примечания

Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных. Среда данных поддерживает коллекции данных (источников данных), содержащие именованные объекты (*элементы данных*), которые будут представлены как объект [Recordset](recordset-object-ado.md) *.*

Свойства **DataMember** и **DataSource** должны использоваться совместно.

Свойство **DataMember** определяет, какой объект, указанный в свойстве **DataSource** , будет представлен как объект **Recordset** . Перед заданием этого свойства необходимо закрыть объект **Recordset** . Ошибка создается, если свойство **DataMember** не задано до свойства **DataSource** , или если имя **DataMember** не распознается объектом, указанным в свойстве **DataSource** .

**Usage**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
