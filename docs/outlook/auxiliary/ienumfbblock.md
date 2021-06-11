---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317628"
---
# <a name="ienumfbblock"></a><span data-ttu-id="c6946-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="c6946-102">IEnumFBBlock</span></span>

<span data-ttu-id="c6946-103">Поддерживает доступ и переумеживающие свободные и загруженные блоки данных для пользователя в пределах диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="c6946-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c6946-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c6946-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6946-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="c6946-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="c6946-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6946-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="c6946-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="c6946-107">Provided by:</span></span>  <br/> |<span data-ttu-id="c6946-108">Бесплатный/занятый поставщик</span><span class="sxs-lookup"><span data-stu-id="c6946-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="c6946-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="c6946-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c6946-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="c6946-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c6946-111">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="c6946-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c6946-112">Next</span><span class="sxs-lookup"><span data-stu-id="c6946-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="c6946-113">Получает следующее указанное количество блоков бесплатных и загруженных данных в переумериях.</span><span class="sxs-lookup"><span data-stu-id="c6946-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="c6946-114">Skip</span><span class="sxs-lookup"><span data-stu-id="c6946-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="c6946-115">Пропускает указанное количество блоков бесплатных и загруженных данных.</span><span class="sxs-lookup"><span data-stu-id="c6946-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="c6946-116">Reset</span><span class="sxs-lookup"><span data-stu-id="c6946-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="c6946-117">Сбрасывает переустановку, установив курсор к началу.</span><span class="sxs-lookup"><span data-stu-id="c6946-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="c6946-118">Clone</span><span class="sxs-lookup"><span data-stu-id="c6946-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="c6946-119">Создает копию этого перемерителя, используя одно и то же ограничение времени, но устанавливая курсор к началу этого.</span><span class="sxs-lookup"><span data-stu-id="c6946-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="c6946-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="c6946-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="c6946-121">Ограничивает указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="c6946-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6946-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6946-122">Remarks</span></span>

<span data-ttu-id="c6946-123">В переумериях содержатся свободные и загруженные блоки данных, которые не совпадают во времени.</span><span class="sxs-lookup"><span data-stu-id="c6946-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="c6946-124">Если в календаре есть перекрывающиеся элементы, Outlook объединяет эти элементы, чтобы сформировать не перекрывающиеся свободные и занятые блоки в переумериях на основе этого порядка приоритета: вне офиса, занят, предварительно.</span><span class="sxs-lookup"><span data-stu-id="c6946-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="c6946-125">Бесплатный/занятый поставщик получает этот интерфейс и переумежение для диапазона времени для пользователя через [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="c6946-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6946-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c6946-126">See also</span></span>

- [<span data-ttu-id="c6946-127">О доступности API</span><span class="sxs-lookup"><span data-stu-id="c6946-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="c6946-128">Константы (API free/busy)</span><span class="sxs-lookup"><span data-stu-id="c6946-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="c6946-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="c6946-129">IFreeBusyData</span></span>](ifreebusydata.md)

