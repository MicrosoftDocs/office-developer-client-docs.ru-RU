---
title: Свойство Атрибуты (ADO)
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
# <a name="attributes-property-ado"></a>Свойство Атрибуты (ADO)


**Область применения**: Access 2013, Office 2013


## <a name="attributes-property"></a>Attributes Property

Указывает одну или несколько характеристик объекта.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long.**

Для объекта [Подключения](connection-object-ado.md) свойство **Атрибуты** является считываемой или записной, а его значение может быть суммой одного или более [значений XactAttributeEnum.](xactattributeenum.md) По умолчанию — ноль (0).

Для объекта [Parameter](parameter-object-ado.md) свойство **Attributes** — это свойство чтения и записи, и его значение может быть суммой любых значений [ParameterAttributesEnum.](parameterattributesenum.md) По умолчанию **adParamSigned**.

Для объекта [Field](field-object-ado.md) свойство **Attributes** может быть суммой одного или более значений [FieldAttributeEnum.](fieldattributeenum.md) Как правило, только для чтения, однако для новых объектов **Field,** которые были добавлены в коллекцию [Полей](fields-collection-ado.md) записи,  Атрибуты считываются/записывают только после того, как свойство [Value](value-property-ado.md) для поля было задано и новое поле успешно добавлено поставщиком данных, позвонив [методу Update](update-method-ado.md) коллекции **Fields.** [](record-object-ado.md)  

Для [объекта Property](property-object-ado.md) свойство **Attributes** является только для чтения, а его значение может быть суммой любых значений [PropertyAttributesEnum.](propertyattributesenum.md)

## <a name="remarks"></a>Примечания

Используйте свойство **Атрибуты** для набора или возврата характеристик объектов **Подключения,** **Объектов Параметр,** [Объектов Поля](field-object-ado.md) или [Свойств.](property-object-ado.md)

При наборе нескольких атрибутов можно подвести соответствующие константы. Если вы установите значение свойства суммой, включая несовместимые константы, возникает ошибка.

**Удаленное использование службы данных** Это свойство не доступно для объекта клиентского **подключения.**

