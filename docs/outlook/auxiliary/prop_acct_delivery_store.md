---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Представляет идентификатор элемента хранилища доставки по умолчанию для учетной записи.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327673"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="a717f-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="a717f-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="a717f-104">Представляет идентификатор элемента хранилища доставки по умолчанию для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a717f-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a717f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a717f-105">Quick info</span></span>

<span data-ttu-id="a717f-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a717f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a717f-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a717f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a717f-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="a717f-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="a717f-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="a717f-109">Property type:</span></span>  <br/> |<span data-ttu-id="a717f-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a717f-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a717f-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="a717f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a717f-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="a717f-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="a717f-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="a717f-113">Access:</span></span>  <br/> |<span data-ttu-id="a717f-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a717f-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a717f-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a717f-115">Remarks</span></span>

<span data-ttu-id="a717f-116">Получите или задайте значение этого свойства с помощью [иолкаккаунт::](iolkaccount-getprop.md) GetProperty или [Иолкаккаунт:: сетпроп](iolkaccount-setprop.md), соответственно.</span><span class="sxs-lookup"><span data-stu-id="a717f-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="a717f-117">Один из побочных эффектов задания хранилища в качестве хранилища доставки по умолчанию для учетной записи состоит в том, что при запуске Outlook создает папки поиска для этого хранилища, если они еще не существуют, и перечислите магазин в списке дел.</span><span class="sxs-lookup"><span data-stu-id="a717f-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a717f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a717f-118">See also</span></span>

- [<span data-ttu-id="a717f-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="a717f-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="a717f-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="a717f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

