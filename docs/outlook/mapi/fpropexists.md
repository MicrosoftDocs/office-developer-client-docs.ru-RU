---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808500"
---
# <a name="fpropexists"></a><span data-ttu-id="850b3-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="850b3-103">FPropExists</span></span>

  
  
<span data-ttu-id="850b3-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="850b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="850b3-105">Выполняет поиск тега заданного свойства в интерфейс [IMAPIProp](imapipropiunknown.md) или интерфейса на основе **IMAPIProp**, такие как [IMessage](imessageimapiprop.md) или [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="850b3-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="850b3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="850b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="850b3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="850b3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="850b3-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="850b3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="850b3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="850b3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="850b3-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="850b3-110">Called by:</span></span>  <br/> |<span data-ttu-id="850b3-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="850b3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="850b3-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="850b3-112">Parameters</span></span>

 <span data-ttu-id="850b3-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="850b3-113">_pobj_</span></span>
  
> <span data-ttu-id="850b3-114">[in] Указатель на интерфейс **IMAPIProp** или интерфейс, производные от **IMAPIProp** , в которой нужно выполнить поиск тега свойства.</span><span class="sxs-lookup"><span data-stu-id="850b3-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="850b3-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="850b3-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="850b3-116">[in] Свойство tag для поиска.</span><span class="sxs-lookup"><span data-stu-id="850b3-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="850b3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="850b3-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="850b3-118">TRUE</span></span> 
  
> <span data-ttu-id="850b3-119">Найдено совпадение для тега данного свойства.</span><span class="sxs-lookup"><span data-stu-id="850b3-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="850b3-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="850b3-120">FALSE</span></span> 
  
> <span data-ttu-id="850b3-121">Не найдено соответствие для указанного свойства тега.</span><span class="sxs-lookup"><span data-stu-id="850b3-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="850b3-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="850b3-122">Remarks</span></span>

<span data-ttu-id="850b3-123">Если свойство tag с помощью параметра _ulPropTag_ имеет тип PT_UNSPECIFIED, функция **FPropExists** выполняет поиск только на основе свойства идентификатора соответствия.</span><span class="sxs-lookup"><span data-stu-id="850b3-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="850b3-124">В противном случае учитывается для тега всего свойства, включая тип.</span><span class="sxs-lookup"><span data-stu-id="850b3-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

