---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Значение true, если учетная запись является учетной записью Exchange.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418234"
---
# <a name="propacctisexch"></a><span data-ttu-id="b4a12-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="b4a12-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="b4a12-104">Значение true, если учетная запись является учетной записью Exchange.</span><span class="sxs-lookup"><span data-stu-id="b4a12-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b4a12-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b4a12-105">Quick info</span></span>

<span data-ttu-id="b4a12-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b4a12-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4a12-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b4a12-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b4a12-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="b4a12-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="b4a12-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="b4a12-109">Property type:</span></span>  <br/> |<span data-ttu-id="b4a12-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4a12-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4a12-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="b4a12-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b4a12-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="b4a12-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="b4a12-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="b4a12-113">Access:</span></span>  <br/> |<span data-ttu-id="b4a12-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4a12-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4a12-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4a12-115">Remarks</span></span>

<span data-ttu-id="b4a12-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="b4a12-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="b4a12-117">Если клиент пытается установить это свойство, это свойство возвращает **е_олк_проп_реад_онли**.</span><span class="sxs-lookup"><span data-stu-id="b4a12-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4a12-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b4a12-118">See also</span></span>

- [<span data-ttu-id="b4a12-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="b4a12-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="b4a12-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="b4a12-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

