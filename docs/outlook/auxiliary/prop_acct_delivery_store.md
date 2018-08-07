---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Представляет идентификатор записи хранилища доставки по умолчанию для учетной записи.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807933"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="d9b1a-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="d9b1a-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="d9b1a-104">Представляет идентификатор записи хранилища доставки по умолчанию для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9b1a-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d9b1a-105">Quick info</span></span>

<span data-ttu-id="d9b1a-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d9b1a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9b1a-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d9b1a-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d9b1a-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="d9b1a-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="d9b1a-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="d9b1a-109">Property type:</span></span>  <br/> |<span data-ttu-id="d9b1a-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d9b1a-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d9b1a-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="d9b1a-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d9b1a-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="d9b1a-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="d9b1a-113">Access:</span><span class="sxs-lookup"><span data-stu-id="d9b1a-113">Access:</span></span>  <br/> |<span data-ttu-id="d9b1a-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9b1a-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9b1a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9b1a-115">Remarks</span></span>

<span data-ttu-id="d9b1a-116">Получение или задание этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="d9b1a-117">Один из побочные эффекты Установка хранилища в качестве хранилища доставки по умолчанию для учетной записи — это, что при запуске Outlook, Outlook создает папки поиска для этого хранилища, если они еще не существует и список дел в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9b1a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d9b1a-118">See also</span></span>

- [<span data-ttu-id="d9b1a-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="d9b1a-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="d9b1a-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="d9b1a-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

