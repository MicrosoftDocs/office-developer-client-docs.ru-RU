---
title: Свойство NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb2c799fd7c9d1cc74c6081c10f7a8d356e79faf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876017"
---
# <a name="numericscale-property-ado"></a>Свойство NumericScale (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает масштаб числовых значений в объекте [параметра](parameter-object-ado.md) или [поля](field-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **битное** значение, указывающее количество десятичных разрядов, к которым будут разрешены числовых значений.

## <a name="remarks"></a>Замечания

Свойство **NumericScale** определяет количество цифр справа от десятичной запятой будет использоваться для представления значений для числовых объекта **параметра** или **поля** .

Для **параметра** объектов свойство **NumericScale** — чтение и запись.

Для объекта **поля** **NumericScale** обычно доступны только для чтения. Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **NumericScale** — чтение и запись только после указано [значение](value-property-ado.md) свойства для **поля** и поставщика данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .

