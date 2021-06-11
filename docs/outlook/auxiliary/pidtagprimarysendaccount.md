---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Указывает основные учетные записи для сообщения.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327708"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="2251c-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="2251c-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="2251c-104">Указывает первичную отметку "отправить" учетную запись для сообщения.</span><span class="sxs-lookup"><span data-stu-id="2251c-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2251c-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="2251c-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2251c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2251c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2251c-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2251c-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="2251c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2251c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2251c-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="2251c-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="2251c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2251c-110">Data type:</span></span>  <br/> |<span data-ttu-id="2251c-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2251c-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2251c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2251c-112">Area:</span></span>  <br/> |<span data-ttu-id="2251c-113">Счет</span><span class="sxs-lookup"><span data-stu-id="2251c-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2251c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2251c-114">Remarks</span></span>

<span data-ttu-id="2251c-115">Это свойство применяется к объекту сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="2251c-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="2251c-116">Для полученного сообщения на главной учетной записи указывается, с какой учетной записью должен быть отправлен форвард или ответ.</span><span class="sxs-lookup"><span data-stu-id="2251c-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="2251c-117">Для исходятого сообщения определяется, с какой учетной записью отправлять сообщение.</span><span class="sxs-lookup"><span data-stu-id="2251c-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="2251c-118">Его значение [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) [интерфейса IOlkAccount](iolkaccount.md) учетной записи, с которой отправляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="2251c-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2251c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2251c-119">See also</span></span>

- [<span data-ttu-id="2251c-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="2251c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="2251c-121">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2251c-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="2251c-122">Каноническое свойство PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="2251c-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

