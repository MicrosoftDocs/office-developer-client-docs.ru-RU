---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые не поддерживаются учетной записью.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326483"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="6e1dc-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6e1dc-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="6e1dc-104">Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые не поддерживаются учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6e1dc-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6e1dc-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="6e1dc-105">Quick info</span></span>

<span data-ttu-id="6e1dc-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="6e1dc-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e1dc-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6e1dc-107">Identifier:</span></span>  <br/> |<span data-ttu-id="6e1dc-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="6e1dc-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="6e1dc-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="6e1dc-109">Property type:</span></span>  <br/> |<span data-ttu-id="6e1dc-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e1dc-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e1dc-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="6e1dc-111">Property tag:</span></span>  <br/> |<span data-ttu-id="6e1dc-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="6e1dc-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="6e1dc-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="6e1dc-113">Access:</span></span>  <br/> |<span data-ttu-id="6e1dc-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6e1dc-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e1dc-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e1dc-115">Remarks</span></span>

<span data-ttu-id="6e1dc-116">Получите или задайте значение этого свойства с помощью [иолкаккаунт::](iolkaccount-getprop.md) GetProperty или [Иолкаккаунт:: сетпроп](iolkaccount-setprop.md), соответственно.</span><span class="sxs-lookup"><span data-stu-id="6e1dc-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="6e1dc-117">Возвращает **мапиаккт_сенд_онли** , если учетная запись может отправлять только сообщения, но не может получать сообщения.</span><span class="sxs-lookup"><span data-stu-id="6e1dc-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="6e1dc-118">В этом случае Outlook отключает пользовательский интерфейс, который не применяется к учетным записям этого типа (например, Пользовательский интерфейс для **отправки и получения**).</span><span class="sxs-lookup"><span data-stu-id="6e1dc-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e1dc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6e1dc-119">See also</span></span>

- [<span data-ttu-id="6e1dc-120">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="6e1dc-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="6e1dc-121">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="6e1dc-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

