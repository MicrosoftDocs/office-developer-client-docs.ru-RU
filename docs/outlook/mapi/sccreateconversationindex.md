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
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594154"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="a6a41-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="a6a41-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="a6a41-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6a41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6a41-105">Указывает, где принадлежит сообщение в поток сообщений.</span><span class="sxs-lookup"><span data-stu-id="a6a41-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6a41-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a6a41-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6a41-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a6a41-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a6a41-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a6a41-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6a41-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a41-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a6a41-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a6a41-110">Called by:</span></span>  <br/> |<span data-ttu-id="a6a41-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="a6a41-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="a6a41-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6a41-112">Parameters</span></span>

 <span data-ttu-id="a6a41-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="a6a41-113">_cbParent_</span></span>
  
> <span data-ttu-id="a6a41-114">[in] Число байт в индексе родительского беседы.</span><span class="sxs-lookup"><span data-stu-id="a6a41-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="a6a41-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="a6a41-115">_lpbParent_</span></span>
  
> <span data-ttu-id="a6a41-116">[in] Указатель на байт в индексе родительского беседы.</span><span class="sxs-lookup"><span data-stu-id="a6a41-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="a6a41-117">Это может быть NULL, если _cbParent_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a6a41-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="a6a41-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="a6a41-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="a6a41-119">[out] Указатель на число байт в новый индекс беседы, возвращаемого при вызове.</span><span class="sxs-lookup"><span data-stu-id="a6a41-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="a6a41-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="a6a41-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="a6a41-121">[out] Указатель на указатель на новый индекс беседы, возвращаемого при вызове.</span><span class="sxs-lookup"><span data-stu-id="a6a41-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6a41-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6a41-122">Return value</span></span>

<span data-ttu-id="a6a41-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6a41-123">S_OK</span></span> 
  
> <span data-ttu-id="a6a41-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a6a41-124">The call succeeded and has returned the expected value or values.</span></span>
    

