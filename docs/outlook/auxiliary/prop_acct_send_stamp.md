---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Возвращает аккаунтсендстамп.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423008"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="0f53c-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="0f53c-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="0f53c-104">Возвращает штамп "Отправить" для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0f53c-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0f53c-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="0f53c-105">Quick info</span></span>

<span data-ttu-id="0f53c-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="0f53c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f53c-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0f53c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="0f53c-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="0f53c-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="0f53c-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="0f53c-109">Property type:</span></span>  <br/> |<span data-ttu-id="0f53c-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f53c-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0f53c-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="0f53c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="0f53c-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="0f53c-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="0f53c-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="0f53c-113">Access:</span></span>  <br/> |<span data-ttu-id="0f53c-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f53c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f53c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f53c-115">Remarks</span></span>

<span data-ttu-id="0f53c-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="0f53c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="0f53c-117">Если клиент пытается установить это свойство, это свойство возвращает **е_олк_проп_реад_онли**.</span><span class="sxs-lookup"><span data-stu-id="0f53c-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f53c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0f53c-118">See also</span></span>

- [<span data-ttu-id="0f53c-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="0f53c-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="0f53c-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="0f53c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

