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
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809540"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="d9b56-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="d9b56-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="d9b56-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9b56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9b56-105">Получение списка регистраций для файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="d9b56-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="d9b56-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9b56-106">Parameters</span></span>

 <span data-ttu-id="d9b56-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="d9b56-107">_ppmval_</span></span>
  
> <span data-ttu-id="d9b56-108">[in] Указатель на указатель на структуру [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b56-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="d9b56-109">Элемент ulPropTag эта структура является типа PT_MV_UNICODE и член значение MVszW будет массив строк Юникод, завершающуюся символом null.</span><span class="sxs-lookup"><span data-stu-id="d9b56-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="d9b56-110">Эти строки, путей к библиотеки DLL, для которых были сохранены регистрации.</span><span class="sxs-lookup"><span data-stu-id="d9b56-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d9b56-111">Поддержка .pst ANSI не реализован.</span><span class="sxs-lookup"><span data-stu-id="d9b56-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d9b56-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="d9b56-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d9b56-113">S_OK</span></span> 
  
> <span data-ttu-id="d9b56-114">Вызов функции прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="d9b56-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9b56-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d9b56-115">See also</span></span>



[<span data-ttu-id="d9b56-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9b56-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="d9b56-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9b56-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

