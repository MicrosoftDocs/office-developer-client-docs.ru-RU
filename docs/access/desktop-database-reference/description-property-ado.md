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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293933"
---
# <a name="description-property-ado"></a>Свойство Description (ADO)


**Область применения**: Access 2013, Office 2013

Описывает объект [Error.](error-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **String,** содержаное описание ошибки.

## <a name="remarks"></a>Примечания

Чтобы **получить** краткое описание ошибки, используйте свойство Description. Отобразить это свойство, чтобы предупредить пользователя об ошибке, которую невозможно или не нужно обрабатывать. Строка будет приходить либо от ADO, либо от поставщика.

Поставщики несут ответственность за передачу определенного текста ошибки в ADO. ADO добавляет объект [Ошибки](error-object-ado.md) в коллекцию **Ошибок** для каждого поставщика ошибки или предупреждения, которые он получает. Перенацелите коллекцию **ошибок,** чтобы отслеживать ошибки, которые передает поставщик.

