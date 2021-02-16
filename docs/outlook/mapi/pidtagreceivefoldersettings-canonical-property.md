---
title: Каноническое свойство PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415056"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="cf8e7-103">Каноническое свойство PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="cf8e7-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="cf8e7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf8e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf8e7-105">Содержит таблицу параметров папки получения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf8e7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cf8e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf8e7-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="cf8e7-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="cf8e7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cf8e7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf8e7-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="cf8e7-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="cf8e7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cf8e7-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf8e7-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="cf8e7-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="cf8e7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cf8e7-112">Area:</span></span>  <br/> |<span data-ttu-id="cf8e7-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="cf8e7-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf8e7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf8e7-114">Remarks</span></span>

<span data-ttu-id="cf8e7-115">Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="cf8e7-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="cf8e7-116">Свойство типа PT_OBJECT не может быть успешно извлечено методом [IMAPIProp::GetProps;](imapiprop-getprops.md) Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий интерфейс с идентификатором IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="cf8e7-117">Поставщики служб должны сообщить о нем методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не за установлен.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="cf8e7-118">Чтобы получить содержимое таблицы, клиентские приложения должны вызвать [метод IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="cf8e7-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="cf8e7-119">Дополнительные сведения [см. в таблицах папок получения.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="cf8e7-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="cf8e7-120">Это свойство содержит таблицу сопоставлений папок получения для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="cf8e7-121">Вызов **OpenProperty** для этого свойства эквивалентен вызову **GetReceiveFolderTable** в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cf8e7-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cf8e7-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cf8e7-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="cf8e7-123">Header files</span></span>

<span data-ttu-id="cf8e7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf8e7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf8e7-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf8e7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cf8e7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cf8e7-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf8e7-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cf8e7-128">See also</span></span>



[<span data-ttu-id="cf8e7-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cf8e7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf8e7-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cf8e7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf8e7-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cf8e7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf8e7-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cf8e7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

