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
# <a name="openimsgsession"></a><span data-ttu-id="87588-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="87588-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="87588-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87588-105">Создает и открывает сеанс сообщений, в котором группируются сообщения, созданные в нем.</span><span class="sxs-lookup"><span data-stu-id="87588-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87588-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87588-106">Header file:</span></span>  <br/> |<span data-ttu-id="87588-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="87588-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="87588-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="87588-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="87588-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="87588-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="87588-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="87588-110">Called by:</span></span>  <br/> |<span data-ttu-id="87588-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="87588-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="87588-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="87588-112">Parameters</span></span>

 <span data-ttu-id="87588-113">_Лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="87588-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="87588-114">возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для [выделения](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) OLE.</span><span class="sxs-lookup"><span data-stu-id="87588-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="87588-115">При работе с интерфейсом OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) для MAPI необходимо использовать этот метод распределения.</span><span class="sxs-lookup"><span data-stu-id="87588-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="87588-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87588-116">_ulFlags_</span></span>
  
> <span data-ttu-id="87588-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="87588-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="87588-118">_Лппмсгсесс_</span><span class="sxs-lookup"><span data-stu-id="87588-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="87588-119">вышли Указатель на указатель на возвращенный объект сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="87588-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87588-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87588-120">Return value</span></span>

<span data-ttu-id="87588-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="87588-121">S_OK</span></span>
  
> <span data-ttu-id="87588-122">Сеанс открыт.</span><span class="sxs-lookup"><span data-stu-id="87588-122">The session was opened.</span></span>
    
<span data-ttu-id="87588-123">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="87588-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="87588-124">_лпмаллок_ или _ЛППМСГСЕСС_ имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="87588-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="87588-125">МАПИ_Е_ИНВАЛИД_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="87588-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="87588-126">Переданы неДопустимые флаги.</span><span class="sxs-lookup"><span data-stu-id="87588-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="87588-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87588-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="87588-128">При вызове этой функции клиент или поставщик услуг устанавливает флаг МАПИ_УНИКОДЕ для создания файлов Unicode. MSG.</span><span class="sxs-lookup"><span data-stu-id="87588-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="87588-129">Полученный в результате файл [iMessage](imessageimapiprop.md) показывает сторе_уникоде_ок в своем пр_сторе_суппорт_маск и поддерживает свойства Юникода.</span><span class="sxs-lookup"><span data-stu-id="87588-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87588-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="87588-130">Remarks</span></span>

<span data-ttu-id="87588-131">Сеанс сообщений используется клиентскими приложениями и поставщиками услуг, которые хотят работать с несколькими связанными объектами MAPI [iMessage: IMAPIProp](imessageimapiprop.md) , построенными на основе базовых объектов OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87588-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="87588-132">Клиент или поставщик использует функции **опенимсгсессион** и [клосеимсгсессион](closeimsgsession.md) , чтобы создать оболочку для создания таких сообщений в сеансе сообщений.</span><span class="sxs-lookup"><span data-stu-id="87588-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="87588-133">После открытия сеанса сообщения клиент или поставщик передает указатель на него в вызове [опенимсгонистг](openimsgonistg.md) для создания нового объекта **iMessage**-On- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87588-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="87588-134">В сеансе сообщений отслеживается все объекты **iMessage**(ON — **IStorage** ), созданные в течение сеанса, а также все вложения и другие свойства сообщений.</span><span class="sxs-lookup"><span data-stu-id="87588-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="87588-135">Когда клиент или поставщик вызывает **клосеимсгсессион**, он закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="87588-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="87588-136">Вызов **клосеимсгсессион** является единственным способом закрытия объектов **iMessage**-On- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87588-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="87588-137">**Опенимсгсессион** используется клиентами и поставщиками, которым требуется возможность обрабатывать несколько связанных сообщений в виде объектов OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87588-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="87588-138">Если необходимо одновременно открыть только одно такое сообщение, нет необходимости отслеживать несколько сообщений и нет причин создавать сеанс сообщений с **опенимсгсессион**.</span><span class="sxs-lookup"><span data-stu-id="87588-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="87588-139">Так как он работает с базовым объектом OLE, MAPI должен использовать выделение памяти OLE.</span><span class="sxs-lookup"><span data-stu-id="87588-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="87588-140">Более подробную информацию об объектах структурированного хранилища OLE и выделении памяти OLE можно узнать в статье [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="87588-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

