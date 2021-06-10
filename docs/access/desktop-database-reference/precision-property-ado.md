---
title: Свойство Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287477"
---
# <a name="precision-property-ado"></a>Свойство Precision (ADO)


**Область применения**: Access 2013, Office 2013

Указывает степень точности числимых значений в объекте [Parameter](parameter-object-ado.md) или числовые объекты [Field.](field-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Byte,** которое указывает максимальное число цифр, используемых для представления значений.

## <a name="remarks"></a>Примечания

Используйте свойство **Precision,** чтобы определить максимальное число цифр, используемых для представления значений для численного объекта **Параметр** или **Поле.**

Значение — чтение или записи на **объекте Параметр.**

Для объекта **Field** **точность** обычно только для чтения. Однако для новых  объектов [](value-property-ado.md)  **Field,** которые были [](fields-collection-ado.md) добавлены в  коллекцию Полей записи, [](record-object-ado.md)точность считывалась или записывалась только после того, как было задано свойство Value для поля и поставщик данных успешно добавил новое поле, позвонив [методу Update](update-method-ado.md) коллекции **Fields.**

