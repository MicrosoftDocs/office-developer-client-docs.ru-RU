---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True, если учетная запись является Exchange учетной записью.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418234"
---
# <a name="prop_acct_is_exch"></a><span data-ttu-id="40676-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="40676-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="40676-104">True, если учетная запись является Exchange учетной записью.</span><span class="sxs-lookup"><span data-stu-id="40676-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="40676-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="40676-105">Quick info</span></span>

<span data-ttu-id="40676-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="40676-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40676-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="40676-107">Identifier:</span></span>  <br/> |<span data-ttu-id="40676-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="40676-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="40676-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="40676-109">Property type:</span></span>  <br/> |<span data-ttu-id="40676-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="40676-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="40676-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="40676-111">Property tag:</span></span>  <br/> |<span data-ttu-id="40676-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="40676-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="40676-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="40676-113">Access:</span></span>  <br/> |<span data-ttu-id="40676-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="40676-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40676-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="40676-115">Remarks</span></span>

<span data-ttu-id="40676-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="40676-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="40676-117">Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="40676-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40676-118">См. также</span><span class="sxs-lookup"><span data-stu-id="40676-118">See also</span></span>

- [<span data-ttu-id="40676-119">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="40676-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="40676-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="40676-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

