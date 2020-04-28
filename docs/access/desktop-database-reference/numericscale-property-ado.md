---
title: Свойство NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288555"
---
# <a name="numericscale-property-ado"></a>Свойство NumericScale (ADO)


**Область применения**: Access 2013, Office 2013

Указывает масштаб числовых значений в объекте [параметра](parameter-object-ado.md) или [поля](field-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **байта** , которое указывает количество десятичных разрядов, к которым будут разрешены числовые значения.

## <a name="remarks"></a>Примечания

Используйте свойство **NumericScale** , чтобы определить количество цифр справа от десятичной точки, которое будет использоваться для представления значений числового **параметра** или объекта **field** .

Для объектов **Parameter** свойство **NumericScale** доступно для чтения и записи.

Для объекта **field** **NumericScale** обычно предназначен только для чтения. Однако для новых объектов **field** , добавленных в коллекцию [Fields](fields-collection-ado.md) [записи](record-object-ado.md), **NumericScale** доступен только для чтения и записи после того, как было указано свойство [value](value-property-ado.md) для **поля** , и поставщик данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **Fields** .

