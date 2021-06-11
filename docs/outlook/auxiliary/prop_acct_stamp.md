---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Возвращает штамп учетной записи.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408252"
---
# <a name="prop_acct_stamp"></a><span data-ttu-id="abc5c-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="abc5c-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="abc5c-104">Возвращает штамп учетной записи.</span><span class="sxs-lookup"><span data-stu-id="abc5c-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="abc5c-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="abc5c-105">Quick info</span></span>

<span data-ttu-id="abc5c-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="abc5c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abc5c-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="abc5c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="abc5c-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="abc5c-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="abc5c-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="abc5c-109">Property type:</span></span>  <br/> |<span data-ttu-id="abc5c-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="abc5c-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="abc5c-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="abc5c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="abc5c-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="abc5c-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="abc5c-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="abc5c-113">Access:</span></span>  <br/> |<span data-ttu-id="abc5c-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="abc5c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abc5c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="abc5c-115">Remarks</span></span>

<span data-ttu-id="abc5c-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="abc5c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="abc5c-117">Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="abc5c-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abc5c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="abc5c-118">See also</span></span>

- [<span data-ttu-id="abc5c-119">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="abc5c-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="abc5c-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="abc5c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

