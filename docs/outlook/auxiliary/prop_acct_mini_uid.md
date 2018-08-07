---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Возвращает идентификатор учетной записи, которая является уникальным для профилей Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807944"
---
# <a name="propacctminiuid"></a><span data-ttu-id="c0136-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="c0136-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="c0136-104">Возвращает идентификатор учетной записи, которая является уникальным для профилей Outlook.</span><span class="sxs-lookup"><span data-stu-id="c0136-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c0136-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c0136-105">Quick info</span></span>

<span data-ttu-id="c0136-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="c0136-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0136-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c0136-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c0136-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="c0136-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="c0136-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="c0136-109">Property type:</span></span>  <br/> |<span data-ttu-id="c0136-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c0136-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c0136-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="c0136-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c0136-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="c0136-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="c0136-113">Access:</span><span class="sxs-lookup"><span data-stu-id="c0136-113">Access:</span></span>  <br/> |<span data-ttu-id="c0136-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0136-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0136-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0136-115">Remarks</span></span>

<span data-ttu-id="c0136-116">Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="c0136-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="c0136-117">При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="c0136-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="c0136-118">Это свойство отличается от [PROP_ACCT_ID](prop_acct_id.md) , в том, что его значение однозначно определяет учетную запись в пределах и за ее пределами профилей, в которой была создана учетная запись, то время как **PROP_ACCT_ID** является уникальным только во все учетные записи в пределах одного профиля в котором был создан учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c0136-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="c0136-119">Если сообщение с помощью этих свойств перемещается на второй компьютер с другой профиль Outlook и другой набор учетных записей, **PROP_ACCT_MINI_UID** можно однозначно определить исходной учетной записи в исходный профиль.</span><span class="sxs-lookup"><span data-stu-id="c0136-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="c0136-120">Тем не менее **PROP_ACCT_ID** возможно могут конфликтовать с использованием учетной записи в профиле второй компьютер.</span><span class="sxs-lookup"><span data-stu-id="c0136-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0136-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c0136-121">See also</span></span>

- [<span data-ttu-id="c0136-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="c0136-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="c0136-123">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="c0136-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="c0136-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="c0136-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

