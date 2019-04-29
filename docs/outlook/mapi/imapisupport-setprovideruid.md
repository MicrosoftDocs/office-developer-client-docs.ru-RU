---
title: Имаписуппортсетпровидеруид
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
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="d494b-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="d494b-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="d494b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d494b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d494b-105">Регистрирует структуру [мапиуид](mapiuid.md) , которая уникально представляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d494b-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d494b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d494b-106">Parameters</span></span>

 <span data-ttu-id="d494b-107">_Лппровидерид_</span><span class="sxs-lookup"><span data-stu-id="d494b-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="d494b-108">возврата Указатель на структуру **мапиуид** , которая идентифицирует адресную книгу или поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d494b-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="d494b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d494b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d494b-110">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d494b-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d494b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d494b-111">Return value</span></span>

<span data-ttu-id="d494b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d494b-112">S_OK</span></span> 
  
> <span data-ttu-id="d494b-113">Структура **мапиуид** успешно зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="d494b-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d494b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d494b-114">Remarks</span></span>

<span data-ttu-id="d494b-115">Метод **имаписуппорт:: сетпровидеруид** реализован для адресных книг и объектов поддержки поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d494b-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="d494b-116">Эти поставщики вызывают **сетпровидеруид** , чтобы зарегистрировать уникальный идентификатор, описанный в структуре **мапиуид** , на которую указывает _лппровидерид_.</span><span class="sxs-lookup"><span data-stu-id="d494b-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="d494b-117">Поставщики включают этот идентификатор во все создаваемые им идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="d494b-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="d494b-118">MAPI использует структуру **мапиуид** при отправке исходящих сообщений в Диспетчер очереди MAPI и для определения соответствующего поставщика для обработки запросов клиентов.</span><span class="sxs-lookup"><span data-stu-id="d494b-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="d494b-119">Например, когда клиент вызывает метод [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI проверяет часть идентификатора записи **мапиуид** , сопоставляет ее с поставщиком, который передавал его в **сетпровидеруид**, и вызывает **OpenEntry** поставщика .</span><span class="sxs-lookup"><span data-stu-id="d494b-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d494b-120">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d494b-120">Notes to callers</span></span>

<span data-ttu-id="d494b-121">Call **сетпровидеруид** во время входа, чтобы зарегистрировать структуру **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="d494b-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="d494b-122">MAPI позволяет поставщикам адресных книг и хранилищ сообщений регистрировать несколько идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="d494b-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="d494b-123">При совершении нескольких вызовов **сетпровидеруид**всегда добавляется структура **мапиуид** в набор структур **Мапиуид** поставщика, даже если **мапиуид** является дубликатом.</span><span class="sxs-lookup"><span data-stu-id="d494b-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="d494b-124">**Сетпровидеруид** не удается удалить **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="d494b-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d494b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d494b-125">See also</span></span>



[<span data-ttu-id="d494b-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d494b-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d494b-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d494b-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

