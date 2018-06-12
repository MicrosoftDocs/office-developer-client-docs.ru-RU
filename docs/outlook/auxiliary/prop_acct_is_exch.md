---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Значение true, если учетная запись является учетной записью Exchange.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807930"
---
# <a name="propacctisexch"></a><span data-ttu-id="d7da3-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="d7da3-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="d7da3-104">Значение true, если учетная запись является учетной записью Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7da3-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d7da3-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d7da3-105">Quick info</span></span>

<span data-ttu-id="d7da3-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d7da3-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7da3-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d7da3-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d7da3-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="d7da3-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="d7da3-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="d7da3-109">Property type:</span></span>  <br/> |<span data-ttu-id="d7da3-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7da3-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7da3-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="d7da3-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d7da3-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="d7da3-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="d7da3-113">Access:</span><span class="sxs-lookup"><span data-stu-id="d7da3-113">Access:</span></span>  <br/> |<span data-ttu-id="d7da3-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d7da3-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7da3-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7da3-115">Remarks</span></span>

<span data-ttu-id="d7da3-116">Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="d7da3-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d7da3-117">При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="d7da3-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7da3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d7da3-118">See also</span></span>

- [<span data-ttu-id="d7da3-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="d7da3-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d7da3-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="d7da3-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

