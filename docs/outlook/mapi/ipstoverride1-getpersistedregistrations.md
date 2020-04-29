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
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="d6f8f-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="d6f8f-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="d6f8f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6f8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6f8f-105">Получает список регистраций для файла личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="d6f8f-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="d6f8f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6f8f-106">Parameters</span></span>

 <span data-ttu-id="d6f8f-107">_ппмвал_</span><span class="sxs-lookup"><span data-stu-id="d6f8f-107">_ppmval_</span></span>
  
> <span data-ttu-id="d6f8f-108">возврата Указатель на указатель на структуру [спропвалуе](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d6f8f-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="d6f8f-109">Элемент Улпроптаг данной структуры имеет тип PT_MV_UNICODE, а элемент Мвсзв Value будет массивом строк Юникода с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="d6f8f-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="d6f8f-110">Эти строки представляют собой пути к DLL, для которых была сохранена регистрация.</span><span class="sxs-lookup"><span data-stu-id="d6f8f-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d6f8f-111">Поддержка PST для ANSI не реализована.</span><span class="sxs-lookup"><span data-stu-id="d6f8f-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d6f8f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6f8f-112">Return value</span></span>

<span data-ttu-id="d6f8f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6f8f-113">S_OK</span></span> 
  
> <span data-ttu-id="d6f8f-114">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d6f8f-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6f8f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d6f8f-115">See also</span></span>



[<span data-ttu-id="d6f8f-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6f8f-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="d6f8f-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6f8f-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

