---
title: Иаддрбуккреатеонеофф
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349317"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="3461f-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="3461f-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="3461f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3461f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3461f-105">Создает идентификатор записи для одного адреса.</span><span class="sxs-lookup"><span data-stu-id="3461f-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="3461f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3461f-106">Parameters</span></span>

 <span data-ttu-id="3461f-107">_Лпсзнаме_</span><span class="sxs-lookup"><span data-stu-id="3461f-107">_lpszName_</span></span>
  
> <span data-ttu-id="3461f-108">возврата Указатель на значение свойства **пр_дисплай_наме** получателя ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3461f-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="3461f-109">Параметр _лпсзнаме_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="3461f-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="3461f-110">_Лпсзадртипе_</span><span class="sxs-lookup"><span data-stu-id="3461f-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="3461f-111">возврата Указатель на тип адреса получателя, например Факс или SMTP.</span><span class="sxs-lookup"><span data-stu-id="3461f-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="3461f-112">Параметр _лпсзадртипе_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="3461f-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="3461f-113">_Лпсзаддресс_</span><span class="sxs-lookup"><span data-stu-id="3461f-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="3461f-114">возврата Указатель на адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="3461f-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="3461f-115">Параметр _лпсзаддресс_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="3461f-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="3461f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3461f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="3461f-117">возврата Битовая маска флагов, влияющих на одного получателя.</span><span class="sxs-lookup"><span data-stu-id="3461f-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="3461f-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="3461f-118">The following flags can be set:</span></span>
    
<span data-ttu-id="3461f-119">МАПИ_СЕНД_НО_РИЧ_ИНФО</span><span class="sxs-lookup"><span data-stu-id="3461f-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="3461f-120">Получатель не может обрабатывать форматированное содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="3461f-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="3461f-121">Если задано значение МАПИ_СЕНД_НО_РИЧ_ИНФО, MAPI задает для свойства **пр_сенд_рич_инфо** ([PIDTAGSENDRICHINFO](pidtagsendrichinfo-canonical-property.md)) получателя значение false.</span><span class="sxs-lookup"><span data-stu-id="3461f-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="3461f-122">Если МАПИ_СЕНД_НО_РИЧ_ИНФО не задано, MAPI задает для этого свойства значение TRUE, если адрес обмена сообщениями получателя, на который указывает _лпсзаддресс_ , интерпретируется как адрес в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3461f-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="3461f-123">В этом случае MAPI устанавливает для **ПР_СЕНД_РИЧ_ИНФО** значение false.</span><span class="sxs-lookup"><span data-stu-id="3461f-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="3461f-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3461f-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3461f-125">Отображаемое имя, тип адреса и адрес имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="3461f-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="3461f-126">Если флаг МАПИ_УНИКОДЕ не установлен, эти строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="3461f-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3461f-127">_Лпкбентрид_</span><span class="sxs-lookup"><span data-stu-id="3461f-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="3461f-128">вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ .</span><span class="sxs-lookup"><span data-stu-id="3461f-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3461f-129">_Лппентрид_</span><span class="sxs-lookup"><span data-stu-id="3461f-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="3461f-130">вышли Указатель на указатель на идентификатор записи для одноразового получателя.</span><span class="sxs-lookup"><span data-stu-id="3461f-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3461f-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3461f-131">Return value</span></span>

<span data-ttu-id="3461f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="3461f-132">S_OK</span></span> 
  
> <span data-ttu-id="3461f-133">Идентификатор записи с одноразовым входом успешно создан.</span><span class="sxs-lookup"><span data-stu-id="3461f-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3461f-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="3461f-134">Remarks</span></span>

<span data-ttu-id="3461f-135">Клиенты вызывают метод **креатеонеофф** для создания идентификатора записи для одноразового получателя — получателя, не относящегося к какому-либо из контейнеров из загруженных в текущий момент поставщиков адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3461f-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="3461f-136">У одноразовых получателей может быть любой адрес, поддерживаемый одним из активных поставщиков адресных книг для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="3461f-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="3461f-137">Как правило, одноразовые получатели создаются с помощью шаблона для определенного типа адресов.</span><span class="sxs-lookup"><span data-stu-id="3461f-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="3461f-138">Поставщик адресных книг, поддерживающий тип адреса, предоставляет шаблон.</span><span class="sxs-lookup"><span data-stu-id="3461f-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="3461f-139">Пользователь клиентского приложения вводит соответствующую информацию в шаблон.</span><span class="sxs-lookup"><span data-stu-id="3461f-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="3461f-140">MAPI поддерживает строки символов Юникода для отображаемого имени, типа адреса и параметров адреса **креатеонеофф**.</span><span class="sxs-lookup"><span data-stu-id="3461f-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="3461f-141">Флаг МАПИ_СЕНД_НО_РИЧ_ИНФО определяет, будет ли форматированный текст в формате RTF передаваться вместе с каждым сообщением.</span><span class="sxs-lookup"><span data-stu-id="3461f-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="3461f-142">Формат TNEF, используемый для передачи форматированного текста, отправляется большинством поставщиков транспорта, независимо от того, как получатель задает свойство **пр_сенд_рич_инфо** .</span><span class="sxs-lookup"><span data-stu-id="3461f-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="3461f-143">Это не проблема для клиентов обмена сообщениями, работающих с взаимосвязанными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3461f-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="3461f-144">Тем не менее, так как формат TNEF обычно используется для отправки настраиваемых свойств настраиваемым классам сообщений, он может быть проблемой для клиентов на основе форм или клиентов, которым требуются настраиваемые свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="3461f-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="3461f-145">Более подробную информацию можно узнать [в статье отправка сообщений в формате TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="3461f-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3461f-146">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3461f-146">MFCMAPI reference</span></span>

<span data-ttu-id="3461f-147">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3461f-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3461f-148">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3461f-148">**File**</span></span>|<span data-ttu-id="3461f-149">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3461f-149">**Function**</span></span>|<span data-ttu-id="3461f-150">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3461f-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3461f-151">Мапиабфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="3461f-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="3461f-152">Аддонеоффаддресс</span><span class="sxs-lookup"><span data-stu-id="3461f-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="3461f-153">MFCMAPI использует метод **креатеонеофф** для создания идентификатора записи для адреса, не найденного в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="3461f-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3461f-154">См. также</span><span class="sxs-lookup"><span data-stu-id="3461f-154">See also</span></span>



[<span data-ttu-id="3461f-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="3461f-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="3461f-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3461f-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="3461f-157">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3461f-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

