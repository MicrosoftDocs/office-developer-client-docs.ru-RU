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
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="d0492-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="d0492-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="d0492-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0492-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0492-105">Создает идентификатор записи для разового адреса.</span><span class="sxs-lookup"><span data-stu-id="d0492-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d0492-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d0492-106">Parameters</span></span>

 <span data-ttu-id="d0492-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="d0492-107">_lpszName_</span></span>
  
> <span data-ttu-id="d0492-108">[in] Указатель на значение свойства PR_DISPLAY_NAME  [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d0492-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="d0492-109">Параметр  _lpszName может_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d0492-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d0492-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="d0492-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="d0492-111">[in] Указатель на тип адреса получателя, например ФАКС или SMTP.</span><span class="sxs-lookup"><span data-stu-id="d0492-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="d0492-112">Параметр  _lpszAdrType_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d0492-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d0492-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="d0492-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="d0492-114">[in] Указатель на адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="d0492-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="d0492-115">Параметр  _lpszAddress не_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d0492-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d0492-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0492-116">_ulFlags_</span></span>
  
> <span data-ttu-id="d0492-117">[in] Битмашка флагов, которая влияет на разовую получатель.</span><span class="sxs-lookup"><span data-stu-id="d0492-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="d0492-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d0492-118">The following flags can be set:</span></span>
    
<span data-ttu-id="d0492-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="d0492-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="d0492-120">Получатель не может обрабатывать отформатированный контент сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0492-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="d0492-121">Если MAPI_SEND_NO_RICH_INFO установлено, MAPI задает свойство  [PR_SEND_RICH_INFO (PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false.</span><span class="sxs-lookup"><span data-stu-id="d0492-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="d0492-122">Если MAPI_SEND_NO_RICH_INFO не установлено, MAPI задает это свойство true, если адрес обмена сообщениями получателя, на который указывает  _lpszAddress,_ не интерпретируется как интернет-адрес.</span><span class="sxs-lookup"><span data-stu-id="d0492-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="d0492-123">В этом случае MAPI задает **PR_SEND_RICH_INFO** false.</span><span class="sxs-lookup"><span data-stu-id="d0492-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="d0492-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0492-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d0492-125">Имя отображения, тип адреса и адрес находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="d0492-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="d0492-126">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d0492-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d0492-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d0492-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="d0492-128">[вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="d0492-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d0492-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="d0492-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="d0492-130">[вышел] Указатель на указатель на идентификатор записи для разового получателя.</span><span class="sxs-lookup"><span data-stu-id="d0492-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0492-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0492-131">Return value</span></span>

<span data-ttu-id="d0492-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0492-132">S_OK</span></span> 
  
> <span data-ttu-id="d0492-133">Идентификатор одноавтной записи был создан успешно.</span><span class="sxs-lookup"><span data-stu-id="d0492-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0492-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0492-134">Remarks</span></span>

<span data-ttu-id="d0492-135">Клиенты звонят по методу **CreateOneOff** для создания идентификатора входа для разового получателя — получателя, который не принадлежит ни одному из контейнеров от любого из загруженных в настоящее время поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="d0492-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="d0492-136">У разных получателей может быть любой адрес, поддерживаемый одним из активных поставщиков адресных книг для сеанса.</span><span class="sxs-lookup"><span data-stu-id="d0492-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="d0492-137">Разовые получатели обычно создаются с шаблоном для определенного типа адресов.</span><span class="sxs-lookup"><span data-stu-id="d0492-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="d0492-138">Поставщик адресной книги, который поддерживает тип адресов, поставляет шаблон.</span><span class="sxs-lookup"><span data-stu-id="d0492-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="d0492-139">Пользователь клиентского приложения вводит соответствующую информацию в шаблон.</span><span class="sxs-lookup"><span data-stu-id="d0492-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="d0492-140">MAPI поддерживает строки символов Юникод для параметров отображения, типа адреса **и адреса CreateOneOff.**</span><span class="sxs-lookup"><span data-stu-id="d0492-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="d0492-141">Флаг MAPI_SEND_NO_RICH_INFO, отправляется ли форматированный текст в формате Rich Text Format (RTF) вместе с каждым сообщением.</span><span class="sxs-lookup"><span data-stu-id="d0492-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="d0492-142">Формат транспортной нейтральной инкапсуляции (TNEF) — формат, используемый для передачи форматного текста, отправляется большинством поставщиков транспорта независимо от того, как получатель задает **PR_SEND_RICH_INFO** свойству.</span><span class="sxs-lookup"><span data-stu-id="d0492-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="d0492-143">Это не проблема для клиентов обмена сообщениями, которые работают с межличностными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d0492-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="d0492-144">Однако, поскольку TNEF обычно используется для отправки настраиваемого свойства для настраиваемого класса сообщений, его поддержка может быть проблемой для клиентов или клиентов на основе форм, которые требуют настраиваемые свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0492-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="d0492-145">Дополнительные сведения см. в [рублях Отправка сообщений с помощью TNEF.](sending-messages-with-tnef.md)</span><span class="sxs-lookup"><span data-stu-id="d0492-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d0492-146">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d0492-146">MFCMAPI reference</span></span>

<span data-ttu-id="d0492-147">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d0492-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d0492-148">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d0492-148">**File**</span></span>|<span data-ttu-id="d0492-149">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d0492-149">**Function**</span></span>|<span data-ttu-id="d0492-150">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d0492-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0492-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d0492-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="d0492-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="d0492-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="d0492-153">MFCMAPI использует **метод CreateOneOff** для создания ID записи для адреса, не найденного ни в одной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="d0492-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0492-154">См. также</span><span class="sxs-lookup"><span data-stu-id="d0492-154">See also</span></span>



[<span data-ttu-id="d0492-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="d0492-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="d0492-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d0492-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="d0492-157">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d0492-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

