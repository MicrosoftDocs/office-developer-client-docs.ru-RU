---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Возвращает accountsendstamp.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807934"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="68a54-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="68a54-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="68a54-104">Возвращает отметку учетной записи «отправить».</span><span class="sxs-lookup"><span data-stu-id="68a54-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="68a54-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="68a54-105">Quick info</span></span>

<span data-ttu-id="68a54-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="68a54-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68a54-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="68a54-107">Identifier:</span></span>  <br/> |<span data-ttu-id="68a54-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="68a54-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="68a54-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="68a54-109">Property type:</span></span>  <br/> |<span data-ttu-id="68a54-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68a54-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="68a54-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="68a54-111">Property tag:</span></span>  <br/> |<span data-ttu-id="68a54-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="68a54-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="68a54-113">Access:</span><span class="sxs-lookup"><span data-stu-id="68a54-113">Access:</span></span>  <br/> |<span data-ttu-id="68a54-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="68a54-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68a54-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="68a54-115">Remarks</span></span>

<span data-ttu-id="68a54-116">Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="68a54-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="68a54-117">При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="68a54-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68a54-118">См. также</span><span class="sxs-lookup"><span data-stu-id="68a54-118">See also</span></span>

- [<span data-ttu-id="68a54-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="68a54-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="68a54-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="68a54-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

