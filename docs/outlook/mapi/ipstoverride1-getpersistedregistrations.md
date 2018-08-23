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
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575870"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="d319a-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="d319a-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="d319a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d319a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d319a-105">Получение списка регистраций для файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="d319a-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="d319a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d319a-106">Parameters</span></span>

 <span data-ttu-id="d319a-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="d319a-107">_ppmval_</span></span>
  
> <span data-ttu-id="d319a-108">[in] Указатель на указатель на структуру [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d319a-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="d319a-109">Элемент ulPropTag эта структура является типа PT_MV_UNICODE и член значение MVszW будет массив строк Юникод, завершающуюся символом null.</span><span class="sxs-lookup"><span data-stu-id="d319a-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="d319a-110">Эти строки, путей к библиотеки DLL, для которых были сохранены регистрации.</span><span class="sxs-lookup"><span data-stu-id="d319a-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d319a-111">Поддержка .pst ANSI не реализован.</span><span class="sxs-lookup"><span data-stu-id="d319a-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d319a-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d319a-112">Return value</span></span>

<span data-ttu-id="d319a-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d319a-113">S_OK</span></span> 
  
> <span data-ttu-id="d319a-114">Вызов функции прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="d319a-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d319a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d319a-115">See also</span></span>



[<span data-ttu-id="d319a-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d319a-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="d319a-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d319a-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

