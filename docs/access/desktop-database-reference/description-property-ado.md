---
title: Свойство Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698934"
---
# <a name="description-property-ado"></a>Свойство Description (ADO)


**Применимо к**: Access 2013, Office 2013

Описывает объект [Error](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **String** , содержащее описание ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **Description** для получения краткое описание ошибки. Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать. Строка будет получен из ADO или поставщика.

Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO. Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его. Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.

