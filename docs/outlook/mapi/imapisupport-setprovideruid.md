---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437541"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="c4c91-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="c4c91-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="c4c91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4c91-105">Регистрирует [структуру MAPIUID,](mapiuid.md) которая однозначно представляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="c4c91-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c4c91-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c4c91-106">Parameters</span></span>

 <span data-ttu-id="c4c91-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="c4c91-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="c4c91-108">[in] Указатель на структуру **MAPIUID,** которая определяет адресную книгу или поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="c4c91-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="c4c91-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4c91-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c4c91-110">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="c4c91-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4c91-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4c91-111">Return value</span></span>

<span data-ttu-id="c4c91-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4c91-112">S_OK</span></span> 
  
> <span data-ttu-id="c4c91-113">Структура **MAPIUID** успешно зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="c4c91-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c4c91-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4c91-114">Remarks</span></span>

<span data-ttu-id="c4c91-115">Метод **IMAPISupport::SetProviderUID** реализован для объектов поддержки поставщиков адресной книги и магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="c4c91-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="c4c91-116">Эти поставщики звонят **SetProviderUID** для регистрации уникального идентификатора, описанного в структуре **MAPIUID,** на который указывает _lpProviderID._</span><span class="sxs-lookup"><span data-stu-id="c4c91-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="c4c91-117">Поставщики включают этот идентификатор во все идентификаторы записи, которые они создают.</span><span class="sxs-lookup"><span data-stu-id="c4c91-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="c4c91-118">MapI использует структуру **MAPIUID,** когда отправляет исходящие сообщения в пулер MAPI и определяет подходящего поставщика для обработки запросов клиентов.</span><span class="sxs-lookup"><span data-stu-id="c4c91-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="c4c91-119">Например, когда клиент вызывает метод [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI проверяет часть **MAPIUID** идентификатора входа, передает ее поставщику, передав его **SetProviderUID,** и вызывает **openEntry** этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="c4c91-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c4c91-120">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c4c91-120">Notes to callers</span></span>

<span data-ttu-id="c4c91-121">Вызов **SetProviderUID во** время регистрации **структуры MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="c4c91-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="c4c91-122">MAPI позволяет поставщикам адресных книг и магазинов сообщений регистрировать несколько идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="c4c91-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="c4c91-123">При многократном вызове **в SetProviderUID** структура **MAPIUID** всегда добавляется в набор структур **MAPIUID** поставщика, даже если **MAPIUID** является дубликатом.</span><span class="sxs-lookup"><span data-stu-id="c4c91-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="c4c91-124">**SetProviderUID** не может удалить **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="c4c91-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4c91-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c4c91-125">See also</span></span>



[<span data-ttu-id="c4c91-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c4c91-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c4c91-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4c91-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

