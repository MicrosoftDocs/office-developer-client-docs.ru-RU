---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427775"
---
# <a name="fbadentrylist"></a><span data-ttu-id="7b593-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="7b593-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="7b593-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b593-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b593-105">Проверяет список идентификаторов записей MAPI.</span><span class="sxs-lookup"><span data-stu-id="7b593-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b593-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7b593-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b593-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7b593-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7b593-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7b593-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b593-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b593-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b593-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7b593-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b593-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="7b593-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="7b593-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b593-112">Parameters</span></span>

 <span data-ttu-id="7b593-113">_Лпентрилист_</span><span class="sxs-lookup"><span data-stu-id="7b593-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="7b593-114">возврата Указатель на структуру [ентрилист](entrylist.md) , содержащую массив идентификаторов записей, которые необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="7b593-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b593-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b593-115">Return value</span></span>

<span data-ttu-id="7b593-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="7b593-116">TRUE</span></span> 
  
> <span data-ttu-id="7b593-117">Один или несколько из указанных идентификаторов записей недопустимы.</span><span class="sxs-lookup"><span data-stu-id="7b593-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="7b593-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="7b593-118">FALSE</span></span> 
  
> <span data-ttu-id="7b593-119">Все указанные идентификаторы записей являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="7b593-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b593-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b593-120">Remarks</span></span>

<span data-ttu-id="7b593-121">Функция **фбадентрилист** определяет правильность создания списка идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="7b593-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="7b593-122">Например, недопустимый идентификатор — это один из неправильно выделенной памяти или идентификатор неправильного размера.</span><span class="sxs-lookup"><span data-stu-id="7b593-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

