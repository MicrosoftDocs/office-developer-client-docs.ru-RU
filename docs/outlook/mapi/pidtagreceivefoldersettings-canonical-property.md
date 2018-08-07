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
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811655"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="ca132-103">Каноническое свойство PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="ca132-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="ca132-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca132-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca132-105">Содержит таблицы сообщения магазина принимать параметры папки.</span><span class="sxs-lookup"><span data-stu-id="ca132-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca132-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ca132-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca132-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="ca132-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="ca132-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ca132-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca132-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="ca132-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="ca132-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ca132-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca132-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ca132-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ca132-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ca132-112">Area:</span></span>  <br/> |<span data-ttu-id="ca132-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="ca132-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca132-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca132-114">Remarks</span></span>

<span data-ttu-id="ca132-115">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="ca132-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="ca132-116">Как свойство типа PT_OBJECT не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающий интерфейс с идентификатором IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="ca132-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="ca132-117">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если он имеет значение, но при необходимости можно сообщить или не в том случае, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="ca132-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="ca132-118">Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="ca132-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="ca132-119">Для получения дополнительных сведений см [получают папки](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ca132-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="ca132-120">Это свойство содержит таблицу сопоставления для получения папок для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca132-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="ca132-121">Вызов **OpenProperty** на это свойство эквивалентно вызову **GetReceiveFolderTable** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca132-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ca132-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ca132-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ca132-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ca132-123">Header files</span></span>

<span data-ttu-id="ca132-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca132-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca132-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ca132-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca132-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca132-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ca132-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ca132-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca132-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ca132-128">See also</span></span>



[<span data-ttu-id="ca132-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ca132-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca132-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ca132-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca132-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ca132-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca132-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ca132-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

