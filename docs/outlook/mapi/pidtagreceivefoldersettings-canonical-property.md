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
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="74ee0-103">Каноническое свойство PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="74ee0-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="74ee0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74ee0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74ee0-105">Содержит таблицу параметров получения папки для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="74ee0-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74ee0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="74ee0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74ee0-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="74ee0-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="74ee0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="74ee0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74ee0-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="74ee0-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="74ee0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="74ee0-110">Data type:</span></span>  <br/> |<span data-ttu-id="74ee0-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="74ee0-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="74ee0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="74ee0-112">Area:</span></span>  <br/> |<span data-ttu-id="74ee0-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="74ee0-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74ee0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="74ee0-114">Remarks</span></span>

<span data-ttu-id="74ee0-115">Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="74ee0-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="74ee0-116">Как свойство типа PT_OBJECT, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) GetProperty. к его содержимому должен обращаться метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , который запрашивает интерфейс с идентификатором IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="74ee0-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="74ee0-117">Поставщики услуг должны сообщить об этом в метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="74ee0-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="74ee0-118">Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="74ee0-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="74ee0-119">Дополнительные сведения [см.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="74ee0-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="74ee0-120">Это свойство содержит таблицу сопоставлений папок получения для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="74ee0-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="74ee0-121">Вызов **опенпроперти** для этого свойства эквивалентен вызову **жетрецеивефолдертабле** в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="74ee0-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="74ee0-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="74ee0-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="74ee0-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="74ee0-123">Header files</span></span>

<span data-ttu-id="74ee0-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="74ee0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="74ee0-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="74ee0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="74ee0-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="74ee0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="74ee0-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="74ee0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74ee0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="74ee0-128">See also</span></span>



[<span data-ttu-id="74ee0-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74ee0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74ee0-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="74ee0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74ee0-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="74ee0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74ee0-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="74ee0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

