---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 050068b542616d1ad4d133b289aba46db2888519
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587819"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="b6ab4-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="b6ab4-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="b6ab4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6ab4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6ab4-105">Рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-105">Deprecated.</span></span> <span data-ttu-id="b6ab4-106">Возвращает типы адресов, которые могут быть обработаны всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="b6ab4-107">���������</span><span class="sxs-lookup"><span data-stu-id="b6ab4-107">Parameters</span></span>

 <span data-ttu-id="b6ab4-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6ab4-108">_ulFlags_</span></span>
  
> <span data-ttu-id="b6ab4-109">[in] Битовая маска флаги, которое указывает формат для типов возвращаемых адресов.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="b6ab4-110">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b6ab4-110">The following flag can be set:</span></span>
    
<span data-ttu-id="b6ab4-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6ab4-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b6ab4-112">Типы адресов, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-112">The address types are in Unicode format.</span></span> <span data-ttu-id="b6ab4-113">Если флаг MAPI_UNICODE не установлен, типы адресов, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="b6ab4-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="b6ab4-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="b6ab4-115">[out] Указатель на число типов адрес, на который указывает параметр _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="b6ab4-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="b6ab4-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="b6ab4-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="b6ab4-117">[out] Указатель на массив указатели на типов адресов.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6ab4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6ab4-118">Return value</span></span>

<span data-ttu-id="b6ab4-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6ab4-119">S_OK</span></span> 
  
> <span data-ttu-id="b6ab4-120">Типы адресов были успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6ab4-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="b6ab4-121">Remarks</span></span>

<span data-ttu-id="b6ab4-122">Метод **IMAPISession::EnumAdrTypes** возвращает список типов адресов, которые могут быть обработаны всеми поставщиками транспорта активный в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="b6ab4-123">Типы адресов для поставщиков транспорта, которые не загружаются в настоящее время не включаются в списке.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="b6ab4-124">Поставщики транспорта зарегистрировать для обработки один или несколько типов адресов при MAPI вызывает метод их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="b6ab4-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b6ab4-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b6ab4-125">Notes to callers</span></span>

<span data-ttu-id="b6ab4-126">Вызов [MAPIFreeBuffer](mapifreebuffer.md) для освобождения массив строк, на который указывает параметр _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="b6ab4-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6ab4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b6ab4-127">See also</span></span>



[<span data-ttu-id="b6ab4-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="b6ab4-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="b6ab4-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b6ab4-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b6ab4-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6ab4-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

