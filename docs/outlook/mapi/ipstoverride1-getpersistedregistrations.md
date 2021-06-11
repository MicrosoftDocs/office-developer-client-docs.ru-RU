---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415133"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="05c88-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="05c88-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="05c88-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05c88-105">Извлекает список регистраций для файла "Личные папки" (PST).</span><span class="sxs-lookup"><span data-stu-id="05c88-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="05c88-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="05c88-106">Parameters</span></span>

 <span data-ttu-id="05c88-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="05c88-107">_ppmval_</span></span>
  
> <span data-ttu-id="05c88-108">[in] Указатель на указатель на [структуру SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="05c88-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="05c88-109">Член ulPropTag этой структуры имеет тип PT_MV_UNICODE, а член значения MVszW будет массивом null-terminated строк Юникод.</span><span class="sxs-lookup"><span data-stu-id="05c88-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="05c88-110">Эти строки являются путями к DLLs, для которых регистрация сохраняется.</span><span class="sxs-lookup"><span data-stu-id="05c88-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="05c88-111">Поддержка PST для ANSI не реализована.</span><span class="sxs-lookup"><span data-stu-id="05c88-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="05c88-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05c88-112">Return value</span></span>

<span data-ttu-id="05c88-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="05c88-113">S_OK</span></span> 
  
> <span data-ttu-id="05c88-114">Вызов функции был успешным.</span><span class="sxs-lookup"><span data-stu-id="05c88-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05c88-115">См. также</span><span class="sxs-lookup"><span data-stu-id="05c88-115">See also</span></span>



[<span data-ttu-id="05c88-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05c88-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="05c88-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05c88-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

