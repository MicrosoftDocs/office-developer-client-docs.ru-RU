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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570438"
---
# <a name="fpropexists"></a><span data-ttu-id="c7177-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="c7177-103">FPropExists</span></span>

  
  
<span data-ttu-id="c7177-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7177-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7177-105">Выполняет поиск тега заданного свойства в интерфейс [IMAPIProp](imapipropiunknown.md) или интерфейса на основе **IMAPIProp**, такие как [IMessage](imessageimapiprop.md) или [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="c7177-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7177-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c7177-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7177-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c7177-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c7177-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c7177-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c7177-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c7177-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c7177-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c7177-110">Called by:</span></span>  <br/> |<span data-ttu-id="c7177-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="c7177-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="c7177-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7177-112">Parameters</span></span>

 <span data-ttu-id="c7177-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="c7177-113">_pobj_</span></span>
  
> <span data-ttu-id="c7177-114">[in] Указатель на интерфейс **IMAPIProp** или интерфейс, производные от **IMAPIProp** , в которой нужно выполнить поиск тега свойства.</span><span class="sxs-lookup"><span data-stu-id="c7177-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="c7177-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c7177-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="c7177-116">[in] Свойство tag для поиска.</span><span class="sxs-lookup"><span data-stu-id="c7177-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7177-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7177-117">Return value</span></span>

<span data-ttu-id="c7177-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="c7177-118">TRUE</span></span> 
  
> <span data-ttu-id="c7177-119">Найдено совпадение для тега данного свойства.</span><span class="sxs-lookup"><span data-stu-id="c7177-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="c7177-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7177-120">FALSE</span></span> 
  
> <span data-ttu-id="c7177-121">Не найдено соответствие для указанного свойства тега.</span><span class="sxs-lookup"><span data-stu-id="c7177-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7177-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7177-122">Remarks</span></span>

<span data-ttu-id="c7177-123">Если свойство tag с помощью параметра _ulPropTag_ имеет тип PT_UNSPECIFIED, функция **FPropExists** выполняет поиск только на основе свойства идентификатора соответствия.</span><span class="sxs-lookup"><span data-stu-id="c7177-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="c7177-124">В противном случае учитывается для тега всего свойства, включая тип.</span><span class="sxs-lookup"><span data-stu-id="c7177-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

