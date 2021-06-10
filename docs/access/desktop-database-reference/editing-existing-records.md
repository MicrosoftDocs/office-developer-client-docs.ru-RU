---
title: Редактирование существующих записей
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dae80ddb85709ccc668e80adad0cb0c723c79cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293618"
---
# <a name="editing-existing-records"></a>Редактирование существующих записей


**Область применения**: Access 2013, Office 2013

Чтобы изменить существующие записи, переходить к строке, необходимой для изменения свойства **Value** полей, которые необходимо изменить. Дополнительные сведения о свойстве  значения объекта **Field** см. в главе [3: Изучение данных.](chapter-3-examining-data.md) В зависимости от типа курсора вы будете использовать **Update** или **UpdateBatch** для отправки изменений в источник данных. Дополнительные сведения см. [в главе 5: Обновление и сохраняющиеся данные.](chapter-5-updating-and-persisting-data.md)

Обычно более эффективно использовать сохраненную процедуру с объектом команды для выполнения обновлений, а также для выполнения других операций, так как сохраненная процедура не требует создания курсора. Дополнительные сведения о курсорах см. в [главе 8: Понимание курсоров и блокировки.](chapter-8-understanding-cursors-and-locks.md)

