---
title: Свойство Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db2000c2db48215df42b5cd81fb35be0f0c4be9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869962"
---
# <a name="precision-property-ado"></a>Свойство Precision (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает погрешность числовых значений в объект [параметра](parameter-object-ado.md) или для объектов числового [поля](field-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **битное** значение, указывающее максимальное число знаков, используемых для представления значений.

## <a name="remarks"></a>Замечания

Свойство **точности** определяет максимальное число знаков, используемых для представления значений для числовых объекта **параметра** или **поля** .

Значение является чтение и запись в объект **параметра** .

Для объекта **поля** **точности** обычно доступны только для чтения. Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **точность** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и имеет поставщика данных успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .

