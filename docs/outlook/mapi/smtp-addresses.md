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
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812347"
---
# <a name="smtp-addresses"></a><span data-ttu-id="174b4-103">SMTP-адреса</span><span class="sxs-lookup"><span data-stu-id="174b4-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="174b4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="174b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="174b4-105">Формат адреса электронной почты SMTP определен в RFC 822.</span><span class="sxs-lookup"><span data-stu-id="174b4-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="174b4-106">Компоненты MAPI должен обрабатывать любого адреса, соответствующие этому стандарту.</span><span class="sxs-lookup"><span data-stu-id="174b4-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="174b4-107">Однако существует определенной формы RFC 822 адрес, который лучше всего кодирует MAPI адреса:</span><span class="sxs-lookup"><span data-stu-id="174b4-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="174b4-108">_отображаемое имя_ **\<** _адрес электронной почты_**\>**</span><span class="sxs-lookup"><span data-stu-id="174b4-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="174b4-109">Угловые скобки включены в качестве литералов.</span><span class="sxs-lookup"><span data-stu-id="174b4-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="174b4-110">Пустые ячейки являются стандартными в отображаемые имена; они должны не заключаться в кавычки.</span><span class="sxs-lookup"><span data-stu-id="174b4-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="174b4-111">Типичная адрес может выглядеть эта команда, которая относится к одному из соавторов RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="174b4-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="174b4-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="174b4-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="174b4-113">Если отображаемое имя содержит символы, которые имеют особое значение в SMTP-адреса, такие как \< или @, всей отображаемое имя должно заключаться в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="174b4-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="174b4-114">На исходящей почты Если общая длина адрес электронной почты и отображения имя содержит более 255 символов, отображаемое имя должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="174b4-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="174b4-115">Части SMTP-адрес сопоставления свойств MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="174b4-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="174b4-116">**Компонент адрес SMTP**</span><span class="sxs-lookup"><span data-stu-id="174b4-116">**SMTP address component**</span></span>|<span data-ttu-id="174b4-117">**Свойство MAPI**</span><span class="sxs-lookup"><span data-stu-id="174b4-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="174b4-118">_отображаемое имя_ для всех получателей</span><span class="sxs-lookup"><span data-stu-id="174b4-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="174b4-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="174b4-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="174b4-120">_отображаемое имя_ из поля</span><span class="sxs-lookup"><span data-stu-id="174b4-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="174b4-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="174b4-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="174b4-122">_отображаемое имя_ поля отправителя</span><span class="sxs-lookup"><span data-stu-id="174b4-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="174b4-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="174b4-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="174b4-124">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="174b4-124">_email-address_</span></span> <br/> |<span data-ttu-id="174b4-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="174b4-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="174b4-126">неявные, всегда «SMTP»</span><span class="sxs-lookup"><span data-stu-id="174b4-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="174b4-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="174b4-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="174b4-128">Если не отображаемое имя для адреса в входящей почты, должен использоваться адрес электронной почты всей.</span><span class="sxs-lookup"><span data-stu-id="174b4-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="174b4-129">Тип адреса всегда является SMTP.</span><span class="sxs-lookup"><span data-stu-id="174b4-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="174b4-130">Свойствами получателя, взяты из таблицы получателей сообщения MAPI. свойства отправителя, взяты из сообщения.</span><span class="sxs-lookup"><span data-stu-id="174b4-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

