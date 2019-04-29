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
# <a name="closeimsgsession"></a><span data-ttu-id="fd827-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="fd827-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="fd827-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd827-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd827-105">ЗаКрывает сеанс сообщения и все сообщения, созданные в этом сеансе.</span><span class="sxs-lookup"><span data-stu-id="fd827-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd827-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fd827-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd827-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="fd827-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="fd827-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="fd827-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fd827-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fd827-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fd827-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="fd827-110">Called by:</span></span>  <br/> |<span data-ttu-id="fd827-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="fd827-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="fd827-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd827-112">Parameters</span></span>

 <span data-ttu-id="fd827-113">_Лпмсгсесс_</span><span class="sxs-lookup"><span data-stu-id="fd827-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="fd827-114">возврата Указатель на объект сеанса сообщения, полученный с помощью функции [опенимсгсессион](openimsgsession.md) в начале сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="fd827-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fd827-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd827-115">Return value</span></span>

<span data-ttu-id="fd827-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="fd827-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd827-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd827-117">Remarks</span></span>

<span data-ttu-id="fd827-118">Сеанс сообщений используется клиентскими приложениями и поставщиками услуг, которые хотят работать с несколькими связанными объектами MAPI **iMessage** , построенными на основе базовых объектов OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="fd827-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="fd827-119">Клиент или поставщик использует функции [опенимсгсессион](openimsgsession.md) и **клосеимсгсессион** , чтобы создать оболочку для создания таких сообщений в сеансе сообщений.</span><span class="sxs-lookup"><span data-stu-id="fd827-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="fd827-120">После открытия сеанса сообщения клиент или поставщик передает указатель на него в вызове [опенимсгонистг](openimsgonistg.md) для создания нового объекта **iMessage**-On- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="fd827-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="fd827-121">В сеансе сообщений отслеживается все объекты **iMessage**(ON — **IStorage** ), открытые в течение сеанса, а также все вложения и другие свойства сообщений.</span><span class="sxs-lookup"><span data-stu-id="fd827-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="fd827-122">Когда клиент или поставщик вызывает **клосеимсгсессион**, он закрывает все эти объекты.</span><span class="sxs-lookup"><span data-stu-id="fd827-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="fd827-123">Вызов **клосеимсгсессион** является единственным способом закрытия объектов **iMessage**-On- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="fd827-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

