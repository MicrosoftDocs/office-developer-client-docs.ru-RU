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

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** которая указывает имя объекта.

## <a name="remarks"></a>Заметки

Используйте свойство **Name,** чтобы назначить имя или получить имя объекта **Command,** **Property,** **Field** или **Parameter.**

Значение считывать и записывать в **объекте Command** и только для чтения в **объекте Property.**

Для  объекта Field **имя** обычно только для чтения. Однако для новых объектов **Field,** добавленных в коллекцию [Fields](fields-collection-ado.md) записи, имя считывалось  и записывалось только после того,  как было задано свойство [Value](value-property-ado.md) для поля и поставщик данных успешно добавил новое поле, вызывая метод [Update](update-method-ado.md) коллекции **Fields.** [](record-object-ado.md) 

Для **объектов Parameter,** еще не вносимых в коллекцию [Parameters,](parameters-collection-ado.md) свойство **Name** доступно для чтения и записи. Для объектов **appended Parameter** и всех остальных объектов свойство **Name** доступно только для чтения. Имена не должны быть уникальными в коллекции.

Свойство **Name** объекта можно получить по порядковой ссылке, после чего можно ссылаться на объект напрямую по имени. Например, если rstMain.Properties(20). Имя дает возможность updatability. Впоследствии вы можете ссылаться на это свойство как на возможность обеспечения updatability. Впоследствии вы можете ссылаться на это свойство как rstMain.Properties("Updatability") .

