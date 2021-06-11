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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419627"
---
# <a name="smtp-addresses"></a><span data-ttu-id="d9d3a-103">SMTP-адреса</span><span class="sxs-lookup"><span data-stu-id="d9d3a-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="d9d3a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9d3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9d3a-105">Формат адресов электронной почты SMTP определяется в RFC 822.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="d9d3a-106">Компоненты MAPI должны обрабатывать любой адрес, который соответствует этому стандарту.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="d9d3a-107">Однако существует определенная форма адреса RFC 822, который лучше всего кодирует АДРЕСА MAPI:</span><span class="sxs-lookup"><span data-stu-id="d9d3a-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="d9d3a-108">_display-name_ **\<** _адрес электронной почты_**\>**</span><span class="sxs-lookup"><span data-stu-id="d9d3a-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="d9d3a-109">Угловые скобки включены в качестве литералов.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="d9d3a-110">Пробелы являются распространенными в именах отображения; их не нужно цитировать.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="d9d3a-111">Типичный адрес может выглядеть как этот, который принадлежит одному из соавторов RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="d9d3a-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="d9d3a-112">Натаниэль \< Боренштейн nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="d9d3a-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="d9d3a-113">Если имя отображения содержит символы, которые имеют особое значение в SMTP-адресах, например или @, все имя отображения должно быть заключено в \< двойные кавычка.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="d9d3a-114">При исходящую почту, если общая длина адреса электронной почты плюс имя отображения превышает 255 символов, имя отображения должно быть отброшено.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="d9d3a-115">Части адресной карты SMTP в свойства MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9d3a-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="d9d3a-116">**Компонент адресов SMTP**</span><span class="sxs-lookup"><span data-stu-id="d9d3a-116">**SMTP address component**</span></span>|<span data-ttu-id="d9d3a-117">**Свойство MAPI**</span><span class="sxs-lookup"><span data-stu-id="d9d3a-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d9d3a-118">_отображение имени_ для всех получателей</span><span class="sxs-lookup"><span data-stu-id="d9d3a-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="d9d3a-119">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="d9d3a-120">_display-name_ for From field</span><span class="sxs-lookup"><span data-stu-id="d9d3a-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="d9d3a-121">**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="d9d3a-122">_display-name_ для поля Отправитель</span><span class="sxs-lookup"><span data-stu-id="d9d3a-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="d9d3a-123">**PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="d9d3a-124">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="d9d3a-124">_email-address_</span></span> <br/> |<span data-ttu-id="d9d3a-125">**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d9d3a-126">неявный, всегда "SMTP"</span><span class="sxs-lookup"><span data-stu-id="d9d3a-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="d9d3a-127">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="d9d3a-128">Если в входящий почтовый ящик не отображается имя отображения, вместо него следует использовать весь адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="d9d3a-129">Тип адреса всегда SMTP.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="d9d3a-130">Свойства получателей взяты из таблицы получателей сообщения MAPI; Свойства отправитель взяты из самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

