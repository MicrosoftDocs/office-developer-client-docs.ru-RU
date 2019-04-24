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
# <a name="editing-existing-records"></a><span data-ttu-id="0ba25-102">Редактирование существующих записей</span><span class="sxs-lookup"><span data-stu-id="0ba25-102">Editing existing records</span></span>


<span data-ttu-id="0ba25-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ba25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ba25-104">Чтобы изменить существующие записи, перейдите к строке, которую нужно изменить, и измените свойство **value** полей, которые требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="0ba25-104">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change.</span></span> <span data-ttu-id="0ba25-105">Дополнительные сведения о свойстве **value** объекта **field** содержатся в [главе 3: исследование данных](chapter-3-examining-data.md).</span><span class="sxs-lookup"><span data-stu-id="0ba25-105">For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md).</span></span> <span data-ttu-id="0ba25-106">В зависимости от типа курсора вы будете использовать **Update** или **UpdateBatch** для отправки изменений в источник данных.</span><span class="sxs-lookup"><span data-stu-id="0ba25-106">Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source.</span></span> <span data-ttu-id="0ba25-107">Более подробную информацию можно найти в [главе 5: обновление и постоянное обновление данных](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="0ba25-107">For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="0ba25-108">Обычно более эффективно использовать хранимую процедуру с объектом Command для выполнения обновлений, а также для выполнения других операций, так как хранимая процедура не требует создания курсора.</span><span class="sxs-lookup"><span data-stu-id="0ba25-108">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor.</span></span> <span data-ttu-id="0ba25-109">Дополнительные сведения о курсорах приведены в [главе 8: Общие сведения о курсорах и блокировках](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="0ba25-109">For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

