---
title: RDS возвращает ошибку "Поток не прочитан"
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300856"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS возвращает ошибку \" Stream Not Read \"


**Область применения**: Access 2013, Office 2013

"Не удалось прочитать объект Stream, так как он пуст или текущая позиция находится в конце потока. Для непустых потоков установите текущее положение со свойством Position. Чтобы определить, пуст ли поток, проверьте свойство Size".

Если вы получите ошибку выше, это может быть результатом попытки использовать параметризованный иерархический запрос по протоколу http. RDS не разрешает удаленные параметровизированные иерархии.

