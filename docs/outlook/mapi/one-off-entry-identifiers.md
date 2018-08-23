---
title: Идентификаторы единичных записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3a086d1b9bcc1eae620b2f0a5ce96a545ce68342
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585537"
---
# <a name="one-off-entry-identifiers"></a><span data-ttu-id="06d04-103">Идентификаторы единичных записей</span><span class="sxs-lookup"><span data-stu-id="06d04-103">One-off entry identifiers</span></span>
  
<span data-ttu-id="06d04-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06d04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06d04-105">Идентификаторы единичных записей создается путем MAPI в методе **IAddrBook::CreateOneOff** и компонентов, которые не имеют доступа к подсистеме MAPI, такие как шлюз компонентов.</span><span class="sxs-lookup"><span data-stu-id="06d04-105">One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components.</span></span> <span data-ttu-id="06d04-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span><span class="sxs-lookup"><span data-stu-id="06d04-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span> <span data-ttu-id="06d04-107">На следующем рисунке показана формат идентификатора единичных записей.</span><span class="sxs-lookup"><span data-stu-id="06d04-107">The following illustration shows the format of a one-off entry identifier.</span></span>
  
<span data-ttu-id="06d04-108">**Формат идентификатора единичных записей**</span><span class="sxs-lookup"><span data-stu-id="06d04-108">**One-off entry identifier format**</span></span>
  
<span data-ttu-id="06d04-109">![Формат идентификатора единичных записей] (media/amapi_69.gif "Формат идентификатора единичных записей")</span><span class="sxs-lookup"><span data-stu-id="06d04-109">![One-off entry identifier format](media/amapi_69.gif "One-off entry identifier format")</span></span>
  
<span data-ttu-id="06d04-110">Первое поле — это специальные структура [MAPIUID](mapiuid.md) , который определяет идентификатор записи как представление настраиваемого получателя.</span><span class="sxs-lookup"><span data-stu-id="06d04-110">The first field is a special [MAPIUID](mapiuid.md) structure that identifies the entry identifier as representing a custom recipient.</span></span> <span data-ttu-id="06d04-111">Эта структура **MAPIUID** должен иметь значение константы MAPI_ONE_OFF_UID.</span><span class="sxs-lookup"><span data-stu-id="06d04-111">This **MAPIUID** structure must be set to the constant MAPI_ONE_OFF_UID.</span></span> <span data-ttu-id="06d04-112">MAPI_ONE_OFF_UID определяется в файле заголовка MAPIDEFS. З.</span><span class="sxs-lookup"><span data-stu-id="06d04-112">MAPI_ONE_OFF_UID is defined in the header file MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="06d04-113">Поля версии и флаги, 16-разрядный слова в байтовом формате Intel.</span><span class="sxs-lookup"><span data-stu-id="06d04-113">The version and flags fields are 16-bit words in Intel byte order.</span></span> <span data-ttu-id="06d04-114">Поле версии должно быть установлено равным нулю.</span><span class="sxs-lookup"><span data-stu-id="06d04-114">The version field must be set to zero.</span></span> <span data-ttu-id="06d04-115">В поле флаги можно задать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="06d04-115">The flags field can be set to the following values:</span></span>
  
<span data-ttu-id="06d04-116">MAPI_ONE_OFF_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="06d04-116">MAPI_ONE_OFF_NO_RICH_INFO</span></span>
  
<span data-ttu-id="06d04-117">MAPI_ONE_OFF_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06d04-117">MAPI_ONE_OFF_UNICODE</span></span>
  
<span data-ttu-id="06d04-118">Флаг MAPI_ONE_OFF_NO_RICH_INFO устанавливается, если получатель не должны получать содержимое сообщения в транспорта Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="06d04-118">The MAPI_ONE_OFF_NO_RICH_INFO flag is set if a recipient should not receive message content in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="06d04-119">Этот флаг устанавливается при MAPI_SEND_NO_RICH_INFO передается методу [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) .</span><span class="sxs-lookup"><span data-stu-id="06d04-119">This flag is set when MAPI_SEND_NO_RICH_INFO is passed to [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method.</span></span> 
  
<span data-ttu-id="06d04-120">Флаг MAPI_ONE_OFF_UNICODE установлен отображаемое имя и адрес электронной почты выполняются строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="06d04-120">The MAPI_ONE_OFF_UNICODE flag is set if the display name and email address are Unicode strings.</span></span> <span data-ttu-id="06d04-121">Этот флаг устанавливается при передаче MAPI_UNICODE **IAddrBook::CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="06d04-121">This flag is set when the MAPI_UNICODE is passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="06d04-122">Когда флаг MAPI_UNICODE **CreateOneOff**не передается, MAPI предполагается, что отображаемое имя и адрес электронной почты адрес они на рабочей станции текущий набор символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="06d04-122">When the MAPI_UNICODE flag is not passed to **CreateOneOff**, MAPI assumes that the display name and email address strings are in the workstation's current ANSI character set.</span></span> <span data-ttu-id="06d04-123">Обычно строки ANSI не работают в сообщения, отправленные между платформ, при использовании различных наборов символов, так как кодовая страница не кодируются в идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="06d04-123">ANSI strings generally do not work well in messages that are sent between platforms using different character sets because the code page is not encoded in the entry identifier.</span></span> <span data-ttu-id="06d04-124">Чтобы избежать этой потенциальных проблем несовместимости, множество типов адресов ограничены только тех знаков, которые являются общими для нескольких наборов знаков.</span><span class="sxs-lookup"><span data-stu-id="06d04-124">To protect against this potential incompatibility, many address types are limited to only those characters that are common across multiple character sets.</span></span> <span data-ttu-id="06d04-125">Тем не менее для обеспечения совместимости платформы и набор знаков, клиенты следует использовать Юникод для строк в сообщения.</span><span class="sxs-lookup"><span data-stu-id="06d04-125">However, to ensure character set and platform compatibility, clients should use Unicode for the character strings in their messages.</span></span>
  
<span data-ttu-id="06d04-126">Отображаемое имя — это строка символом null, соответствует свойству получателя **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), а параметр _lpszName_ , передаваемый **IAddrBook::CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="06d04-126">The display name is a null-terminated string that corresponds to the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and to the  _lpszName_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="06d04-127">Набор символов — Юникод, если флаг MAPI_ONE_OFF_UNICODE set и ANSI, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="06d04-127">The character set is Unicode if the MAPI_ONE_OFF_UNICODE flag is set and ANSI if it is clear.</span></span> 
  
<span data-ttu-id="06d04-128">Тип адреса — это строка символом null, соответствует свойству получателя **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), а параметр _lpszAdrType_ , передаваемый **IAddrBook::CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="06d04-128">The address type is a null-terminated string that corresponds to the recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property and to the  _lpszAdrType_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
<span data-ttu-id="06d04-129">Адрес электронной почты — это строка символом null, соответствует свойству получателя **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), а параметр _lpszAddress_ , передаваемый **IAddrBook::CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="06d04-129">The email address is a null-terminated string that corresponds to the recipient's **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property and to the  _lpszAddress_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="06d04-130">Нет без заполнения структуры идентификатора единичных записей; байты упакованы так же, как указано выше, и длина идентификатор элемента не должен содержать любые байт за прерывающие символом null адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="06d04-130">There is no padding in one-off entry identifier structures; the bytes are packed exactly as indicated above and the entry identifier length should not include any bytes beyond the terminating null character of the email address.</span></span> 
  
<span data-ttu-id="06d04-131">Клиенты и поставщиками адресных книг, которые вручную создания идентификаторов единичных записей также может потребоваться создать значения для свойства **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) и **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d04-131">Clients and address book providers that manually construct one-off entry identifiers might also need to generate values for the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) properties.</span></span> <span data-ttu-id="06d04-132">Ключ записи совпадает с идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="06d04-132">The record key is identical to the entry identifier.</span></span> <span data-ttu-id="06d04-133">Клавиша поиска следует созданных путем объединения следующие поля в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="06d04-133">The search key should be formed by concatenating the following fields in the following order:</span></span>
  
1. <span data-ttu-id="06d04-134">Тип адреса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="06d04-134">The address type, converted to uppercase characters.</span></span>
    
2. <span data-ttu-id="06d04-135">Двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="06d04-135">A colon (:).</span></span>
    
3. <span data-ttu-id="06d04-136">Адрес электронной почты, преобразуется в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="06d04-136">The email address, converted to uppercase characters.</span></span>
    
4. <span data-ttu-id="06d04-137">Завершающий знак null.</span><span class="sxs-lookup"><span data-stu-id="06d04-137">A terminating null character.</span></span>
    
<span data-ttu-id="06d04-138">При создании ключа поиска необходимо выполнить преобразование набора символов.</span><span class="sxs-lookup"><span data-stu-id="06d04-138">No character set conversion must be done when generating the search key.</span></span>
  

