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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314016"
---
# <a name="type-property-ado"></a>Свойство Type (ADO)


**Область применения**: Access 2013, Office 2013

Указывает операционный тип или тип данных для [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или объекта [Property](property-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [DataTypeEnum](datatypeenum.md) .

## <a name="remarks"></a>Примечания

Для объектов **Parameter** свойство **Type** доступно для чтения и записи. Для новых **объектов Field** , добавленных в коллекцию Fields [](fields-collection-ado.md) [записи](record-object-ado.md), **тип** доступен для чтения и записи только после того, как было указано свойство [value](value-property-ado.md) для **поля** , и поставщик данных успешно Добавлено новое **поле** путем вызова метода [Update](update-method-ado.md) коллекции Fields. ****

Для всех остальных объектов свойство **Type** доступно только для чтения.

