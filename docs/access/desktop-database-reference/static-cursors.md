---
title: Статические курсоры (ссылка на настольные базы данных)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2eb019a6fc960d58771ff5ab0de7dca547c55f1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308542"
---
# <a name="static-cursors"></a><span data-ttu-id="dac08-102">Статические курсоры</span><span class="sxs-lookup"><span data-stu-id="dac08-102">Static cursors</span></span>


<span data-ttu-id="dac08-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dac08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dac08-104">Статичный курсор всегда отображает набор результатов, как это было при первом открываемом курсоре.</span><span class="sxs-lookup"><span data-stu-id="dac08-104">The static cursor always displays the result set as it was when the cursor was first opened.</span></span> <span data-ttu-id="dac08-105">В зависимости от реализации статические курсоры являются только для чтения или чтения/записи и обеспечивают прокрутку вперед и назад.</span><span class="sxs-lookup"><span data-stu-id="dac08-105">Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling.</span></span> <span data-ttu-id="dac08-106">Обычно статичный курсор не определяет изменения, внесенные в состав, порядок или значения результата, за набором после открытия курсора.</span><span class="sxs-lookup"><span data-stu-id="dac08-106">The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened.</span></span> <span data-ttu-id="dac08-107">Статические курсоры могут обнаруживать собственные обновления, удаления и вставки, хотя они не требуются для этого.</span><span class="sxs-lookup"><span data-stu-id="dac08-107">Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="dac08-108">Статические курсоры никогда не обнаруживают другие обновления, удаления и вставки.</span><span class="sxs-lookup"><span data-stu-id="dac08-108">Static cursors never detect other updates, deletes, and inserts.</span></span> <span data-ttu-id="dac08-109">Например, предположим, что статический курсор извлекает строку, а другое приложение затем обновляет строку.</span><span class="sxs-lookup"><span data-stu-id="dac08-109">For example, suppose a static cursor fetches a row, and another application then updates that row.</span></span> <span data-ttu-id="dac08-110">Если приложение повторно передает строку из статического курсора, значения, которые он видит, остаются неизменными, несмотря на изменения, внесенные другим приложением.</span><span class="sxs-lookup"><span data-stu-id="dac08-110">If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application.</span></span> <span data-ttu-id="dac08-111">Все типы прокрутки поддерживаются, но поставщики могут или не могут поддерживать закладки.</span><span class="sxs-lookup"><span data-stu-id="dac08-111">All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="dac08-112">Если вашему приложению не требуется обнаруживать изменения данных и требуется прокрутка, лучше всего выбрать статичный курсор.</span><span class="sxs-lookup"><span data-stu-id="dac08-112">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice.</span></span> <span data-ttu-id="dac08-113">Используйте **adOpenStatic** **CursorTypeEnum,** чтобы указать, что вы хотите использовать статический курсор в ADO.</span><span class="sxs-lookup"><span data-stu-id="dac08-113">Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

