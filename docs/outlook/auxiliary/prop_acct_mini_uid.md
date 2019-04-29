---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Возвращает идентификатор учетной записи, уникальный для профилей Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409435"
---
# <a name="propacctminiuid"></a><span data-ttu-id="c90e9-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="c90e9-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="c90e9-104">Возвращает идентификатор учетной записи, уникальный для профилей Outlook.</span><span class="sxs-lookup"><span data-stu-id="c90e9-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c90e9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c90e9-105">Quick info</span></span>

<span data-ttu-id="c90e9-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="c90e9-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c90e9-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c90e9-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c90e9-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="c90e9-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="c90e9-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="c90e9-109">Property type:</span></span>  <br/> |<span data-ttu-id="c90e9-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c90e9-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c90e9-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="c90e9-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c90e9-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="c90e9-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="c90e9-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="c90e9-113">Access:</span></span>  <br/> |<span data-ttu-id="c90e9-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c90e9-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c90e9-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c90e9-115">Remarks</span></span>

<span data-ttu-id="c90e9-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="c90e9-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="c90e9-117">Если клиент пытается установить это свойство, это свойство возвращает **е_олк_проп_реад_онли**.</span><span class="sxs-lookup"><span data-stu-id="c90e9-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="c90e9-118">Это свойство отличается от [проп_аккт_ид](prop_acct_id.md) в том, что его значение однозначно определяет учетную запись внутри и снаружи профиля, в котором была создана учетная запись, а **проп_аккт_ид** является уникальным только для всех учетных записей в пределах этого профиля. в котором была создана учетная запись.</span><span class="sxs-lookup"><span data-stu-id="c90e9-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="c90e9-119">Когда сообщение с этими свойствами перемещается на второй компьютер с другим профилем Outlook и разными наборами учетных записей, **проп_аккт_мини_уид** может однозначно определить исходную учетную запись в исходном профиле.</span><span class="sxs-lookup"><span data-stu-id="c90e9-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="c90e9-120">Однако **проп_аккт_ид** может конфликтовать с учетной записью в профиле второго компьютера.</span><span class="sxs-lookup"><span data-stu-id="c90e9-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c90e9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c90e9-121">See also</span></span>

- [<span data-ttu-id="c90e9-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="c90e9-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="c90e9-123">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="c90e9-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="c90e9-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="c90e9-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

