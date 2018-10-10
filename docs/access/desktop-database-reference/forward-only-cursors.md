---
title: Forward-Only Cursors
TOCTitle: Forward-Only Cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fdcdde9859ec0f31326134a240c7b703f4a71d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481171"
---
# <a name="forward-only-cursors"></a><span data-ttu-id="de4d1-102">Forward-Only Cursors</span><span class="sxs-lookup"><span data-stu-id="de4d1-102">Forward-Only Cursors</span></span>


<span data-ttu-id="de4d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de4d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de4d1-104">Тип курсора типичного по умолчанию, называемый курсор последовательного доступа (или не прокручиваемым), можно переместить только вперед через набор результатов.</span><span class="sxs-lookup"><span data-stu-id="de4d1-104">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set.</span></span> <span data-ttu-id="de4d1-105">Последовательный курсор не поддерживает прокрутку (возможность переместить вперед и назад в наборе результатов); он поддерживает только выборка строк от начала до конца набора результатов.</span><span class="sxs-lookup"><span data-stu-id="de4d1-105">A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set.</span></span> <span data-ttu-id="de4d1-106">С помощью некоторых курсоров (например, с библиотекой курсора SQL Server), все insert, update и delete операторов текущий пользователь (или зафиксирует другими пользователями) влияют на строк в результирующем наборе отображаются, как извлечь строки.</span><span class="sxs-lookup"><span data-stu-id="de4d1-106">With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched.</span></span> <span data-ttu-id="de4d1-107">Поскольку курсор нельзя прокручивать назад, однако изменения, внесенные в строки в базе данных после получения строки не видны посредством курсора.</span><span class="sxs-lookup"><span data-stu-id="de4d1-107">Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</span></span>

<span data-ttu-id="de4d1-108">После обработки данных для текущей строки курсора только для прямого освобождает ресурсы, которые использовались для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="de4d1-108">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data.</span></span> <span data-ttu-id="de4d1-109">Курсоров динамических по умолчанию, что означает, что все изменения будут определяться как обработки текущей строки.</span><span class="sxs-lookup"><span data-stu-id="de4d1-109">Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed.</span></span> <span data-ttu-id="de4d1-110">Это обеспечивает более быстрый открытия курсора и позволяет результирующий набор для отображения обновлений, внесенных в таблицах.</span><span class="sxs-lookup"><span data-stu-id="de4d1-110">This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</span></span>

<span data-ttu-id="de4d1-111">Во время курсоров не поддерживают назад прокрутки, приложение может вернуться к началу наборе результатов по закрыть и повторно открыть курсор.</span><span class="sxs-lookup"><span data-stu-id="de4d1-111">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor.</span></span> <span data-ttu-id="de4d1-112">Это эффективный способ работы с небольшие объемы данных.</span><span class="sxs-lookup"><span data-stu-id="de4d1-112">This is an effective way to work with small amounts of data.</span></span> <span data-ttu-id="de4d1-113">В качестве альтернативы приложения может один раз чтения набора результатов, кэшировать данные локально и найдите локального кэша данных.</span><span class="sxs-lookup"><span data-stu-id="de4d1-113">As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</span></span>

<span data-ttu-id="de4d1-114">Если ваше приложение не требуется прокручивание набора результатов, последовательный курсор — лучший способ извлечь данные быстро с наименьшими объем нагрузки.</span><span class="sxs-lookup"><span data-stu-id="de4d1-114">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead.</span></span> <span data-ttu-id="de4d1-115">Чтобы указать, что необходимо использовать только для прямого курсора в ADO используйте **adOpenForwardOnly** **CursorTypeEnum** .</span><span class="sxs-lookup"><span data-stu-id="de4d1-115">Use the **adOpenForwardOnly** **CursorTypeEnum** to indicate that you want to use a forward-only cursor in ADO.</span></span>

