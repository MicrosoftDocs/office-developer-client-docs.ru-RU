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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351326"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="2f24d-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="2f24d-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="2f24d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f24d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f24d-105">Указывает, относится ли сообщение к сообщению в цепочке сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f24d-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f24d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2f24d-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f24d-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="2f24d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2f24d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2f24d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f24d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2f24d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2f24d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2f24d-110">Called by:</span></span>  <br/> |<span data-ttu-id="2f24d-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2f24d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="2f24d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f24d-112">Parameters</span></span>

 <span data-ttu-id="2f24d-113">_Кбпарент_</span><span class="sxs-lookup"><span data-stu-id="2f24d-113">_cbParent_</span></span>
  
> <span data-ttu-id="2f24d-114">возврата Количество байтов в родительском индексе беседы.</span><span class="sxs-lookup"><span data-stu-id="2f24d-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="2f24d-115">_Лпбпарент_</span><span class="sxs-lookup"><span data-stu-id="2f24d-115">_lpbParent_</span></span>
  
> <span data-ttu-id="2f24d-116">возврата Указатель на байты в родительском индексе беседы.</span><span class="sxs-lookup"><span data-stu-id="2f24d-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="2f24d-117">Может иметь значение NULL, если _кбпарент_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2f24d-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="2f24d-118">_Лпкбиндекс_</span><span class="sxs-lookup"><span data-stu-id="2f24d-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="2f24d-119">вышли Указатель на число байтов в новом индексе беседы, возвращенном при вызове.</span><span class="sxs-lookup"><span data-stu-id="2f24d-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="2f24d-120">_Лппбиндекс_</span><span class="sxs-lookup"><span data-stu-id="2f24d-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="2f24d-121">вышли Указатель на указатель на новый индекс беседы, возвращенный при вызове.</span><span class="sxs-lookup"><span data-stu-id="2f24d-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f24d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f24d-122">Return value</span></span>

<span data-ttu-id="2f24d-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f24d-123">S_OK</span></span> 
  
> <span data-ttu-id="2f24d-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2f24d-124">The call succeeded and has returned the expected value or values.</span></span>
    

