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
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812208"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="9f3bd-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="9f3bd-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="9f3bd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f3bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f3bd-105">Указывает, где принадлежит сообщение в поток сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f3bd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9f3bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f3bd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9f3bd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9f3bd-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9f3bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f3bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f3bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f3bd-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9f3bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f3bd-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="9f3bd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="9f3bd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f3bd-112">Parameters</span></span>

 <span data-ttu-id="9f3bd-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="9f3bd-113">_cbParent_</span></span>
  
> <span data-ttu-id="9f3bd-114">[in] Число байт в индексе родительского беседы.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="9f3bd-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="9f3bd-115">_lpbParent_</span></span>
  
> <span data-ttu-id="9f3bd-116">[in] Указатель на байт в индексе родительского беседы.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="9f3bd-117">Это может быть NULL, если _cbParent_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="9f3bd-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="9f3bd-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="9f3bd-119">[out] Указатель на число байт в новый индекс беседы, возвращаемого при вызове.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="9f3bd-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="9f3bd-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="9f3bd-121">[out] Указатель на указатель на новый индекс беседы, возвращаемого при вызове.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f3bd-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="9f3bd-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9f3bd-123">S_OK</span></span> 
  
> <span data-ttu-id="9f3bd-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9f3bd-124">The call succeeded and has returned the expected value or values.</span></span>
    

