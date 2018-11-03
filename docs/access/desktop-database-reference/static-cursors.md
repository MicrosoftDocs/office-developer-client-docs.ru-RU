---
title: Статические курсоры (Справочник по для настольных баз данных Access)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac6d55f8869cb273aceb1d55b226ef97585f7f4a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943887"
---
# <a name="static-cursors"></a><span data-ttu-id="c11eb-102">Статические курсоры</span><span class="sxs-lookup"><span data-stu-id="c11eb-102">Static cursors</span></span>


<span data-ttu-id="c11eb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c11eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c11eb-104">Статический курсор всегда отображает результирующий набор, который был впервые открытия курсора.</span><span class="sxs-lookup"><span data-stu-id="c11eb-104">The static cursor always displays the result set as it was when the cursor was first opened.</span></span> <span data-ttu-id="c11eb-105">В зависимости от реализации, статические курсоры имеют только для чтения или чтения и записи и предоставления прокрутку вперед и назад.</span><span class="sxs-lookup"><span data-stu-id="c11eb-105">Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling.</span></span> <span data-ttu-id="c11eb-106">Статический курсор не находит обычно изменений, внесенных в членство, заказа или значения результирующего набора после открытия курсора.</span><span class="sxs-lookup"><span data-stu-id="c11eb-106">The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened.</span></span> <span data-ttu-id="c11eb-107">Статические курсоры может обнаружить собственные обновления, удаления и вставки, хотя для этого не требуется.</span><span class="sxs-lookup"><span data-stu-id="c11eb-107">Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="c11eb-108">Статические курсоры никогда не определять другое обновляет, удаление и вставляет.</span><span class="sxs-lookup"><span data-stu-id="c11eb-108">Static cursors never detect other updates, deletes, and inserts.</span></span> <span data-ttu-id="c11eb-109">Предположим, например, статический курсор извлекает строки и другого приложения, затем обновляет эту строку.</span><span class="sxs-lookup"><span data-stu-id="c11eb-109">For example, suppose a static cursor fetches a row, and another application then updates that row.</span></span> <span data-ttu-id="c11eb-110">Если приложение refetches строку из статического курсора, значения, которые он видит не изменяются, несмотря на изменения, внесенные с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="c11eb-110">If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application.</span></span> <span data-ttu-id="c11eb-111">Поддерживаются все типы прокрутки, но поставщиков может отображаться или не поддерживать закладки.</span><span class="sxs-lookup"><span data-stu-id="c11eb-111">All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="c11eb-112">Если ваше приложение не требуется для обнаружения данных меняется и требует прокрутки, статический курсор — это лучший вариант.</span><span class="sxs-lookup"><span data-stu-id="c11eb-112">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice.</span></span> <span data-ttu-id="c11eb-113">Чтобы указать, что вы хотите использовать статический курсор в ADO используйте **adOpenStatic** **CursorTypeEnum** .</span><span class="sxs-lookup"><span data-stu-id="c11eb-113">Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

