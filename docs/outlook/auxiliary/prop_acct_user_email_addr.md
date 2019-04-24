---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Указывает адрес электронной почты для учетной записи.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326532"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="f1042-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="f1042-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="f1042-104">Указывает адрес электронной почты для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1042-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f1042-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f1042-105">Quick info</span></span>

<span data-ttu-id="f1042-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f1042-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1042-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f1042-107">Identifier:</span></span>  <br/> |<span data-ttu-id="f1042-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="f1042-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="f1042-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="f1042-109">Property type:</span></span>  <br/> |<span data-ttu-id="f1042-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f1042-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f1042-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="f1042-111">Property tag:</span></span>  <br/> |<span data-ttu-id="f1042-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="f1042-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="f1042-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="f1042-113">Access:</span></span>  <br/> |<span data-ttu-id="f1042-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f1042-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1042-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f1042-115">Remarks</span></span>

 <span data-ttu-id="f1042-116">**Проп_аккт_усер_емаил_аддр** не должен существовать на каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1042-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="f1042-117">Например, учетная запись Exchange может иметь [проп_мапи_идентити_ентрид](prop_mapi_identity_entryid.md) , но не **проп_аккт_усер_емаил_аддр**, в то время как для учетной записи SMTP/POP3 ситуация обратна.</span><span class="sxs-lookup"><span data-stu-id="f1042-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1042-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f1042-118">See also</span></span>

- [<span data-ttu-id="f1042-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="f1042-119">About the Account Management API</span></span>](about-the-account-management-api.md)

