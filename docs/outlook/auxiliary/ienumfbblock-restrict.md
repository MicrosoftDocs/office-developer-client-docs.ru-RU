---
title: иенумфбблоккрестрикт
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Ограничит перечисление до указанного периода времени.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431948"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="f1092-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="f1092-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="f1092-104">Ограничит перечисление до указанного периода времени.</span><span class="sxs-lookup"><span data-stu-id="f1092-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f1092-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f1092-105">Quick info</span></span>

<span data-ttu-id="f1092-106">Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="f1092-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="f1092-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1092-107">Parameters</span></span>

<span data-ttu-id="f1092-108">_фтмстарт_</span><span class="sxs-lookup"><span data-stu-id="f1092-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="f1092-109">возврата Время начала, ограничивающее перечисление.</span><span class="sxs-lookup"><span data-stu-id="f1092-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="f1092-110">_фтменд_</span><span class="sxs-lookup"><span data-stu-id="f1092-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="f1092-111">возврата Время окончания для ограничения перечисления.</span><span class="sxs-lookup"><span data-stu-id="f1092-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f1092-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f1092-112">Return values</span></span>

<span data-ttu-id="f1092-113">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="f1092-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1092-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1092-114">Remarks</span></span>

<span data-ttu-id="f1092-115">Этот метод также сбрасывает перечисление.</span><span class="sxs-lookup"><span data-stu-id="f1092-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1092-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f1092-116">See also</span></span>

- [<span data-ttu-id="f1092-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="f1092-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="f1092-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="f1092-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="f1092-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="f1092-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="f1092-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="f1092-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="f1092-121">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="f1092-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

