---
title: Тип свойства (ADO)
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
# <a name="type-property-ado"></a>Тип свойства (ADO)


**Область применения**: Access 2013, Office 2013

Указывает тип или тип данных объекта [Параметр,](parameter-object-ado.md) [Поле](field-object-ado.md)или [Свойство.](property-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение [DataTypeEnum.](datatypeenum.md)

## <a name="remarks"></a>Примечания

Для **объектов Parameter** свойство **Type** — это чтение и записи. Для новых  объектов [](value-property-ado.md) **Field,** которые были [](fields-collection-ado.md) добавлены в  коллекцию Полей записи, тип  считываю и записываю только после того, как будет задано свойство Value для поля и поставщик данных успешно добавил новое поле, назвав метод [Update](update-method-ado.md) коллекции [](record-object-ado.md) **Fields.**

Для всех остальных объектов **свойство Type** является только для чтения.

