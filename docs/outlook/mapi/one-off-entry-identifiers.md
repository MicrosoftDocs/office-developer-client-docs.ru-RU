---
title: Одноразовые идентификаторы записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411045"
---
# <a name="one-off-entry-identifiers"></a><span data-ttu-id="d6acb-103">Одноразовые идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="d6acb-103">One-off entry identifiers</span></span>
  
<span data-ttu-id="d6acb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6acb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6acb-105">Идентификаторы однофайловой записи создаются с помощью MAPI в методе **IAddrBook::CreateOneOff** и компонентами, которые не имеют доступа к подсистеме MAPI, например компонентам шлюза.</span><span class="sxs-lookup"><span data-stu-id="d6acb-105">One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components.</span></span> <span data-ttu-id="d6acb-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span><span class="sxs-lookup"><span data-stu-id="d6acb-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span> <span data-ttu-id="d6acb-107">На следующем рисунке показан формат идентификатора однораховой записи.</span><span class="sxs-lookup"><span data-stu-id="d6acb-107">The following illustration shows the format of a one-off entry identifier.</span></span>
  
<span data-ttu-id="d6acb-108">**Формат идентификатора единичных записей**</span><span class="sxs-lookup"><span data-stu-id="d6acb-108">**One-off entry identifier format**</span></span>
  
<span data-ttu-id="d6acb-109">![Формат одноавъемного идентификатора]записи в формате(media/amapi_69.gif "одноавъемной записи")</span><span class="sxs-lookup"><span data-stu-id="d6acb-109">![One-off entry identifier format](media/amapi_69.gif "One-off entry identifier format")</span></span>
  
<span data-ttu-id="d6acb-110">Первое поле — это специальная [структура MAPIUID,](mapiuid.md) которая определяет идентификатор записи как представляющий настраиваемую получатель.</span><span class="sxs-lookup"><span data-stu-id="d6acb-110">The first field is a special [MAPIUID](mapiuid.md) structure that identifies the entry identifier as representing a custom recipient.</span></span> <span data-ttu-id="d6acb-111">Для **этой структуры MAPIUID** необходимо установить константу MAPI_ONE_OFF_UID.</span><span class="sxs-lookup"><span data-stu-id="d6acb-111">This **MAPIUID** structure must be set to the constant MAPI_ONE_OFF_UID.</span></span> <span data-ttu-id="d6acb-112">MAPI_ONE_OFF_UID определяется в файле header MAPIDEFS.H.</span><span class="sxs-lookup"><span data-stu-id="d6acb-112">MAPI_ONE_OFF_UID is defined in the header file MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="d6acb-113">Поля версий и флагов — это 16-битные слова в порядке byte Intel.</span><span class="sxs-lookup"><span data-stu-id="d6acb-113">The version and flags fields are 16-bit words in Intel byte order.</span></span> <span data-ttu-id="d6acb-114">Для поля версии должно быть установлено значение 0.</span><span class="sxs-lookup"><span data-stu-id="d6acb-114">The version field must be set to zero.</span></span> <span data-ttu-id="d6acb-115">Для поля флагов можно установить следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d6acb-115">The flags field can be set to the following values:</span></span>
  
<span data-ttu-id="d6acb-116">MAPI_ONE_OFF_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="d6acb-116">MAPI_ONE_OFF_NO_RICH_INFO</span></span>
  
<span data-ttu-id="d6acb-117">MAPI_ONE_OFF_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6acb-117">MAPI_ONE_OFF_UNICODE</span></span>
  
<span data-ttu-id="d6acb-118">Флаг MAPI_ONE_OFF_NO_RICH_INFO, если получатель не должен получать содержимое сообщения в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="d6acb-118">The MAPI_ONE_OFF_NO_RICH_INFO flag is set if a recipient should not receive message content in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="d6acb-119">Этот флаг устанавливается, MAPI_SEND_NO_RICH_INFO передается [методу IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md)</span><span class="sxs-lookup"><span data-stu-id="d6acb-119">This flag is set when MAPI_SEND_NO_RICH_INFO is passed to [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method.</span></span> 
  
<span data-ttu-id="d6acb-120">Флаг MAPI_ONE_OFF_UNICODE, если отображаемого имени и адреса электронной почты являются строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="d6acb-120">The MAPI_ONE_OFF_UNICODE flag is set if the display name and email address are Unicode strings.</span></span> <span data-ttu-id="d6acb-121">Этот флаг устанавливается, когда MAPI_UNICODE передается **в IAddrBook::CreateOneOff.**</span><span class="sxs-lookup"><span data-stu-id="d6acb-121">This flag is set when the MAPI_UNICODE is passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="d6acb-122">Если флаг MAPI_UNICODE не передается **в CreateOneOff,** MAPI предполагает, что отображаемая имя и строки адресов электронной почты находятся в текущем наборе символов ANSI рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d6acb-122">When the MAPI_UNICODE flag is not passed to **CreateOneOff**, MAPI assumes that the display name and email address strings are in the workstation's current ANSI character set.</span></span> <span data-ttu-id="d6acb-123">Строки ANSI обычно не очень хорошо работают в сообщениях, которые отправляются между платформами с использованием разных кодировок, так как кодовая страница не закодирована в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="d6acb-123">ANSI strings generally do not work well in messages that are sent between platforms using different character sets because the code page is not encoded in the entry identifier.</span></span> <span data-ttu-id="d6acb-124">Чтобы защититься от этой потенциальной несовместимости, многие типы адресов ограничены только теми символами, которые являются общими для нескольких наборов символов.</span><span class="sxs-lookup"><span data-stu-id="d6acb-124">To protect against this potential incompatibility, many address types are limited to only those characters that are common across multiple character sets.</span></span> <span data-ttu-id="d6acb-125">Однако для обеспечения совместимости кодировки и платформы клиенты должны использовать Юникод для строк символов в своих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="d6acb-125">However, to ensure character set and platform compatibility, clients should use Unicode for the character strings in their messages.</span></span>
  
<span data-ttu-id="d6acb-126">Отображаемая имя — это строка с нулью, которая соответствует свойству **PR_DISPLAY_NAME получателя** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и _параметру lpszName,_ переданным **в IAddrBook::CreateOneOff.**</span><span class="sxs-lookup"><span data-stu-id="d6acb-126">The display name is a null-terminated string that corresponds to the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and to the  _lpszName_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="d6acb-127">Набор символов — Юникод, если MAPI_ONE_OFF_UNICODE установлен, и ANSI, если он понятен.</span><span class="sxs-lookup"><span data-stu-id="d6acb-127">The character set is Unicode if the MAPI_ONE_OFF_UNICODE flag is set and ANSI if it is clear.</span></span> 
  
<span data-ttu-id="d6acb-128">Тип адреса — это строка с нулью, которая соответствует свойству PR_ADDRTYPE [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)получателя и параметру _lpszAdrType,_ переданным **в IAddrBook::CreateOneOff.** </span><span class="sxs-lookup"><span data-stu-id="d6acb-128">The address type is a null-terminated string that corresponds to the recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property and to the  _lpszAdrType_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
<span data-ttu-id="d6acb-129">Адрес электронной почты — это строка с нулью, которая соответствует свойству **PR_EMAIL_ADDRESS** получателя [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)и _параметру lpszAddress,_ переданной в **IAddrBook::CreateOneOff.**</span><span class="sxs-lookup"><span data-stu-id="d6acb-129">The email address is a null-terminated string that corresponds to the recipient's **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property and to the  _lpszAddress_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6acb-130">В структурах идентификаторов однораховых записей заполнение не существует; эти данные упаковываются точно так же, как указано выше, а длина идентификатора записи не должна включать в себя ни одного из них, кроме символа null, превысякающий нулевую символику адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d6acb-130">There is no padding in one-off entry identifier structures; the bytes are packed exactly as indicated above and the entry identifier length should not include any bytes beyond the terminating null character of the email address.</span></span> 
  
<span data-ttu-id="d6acb-131">Клиентам и поставщикам адресных книг, которые вручную создают идентификаторы одноразовых записей, также может потребоваться создать значения для свойств **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и **PR_SEARCH_KEY** ([PidTagSearchKey).](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d6acb-131">Clients and address book providers that manually construct one-off entry identifiers might also need to generate values for the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) properties.</span></span> <span data-ttu-id="d6acb-132">Ключ записи идентичен идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="d6acb-132">The record key is identical to the entry identifier.</span></span> <span data-ttu-id="d6acb-133">Ключ поиска должен быть сформирован путем совмества следующих полей в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d6acb-133">The search key should be formed by concatenating the following fields in the following order:</span></span>
  
1. <span data-ttu-id="d6acb-134">Тип адреса, преобразованный в верхние буквы.</span><span class="sxs-lookup"><span data-stu-id="d6acb-134">The address type, converted to uppercase characters.</span></span>
    
2. <span data-ttu-id="d6acb-135">Двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="d6acb-135">A colon (:).</span></span>
    
3. <span data-ttu-id="d6acb-136">Адрес электронной почты, преобразованный в верхние буквы.</span><span class="sxs-lookup"><span data-stu-id="d6acb-136">The email address, converted to uppercase characters.</span></span>
    
4. <span data-ttu-id="d6acb-137">Символ null, завершающийся.</span><span class="sxs-lookup"><span data-stu-id="d6acb-137">A terminating null character.</span></span>
    
<span data-ttu-id="d6acb-138">При создании ключа поиска преобразование наборов символов не нужно.</span><span class="sxs-lookup"><span data-stu-id="d6acb-138">No character set conversion must be done when generating the search key.</span></span>
  

