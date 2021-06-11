---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Возвращает учетную запись.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423008"
---
# <a name="prop_acct_send_stamp"></a><span data-ttu-id="25956-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="25956-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="25956-104">Возвращает штамп "отправить" учетную запись.</span><span class="sxs-lookup"><span data-stu-id="25956-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="25956-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="25956-105">Quick info</span></span>

<span data-ttu-id="25956-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="25956-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25956-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="25956-107">Identifier:</span></span>  <br/> |<span data-ttu-id="25956-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="25956-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="25956-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="25956-109">Property type:</span></span>  <br/> |<span data-ttu-id="25956-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25956-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25956-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="25956-111">Property tag:</span></span>  <br/> |<span data-ttu-id="25956-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="25956-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="25956-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="25956-113">Access:</span></span>  <br/> |<span data-ttu-id="25956-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25956-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25956-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="25956-115">Remarks</span></span>

<span data-ttu-id="25956-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="25956-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="25956-117">Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="25956-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25956-118">См. также</span><span class="sxs-lookup"><span data-stu-id="25956-118">See also</span></span>

- [<span data-ttu-id="25956-119">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="25956-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="25956-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="25956-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

