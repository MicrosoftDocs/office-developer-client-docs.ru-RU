---
title: Свойство Type (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698255"
---
# <a name="type-property-ado"></a>Свойство Type (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает тип действующие или тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md) объекта.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [DataTypeEnum](datatypeenum.md) .

## <a name="remarks"></a>Замечания

Для **параметра** объектов свойство **Type** — чтение и запись. Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md) **Тип** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и поставщик данных имеет успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .

Для всех других объектов свойство **Type** — только для чтения.

