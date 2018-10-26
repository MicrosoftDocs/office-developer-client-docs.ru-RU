---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddb87af4b14be6d728bcceddb4d958ba49229ad4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579041"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="1ad3b-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1ad3b-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="1ad3b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ad3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ad3b-105">Создает запись идентификатор указывает адрес.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="1ad3b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ad3b-106">Parameters</span></span>

 <span data-ttu-id="1ad3b-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="1ad3b-107">_lpszName_</span></span>
  
> <span data-ttu-id="1ad3b-108">[in] Указатель на значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) получателя.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="1ad3b-109">Параметр _lpszName_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="1ad3b-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="1ad3b-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="1ad3b-111">[in] Указатель на тип адреса получателя, например, ФАКС или SMTP.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="1ad3b-112">Параметр _lpszAdrType_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1ad3b-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="1ad3b-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="1ad3b-114">[in] Указатель на адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="1ad3b-115">Параметр _lpszAddress_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1ad3b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ad3b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1ad3b-117">[in] Битовая маска флаги, влияющей на одноразовых получателя.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="1ad3b-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="1ad3b-118">The following flags can be set:</span></span>
    
<span data-ttu-id="1ad3b-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="1ad3b-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="1ad3b-120">Получатель не может обрабатывать сообщения Форматированный контент.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="1ad3b-121">Если значение MAPI_SEND_NO_RICH_INFO, MAPI свойству получателя **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) присваивается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="1ad3b-122">Если MAPI_SEND_NO_RICH_INFO не задано, MAPI этому свойству значение TRUE, если адрес получателя обмена мгновенными сообщениями, на который указывает _lpszAddress_ интерпретируется быть адрес в Интернете.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="1ad3b-123">В этом случае MAPI задает **PR_SEND_RICH_INFO** значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="1ad3b-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1ad3b-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1ad3b-125">Отображаемое имя, тип адреса и адрес находятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="1ad3b-126">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1ad3b-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1ad3b-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="1ad3b-128">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1ad3b-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1ad3b-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="1ad3b-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="1ad3b-130">[out] Указатель на указатель на идентификатор записи для одноразовых получателя.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ad3b-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ad3b-131">Return value</span></span>

<span data-ttu-id="1ad3b-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ad3b-132">S_OK</span></span> 
  
> <span data-ttu-id="1ad3b-133">Идентификатор единичных записей успешно создан.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ad3b-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ad3b-134">Remarks</span></span>

<span data-ttu-id="1ad3b-135">Клиенты вызовите метод **CreateOneOff** для создания записи идентификатора для одноразовых получателя — получателя, не принадлежащие ни контейнеры из любого из поставщиками в настоящее время загрузки адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="1ad3b-136">Одноразовых получателей может иметь любой тип адреса, который поддерживается с помощью одного из поставщиками active адресной книги для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="1ad3b-137">Получатели одноразовых обычно создаются с помощью шаблона для их адрес определенного типа.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="1ad3b-138">Поставщик адресной книги, поддерживающего тип адреса предоставляет шаблон.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="1ad3b-139">Пользователь из клиентского приложения вводит информацию в шаблон.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="1ad3b-140">MAPI поддерживает знаков Юникод для отображаемое имя, тип адреса и параметры адреса из **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="1ad3b-141">Флаг MAPI_SEND_NO_RICH_INFO определяет, является ли форматированный текст в форматированный текст (RTF) отправляется вместе с каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="1ad3b-142">Транспорта Neutral Encapsulation формата TNEF — формат, используемый для передачи форматированный текст, отправляемого большинство поставщиков транспорта, независимо от того, как получатель задает его свойство **PR_SEND_RICH_INFO** .</span><span class="sxs-lookup"><span data-stu-id="1ad3b-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="1ad3b-143">Эта проблема не возникает для сообщений (en), которые работают с сообщениями электронной почты — это.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="1ad3b-144">Тем не менее так как TNEF обычно используется для отправки настраиваемых свойств для пользовательских классов сообщений, не поддерживает может вызвать проблемы для клиентов на основе форм или клиентов, которым требуется настраиваемых свойств MAPI.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="1ad3b-145">Дополнительные сведения можно [Отправлять сообщения с TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="1ad3b-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ad3b-146">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1ad3b-146">MFCMAPI reference</span></span>

<span data-ttu-id="1ad3b-147">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ad3b-148">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1ad3b-148">**File**</span></span>|<span data-ttu-id="1ad3b-149">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1ad3b-149">**Function**</span></span>|<span data-ttu-id="1ad3b-150">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1ad3b-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ad3b-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1ad3b-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="1ad3b-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="1ad3b-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="1ad3b-153">Mfcmapi (en) использует метод **CreateOneOff** для создания идентификатор записи адреса, который не найден в любой адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1ad3b-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ad3b-154">См. также</span><span class="sxs-lookup"><span data-stu-id="1ad3b-154">See also</span></span>



[<span data-ttu-id="1ad3b-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1ad3b-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="1ad3b-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1ad3b-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="1ad3b-157">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1ad3b-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

