---
title: Редактирование существующих записей
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c500f89b0f16062e43ace45f55eab9a593d071a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884235"
---
# <a name="editing-existing-records"></a>Редактирование существующих записей


**Применимо к**: Access 2013, Office 2013

Изменение существующих записей, переместите строку, которую вы хотите изменить и измените **значение** свойства поля, которые требуется изменить. Дополнительные сведения о свойство **Value** объекта **поля** можно [Глава 3: проверка данных](chapter-3-examining-data.md). В зависимости от типа вашей текущей позиции будет использоваться **обновления** или **UpdateBatch** для отправки изменений обратно в источник данных. Дополнительные сведения можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).

Это обычно более эффективно использовать хранимую процедуру с объектом команду выполнить обновления, а также для выполнения других операций, поскольку хранимую процедуру не требуется создание курсора. Дополнительные сведения о курсорах можно [главы 8: Общее представление о курсоры и блокировки](chapter-8-understanding-cursors-and-locks.md).

