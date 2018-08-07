---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Возвращает идентификатор, который уникальным образом определяет учетную запись в профиль, в котором создается учетная запись.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807943"
---
# <a name="propacctid"></a><span data-ttu-id="92e81-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="92e81-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="92e81-104">Возвращает идентификатор, который уникальным образом определяет учетную запись в профиль, в котором создается учетная запись.</span><span class="sxs-lookup"><span data-stu-id="92e81-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="92e81-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="92e81-105">Quick info</span></span>

<span data-ttu-id="92e81-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="92e81-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92e81-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="92e81-107">Identifier:</span></span>  <br/> |<span data-ttu-id="92e81-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="92e81-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="92e81-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="92e81-109">Property type:</span></span>  <br/> |<span data-ttu-id="92e81-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="92e81-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="92e81-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="92e81-111">Property tag:</span></span>  <br/> |<span data-ttu-id="92e81-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="92e81-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="92e81-113">Access:</span><span class="sxs-lookup"><span data-stu-id="92e81-113">Access:</span></span>  <br/> |<span data-ttu-id="92e81-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="92e81-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92e81-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="92e81-115">Remarks</span></span>

<span data-ttu-id="92e81-116">Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="92e81-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="92e81-117">При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="92e81-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="92e81-118">Это свойство отличается от [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) , в том, что его значение является уникальным только среди всех учетных записей в этот профиль, в котором был создан учетной записи, в то время как **Свойства\_ACCT_MINI_UID** однозначно определяет учетную запись в пределах и за пределами профилей, в которой была создана учетная запись.</span><span class="sxs-lookup"><span data-stu-id="92e81-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="92e81-119">Когда сообщение с помощью этих свойств перемещается на второй компьютер с другой профиль Outlook и другой набор учетных записей, **PROP_ACCT_ID** можно возможно конфликтов с использованием учетной записи в профиле второй компьютер и **PROP_ACCT_MINI_UID** можно однозначно определить исходной учетной записи в исходный профиль.</span><span class="sxs-lookup"><span data-stu-id="92e81-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92e81-120">См. также</span><span class="sxs-lookup"><span data-stu-id="92e81-120">See also</span></span>

- [<span data-ttu-id="92e81-121">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="92e81-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="92e81-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="92e81-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

