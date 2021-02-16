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
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412039"
---
# <a name="closeimsgsession"></a><span data-ttu-id="ff32b-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="ff32b-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="ff32b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff32b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff32b-105">Закрывает сеанс сообщений и все сообщения, созданные в этом сеансе.</span><span class="sxs-lookup"><span data-stu-id="ff32b-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff32b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ff32b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff32b-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="ff32b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="ff32b-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ff32b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff32b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff32b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff32b-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ff32b-110">Called by:</span></span>  <br/> |<span data-ttu-id="ff32b-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ff32b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="ff32b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff32b-112">Parameters</span></span>

 <span data-ttu-id="ff32b-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="ff32b-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="ff32b-114">[in] Указатель на объект сеанса сообщения, полученный с помощью [функции OpenIMsgSession](openimsgsession.md) в начале сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="ff32b-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff32b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff32b-115">Return value</span></span>

<span data-ttu-id="ff32b-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="ff32b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff32b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff32b-117">Remarks</span></span>

<span data-ttu-id="ff32b-118">Сеанс сообщений используется клиентские приложения и поставщики служб, которые хотят работать с несколькими связанными объектами **MAPI IMessage,** построенными на основе соответствующих объектов OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="ff32b-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="ff32b-119">Клиент или поставщик использует функции [OpenIMsgSession](openimsgsession.md) и **CloseIMsgSession** для переноса создания таких сообщений в сеансе сообщений.</span><span class="sxs-lookup"><span data-stu-id="ff32b-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="ff32b-120">После открытия сеанса сообщения клиент или поставщик передает ему указатель в [вызове OpenIMsgOnIStg](openimsgonistg.md) для создания нового объекта **IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="ff32b-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="ff32b-121">Сеанс сообщения отслеживает все объекты **IMessage** **-on-IStorage,** открытые во время сеанса, а также все вложения и другие свойства сообщений.</span><span class="sxs-lookup"><span data-stu-id="ff32b-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="ff32b-122">Когда клиент или поставщик вызывает **CloseIMsgSession,** он закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="ff32b-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="ff32b-123">Вызов **CloseIMsgSession** — единственный способ закрыть **объекты IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="ff32b-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

