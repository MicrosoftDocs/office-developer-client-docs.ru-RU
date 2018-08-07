---
title: Каноническое свойство PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 498a740a6523434cc6c70793cf98fd1e2ccfbdb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811865"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="00caa-103">Каноническое свойство PidTagSearchRecipientEmailBcc</span><span class="sxs-lookup"><span data-stu-id="00caa-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="00caa-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00caa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00caa-105">Содержит строку Юникод, запрашиваемый в список адресов электронной почты или отображаемые имена получателей, которые рассматриваются в строки **Скрытая копия** неотправленные сообщения в хранилище.</span><span class="sxs-lookup"><span data-stu-id="00caa-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="00caa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="00caa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00caa-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="00caa-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="00caa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="00caa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00caa-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="00caa-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="00caa-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="00caa-110">Property type:</span></span>  <br/> |<span data-ttu-id="00caa-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00caa-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="00caa-112">Access:</span><span class="sxs-lookup"><span data-stu-id="00caa-112">Access:</span></span>  <br/> |<span data-ttu-id="00caa-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="00caa-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00caa-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="00caa-114">Remarks</span></span>

<span data-ttu-id="00caa-115">Это свойство применяется только в том к сообщениям в хранилище, которые не были отправлены, поскольку сообщений, отправленных или полученных не содержат сведения о скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="00caa-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="00caa-116">Этот тег ограничений MAPI, используется при поиске адресов электронной почты или отображаемые имена, в которых будет отправлено сообщение как скрытую копию, не могут быть определены в файле загружаемых заголовка, который в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="00caa-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="00caa-117">Добавьте в код с помощью следующее значение: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="00caa-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00caa-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="00caa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00caa-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="00caa-119">Protocol specifications</span></span>

<span data-ttu-id="00caa-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00caa-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00caa-121">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="00caa-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00caa-122">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00caa-122">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00caa-123">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="00caa-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00caa-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="00caa-124">Header files</span></span>

<span data-ttu-id="00caa-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00caa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="00caa-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="00caa-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="00caa-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00caa-127">Mapitags.h</span></span>
  
> <span data-ttu-id="00caa-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="00caa-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00caa-129">См. также</span><span class="sxs-lookup"><span data-stu-id="00caa-129">See also</span></span>



[<span data-ttu-id="00caa-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00caa-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00caa-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00caa-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00caa-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="00caa-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00caa-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="00caa-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

