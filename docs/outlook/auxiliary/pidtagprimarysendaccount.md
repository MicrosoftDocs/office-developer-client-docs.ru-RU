---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Указывает основную учетную запись для сообщения.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327708"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="46680-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="46680-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="46680-104">Указывает основную учетную запись "отправить" для сообщения.</span><span class="sxs-lookup"><span data-stu-id="46680-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="46680-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="46680-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46680-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="46680-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46680-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="46680-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="46680-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="46680-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46680-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="46680-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="46680-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="46680-110">Data type:</span></span>  <br/> |<span data-ttu-id="46680-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46680-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="46680-112">Область:</span><span class="sxs-lookup"><span data-stu-id="46680-112">Area:</span></span>  <br/> |<span data-ttu-id="46680-113">Счет</span><span class="sxs-lookup"><span data-stu-id="46680-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46680-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="46680-114">Remarks</span></span>

<span data-ttu-id="46680-115">Это свойство применяется к объекту сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="46680-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="46680-116">В полученном сообщении в основной учетной записи указывается, с какой учетной записью следует отправить сообщение или ответ.</span><span class="sxs-lookup"><span data-stu-id="46680-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="46680-117">Для исходяния сообщения оно определяет, с какой учетной записью отправлять сообщение.</span><span class="sxs-lookup"><span data-stu-id="46680-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="46680-118">Его значением является [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) из интерфейса [IOlkAccount](iolkaccount.md) учетной записи, с которой отправляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="46680-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46680-119">См. также</span><span class="sxs-lookup"><span data-stu-id="46680-119">See also</span></span>

- [<span data-ttu-id="46680-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="46680-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="46680-121">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="46680-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="46680-122">Каноническое свойство PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="46680-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

