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
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327274"
---
# <a name="fpropexists"></a><span data-ttu-id="c1efb-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="c1efb-103">FPropExists</span></span>

  
  
<span data-ttu-id="c1efb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1efb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1efb-105">Ищет заданный тег свойства в интерфейсе [IMAPIProp](imapipropiunknown.md) или интерфейсе, производном от **IMAPIProp**, например [iMessage](imessageimapiprop.md) или [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="c1efb-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1efb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c1efb-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1efb-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="c1efb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c1efb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c1efb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1efb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1efb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1efb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c1efb-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1efb-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c1efb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="c1efb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1efb-112">Parameters</span></span>

 <span data-ttu-id="c1efb-113">_побж_</span><span class="sxs-lookup"><span data-stu-id="c1efb-113">_pobj_</span></span>
  
> <span data-ttu-id="c1efb-114">возврата Указатель на интерфейс или интерфейс **IMAPIProp** , производный от **IMAPIProp** , в котором нужно найти тег свойства.</span><span class="sxs-lookup"><span data-stu-id="c1efb-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="c1efb-115">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="c1efb-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="c1efb-116">возврата Тег свойства для поиска.</span><span class="sxs-lookup"><span data-stu-id="c1efb-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1efb-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1efb-117">Return value</span></span>

<span data-ttu-id="c1efb-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="c1efb-118">TRUE</span></span> 
  
> <span data-ttu-id="c1efb-119">Обнаружено сравнение С указанным тегом свойства.</span><span class="sxs-lookup"><span data-stu-id="c1efb-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="c1efb-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="c1efb-120">FALSE</span></span> 
  
> <span data-ttu-id="c1efb-121">Не найдено сравнение для данного тега свойства.</span><span class="sxs-lookup"><span data-stu-id="c1efb-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1efb-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="c1efb-122">Remarks</span></span>

<span data-ttu-id="c1efb-123">Если тег свойства в параметре _улпроптаг_ имеет тип пт_унспеЦифиед, функция **фпропексистс** ищет для поиска значение только на основе идентификатора свойства.</span><span class="sxs-lookup"><span data-stu-id="c1efb-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="c1efb-124">В противном случае сравнение выполняется для всего тега свойства, включая тип.</span><span class="sxs-lookup"><span data-stu-id="c1efb-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

