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

Возвращает **строку,** содержаную описание ошибки.

## <a name="remarks"></a>Заметки

Используйте свойство **Description,** чтобы получить краткое описание ошибки. Отобразить это свойство, чтобы предупредить пользователя об ошибке, которую невозможно или не нужно обрабатывать. Строка будет от ADO или поставщика.

Поставщики отвечают за передачу определенного текста ошибки в ADO. ADO добавляет объект [Error](error-object-ado.md) в коллекцию **Errors** для каждой получаемой ошибки или предупреждения поставщика. Enumerate the **Errors** collection to trace the errors that the provider passes.

