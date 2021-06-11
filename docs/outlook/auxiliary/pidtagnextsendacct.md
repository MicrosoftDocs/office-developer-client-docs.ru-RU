---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Указывает дополнительные учетные записи для сообщения.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327715"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="92d7b-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="92d7b-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="92d7b-104">Указывает вторичную отметку "Отправить" для сообщения.</span><span class="sxs-lookup"><span data-stu-id="92d7b-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="92d7b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="92d7b-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92d7b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="92d7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92d7b-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="92d7b-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="92d7b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="92d7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92d7b-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="92d7b-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="92d7b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="92d7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="92d7b-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92d7b-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="92d7b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="92d7b-112">Area:</span></span>  <br/> |<span data-ttu-id="92d7b-113">Outlook приложение</span><span class="sxs-lookup"><span data-stu-id="92d7b-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92d7b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="92d7b-114">Remarks</span></span>

<span data-ttu-id="92d7b-115">Это свойство применяется к объекту сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="92d7b-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="92d7b-116">Для полученного сообщения на вторичной учетной записи указывается, с какой учетной записью следует отправить форвард или ответ, если форвард или ответ не могут быть отправлены с основной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="92d7b-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="92d7b-117">Для исходя из сообщения вторичная учетная запись "отправить" печать определяет, с какой учетной записью отправить сообщение, если сообщение не может быть отправлено с основной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="92d7b-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="92d7b-118">Его значение [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) [интерфейса IOlkAccount](iolkaccount.md) учетной записи, с которой отправляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="92d7b-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92d7b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="92d7b-119">See also</span></span>

- [<span data-ttu-id="92d7b-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="92d7b-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="92d7b-121">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="92d7b-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="92d7b-122">Каноническое свойство PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="92d7b-122">PidTagNextSendAcct Canonical Property</span></span>](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

