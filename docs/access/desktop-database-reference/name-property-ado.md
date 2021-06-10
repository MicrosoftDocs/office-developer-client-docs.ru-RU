---
title: Свойство Name (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288667"
---
# <a name="name-property-ado"></a>Свойство Name (ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **String,** которое указывает имя объекта.

## <a name="remarks"></a>Примечания

Используйте свойство **Name,** чтобы назначить имя или получить имя объекта **Command,** **Property,** **Field** или **Parameter.**

Значение — чтение или записи на **объекте Command** и только чтение на **объекте Property.**

Для объекта **Field** **имя** обычно только для чтения. Однако для новых  объектов [](value-property-ado.md) **Field,** которые были [](fields-collection-ado.md) добавлены в  коллекцию Полей записи, имя  считывалось или записывалось только после того, как было задано свойство Value для поля и поставщик данных успешно добавил новое поле, позвонив методу [Update](update-method-ado.md) коллекции [](record-object-ado.md) **Fields.**

Для **объектов Parameter,** которые еще не примыкают к коллекции [Параметры,](parameters-collection-ado.md) свойство **Name** читается или записи. Для объектов **параметра и** всех остальных объектов свойство **Name** доступно только для чтения. Имена не должны быть уникальными в коллекции.

Свойство **Name** объекта можно получить по порядковой ссылке, после чего можно обратиться к объекту напрямую по имени. Например, если rstMain.Properties (20). Имя дает updatability , вы можете впоследствии ссылаться на это свойство как уступает updatability , вы можете впоследствии ссылаться на это свойство как rstMain.Properties ("Updatability") .

