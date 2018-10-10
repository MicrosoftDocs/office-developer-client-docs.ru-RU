---
title: Description Property (ADO)
TOCTitle: Description Property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3837d60b58772bbe6b65af6673c4eaa471507e66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480538"
---
# <a name="description-property-ado"></a>Description Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Описывает объект [Error](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **String** , содержащее описание ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **Description** для получения краткое описание ошибки. Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать. Строка будет получен из ADO или поставщика.

Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO. Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его. Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.

