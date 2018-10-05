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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389626"
---
# <a name="openimsgsession"></a><span data-ttu-id="dd52b-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="dd52b-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="dd52b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd52b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd52b-105">Создает и открывает сеанс сообщения с группировкой сообщения, создаваемые в ней.</span><span class="sxs-lookup"><span data-stu-id="dd52b-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd52b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dd52b-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd52b-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="dd52b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="dd52b-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="dd52b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd52b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd52b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd52b-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="dd52b-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd52b-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="dd52b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="dd52b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd52b-112">Parameters</span></span>

 <span data-ttu-id="dd52b-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="dd52b-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="dd52b-114">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="dd52b-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="dd52b-115">Необходимо использовать этот метод для распределения при работе с помощью интерфейса OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) MAPI.</span><span class="sxs-lookup"><span data-stu-id="dd52b-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="dd52b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd52b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="dd52b-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="dd52b-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="dd52b-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="dd52b-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="dd52b-119">[out] Указатель на указатель на объект сеанса возвращенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd52b-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd52b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd52b-120">Return value</span></span>

<span data-ttu-id="dd52b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd52b-121">S_OK</span></span>
  
> <span data-ttu-id="dd52b-122">Сеанс был открыт.</span><span class="sxs-lookup"><span data-stu-id="dd52b-122">The session was opened.</span></span>
    
<span data-ttu-id="dd52b-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd52b-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="dd52b-124">_lpMalloc_ или _lppMsgSess_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dd52b-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="dd52b-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dd52b-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="dd52b-126">Переданы недопустимые флаги.</span><span class="sxs-lookup"><span data-stu-id="dd52b-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="dd52b-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd52b-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="dd52b-128">При вызове этой функции клиента или поставщика задается флаг MAPI_UNICODE для создания файлов MSG-файл в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="dd52b-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="dd52b-129">Созданный файл [Imessage](imessageimapiprop.md) показывает STORE_UNICODE_OK в его PR_STORE_SUPPORT_MASK и поддерживает Юникод свойства.</span><span class="sxs-lookup"><span data-stu-id="dd52b-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dd52b-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd52b-130">Remarks</span></span>

<span data-ttu-id="dd52b-131">Сеанса сообщения используется клиентскими приложениями, а также поставщиков услуг, чтобы работать с несколькими соответствующие MAPI [IMessage: IMAPIProp](imessageimapiprop.md) объекты, построенные на основе базовых объектов OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="dd52b-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="dd52b-132">Клиента или поставщика с помощью функции **OpenIMsgSession** и [CloseIMsgSession](closeimsgsession.md) для создания таких сообщений во время сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="dd52b-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="dd52b-133">После запуска сеанса сообщения клиента или поставщика передает указатель на него в вызове [OpenIMsgOnIStg](openimsgonistg.md) для создания нового **IMessage**- на - **IStorage** объект.</span><span class="sxs-lookup"><span data-stu-id="dd52b-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="dd52b-134">Сообщение сеанса хранит информацию о всех **IMessage**- on - **IStorage** объекты, созданные во время на протяжении сеанса, помимо все вложения и другие свойства сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd52b-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="dd52b-135">Когда клиента или поставщика вызывает **CloseIMsgSession**, закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="dd52b-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="dd52b-136">Вызов **CloseIMsgSession** — это единственный способ закрыть **IMessage**- on - **IStorage** объекты.</span><span class="sxs-lookup"><span data-stu-id="dd52b-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="dd52b-137">**OpenIMsgSession** используется клиентов и поставщиков, которым требуется возможность обработки нескольких связанных сообщений как объекты OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="dd52b-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="dd52b-138">Если только одного сообщения должны быть открыты одновременно, нет необходимости для отслеживания нескольких сообщений и нет причин для создания сеанса сообщения с **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="dd52b-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="dd52b-139">Так как иметь дело с базовым объектом OLE, MAPI необходимо использовать выделения памяти для OLE.</span><span class="sxs-lookup"><span data-stu-id="dd52b-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="dd52b-140">Дополнительные сведения об объектах СТРУКТУРИРОВАННОГО хранилища и выделение памяти OLE можно [OLE и передачи данных](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd52b-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

