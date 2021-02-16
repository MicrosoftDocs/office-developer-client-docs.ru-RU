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
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427383"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="39337-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="39337-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="39337-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39337-105">Создает идентификатор записи для разовый адрес.</span><span class="sxs-lookup"><span data-stu-id="39337-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="39337-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39337-106">Parameters</span></span>

 <span data-ttu-id="39337-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="39337-107">_lpszName_</span></span>
  
> <span data-ttu-id="39337-108">[in] Указатель на значение свойства PR_DISPLAY_NAME **(** [PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="39337-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="39337-109">Параметр  _lpszName может_ иметь параметр NULL.</span><span class="sxs-lookup"><span data-stu-id="39337-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="39337-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="39337-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="39337-111">[in] Указатель на тип адреса получателя, например ФАКС или SMTP.</span><span class="sxs-lookup"><span data-stu-id="39337-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="39337-112">Параметр  _lpszAdrType не_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="39337-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="39337-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="39337-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="39337-114">[in] Указатель на адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="39337-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="39337-115">Параметр  _lpszAddress не_ может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="39337-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="39337-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39337-116">_ulFlags_</span></span>
  
> <span data-ttu-id="39337-117">[in] Битоваяmas флагов, влияющих на одного получателя.</span><span class="sxs-lookup"><span data-stu-id="39337-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="39337-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="39337-118">The following flags can be set:</span></span>
    
<span data-ttu-id="39337-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="39337-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="39337-120">Получатель не может обрабатывать отформатированный контент сообщения.</span><span class="sxs-lookup"><span data-stu-id="39337-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="39337-121">Если MAPI_SEND_NO_RICH_INFO задан, MAPI устанавливает для свойства **PR_SEND_RICH_INFO** получателя [(PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false.</span><span class="sxs-lookup"><span data-stu-id="39337-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="39337-122">Если MAPI_SEND_NO_RICH_INFO не заданная, MAPI устанавливает для этого свойства true, если адрес получателя сообщений, на который указывает  _lpszAddress,_ не интерпретируется как адрес Интернета.</span><span class="sxs-lookup"><span data-stu-id="39337-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="39337-123">В этом случае MAPI **PR_SEND_RICH_INFO** false.</span><span class="sxs-lookup"><span data-stu-id="39337-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="39337-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39337-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="39337-125">Отображаемого имени, типа адреса и адреса в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="39337-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="39337-126">Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="39337-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="39337-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="39337-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="39337-128">[out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="39337-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="39337-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="39337-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="39337-130">[out] Указатель на указатель на идентификатор записи для одного получателя.</span><span class="sxs-lookup"><span data-stu-id="39337-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39337-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39337-131">Return value</span></span>

<span data-ttu-id="39337-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="39337-132">S_OK</span></span> 
  
> <span data-ttu-id="39337-133">Идентификатор однорахой записи успешно создан.</span><span class="sxs-lookup"><span data-stu-id="39337-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39337-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="39337-134">Remarks</span></span>

<span data-ttu-id="39337-135">Клиенты **вызывали метод CreateOneOff,** чтобы создать идентификатор записи для одного получателя — получателя, который не принадлежит ни к одному из контейнеров ни от одного из текущих загруженных поставщиков адресной книги.</span><span class="sxs-lookup"><span data-stu-id="39337-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="39337-136">У разных получателей может быть любой адрес, поддерживаемый одним из активных поставщиков адресных книг для сеанса.</span><span class="sxs-lookup"><span data-stu-id="39337-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="39337-137">Как правило, для разных получателей создается шаблон для конкретного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="39337-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="39337-138">Поставщик адресной книги, который поддерживает тип адреса, передает шаблон.</span><span class="sxs-lookup"><span data-stu-id="39337-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="39337-139">Пользователь клиентского приложения вводит соответствующую информацию в шаблон.</span><span class="sxs-lookup"><span data-stu-id="39337-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="39337-140">MAPI поддерживает строки символов Юникода для отображаемого имени, типа адреса и параметров **адреса CreateOneOff.**</span><span class="sxs-lookup"><span data-stu-id="39337-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="39337-141">Флаг MAPI_SEND_NO_RICH_INFO контролирует, отправляется ли форматированный текст в формате RTF вместе с каждым сообщением.</span><span class="sxs-lookup"><span data-stu-id="39337-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="39337-142">Формат TNEF ( формат, используемый для передачи форматного текста) отправляется большинством поставщиков транспорта независимо от того, как получатель задает PR_SEND_RICH_INFO. </span><span class="sxs-lookup"><span data-stu-id="39337-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="39337-143">Это не проблема для клиентов обмена сообщениями, которые работают с межличностными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="39337-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="39337-144">Однако, так как формат TNEF обычно используется для отправки настраиваемого свойства для настраиваемого класса сообщений, его поддержка может быть проблемой для клиентов на основе форм, которые требуют настраиваемые свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="39337-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="39337-145">Дополнительные сведения [см. в теме "Отправка сообщений с помощью TNEF".](sending-messages-with-tnef.md)</span><span class="sxs-lookup"><span data-stu-id="39337-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="39337-146">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="39337-146">MFCMAPI reference</span></span>

<span data-ttu-id="39337-147">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="39337-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="39337-148">**Файл**</span><span class="sxs-lookup"><span data-stu-id="39337-148">**File**</span></span>|<span data-ttu-id="39337-149">**Функция**</span><span class="sxs-lookup"><span data-stu-id="39337-149">**Function**</span></span>|<span data-ttu-id="39337-150">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="39337-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39337-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="39337-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="39337-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="39337-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="39337-153">MFCMAPI использует метод **CreateOneOff** для создания ИД записи для адреса, который не найден ни в одной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="39337-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39337-154">См. также</span><span class="sxs-lookup"><span data-stu-id="39337-154">See also</span></span>



[<span data-ttu-id="39337-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="39337-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="39337-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="39337-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="39337-157">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="39337-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

