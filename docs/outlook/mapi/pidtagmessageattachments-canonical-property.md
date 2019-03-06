---
title: Каноническое свойство PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413975"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="323ca-103">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="323ca-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="323ca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="323ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="323ca-105">Содержит таблицу вложений для сообщения.</span><span class="sxs-lookup"><span data-stu-id="323ca-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="323ca-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="323ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="323ca-107">ПР_МЕССАЖЕ_АТТАЧМЕНТС</span><span class="sxs-lookup"><span data-stu-id="323ca-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="323ca-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="323ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="323ca-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="323ca-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="323ca-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="323ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="323ca-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="323ca-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="323ca-112">Область:</span><span class="sxs-lookup"><span data-stu-id="323ca-112">Area:</span></span>  <br/> |<span data-ttu-id="323ca-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="323ca-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="323ca-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="323ca-114">Remarks</span></span>

<span data-ttu-id="323ca-115">Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="323ca-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="323ca-116">Как свойство типа ПТ_ОБЖЕКТ, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="323ca-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="323ca-117">К его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса **иид_имапитабле** .</span><span class="sxs-lookup"><span data-stu-id="323ca-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="323ca-118">Поставщики услуг должны сообщить о ней методу [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="323ca-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="323ca-119">Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [iMessage:: жетаттачменттабле](imessage-getattachmenttable.md) .</span><span class="sxs-lookup"><span data-stu-id="323ca-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="323ca-120">For more information, see [������� ��������](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="323ca-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="323ca-121">Это свойство можно использовать для ограничения подобъекта, указав его в структуре [ссубрестриктион](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="323ca-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="323ca-122">Это позволяет клиенту ограничить представление контейнера сообщениями с вложениями, которые удовлетворяют заданным условиям.</span><span class="sxs-lookup"><span data-stu-id="323ca-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="323ca-123">Сообщение просматривается, если по крайней мере одна строка в таблице вложений, то есть одно вложение, удовлетворяет ограничению этого подобъекта.</span><span class="sxs-lookup"><span data-stu-id="323ca-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="323ca-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="323ca-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="323ca-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="323ca-125">Protocol specifications</span></span>

<span data-ttu-id="323ca-126">[[MS — ОКСКДАТА]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="323ca-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="323ca-127">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="323ca-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="323ca-128">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="323ca-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="323ca-129">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="323ca-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="323ca-130">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="323ca-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="323ca-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="323ca-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="323ca-132">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="323ca-132">Header files</span></span>

<span data-ttu-id="323ca-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="323ca-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="323ca-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="323ca-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="323ca-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="323ca-135">Mapitags.h</span></span>
  
> <span data-ttu-id="323ca-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="323ca-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="323ca-137">См. также</span><span class="sxs-lookup"><span data-stu-id="323ca-137">See also</span></span>



[<span data-ttu-id="323ca-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="323ca-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="323ca-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="323ca-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="323ca-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="323ca-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="323ca-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="323ca-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

