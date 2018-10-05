---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388191"
---
# <a name="ienumfbblock"></a><span data-ttu-id="b3846-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="b3846-102">IEnumFBBlock</span></span>

<span data-ttu-id="b3846-103">Поддерживает доступ к и перечисление занятости блоков данных для пользователя в интервал времени.</span><span class="sxs-lookup"><span data-stu-id="b3846-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b3846-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b3846-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3846-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="b3846-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="b3846-106">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3846-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b3846-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="b3846-107">Provided by:</span></span>  <br/> |<span data-ttu-id="b3846-108">Обмен сведениями о доступности поставщика</span><span class="sxs-lookup"><span data-stu-id="b3846-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="b3846-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b3846-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b3846-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="b3846-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b3846-111">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="b3846-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b3846-112">Далее</span><span class="sxs-lookup"><span data-stu-id="b3846-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="b3846-113">Получает указанное количество блоков данных о доступности в перечислении.</span><span class="sxs-lookup"><span data-stu-id="b3846-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="b3846-114">Пропустить</span><span class="sxs-lookup"><span data-stu-id="b3846-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="b3846-115">Пропускает указанное число блоков данных о доступности.</span><span class="sxs-lookup"><span data-stu-id="b3846-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="b3846-116">Reset (Сбросить)</span><span class="sxs-lookup"><span data-stu-id="b3846-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="b3846-117">Сбрасывает перечислитель путем установки курсора в начало.</span><span class="sxs-lookup"><span data-stu-id="b3846-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="b3846-118">Копия</span><span class="sxs-lookup"><span data-stu-id="b3846-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="b3846-119">Создает копию перечислителя, с помощью же ограничения времени, но установки курсора в начало перечислитель.</span><span class="sxs-lookup"><span data-stu-id="b3846-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="b3846-120">Ограничить</span><span class="sxs-lookup"><span data-stu-id="b3846-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="b3846-121">Ограничивает число перечисления для заданного периода времени.</span><span class="sxs-lookup"><span data-stu-id="b3846-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3846-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3846-122">Remarks</span></span>

<span data-ttu-id="b3846-123">Перечисление содержит занятости блоки данных, которые не пересекаются в времени.</span><span class="sxs-lookup"><span data-stu-id="b3846-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="b3846-124">Если есть перекрывающиеся элементы календаря, Outlook объединяет эти элементы для без перекрытия блоков сведений о доступности в перечисление, основанное на этом приоритет: документов office, «занят», под вопросом.</span><span class="sxs-lookup"><span data-stu-id="b3846-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="b3846-125">Обмен сведениями о доступности поставщика получает этот интерфейс и перечисления для интервала времени для пользователя через [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="b3846-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3846-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b3846-126">See also</span></span>

- [<span data-ttu-id="b3846-127">About the Free/Busy API</span><span class="sxs-lookup"><span data-stu-id="b3846-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="b3846-128">Константы (занятости API)</span><span class="sxs-lookup"><span data-stu-id="b3846-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="b3846-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="b3846-129">IFreeBusyData</span></span>](ifreebusydata.md)

