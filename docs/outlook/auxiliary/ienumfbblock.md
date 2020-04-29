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
# <a name="ienumfbblock"></a><span data-ttu-id="d3a28-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="d3a28-102">IEnumFBBlock</span></span>

<span data-ttu-id="d3a28-103">Поддерживает доступ и перечисление блоков сведений о занятости для пользователя в диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="d3a28-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d3a28-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d3a28-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3a28-105">Наследование от:</span><span class="sxs-lookup"><span data-stu-id="d3a28-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="d3a28-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d3a28-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d3a28-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="d3a28-107">Provided by:</span></span>  <br/> |<span data-ttu-id="d3a28-108">Поставщик сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="d3a28-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="d3a28-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="d3a28-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d3a28-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="d3a28-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d3a28-111">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="d3a28-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d3a28-112">Next</span><span class="sxs-lookup"><span data-stu-id="d3a28-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="d3a28-113">Получает следующее указанное количество блоков данных о занятости в перечислении.</span><span class="sxs-lookup"><span data-stu-id="d3a28-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="d3a28-114">Skip</span><span class="sxs-lookup"><span data-stu-id="d3a28-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="d3a28-115">Пропускает указанное количество блоков данных о занятости.</span><span class="sxs-lookup"><span data-stu-id="d3a28-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="d3a28-116">Reset</span><span class="sxs-lookup"><span data-stu-id="d3a28-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="d3a28-117">Сбрасывает перечислитель, устанавливая курсор в начало.</span><span class="sxs-lookup"><span data-stu-id="d3a28-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="d3a28-118">Clone</span><span class="sxs-lookup"><span data-stu-id="d3a28-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="d3a28-119">Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.</span><span class="sxs-lookup"><span data-stu-id="d3a28-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d3a28-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="d3a28-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="d3a28-121">Ограничит перечисление до указанного периода времени.</span><span class="sxs-lookup"><span data-stu-id="d3a28-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3a28-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3a28-122">Remarks</span></span>

<span data-ttu-id="d3a28-123">Перечисление содержит блоки данных о занятости, которые не перекрываются в течение времени.</span><span class="sxs-lookup"><span data-stu-id="d3a28-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="d3a28-124">При наличии перекрывающихся элементов в календаре Outlook выполняет слияние этих элементов для формирования неперекрывающихся блоков сведений о занятости в перечислении на основе следующего порядка приоритетов: "нет на месте", "занято" и "под вопросом".</span><span class="sxs-lookup"><span data-stu-id="d3a28-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="d3a28-125">Поставщик сведений о доступности получает этот интерфейс и перечисление для диапазона времени для пользователя с помощью [ифрибусидата](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="d3a28-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3a28-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d3a28-126">See also</span></span>

- [<span data-ttu-id="d3a28-127">О доступности API</span><span class="sxs-lookup"><span data-stu-id="d3a28-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="d3a28-128">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="d3a28-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="d3a28-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="d3a28-129">IFreeBusyData</span></span>](ifreebusydata.md)

