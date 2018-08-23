---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f358467d72f2a9f395762f529244041a5d9d8d6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575982"
---
# <a name="closeimsgsession"></a><span data-ttu-id="ad4fe-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="ad4fe-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="ad4fe-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad4fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad4fe-105">Закрывает сеанса сообщения и все сообщения, созданные в течение этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad4fe-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ad4fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="ad4fe-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="ad4fe-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="ad4fe-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="ad4fe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ad4fe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ad4fe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ad4fe-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ad4fe-110">Called by:</span></span>  <br/> |<span data-ttu-id="ad4fe-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ad4fe-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="ad4fe-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad4fe-112">Parameters</span></span>

 <span data-ttu-id="ad4fe-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="ad4fe-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="ad4fe-114">[in] Указатель на объект сеанса сообщения, полученные с помощью функции [OpenIMsgSession](openimsgsession.md) в начале сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ad4fe-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad4fe-115">Return value</span></span>

<span data-ttu-id="ad4fe-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad4fe-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ad4fe-117">Remarks</span></span>

<span data-ttu-id="ad4fe-118">Сообщение сеанса используется клиентскими приложениями и поставщиками услуг, которые хотите работать с нескольких связанных объектов MAPI **IMessage** , построенные базовые объекты OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="ad4fe-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="ad4fe-119">Клиента или поставщика с помощью функции [OpenIMsgSession](openimsgsession.md) и **CloseIMsgSession** для создания таких сообщений во время сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="ad4fe-120">После запуска сеанса сообщения клиента или поставщика передает указатель на него в вызове [OpenIMsgOnIStg](openimsgonistg.md) для создания нового **IMessage**- на - **IStorage** объект.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="ad4fe-121">Сообщение сеанса хранит информацию о всех объектов **IMessage**- on - **IStorage** , открытых в течение сеанса, помимо все вложения и другие свойства сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="ad4fe-122">Когда клиента или поставщика вызывает **CloseIMsgSession**, закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="ad4fe-123">Вызов **CloseIMsgSession** — это единственный способ закрыть **IMessage**- on - **IStorage** объекты.</span><span class="sxs-lookup"><span data-stu-id="ad4fe-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

