---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Возвращает идентификатор, уникальный идентификатор учетной записи в профиле, в котором создается учетная запись.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407167"
---
# <a name="prop_acct_id"></a><span data-ttu-id="a7ef7-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="a7ef7-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="a7ef7-104">Возвращает идентификатор, уникальный идентификатор учетной записи в профиле, в котором создается учетная запись.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a7ef7-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a7ef7-105">Quick info</span></span>

<span data-ttu-id="a7ef7-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a7ef7-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7ef7-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a7ef7-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a7ef7-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="a7ef7-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="a7ef7-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="a7ef7-109">Property type:</span></span>  <br/> |<span data-ttu-id="a7ef7-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a7ef7-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a7ef7-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="a7ef7-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a7ef7-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="a7ef7-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="a7ef7-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="a7ef7-113">Access:</span></span>  <br/> |<span data-ttu-id="a7ef7-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7ef7-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7ef7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7ef7-115">Remarks</span></span>

<span data-ttu-id="a7ef7-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="a7ef7-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="a7ef7-117">Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="a7ef7-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="a7ef7-118">Это свойство отличается от [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) тем, что его значение уникально только для всех учетных записей в том профиле, в котором была создана учетная запись, в то время как **PROP \_ ACCT_MINI_UID** однозначно определяет учетную запись в профиле и за его пределами.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="a7ef7-119">Если сообщение с этими свойствами перемещается на второй компьютер с другим профилем Outlook и другим набором учетных записей, PROP_ACCT_ID может конфликтировать с учетной записью в профиле второго компьютера, а PROP_ACCT_MINI_UID может однозначно идентифицировать исходную учетную запись в исходном профиле.  </span><span class="sxs-lookup"><span data-stu-id="a7ef7-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7ef7-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a7ef7-120">See also</span></span>

- [<span data-ttu-id="a7ef7-121">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="a7ef7-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="a7ef7-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="a7ef7-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

