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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342569"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="8d04e-103">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="8d04e-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="8d04e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d04e-105">Содержит таблицу вложений для сообщения.</span><span class="sxs-lookup"><span data-stu-id="8d04e-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d04e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8d04e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d04e-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="8d04e-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="8d04e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8d04e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d04e-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="8d04e-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="8d04e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8d04e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d04e-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8d04e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8d04e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8d04e-112">Area:</span></span>  <br/> |<span data-ttu-id="8d04e-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="8d04e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d04e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d04e-114">Remarks</span></span>

<span data-ttu-id="8d04e-115">Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="8d04e-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="8d04e-116">В качестве свойства типа PT_OBJECT его не удается получить с помощью метода [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="8d04e-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="8d04e-117">Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий идентификатор IID_IMAPITable интерфейса. </span><span class="sxs-lookup"><span data-stu-id="8d04e-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="8d04e-118">Поставщики служб должны сообщить о нем методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не за установлен.</span><span class="sxs-lookup"><span data-stu-id="8d04e-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="8d04e-119">Чтобы получить содержимое таблицы, клиентские приложения должны вызвать [метод IMessage::GetAttachmentTable.](imessage-getattachmenttable.md)</span><span class="sxs-lookup"><span data-stu-id="8d04e-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="8d04e-120">For more information, see [������� ��������](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8d04e-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="8d04e-121">Это свойство можно использовать для ограничения подобектов, указав его в структуре [SSubRestriction.](ssubrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="8d04e-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="8d04e-122">Это позволяет клиенту ограничить представление контейнера сообщениями с вложениями, которые соответствуют заданным критериям.</span><span class="sxs-lookup"><span data-stu-id="8d04e-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="8d04e-123">Сообщение квалификаторы для просмотра, если по крайней мере одна строка в таблице вложений, то есть одно вложение, удовлетворяет ограничению subobject.</span><span class="sxs-lookup"><span data-stu-id="8d04e-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d04e-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8d04e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d04e-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8d04e-125">Protocol specifications</span></span>

<span data-ttu-id="8d04e-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d04e-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d04e-127">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="8d04e-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="8d04e-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d04e-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d04e-129">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="8d04e-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="8d04e-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d04e-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d04e-131">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="8d04e-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d04e-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="8d04e-132">Header files</span></span>

<span data-ttu-id="8d04e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d04e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d04e-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8d04e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d04e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d04e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="8d04e-136">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8d04e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d04e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="8d04e-137">See also</span></span>



[<span data-ttu-id="8d04e-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d04e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d04e-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d04e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d04e-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8d04e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d04e-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8d04e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

