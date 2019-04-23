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

Указывает степень точности для числовых значений в объекте [Parameter](parameter-object-ado.md) или числовых объектах [полей](field-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Byte** , указывающее максимальное количество цифр, используемых для представления значений.

## <a name="remarks"></a>Замечания

Используйте свойство **Precision** для определения максимального числа цифр, используемых для представления значений числового **параметра** или объекта **field** .

Значение доступно для чтения и записи в объекте **Parameter** .

Для объекта **field** **точность** обычно доступна только для чтения. Тем не менее, для новых объектов **field** , добавленных в коллекцию [Fields](fields-collection-ado.md) [записи](record-object-ado.md), **точность** доступна только после того, как было указано свойство [value](value-property-ado.md) для **поля** , и у поставщика данных новое **поле** успешно добавлено путем вызова метода [Update](update-method-ado.md) коллекции Fields. ****

