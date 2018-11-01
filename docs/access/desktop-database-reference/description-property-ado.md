---
title: Свойство Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc2a7706afbf69d9949e8b04122b144c6826ec40
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882940"
---
# <a name="description-property-ado"></a>Свойство Description (ADO)


**Применимо к**: Access 2013, Office 2013

Описывает объект [Error](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **String** , содержащее описание ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **Description** для получения краткое описание ошибки. Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать. Строка будет получен из ADO или поставщика.

Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO. Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его. Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.

