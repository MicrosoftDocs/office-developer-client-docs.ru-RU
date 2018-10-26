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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582912"
---
# <a name="fbadentrylist"></a><span data-ttu-id="3b009-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="3b009-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="3b009-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b009-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b009-105">Проверяет список идентификаторов запись MAPI.</span><span class="sxs-lookup"><span data-stu-id="3b009-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b009-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3b009-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b009-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="3b009-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="3b009-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3b009-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b009-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3b009-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3b009-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3b009-110">Called by:</span></span>  <br/> |<span data-ttu-id="3b009-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3b009-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="3b009-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b009-112">Parameters</span></span>

 <span data-ttu-id="3b009-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="3b009-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="3b009-114">[in] Указатель на структуру [ENTRYLIST](entrylist.md) , который содержит массив идентификаторов запись для проверки.</span><span class="sxs-lookup"><span data-stu-id="3b009-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b009-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b009-115">Return value</span></span>

<span data-ttu-id="3b009-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b009-116">TRUE</span></span> 
  
> <span data-ttu-id="3b009-117">Один или несколько идентификаторов указанного элемента являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="3b009-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="3b009-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="3b009-118">FALSE</span></span> 
  
> <span data-ttu-id="3b009-119">Все идентификаторы перечисленных записи являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="3b009-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b009-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b009-120">Remarks</span></span>

<span data-ttu-id="3b009-121">Функция **FBadEntryList** определяет, если список идентификаторов запись был создан неправильно.</span><span class="sxs-lookup"><span data-stu-id="3b009-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="3b009-122">Пример недопустимый идентификатор — один для неправильно выделенной памяти или идентификатор неправильный размер.</span><span class="sxs-lookup"><span data-stu-id="3b009-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

