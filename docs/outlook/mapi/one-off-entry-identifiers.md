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
# <a name="one-off-entry-identifiers"></a><span data-ttu-id="0163f-103">Одноразовые идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="0163f-103">One-off entry identifiers</span></span>
  
<span data-ttu-id="0163f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0163f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0163f-105">Одноразовые идентификаторы записей создаются MAPI в методе **IAddrBook:: креатеонеофф** и компонентах, у которых нет доступа к подсистеме MAPI, например, к компонентам шлюза.</span><span class="sxs-lookup"><span data-stu-id="0163f-105">One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components.</span></span> <span data-ttu-id="0163f-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span><span class="sxs-lookup"><span data-stu-id="0163f-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span> <span data-ttu-id="0163f-107">На следующем рисунке показан формат идентификатора одноразовой записи.</span><span class="sxs-lookup"><span data-stu-id="0163f-107">The following illustration shows the format of a one-off entry identifier.</span></span>
  
<span data-ttu-id="0163f-108">**Формат идентификатора единичных записей**</span><span class="sxs-lookup"><span data-stu-id="0163f-108">**One-off entry identifier format**</span></span>
  
<span data-ttu-id="0163f-109">![Одноразовый](media/amapi_69.gif "One-off entry identifier format") формат идентификатора записи с одноразовым входом</span><span class="sxs-lookup"><span data-stu-id="0163f-109">![One-off entry identifier format](media/amapi_69.gif "One-off entry identifier format")</span></span>
  
<span data-ttu-id="0163f-110">Первое поле — это особая структура [мапиуид](mapiuid.md) , определяющая идентификатор записи, представляющий настраиваемого получателя.</span><span class="sxs-lookup"><span data-stu-id="0163f-110">The first field is a special [MAPIUID](mapiuid.md) structure that identifies the entry identifier as representing a custom recipient.</span></span> <span data-ttu-id="0163f-111">Этой структуре **мапиуид** должно быть присвоено значение константы MAPI_ONE_OFF_UID.</span><span class="sxs-lookup"><span data-stu-id="0163f-111">This **MAPIUID** structure must be set to the constant MAPI_ONE_OFF_UID.</span></span> <span data-ttu-id="0163f-112">MAPI_ONE_OFF_UID задается в файле заголовка MAPIDEFS. Высоты.</span><span class="sxs-lookup"><span data-stu-id="0163f-112">MAPI_ONE_OFF_UID is defined in the header file MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="0163f-113">Поля Version и flags — это 16 разрядные слова в порядке байтов Intel.</span><span class="sxs-lookup"><span data-stu-id="0163f-113">The version and flags fields are 16-bit words in Intel byte order.</span></span> <span data-ttu-id="0163f-114">Поле Version должно иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0163f-114">The version field must be set to zero.</span></span> <span data-ttu-id="0163f-115">Для поля Flags можно задать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0163f-115">The flags field can be set to the following values:</span></span>
  
<span data-ttu-id="0163f-116">MAPI_ONE_OFF_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="0163f-116">MAPI_ONE_OFF_NO_RICH_INFO</span></span>
  
<span data-ttu-id="0163f-117">MAPI_ONE_OFF_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0163f-117">MAPI_ONE_OFF_UNICODE</span></span>
  
<span data-ttu-id="0163f-118">Флаг MAPI_ONE_OFF_NO_RICH_INFO задается, если получатель не должен получать содержимое сообщения в формате TNEF, нейтральном к транспорту.</span><span class="sxs-lookup"><span data-stu-id="0163f-118">The MAPI_ONE_OFF_NO_RICH_INFO flag is set if a recipient should not receive message content in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="0163f-119">Этот флаг задается, когда MAPI_SEND_NO_RICH_INFO передается в метод [IAddrBook:: креатеонеофф](iaddrbook-createoneoff.md) .</span><span class="sxs-lookup"><span data-stu-id="0163f-119">This flag is set when MAPI_SEND_NO_RICH_INFO is passed to [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method.</span></span> 
  
<span data-ttu-id="0163f-120">Флаг MAPI_ONE_OFF_UNICODE задается, если отображаемое имя и адрес электронной почты являются строками в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="0163f-120">The MAPI_ONE_OFF_UNICODE flag is set if the display name and email address are Unicode strings.</span></span> <span data-ttu-id="0163f-121">Этот флаг задается, когда MAPI_UNICODE передается в **IAddrBook:: креатеонеофф**.</span><span class="sxs-lookup"><span data-stu-id="0163f-121">This flag is set when the MAPI_UNICODE is passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="0163f-122">Если флаг MAPI_UNICODE не передается в **креатеонеофф**, MAPI предполагает, что отображаемое имя и строки адреса электронной почты находятся в текущем наборе знаков ANSI на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="0163f-122">When the MAPI_UNICODE flag is not passed to **CreateOneOff**, MAPI assumes that the display name and email address strings are in the workstation's current ANSI character set.</span></span> <span data-ttu-id="0163f-123">Строки ANSI обычно плохо работают в сообщениях, которые передаются между платформами с использованием разных наборов символов, так как кодовая страница не кодируется в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="0163f-123">ANSI strings generally do not work well in messages that are sent between platforms using different character sets because the code page is not encoded in the entry identifier.</span></span> <span data-ttu-id="0163f-124">Чтобы защититься от этого потенциально несовместимости, многие типы адресов ограничены только теми символами, которые являются общими для нескольких наборов символов.</span><span class="sxs-lookup"><span data-stu-id="0163f-124">To protect against this potential incompatibility, many address types are limited to only those characters that are common across multiple character sets.</span></span> <span data-ttu-id="0163f-125">Тем не менее, чтобы обеспечить совместимость набора символов и платформы, клиенты должны использовать Юникод для символьных строк в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="0163f-125">However, to ensure character set and platform compatibility, clients should use Unicode for the character strings in their messages.</span></span>
  
<span data-ttu-id="0163f-126">Отображаемое имя — это строка с завершающим нулем, которая соответствует свойству **PR_DISPLAY_NAME** получателя ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и параметру _лпсзнаме_ , переданному в **IAddrBook:: креатеонеофф**.</span><span class="sxs-lookup"><span data-stu-id="0163f-126">The display name is a null-terminated string that corresponds to the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and to the  _lpszName_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="0163f-127">Кодировка Юникод, если установлен флаг MAPI_ONE_OFF_UNICODE и ANSI, если он является понятным.</span><span class="sxs-lookup"><span data-stu-id="0163f-127">The character set is Unicode if the MAPI_ONE_OFF_UNICODE flag is set and ANSI if it is clear.</span></span> 
  
<span data-ttu-id="0163f-128">Тип адреса — это строка с завершающим нулем, которая соответствует свойству **PR_ADDRTYPE** получателя ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) и параметру _лпсзадртипе_ , переданному в **IAddrBook:: креатеонеофф**.</span><span class="sxs-lookup"><span data-stu-id="0163f-128">The address type is a null-terminated string that corresponds to the recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property and to the  _lpszAdrType_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
<span data-ttu-id="0163f-129">Адрес электронной почты — это строка с завершающим нулем, которая соответствует свойству **PR_EMAIL_ADDRESS** получателя ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и параметру _лпсзаддресс_ , переданному в **IAddrBook:: креатеонеофф**.</span><span class="sxs-lookup"><span data-stu-id="0163f-129">The email address is a null-terminated string that corresponds to the recipient's **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property and to the  _lpszAddress_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0163f-130">В непустых структурах идентификаторов записей нет внутреннего поля; байты упаковываются точно так, как показано выше, а длина идентификатора записи не должна содержать байты за завершающим нулевым символом в адресе электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0163f-130">There is no padding in one-off entry identifier structures; the bytes are packed exactly as indicated above and the entry identifier length should not include any bytes beyond the terminating null character of the email address.</span></span> 
  
<span data-ttu-id="0163f-131">Для клиентов и поставщиков адресных книг, которые вручную создают одноразовые идентификаторы записей, может также потребоваться создать значения для свойств **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0163f-131">Clients and address book providers that manually construct one-off entry identifiers might also need to generate values for the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) properties.</span></span> <span data-ttu-id="0163f-132">Ключ записи идентичен идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="0163f-132">The record key is identical to the entry identifier.</span></span> <span data-ttu-id="0163f-133">Ключ поиска должен быть сформирован путем сцепления следующих полей в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="0163f-133">The search key should be formed by concatenating the following fields in the following order:</span></span>
  
1. <span data-ttu-id="0163f-134">Тип адреса, преобразованный в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="0163f-134">The address type, converted to uppercase characters.</span></span>
    
2. <span data-ttu-id="0163f-135">Двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="0163f-135">A colon (:).</span></span>
    
3. <span data-ttu-id="0163f-136">Адрес электронной почты, преобразованный в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="0163f-136">The email address, converted to uppercase characters.</span></span>
    
4. <span data-ttu-id="0163f-137">Завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="0163f-137">A terminating null character.</span></span>
    
<span data-ttu-id="0163f-138">Не следует выполнять преобразование набора символов при создании ключа поиска.</span><span class="sxs-lookup"><span data-stu-id="0163f-138">No character set conversion must be done when generating the search key.</span></span>
  

