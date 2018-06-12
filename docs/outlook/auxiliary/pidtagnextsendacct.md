---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Указывает дополнительный accountsendstamp для сообщения.
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807937"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="374d2-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="374d2-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="374d2-104">Указывает дополнительный учетной записи «отправить» метка для сообщения.</span><span class="sxs-lookup"><span data-stu-id="374d2-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="374d2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="374d2-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="374d2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="374d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="374d2-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="374d2-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="374d2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="374d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="374d2-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="374d2-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="374d2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="374d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="374d2-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="374d2-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="374d2-112">Области:</span><span class="sxs-lookup"><span data-stu-id="374d2-112">Area:</span></span>  <br/> |<span data-ttu-id="374d2-113">Приложения Outlook</span><span class="sxs-lookup"><span data-stu-id="374d2-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="374d2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="374d2-114">Remarks</span></span>

<span data-ttu-id="374d2-115">Это свойство применяется к объекту сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="374d2-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="374d2-116">Для полученного сообщения отметку «отправить» дополнительного учетной записи указывает учетную запись вперед или ответ направляются в организации, если прямого или ответ, не удается отправить с основная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="374d2-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="374d2-117">Для исходящих сообщений дополнительного учетная запись «отправить» метка определяет учетную запись для отправки сообщения, если не удается отправить сообщение с учетной записью основной.</span><span class="sxs-lookup"><span data-stu-id="374d2-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="374d2-118">Значением является значение [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) в интерфейсе [IOlkAccount](iolkaccount.md) учетной записи, с которого отправляются сообщения.</span><span class="sxs-lookup"><span data-stu-id="374d2-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="374d2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="374d2-119">See also</span></span>

- [<span data-ttu-id="374d2-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="374d2-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="374d2-121">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="374d2-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="374d2-122">Каноническое свойство PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="374d2-122">PidTagNextSendAcct Canonical Property</span></span>](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

