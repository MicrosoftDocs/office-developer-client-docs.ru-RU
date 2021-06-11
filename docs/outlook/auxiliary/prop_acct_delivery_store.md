---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Представляет ID входа в хранилище доставки по умолчанию для учетной записи.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418899"
---
# <a name="prop_acct_delivery_store"></a><span data-ttu-id="4d350-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="4d350-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="4d350-104">Представляет ID входа в хранилище доставки по умолчанию для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4d350-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4d350-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4d350-105">Quick info</span></span>

<span data-ttu-id="4d350-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4d350-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d350-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4d350-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4d350-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="4d350-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="4d350-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="4d350-109">Property type:</span></span>  <br/> |<span data-ttu-id="4d350-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4d350-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4d350-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="4d350-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4d350-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="4d350-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="4d350-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="4d350-113">Access:</span></span>  <br/> |<span data-ttu-id="4d350-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4d350-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d350-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d350-115">Remarks</span></span>

<span data-ttu-id="4d350-116">Получите или установите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="4d350-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="4d350-117">Одним из побочных эффектов настройки магазина в качестве магазина доставки по умолчанию для учетной записи является то, что при запуске Outlook Outlook создает папки поиска для этого магазина, если они еще не существуют, и перечислить магазин в To-Do Bar.</span><span class="sxs-lookup"><span data-stu-id="4d350-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d350-118">См. также</span><span class="sxs-lookup"><span data-stu-id="4d350-118">See also</span></span>

- [<span data-ttu-id="4d350-119">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="4d350-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="4d350-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="4d350-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

