---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Возвращает штамп учетной записи.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19807953"
---
# <a name="propacctstamp"></a><span data-ttu-id="ac42f-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="ac42f-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="ac42f-104">Возвращает штамп учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ac42f-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ac42f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ac42f-105">Quick info</span></span>

<span data-ttu-id="ac42f-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ac42f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac42f-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ac42f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ac42f-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="ac42f-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="ac42f-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="ac42f-109">Property type:</span></span>  <br/> |<span data-ttu-id="ac42f-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac42f-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ac42f-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="ac42f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ac42f-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="ac42f-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="ac42f-113">Access:</span><span class="sxs-lookup"><span data-stu-id="ac42f-113">Access:</span></span>  <br/> |<span data-ttu-id="ac42f-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac42f-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac42f-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac42f-115">Remarks</span></span>

<span data-ttu-id="ac42f-116">Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="ac42f-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="ac42f-117">При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="ac42f-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac42f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ac42f-118">See also</span></span>

- [<span data-ttu-id="ac42f-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="ac42f-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="ac42f-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="ac42f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

