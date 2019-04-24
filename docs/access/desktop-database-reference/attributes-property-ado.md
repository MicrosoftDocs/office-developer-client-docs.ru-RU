---
title: Свойство Attributes (ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6495c70f64930e1b335c603f13e720ad581203a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296985"
---
# <a name="attributes-property-ado"></a>Свойство Attributes (ADO)


**Область применения**: Access 2013, Office 2013


## <a name="attributes-property"></a>Attributes Property

Указывает одну или несколько характеристик объекта.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Long** .

Для объекта [Connection](connection-object-ado.md) свойство Attributes **** доступно для чтения и записи, а его значение может быть суммой одного или нескольких значений [ксактаттрибутинум](xactattributeenum.md) . Значение по умолчанию — ноль (0).

Для объекта [Parameter](parameter-object-ado.md) свойство Attributes **** доступно для чтения и записи, а его значение может быть суммой одного или нескольких значений [параметераттрибутесенум](parameterattributesenum.md) . Значение по умолчанию — **адпарамсигнед**.

Для объекта [field](field-object-ado.md) свойство Attributes **** может быть суммой одного или нескольких значений [фиелдаттрибутинум](fieldattributeenum.md) . Однако обычно он доступен только для чтения, но для новых **объектов Field** , добавленных в коллекцию Fields [](fields-collection-ado.md) [записи](record-object-ado.md), **атрибуты** доступны только для чтения и записи после того, как свойство [value](value-property-ado.md) для этого **поля** . , и поставщик данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **Fields** .

Для объекта [Property](property-object-ado.md) свойство Attributes **** доступно только для чтения, а его значение может быть суммой одного или нескольких значений [пропертяттрибутесенум](propertyattributesenum.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **Attributes** , чтобы задать или вернуть характеристики объектов **подключения** , объектов **параметров** , объектов [полей](field-object-ado.md) или объектов [Property](property-object-ado.md) .

При задании нескольких атрибутов можно суммировать соответствующие константы. Если присвоить свойству значение Sum, включая несовместимые константы, возникает ошибка.

**Использование удаленной службы данных** Это свойство недоступно для объекта **подключения** на стороне клиента.

