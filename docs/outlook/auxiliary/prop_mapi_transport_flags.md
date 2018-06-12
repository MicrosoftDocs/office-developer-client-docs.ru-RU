---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Представляет параметры транспорта, используемые Outlook для определения необходимости синхронизации задач и отключить элементы пользовательского интерфейса (UI), которые учетной записи не поддерживаются.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807946"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="a74a2-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a74a2-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="a74a2-104">Представляет параметры транспорта, используемые Outlook для определения необходимости синхронизации задач и отключить элементы пользовательского интерфейса (UI), которые учетной записи не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a74a2-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a74a2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a74a2-105">Quick info</span></span>

<span data-ttu-id="a74a2-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a74a2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a74a2-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a74a2-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a74a2-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="a74a2-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="a74a2-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="a74a2-109">Property type:</span></span>  <br/> |<span data-ttu-id="a74a2-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a74a2-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a74a2-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="a74a2-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a74a2-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="a74a2-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="a74a2-113">Access:</span><span class="sxs-lookup"><span data-stu-id="a74a2-113">Access:</span></span>  <br/> |<span data-ttu-id="a74a2-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a74a2-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a74a2-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a74a2-115">Remarks</span></span>

<span data-ttu-id="a74a2-116">Получение или задание этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="a74a2-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="a74a2-117">Возвращает **MAPIACCT_SEND_ONLY** , если учетная запись можно только отправлять сообщения, но не могут получать сообщения.</span><span class="sxs-lookup"><span data-stu-id="a74a2-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="a74a2-118">В этом случае Outlook отключает пользовательского интерфейса, который не применяется к этому типу учетные записи (например, пользовательский Интерфейс для **Отправки и получения**).</span><span class="sxs-lookup"><span data-stu-id="a74a2-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a74a2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a74a2-119">See also</span></span>

- [<span data-ttu-id="a74a2-120">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="a74a2-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="a74a2-121">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="a74a2-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

