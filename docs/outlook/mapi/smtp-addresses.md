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
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344564"
---
# <a name="smtp-addresses"></a><span data-ttu-id="92b39-103">SMTP-адреса</span><span class="sxs-lookup"><span data-stu-id="92b39-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="92b39-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92b39-105">Формат SMTP-адресов электронной почты определен в RFC 822.</span><span class="sxs-lookup"><span data-stu-id="92b39-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="92b39-106">Компоненты MAPI должны обрабатывать любой адрес, который соответствует этому стандарту.</span><span class="sxs-lookup"><span data-stu-id="92b39-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="92b39-107">Тем не менее, существует определенная форма адреса RFC 822, которая наилучшим образом кодирует адреса MAPI:</span><span class="sxs-lookup"><span data-stu-id="92b39-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="92b39-108">_имя для отображения_ **\<** _адрес электронной почты_**\>**</span><span class="sxs-lookup"><span data-stu-id="92b39-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="92b39-109">Угловые скобки включены как литералы.</span><span class="sxs-lookup"><span data-stu-id="92b39-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="92b39-110">Пустые ячейки часто используются в отображаемых именах; их не нужно заключать в кавычки.</span><span class="sxs-lookup"><span data-stu-id="92b39-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="92b39-111">Типичный адрес может выглядеть следующим образом, который относится к одному из соавторов RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="92b39-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="92b39-112">Насаниел Боренстеин \<NSB@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="92b39-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="92b39-113">Если отображаемое имя содержит символы, которые имеют особое значение в SMTP-адресах \< , например, или @, то полное отображаемое имя должно быть заключено в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="92b39-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="92b39-114">В случае исходящей почты, если общая длина адреса электронной почты и отображаемого имени превышает 255 символов, отображаемое имя необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="92b39-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="92b39-115">Части карты SMTP-адресов в свойства MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="92b39-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="92b39-116">**Компонент SMTP-адреса**</span><span class="sxs-lookup"><span data-stu-id="92b39-116">**SMTP address component**</span></span>|<span data-ttu-id="92b39-117">**Свойство MAPI**</span><span class="sxs-lookup"><span data-stu-id="92b39-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="92b39-118">_Отображение имен_ для всех получателей</span><span class="sxs-lookup"><span data-stu-id="92b39-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="92b39-119">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92b39-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="92b39-120">_отобразить — имя_ для поля "от"</span><span class="sxs-lookup"><span data-stu-id="92b39-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="92b39-121">**Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92b39-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="92b39-122">_Отображение — имя_ для поля "отправитель"</span><span class="sxs-lookup"><span data-stu-id="92b39-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="92b39-123">**Пр_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92b39-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="92b39-124">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="92b39-124">_email-address_</span></span> <br/> |<span data-ttu-id="92b39-125">**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92b39-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="92b39-126">неявный, всегда "SMTP"</span><span class="sxs-lookup"><span data-stu-id="92b39-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="92b39-127">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92b39-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="92b39-128">Если для адреса в входящей почте нет отображаемого имени, будет использоваться весь адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="92b39-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="92b39-129">Типом адреса всегда является SMTP.</span><span class="sxs-lookup"><span data-stu-id="92b39-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="92b39-130">Свойства получателей берутся из таблицы получателей сообщения MAPI; Свойства отправителя берутся из самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="92b39-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

