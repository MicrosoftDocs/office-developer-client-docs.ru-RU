---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326196"
---
# <a name="openimsgsession"></a><span data-ttu-id="238d6-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="238d6-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="238d6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="238d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="238d6-105">Создает и открывает сеанс сообщений, который группит созданные в нем сообщения.</span><span class="sxs-lookup"><span data-stu-id="238d6-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="238d6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="238d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="238d6-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="238d6-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="238d6-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="238d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="238d6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="238d6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="238d6-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="238d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="238d6-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="238d6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="238d6-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="238d6-112">Parameters</span></span>

 <span data-ttu-id="238d6-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="238d6-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="238d6-114">[in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE [IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)</span><span class="sxs-lookup"><span data-stu-id="238d6-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="238d6-115">MAPI должен использовать этот метод выделения при работе с интерфейсом [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) OLE.</span><span class="sxs-lookup"><span data-stu-id="238d6-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="238d6-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="238d6-116">_ulFlags_</span></span>
  
> <span data-ttu-id="238d6-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="238d6-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="238d6-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="238d6-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="238d6-119">[вышел] Указатель на указатель на объект сеанса возвращенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="238d6-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="238d6-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="238d6-120">Return value</span></span>

<span data-ttu-id="238d6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="238d6-121">S_OK</span></span>
  
> <span data-ttu-id="238d6-122">Сеанс был открыт.</span><span class="sxs-lookup"><span data-stu-id="238d6-122">The session was opened.</span></span>
    
<span data-ttu-id="238d6-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="238d6-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="238d6-124">_lpMalloc_ или  _lppMsgSess_ — это NULL.</span><span class="sxs-lookup"><span data-stu-id="238d6-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="238d6-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="238d6-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="238d6-126">Были переданы недействительные флаги.</span><span class="sxs-lookup"><span data-stu-id="238d6-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="238d6-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="238d6-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="238d6-128">При вызове этой функции клиент или поставщик услуг задает флаг MAPI_UNICODE для создания файлов Unicode .msg.</span><span class="sxs-lookup"><span data-stu-id="238d6-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="238d6-129">В результате файл [Imessage](imessageimapiprop.md) STORE_UNICODE_OK в PR_STORE_SUPPORT_MASK поддерживает свойства Unicode.</span><span class="sxs-lookup"><span data-stu-id="238d6-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="238d6-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="238d6-130">Remarks</span></span>

<span data-ttu-id="238d6-131">Сеанс сообщений используется клиентских приложений и поставщиков услуг, которые хотят иметь дело с несколькими связанными объектами [MAPI IMessage: IMAPIProp,](imessageimapiprop.md) построенными на основе встроенных объектов **IStorage** OLE.</span><span class="sxs-lookup"><span data-stu-id="238d6-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="238d6-132">Клиент или поставщик используют функции **OpenIMsgSession** и [CloseIMsgSession](closeimsgsession.md) для упаковки создания таких сообщений в сеансе сообщений.</span><span class="sxs-lookup"><span data-stu-id="238d6-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="238d6-133">После открытия сеанса сообщений клиент или поставщик передает ему указатель в [вызове в OpenIMsgOnIStg](openimsgonistg.md) для создания нового **объекта IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="238d6-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="238d6-134">Сеанс сообщений отслеживает все **объекты IMessage**-on-IStorage, созданные во время сеанса, а также все вложения и другие свойства сообщений. </span><span class="sxs-lookup"><span data-stu-id="238d6-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="238d6-135">Когда клиент или поставщик вызывает **CloseIMsgSession,** он закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="238d6-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="238d6-136">Вызов **CloseIMsgSession** — это единственный способ закрыть **объекты IMessage-on-IStorage.** </span><span class="sxs-lookup"><span data-stu-id="238d6-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="238d6-137">**OpenIMsgSession** используется клиентами и поставщиками, которые требуют возможности обрабатывать несколько связанных сообщений в качестве объектов **IStorage** OLE.</span><span class="sxs-lookup"><span data-stu-id="238d6-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="238d6-138">Если одновременно должно быть открыто только одно такое сообщение, нет необходимости отслеживать несколько сообщений и нет причин создавать сеанс сообщений с **openIMsgSession.**</span><span class="sxs-lookup"><span data-stu-id="238d6-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="238d6-139">Так как он имеет дело с объектом OLE, MAPI должна использовать распределение памяти OLE.</span><span class="sxs-lookup"><span data-stu-id="238d6-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="238d6-140">Дополнительные сведения о структурированных объектах хранения OLE и распределении памяти OLE см. в [OLE и Data Transfer.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="238d6-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

