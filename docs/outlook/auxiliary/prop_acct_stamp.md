---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Возвращает метку учетной записи.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408252"
---
# <a name="prop_acct_stamp"></a><span data-ttu-id="02624-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="02624-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="02624-104">Возвращает метку учетной записи.</span><span class="sxs-lookup"><span data-stu-id="02624-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="02624-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="02624-105">Quick info</span></span>

<span data-ttu-id="02624-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="02624-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02624-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="02624-107">Identifier:</span></span>  <br/> |<span data-ttu-id="02624-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="02624-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="02624-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="02624-109">Property type:</span></span>  <br/> |<span data-ttu-id="02624-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="02624-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="02624-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="02624-111">Property tag:</span></span>  <br/> |<span data-ttu-id="02624-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="02624-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="02624-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="02624-113">Access:</span></span>  <br/> |<span data-ttu-id="02624-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="02624-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02624-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="02624-115">Remarks</span></span>

<span data-ttu-id="02624-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="02624-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="02624-117">Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="02624-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02624-118">См. также</span><span class="sxs-lookup"><span data-stu-id="02624-118">See also</span></span>

- [<span data-ttu-id="02624-119">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="02624-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="02624-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="02624-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

