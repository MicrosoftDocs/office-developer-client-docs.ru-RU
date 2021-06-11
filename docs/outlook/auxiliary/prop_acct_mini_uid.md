---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Возвращает идентификатор учетной записи, уникальный для Outlook профилей.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409435"
---
# <a name="prop_acct_mini_uid"></a><span data-ttu-id="30641-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="30641-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="30641-104">Возвращает идентификатор учетной записи, уникальный для Outlook профилей.</span><span class="sxs-lookup"><span data-stu-id="30641-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30641-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="30641-105">Quick info</span></span>

<span data-ttu-id="30641-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="30641-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30641-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="30641-107">Identifier:</span></span>  <br/> |<span data-ttu-id="30641-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="30641-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="30641-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="30641-109">Property type:</span></span>  <br/> |<span data-ttu-id="30641-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="30641-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="30641-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="30641-111">Property tag:</span></span>  <br/> |<span data-ttu-id="30641-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="30641-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="30641-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="30641-113">Access:</span></span>  <br/> |<span data-ttu-id="30641-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="30641-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30641-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="30641-115">Remarks</span></span>

<span data-ttu-id="30641-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="30641-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="30641-117">Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="30641-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="30641-118">Это свойство отличается от [PROP_ACCT_ID](prop_acct_id.md) тем, что его значение уникально определяет учетную запись в профиле, в  котором была создана учетная запись, и за ее пределами, в то время как PROP_ACCT_ID уникальна только среди всех учетных записей в том профиле, в котором была создана учетная запись.</span><span class="sxs-lookup"><span data-stu-id="30641-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="30641-119">Когда сообщение с **этими** свойствами перемещается на второй компьютер с другим профилем Outlook и другим набором учетных записей, PROP_ACCT_MINI_UID может однозначно определить исходную учетную запись в исходном профиле.</span><span class="sxs-lookup"><span data-stu-id="30641-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="30641-120">Однако **PROP_ACCT_ID** может привести к конфликту с учетной записью в профиле второго компьютера.</span><span class="sxs-lookup"><span data-stu-id="30641-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30641-121">См. также</span><span class="sxs-lookup"><span data-stu-id="30641-121">See also</span></span>

- [<span data-ttu-id="30641-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="30641-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="30641-123">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="30641-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="30641-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="30641-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

