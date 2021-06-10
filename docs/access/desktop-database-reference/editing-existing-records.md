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
# <a name="editing-existing-records"></a><span data-ttu-id="2cbf1-102">Редактирование существующих записей</span><span class="sxs-lookup"><span data-stu-id="2cbf1-102">Editing existing records</span></span>


<span data-ttu-id="2cbf1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cbf1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2cbf1-104">Чтобы изменить существующие записи, переходить к строке, необходимой для изменения свойства **Value** полей, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="2cbf1-104">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change.</span></span> <span data-ttu-id="2cbf1-105">Дополнительные сведения о свойстве  значения объекта **Field** см. в главе [3: Изучение данных.](chapter-3-examining-data.md)</span><span class="sxs-lookup"><span data-stu-id="2cbf1-105">For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md).</span></span> <span data-ttu-id="2cbf1-106">В зависимости от типа курсора вы будете использовать **Update** или **UpdateBatch** для отправки изменений в источник данных.</span><span class="sxs-lookup"><span data-stu-id="2cbf1-106">Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source.</span></span> <span data-ttu-id="2cbf1-107">Дополнительные сведения см. [в главе 5: Обновление и сохраняющиеся данные.](chapter-5-updating-and-persisting-data.md)</span><span class="sxs-lookup"><span data-stu-id="2cbf1-107">For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="2cbf1-108">Обычно более эффективно использовать сохраненную процедуру с объектом команды для выполнения обновлений, а также для выполнения других операций, так как сохраненная процедура не требует создания курсора.</span><span class="sxs-lookup"><span data-stu-id="2cbf1-108">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor.</span></span> <span data-ttu-id="2cbf1-109">Дополнительные сведения о курсорах см. в [главе 8: Понимание курсоров и блокировки.](chapter-8-understanding-cursors-and-locks.md)</span><span class="sxs-lookup"><span data-stu-id="2cbf1-109">For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

