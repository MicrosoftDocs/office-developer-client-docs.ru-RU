---
title: Editing Existing Records
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 274cd7667506159e2309fffb3596781c004f7006
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481646"
---
# <a name="editing-existing-records"></a><span data-ttu-id="ae605-102">Editing Existing Records</span><span class="sxs-lookup"><span data-stu-id="ae605-102">Editing Existing Records</span></span>


<span data-ttu-id="ae605-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae605-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ae605-104">Изменение существующих записей, переместите строку, которую вы хотите изменить и измените **значение** свойства поля, которые требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="ae605-104">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change.</span></span> <span data-ttu-id="ae605-105">Дополнительные сведения о свойство **Value** объекта **поля** можно [Глава 3: проверка данных](chapter-3-examining-data.md).</span><span class="sxs-lookup"><span data-stu-id="ae605-105">For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md).</span></span> <span data-ttu-id="ae605-106">В зависимости от типа вашей текущей позиции будет использоваться **обновления** или **UpdateBatch** для отправки изменений обратно в источник данных.</span><span class="sxs-lookup"><span data-stu-id="ae605-106">Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source.</span></span> <span data-ttu-id="ae605-107">Дополнительные сведения можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="ae605-107">For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="ae605-108">Это обычно более эффективно использовать хранимую процедуру с объектом команду выполнить обновления, а также для выполнения других операций, поскольку хранимую процедуру не требуется создание курсора.</span><span class="sxs-lookup"><span data-stu-id="ae605-108">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor.</span></span> <span data-ttu-id="ae605-109">Дополнительные сведения о курсорах можно [главы 8: Общее представление о курсоры и блокировки](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="ae605-109">For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

