---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Возвращает идентификатор, который уникальным образом определяет учетную запись в профиле, в котором создается учетная запись.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327659"
---
# <a name="propacctid"></a><span data-ttu-id="f94f8-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="f94f8-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="f94f8-104">Возвращает идентификатор, который уникальным образом определяет учетную запись в профиле, в котором создается учетная запись.</span><span class="sxs-lookup"><span data-stu-id="f94f8-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f94f8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f94f8-105">Quick info</span></span>

<span data-ttu-id="f94f8-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f94f8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f94f8-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f94f8-107">Identifier:</span></span>  <br/> |<span data-ttu-id="f94f8-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="f94f8-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="f94f8-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="f94f8-109">Property type:</span></span>  <br/> |<span data-ttu-id="f94f8-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f94f8-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f94f8-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="f94f8-111">Property tag:</span></span>  <br/> |<span data-ttu-id="f94f8-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="f94f8-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="f94f8-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="f94f8-113">Access:</span></span>  <br/> |<span data-ttu-id="f94f8-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f94f8-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f94f8-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f94f8-115">Remarks</span></span>

<span data-ttu-id="f94f8-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="f94f8-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="f94f8-117">Если клиент пытается установить это свойство, это свойство возвращает **е_олк_проп_реад_онли**.</span><span class="sxs-lookup"><span data-stu-id="f94f8-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="f94f8-118">Это свойство отличается от [проп_аккт_мини_уид](prop_acct_mini_uid.md) в том, что его значение уникально только для всех учетных записей в пределах того профиля, в котором была создана учетная запись, а свойство **prop\_аккт_мини_уид** однозначно определяет учетную запись в пределах и вне профиля, в котором была создана учетная запись.</span><span class="sxs-lookup"><span data-stu-id="f94f8-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="f94f8-119">Когда сообщение с этими свойствами перемещается на второй компьютер с другим профилем Outlook и разными наборами учетных записей, **проп_аккт_ид** может конфликтовать с учетной записью в профиле второго компьютера и **проп_аккт_мини_уид** может однозначно определять исходную учетную запись в исходном профиле.</span><span class="sxs-lookup"><span data-stu-id="f94f8-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f94f8-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f94f8-120">See also</span></span>

- [<span data-ttu-id="f94f8-121">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="f94f8-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="f94f8-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="f94f8-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

