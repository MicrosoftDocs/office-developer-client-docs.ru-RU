---
title: Свойство Value (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00b82706d934356621ac1e41fffca61ec88e081f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305896"
---
# <a name="value-property-ado"></a>Свойство Value (ADO)

**Область применения**: Access 2013, Office 2013

Указывает значение, назначенное [полю](field-object-ado.md), [параметру](parameter-object-ado.md)или объекту [Property](property-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Variant** , которое указывает значение объекта. Значение по умолчанию зависит от свойства [Type](type-property-ado.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **value** , чтобы задать или вернуть данные из объектов **field** , чтобы задать или вернуть значения параметров с помощью объектов **Parameter** или задать или вернуть параметры свойств с помощью объектов **Property** . Независимо от того, является ли свойство **value** доступно для чтения и записи или только для чтения, зависит от множества факторов — просмотрите разделы, посвященные соответствующим объектам, для получения дополнительных сведений.

С помощью ADO можно задавать и возвращать длинные двоичные данные со свойством **value** .

> [!NOTE]
> Для объектов **Parameter** ADO читает свойство **value** только один раз от поставщика. Если команда содержит **параметр** , свойство **value** которого пустое, и создан [набор записей](recordset-object-ado.md) из команды, убедитесь, что сначала закрывается **набор записей** , прежде чем будет получено свойство **value** . В противном случае для некоторых поставщиков свойство **value** может быть пустым и не будет содержать правильное значение.

Для новых объектов **field** , добавленных в коллекцию Fields [](fields-collection-ado.md) объекта [Record](record-object-ado.md) , свойство **value** должно быть задано до того, как можно будет указать другие свойства **поля** . Во-первых, в коллекции Fields должно быть назначено и [Обновлено](update-method-ado.md) определенное значение свойства **** **value** . Затем можно получить доступ к другим свойствам, таким как [Type](type-property-ado.md) или [Attributes](attributes-property-ado.md) .

