---
title: Глава 7. Обработка событий ADO
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7357cc60a3bddbf96c2abae39fecfb7107025e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296404"
---
# <a name="chapter-7-handling-ado-events"></a>Глава 7. Обработка событий ADO

**Область применения**: Access 2013, Office 2013

Модель событий ADO поддерживает определенные синхронные и асинхронные операции *ADO,* которые выпускают события или уведомления, до начала или завершения операции. Событие фактически является вызовом процедуры обработки событий, определенной в приложении.

Если вы предоставляете функции или процедуры обработки для группы событий, которые происходят перед началом операции, вы можете проверить или изменить параметры, переданные в операцию. Так как она еще не выполнена, можно отменить операцию или разрешить ее выполнение.

Группа событий, происходящих после завершения операции, особенно важна при асинхронном использовании ADO. Например, приложение, которое запускает асинхронную операцию [Recordset.Open,](open-method-ado-recordset.md) по ее завершению уведомлено о выполнении.

Использование модели событий ADO добавляет определенные дополнительные расходы в приложение, но обеспечивает гораздо большую гибкость, чем другие методы работы с асинхронными операциями, например отслеживание свойства [State](state-property-ado.md) объекта с помощью цикла.

В этой главе освещались следующие темы:

- [Сводка по обработчикам событий ADO](ado-event-handler-summary.md)
- [Типы событий](types-of-events.md)
- [Параметры событий](event-parameters.md)
- [Взаимодействие обработчиков событий](how-event-handlers-work-together.md)
- [ADO event instantiation by language (ADO)](ado-event-instantiation-by-language-ado.md)
