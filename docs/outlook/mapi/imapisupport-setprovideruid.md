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
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809169"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="da0e9-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="da0e9-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="da0e9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da0e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da0e9-105">Регистрирует [MAPIUID](mapiuid.md) структуры, который уникальным образом представляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="da0e9-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="da0e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da0e9-106">Parameters</span></span>

 <span data-ttu-id="da0e9-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="da0e9-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="da0e9-108">[in] Указатель на структуру **MAPIUID** , идентифицирующий поставщика хранилища адресной книги или сообщения.</span><span class="sxs-lookup"><span data-stu-id="da0e9-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="da0e9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da0e9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="da0e9-110">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="da0e9-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da0e9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="da0e9-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="da0e9-112">S_OK</span></span> 
  
> <span data-ttu-id="da0e9-113">Структура **MAPIUID** успешно зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="da0e9-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="da0e9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="da0e9-114">Remarks</span></span>

<span data-ttu-id="da0e9-115">Метод **IMAPISupport::SetProviderUID** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки.</span><span class="sxs-lookup"><span data-stu-id="da0e9-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="da0e9-116">Эти поставщики вызов **SetProviderUID** для регистрации уникальный идентификатор, описанного в структуре **MAPIUID** , который указывает _lpProviderID_.</span><span class="sxs-lookup"><span data-stu-id="da0e9-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="da0e9-117">Поставщики включают этот идентификатор в все идентификаторы записи, которые они создают.</span><span class="sxs-lookup"><span data-stu-id="da0e9-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="da0e9-118">MAPI использует структуру **MAPIUID** при отправке исходящих сообщений в очередь MAPI и для определения соответствующего поставщика для обработки запросов клиентов.</span><span class="sxs-lookup"><span data-stu-id="da0e9-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="da0e9-119">Например когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI проверяет **MAPIUID** часть идентификатор записи, сопоставляет его с поставщиком, который передается **SetProviderUID**и вызывает его **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="da0e9-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="da0e9-120">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="da0e9-120">Notes to callers</span></span>

<span data-ttu-id="da0e9-121">Вызов **SetProviderUID** во время входа для регистрации структуры **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="da0e9-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="da0e9-122">MAPI позволяет адресной книги и сообщения поставщиков хранилища для регистрации несколько идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="da0e9-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="da0e9-123">При внесении нескольких звонков на **SetProviderUID**всегда Добавление структуры **MAPIUID** набору поставщика **MAPIUID** структуры, даже в том случае, если **MAPIUID** уже существует.</span><span class="sxs-lookup"><span data-stu-id="da0e9-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="da0e9-124">**SetProviderUID** нельзя удалить **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="da0e9-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da0e9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="da0e9-125">See also</span></span>



[<span data-ttu-id="da0e9-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="da0e9-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="da0e9-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="da0e9-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

