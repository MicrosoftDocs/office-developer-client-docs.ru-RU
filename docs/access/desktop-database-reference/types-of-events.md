---
title: Типы событий (ссылка на настольные базы данных)
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



Существует два основных типа событий. "События will", которые называются перед началом операции, обычно включают в свои имена "Will" ( **например, WillChangeRecordset** или **WillConnect).** События, которые вызваны после завершения события, обычно включают в свои имена "Complete" ( например, **RecordChangeComplete** или **ConnectComplete).** Исключения существуют , например **InfoMessage,** но они возникают после завершения связанной операции.

## <a name="will-events"></a>События Will

Обработчики событий, вызванные перед началом операции, предоставляют вам возможность изучить или изменить параметры операции, а затем отменить операцию или разрешить ее завершить. Эти процедуры обработки событий обычно имеют имена формы **Will* Event ****.

## <a name="complete-events"></a>Завершение событий

Обработчики событий, вызванные после завершения операции, могут уведомить приложение о том, что операция завершена. Обработник событий также уведомлен, когда обработник событий Will отменяет ожидаемую операцию. Эти процедуры обработки событий обычно имеют имена формы ***Event*Complete**.

События Will и Complete обычно используются в парах.

## <a name="other-events"></a>Другие события

Другие обработчики событий, т. е. события, имена которых не являются формой **Will*Event*** или ***Event*Complete,** называются только после завершения операции. Это события **Disconnect,** **EndOfRecordset** и **InfoMessage.**

