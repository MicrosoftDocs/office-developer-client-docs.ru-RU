---
title: Имаписессионенумадртипес
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
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338439"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="4b06a-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="4b06a-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="4b06a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b06a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b06a-105">Устаревшие.</span><span class="sxs-lookup"><span data-stu-id="4b06a-105">Deprecated.</span></span> <span data-ttu-id="4b06a-106">Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4b06a-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="4b06a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b06a-107">Parameters</span></span>

 <span data-ttu-id="4b06a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b06a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="4b06a-109">возврата Битовая маска флагов, указывающая формат для возвращаемых типов адресов.</span><span class="sxs-lookup"><span data-stu-id="4b06a-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="4b06a-110">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4b06a-110">The following flag can be set:</span></span>
    
<span data-ttu-id="4b06a-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4b06a-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4b06a-112">Типы адреса представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="4b06a-112">The address types are in Unicode format.</span></span> <span data-ttu-id="4b06a-113">Если флаг МАПИ_УНИКОДЕ не установлен, типы адреса представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4b06a-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="4b06a-114">_Лпкадртипес_</span><span class="sxs-lookup"><span data-stu-id="4b06a-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="4b06a-115">вышли Указатель на количество типов адресов, на которые указывает параметр _лпппсзадртипес_ .</span><span class="sxs-lookup"><span data-stu-id="4b06a-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="4b06a-116">_Лпппсзадртипес_</span><span class="sxs-lookup"><span data-stu-id="4b06a-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="4b06a-117">вышли Указатель на массив указателей на типы адресов.</span><span class="sxs-lookup"><span data-stu-id="4b06a-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b06a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b06a-118">Return value</span></span>

<span data-ttu-id="4b06a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b06a-119">S_OK</span></span> 
  
> <span data-ttu-id="4b06a-120">Типы адресов успешно получены.</span><span class="sxs-lookup"><span data-stu-id="4b06a-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b06a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b06a-121">Remarks</span></span>

<span data-ttu-id="4b06a-122">Метод **IMAPISession:: енумадртипес** возвращает список типов адресов, которые могут обрабатываться всеми активными поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4b06a-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="4b06a-123">Типы адресов для поставщиков транспорта, которые не загружены в данный момент, не включены в список.</span><span class="sxs-lookup"><span data-stu-id="4b06a-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="4b06a-124">Поставщики транспорта регистрируются для обработки одного или нескольких типов адресов, когда MAPI вызывает метод [иксплогон:: аддресстипес](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="4b06a-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4b06a-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4b06a-125">Notes to callers</span></span>

<span data-ttu-id="4b06a-126">ВыЗовите метод [мапифрибуффер](mapifreebuffer.md) , чтобы освободить массив строк, на который указывает параметр _лпппсзадртипес_ .</span><span class="sxs-lookup"><span data-stu-id="4b06a-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b06a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4b06a-127">See also</span></span>



[<span data-ttu-id="4b06a-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="4b06a-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="4b06a-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4b06a-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4b06a-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b06a-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

