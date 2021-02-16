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
# <a name="openimsgsession"></a><span data-ttu-id="87fd2-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="87fd2-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="87fd2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87fd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87fd2-105">Создает и открывает сеанс сообщений, в который будут сгруппы сообщения, созданные в нем.</span><span class="sxs-lookup"><span data-stu-id="87fd2-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87fd2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87fd2-106">Header file:</span></span>  <br/> |<span data-ttu-id="87fd2-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="87fd2-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="87fd2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="87fd2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="87fd2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="87fd2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="87fd2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="87fd2-110">Called by:</span></span>  <br/> |<span data-ttu-id="87fd2-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="87fd2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="87fd2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="87fd2-112">Parameters</span></span>

 <span data-ttu-id="87fd2-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="87fd2-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="87fd2-114">[in] Указатель на объект-память для размещения интерфейса OLE [IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)</span><span class="sxs-lookup"><span data-stu-id="87fd2-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="87fd2-115">MAPI должен использовать этот метод выделения при работе с интерфейсом OLE [IStorage.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)</span><span class="sxs-lookup"><span data-stu-id="87fd2-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="87fd2-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87fd2-116">_ulFlags_</span></span>
  
> <span data-ttu-id="87fd2-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="87fd2-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="87fd2-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="87fd2-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="87fd2-119">[out] Указатель на указатель на возвращенный объект сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="87fd2-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87fd2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87fd2-120">Return value</span></span>

<span data-ttu-id="87fd2-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="87fd2-121">S_OK</span></span>
  
> <span data-ttu-id="87fd2-122">Сеанс открыт.</span><span class="sxs-lookup"><span data-stu-id="87fd2-122">The session was opened.</span></span>
    
<span data-ttu-id="87fd2-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87fd2-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="87fd2-124">_lpMalloc_ или  _lppMsgSess имеет_ NULL.</span><span class="sxs-lookup"><span data-stu-id="87fd2-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="87fd2-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="87fd2-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="87fd2-126">Были переданы недопустимые флаги.</span><span class="sxs-lookup"><span data-stu-id="87fd2-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="87fd2-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87fd2-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="87fd2-128">При вызове этой функции клиент или поставщик услуг устанавливает флаг MAPI_UNICODE для создания MSG-файлов Юникода.</span><span class="sxs-lookup"><span data-stu-id="87fd2-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="87fd2-129">В [итоговом файле Imessage](imessageimapiprop.md) STORE_UNICODE_OK в PR_STORE_SUPPORT_MASK поддерживаются свойства Юникод.</span><span class="sxs-lookup"><span data-stu-id="87fd2-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87fd2-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="87fd2-130">Remarks</span></span>

<span data-ttu-id="87fd2-131">Сеанс сообщений используется клиентские приложения и поставщики служб, которые хотят иметь дело с несколькими связанными объектами MAPI [IMessage: IMAPIProp,](imessageimapiprop.md) построенными на основе объектов OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="87fd2-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="87fd2-132">Клиент или поставщик использует функции **OpenIMsgSession** и [CloseIMsgSession](closeimsgsession.md) для переноса создания таких сообщений в сеансе сообщений.</span><span class="sxs-lookup"><span data-stu-id="87fd2-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="87fd2-133">После открытия сеанса сообщения клиент или поставщик передает ему указатель в [вызове OpenIMsgOnIStg](openimsgonistg.md) для создания нового объекта **IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="87fd2-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="87fd2-134">Сеанс сообщения отслеживает все объекты **IMessage** **-on-IStorage,** созданные во время сеанса, а также все вложения и другие свойства сообщений.</span><span class="sxs-lookup"><span data-stu-id="87fd2-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="87fd2-135">Когда клиент или поставщик вызывает **CloseIMsgSession,** он закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="87fd2-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="87fd2-136">Вызов **CloseIMsgSession** — единственный способ закрыть **объекты IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="87fd2-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="87fd2-137">**OpenIMsgSession** используется клиентами и поставщиками, которые требуют возможности обработки нескольких связанных сообщений в качестве объектов **OLE IStorage.**</span><span class="sxs-lookup"><span data-stu-id="87fd2-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="87fd2-138">Если одновременно нужно открыть только одно такое сообщение, нет необходимости отслеживать несколько сообщений и нет причин создавать сеанс сообщений с **помощью OpenIMsgSession.**</span><span class="sxs-lookup"><span data-stu-id="87fd2-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="87fd2-139">Так как он имеет дело с объектом OLE, MAPI должен использовать выделение памяти OLE.</span><span class="sxs-lookup"><span data-stu-id="87fd2-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="87fd2-140">Дополнительные сведения об объектах OLE, структурированных хранилищах и выделении памяти OLE, см. в [OLE и передаче данных.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="87fd2-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

