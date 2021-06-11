---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415658"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="325a8-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="325a8-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="325a8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="325a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="325a8-105">Указывает, где в потоке сообщений принадлежит сообщение.</span><span class="sxs-lookup"><span data-stu-id="325a8-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="325a8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="325a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="325a8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="325a8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="325a8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="325a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="325a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="325a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="325a8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="325a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="325a8-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="325a8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="325a8-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="325a8-112">Parameters</span></span>

 <span data-ttu-id="325a8-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="325a8-113">_cbParent_</span></span>
  
> <span data-ttu-id="325a8-114">[in] Количество bytes в индексе родительского разговора.</span><span class="sxs-lookup"><span data-stu-id="325a8-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="325a8-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="325a8-115">_lpbParent_</span></span>
  
> <span data-ttu-id="325a8-116">[in] Указатель на bytes в родительском индексе разговоров.</span><span class="sxs-lookup"><span data-stu-id="325a8-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="325a8-117">Это может быть NULL, если  _значение cbParent_ нулевое.</span><span class="sxs-lookup"><span data-stu-id="325a8-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="325a8-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="325a8-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="325a8-119">[вышел] Указатель на количество bytes в новом индексе беседы, возвращаемом вызовом.</span><span class="sxs-lookup"><span data-stu-id="325a8-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="325a8-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="325a8-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="325a8-121">[вышел] Указатель на указатель на новый индекс беседы, возвращаемый вызовом.</span><span class="sxs-lookup"><span data-stu-id="325a8-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="325a8-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="325a8-122">Return value</span></span>

<span data-ttu-id="325a8-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="325a8-123">S_OK</span></span> 
  
> <span data-ttu-id="325a8-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="325a8-124">The call succeeded and has returned the expected value or values.</span></span>
    

