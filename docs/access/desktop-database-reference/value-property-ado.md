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

Указывает значение, назначенное объекту [Field,](field-object-ado.md) [Parameter](parameter-object-ado.md)или [Property.](property-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **Variant,** которое указывает значение объекта. Значение по умолчанию зависит от свойства [Type.](type-property-ado.md)

## <a name="remarks"></a>Заметки

Используйте свойство **Value,** чтобы устанавливать или возвращать данные из объектов **Field,** устанавливать или возвращать значения параметров с помощью объектов **Parameter,** а также устанавливать или возвращать параметры свойств с **объектами Property.** То, является ли свойство **Value** чтением, чтением или только чтением, зависит от множества факторов. Дополнительные сведения см. в соответствующих темах объекта.

ADO позволяет устанавливать и возвращать длинные двоичные данные со **свойством Value.**

> [!NOTE]
> Для **объектов Parameter** ADO считыет свойство **Value** только один раз от поставщика. Если команда содержит  параметр, свойство **Value** которого пусто, и создается набор записей из команды, убедитесь, что сначала закройте **recordset** перед искомым [](recordset-object-ado.md) **свойством Value.** В противном случае для некоторых поставщиков свойство **Value** может быть пустым и содержать неправильное значение.

Для новых объектов **Field,** которые были добавлены в коллекцию [Fields](fields-collection-ado.md) объекта [Record,](record-object-ado.md)  свойство **Value** должно быть задано до того, как могут быть указаны другие свойства Field. Во-первых, должно быть назначено определенное [](update-method-ado.md) значение для свойства **Value** и вызвано обновление коллекции **Fields.** Затем можно получить доступ к другим свойствам, таким как [Type](type-property-ado.md) или [Attributes.](attributes-property-ado.md)

