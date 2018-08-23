---
title: SMTP-адреса
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 655d48d1ea937659f85e0ef7379425759ea7e256
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591361"
---
# <a name="smtp-addresses"></a><span data-ttu-id="2ab2d-103">SMTP-адреса</span><span class="sxs-lookup"><span data-stu-id="2ab2d-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="2ab2d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ab2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ab2d-105">Формат адреса электронной почты SMTP определен в RFC 822.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="2ab2d-106">Компоненты MAPI должен обрабатывать любого адреса, соответствующие этому стандарту.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="2ab2d-107">Однако существует определенной формы RFC 822 адрес, который лучше всего кодирует MAPI адреса:</span><span class="sxs-lookup"><span data-stu-id="2ab2d-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="2ab2d-108">_отображаемое имя_ **\<** _адрес электронной почты_**\>**</span><span class="sxs-lookup"><span data-stu-id="2ab2d-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="2ab2d-109">Угловые скобки включены в качестве литералов.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="2ab2d-110">Пустые ячейки являются стандартными в отображаемые имена; они должны не заключаться в кавычки.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="2ab2d-111">Типичная адрес может выглядеть эта команда, которая относится к одному из соавторов RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="2ab2d-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="2ab2d-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="2ab2d-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="2ab2d-113">Если отображаемое имя содержит символы, которые имеют особое значение в SMTP-адреса, такие как \< или @, всей отображаемое имя должно заключаться в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="2ab2d-114">На исходящей почты Если общая длина адрес электронной почты и отображения имя содержит более 255 символов, отображаемое имя должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="2ab2d-115">Части SMTP-адрес сопоставления свойств MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2ab2d-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="2ab2d-116">**Компонент адрес SMTP**</span><span class="sxs-lookup"><span data-stu-id="2ab2d-116">**SMTP address component**</span></span>|<span data-ttu-id="2ab2d-117">**Свойство MAPI**</span><span class="sxs-lookup"><span data-stu-id="2ab2d-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2ab2d-118">_отображаемое имя_ для всех получателей</span><span class="sxs-lookup"><span data-stu-id="2ab2d-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="2ab2d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ab2d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="2ab2d-120">_отображаемое имя_ из поля</span><span class="sxs-lookup"><span data-stu-id="2ab2d-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="2ab2d-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ab2d-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="2ab2d-122">_отображаемое имя_ поля отправителя</span><span class="sxs-lookup"><span data-stu-id="2ab2d-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="2ab2d-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ab2d-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="2ab2d-124">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="2ab2d-124">_email-address_</span></span> <br/> |<span data-ttu-id="2ab2d-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ab2d-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2ab2d-126">неявные, всегда «SMTP»</span><span class="sxs-lookup"><span data-stu-id="2ab2d-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="2ab2d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ab2d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="2ab2d-128">Если не отображаемое имя для адреса в входящей почты, должен использоваться адрес электронной почты всей.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="2ab2d-129">Тип адреса всегда является SMTP.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="2ab2d-130">Свойствами получателя, взяты из таблицы получателей сообщения MAPI. свойства отправителя, взяты из сообщения.</span><span class="sxs-lookup"><span data-stu-id="2ab2d-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

