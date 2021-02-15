---
title: Types of Events (Access desktop database reference)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314156"
---
# <a name="types-of-events"></a>Типы событий


**Область применения**: Access 2013, Office 2013



Существует два основных типа событий. Имена "Will Events", которые называются перед началом операции, обычно включают в свои имена "Will" (например, **WillChangeRecordset** или **WillConnect).** События, которые вызваны после завершения события, обычно включают в свои имена "Complete", например **RecordChangeComplete** или **ConnectComplete.** Существуют исключения, такие как **InfoMessage,** но они возникают после завершения связанной операции.

## <a name="will-events"></a>События Will

Обработчики событий, которые были вызваны перед началом операции, позволяют проверить или изменить параметры операции, а затем отменить операцию или разрешить ее завершение. Эти процедуры обработки событий обычно имеют имена формы **Will* Event****.

## <a name="complete-events"></a>События завершения

Обработчики событий, которые вызваны после завершения операции, могут уведомить приложение о том, что операция завершена. Такой обработник событий также будет уведомлен, когда обработник событий Will отменяет ожидающих операций. Эти процедуры обработки событий обычно имеют имена формы ***Event*Complete**.

События Will и Complete обычно используются парами.

## <a name="other-events"></a>Другие события

Другие обработчики событий, то есть события, имена которых не имеют формы **Will*Event*** или ***Event*Complete,** будут вызваны только после завершения операции. Это события **Disconnect,** **EndOfRecordset** и **InfoMessage.**

