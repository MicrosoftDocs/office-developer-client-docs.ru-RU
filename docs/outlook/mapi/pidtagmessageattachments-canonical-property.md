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
ms.openlocfilehash: 5b76a73a0fde8f4531b99a58646b927724162e81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811336"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="dfb41-103">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="dfb41-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="dfb41-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfb41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfb41-105">Содержит таблицу ограничения, которые могут быть применены к таблице содержимого для поиска всех сообщений, содержащих вложения вложенных объектов, необходимых для ограничения.</span><span class="sxs-lookup"><span data-stu-id="dfb41-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain attachment subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfb41-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dfb41-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dfb41-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="dfb41-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="dfb41-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dfb41-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dfb41-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="dfb41-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="dfb41-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dfb41-110">Data type:</span></span>  <br/> |<span data-ttu-id="dfb41-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="dfb41-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="dfb41-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dfb41-112">Area:</span></span>  <br/> |<span data-ttu-id="dfb41-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="dfb41-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfb41-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dfb41-114">Remarks</span></span>

<span data-ttu-id="dfb41-115">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="dfb41-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="dfb41-116">Как свойство типа PT_OBJECT его нельзя отменить успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb41-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="dfb41-117">Его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="dfb41-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="dfb41-118">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если оно установлено, но может сообщать о его или не в том случае, если не указано.</span><span class="sxs-lookup"><span data-stu-id="dfb41-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="dfb41-119">Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb41-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="dfb41-120">For more information, see [������� ��������](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="dfb41-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="dfb41-121">Это свойство можно использовать для ограничения вложенные объекты, указав в структуре [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb41-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="dfb41-122">Это позволяет клиента для ограничения представления контейнера для сообщений с вложениями собрания, заданному критерию.</span><span class="sxs-lookup"><span data-stu-id="dfb41-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="dfb41-123">Сообщение имеет право на просмотр, если хотя бы одна строка в таблице вложений, то есть одного вложения, удовлетворяет ограничениям вложенные объекты.</span><span class="sxs-lookup"><span data-stu-id="dfb41-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dfb41-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dfb41-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dfb41-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dfb41-125">Protocol specifications</span></span>

<span data-ttu-id="dfb41-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfb41-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfb41-127">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="dfb41-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="dfb41-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfb41-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfb41-129">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="dfb41-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="dfb41-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfb41-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfb41-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="dfb41-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dfb41-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dfb41-132">Header files</span></span>

<span data-ttu-id="dfb41-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dfb41-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="dfb41-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dfb41-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="dfb41-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dfb41-135">Mapitags.h</span></span>
  
> <span data-ttu-id="dfb41-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="dfb41-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfb41-137">См. также</span><span class="sxs-lookup"><span data-stu-id="dfb41-137">See also</span></span>



[<span data-ttu-id="dfb41-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dfb41-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dfb41-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dfb41-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dfb41-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dfb41-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dfb41-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dfb41-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

