---
title: Каноническое свойство PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b357a068249b12468be52f8782f646f394e4060
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567827"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a><span data-ttu-id="b7b78-103">Каноническое свойство PidTagAdditionalRenEntryIds</span><span class="sxs-lookup"><span data-stu-id="b7b78-103">PidTagAdditionalRenEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="b7b78-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7b78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7b78-105">Содержит запись идентификаторы из специальных папок.</span><span class="sxs-lookup"><span data-stu-id="b7b78-105">Contains the entry IDs of certain special folders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7b78-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b7b78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7b78-107">PR_ADDITIONAL_REN_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="b7b78-107">PR_ADDITIONAL_REN_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="b7b78-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b7b78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7b78-109">0x36D8</span><span class="sxs-lookup"><span data-stu-id="b7b78-109">0x36D8</span></span>  <br/> |
|<span data-ttu-id="b7b78-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b7b78-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7b78-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="b7b78-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="b7b78-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b7b78-112">Area:</span></span>  <br/> |<span data-ttu-id="b7b78-113">Приложения Outlook</span><span class="sxs-lookup"><span data-stu-id="b7b78-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7b78-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b7b78-114">Remarks</span></span>

<span data-ttu-id="b7b78-115">Первые пять записей этого многозначные свойства применяются к следующим папкам, если они существуют в хранилище.</span><span class="sxs-lookup"><span data-stu-id="b7b78-115">The first five entries of this multi-valued property apply to following special folders, if they exist in the store:</span></span>
  
<span data-ttu-id="b7b78-116">0 — папки "конфликты"</span><span class="sxs-lookup"><span data-stu-id="b7b78-116">0 - conflicts folder</span></span>
  
<span data-ttu-id="b7b78-117">1 — синхронизации папки проблемы</span><span class="sxs-lookup"><span data-stu-id="b7b78-117">1 - sync issues folder</span></span>
  
<span data-ttu-id="b7b78-118">2 - папка Локальные ошибки</span><span class="sxs-lookup"><span data-stu-id="b7b78-118">2 - local failures folder</span></span>
  
<span data-ttu-id="b7b78-119">3 - папка сбои сервер</span><span class="sxs-lookup"><span data-stu-id="b7b78-119">3 - server failures folder</span></span>
  
<span data-ttu-id="b7b78-120">4 - нежелательной почты в соответствующую папку</span><span class="sxs-lookup"><span data-stu-id="b7b78-120">4 - junk email folder</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7b78-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7b78-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7b78-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b7b78-122">Protocol specifications</span></span>

<span data-ttu-id="b7b78-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b78-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b78-124">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b7b78-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7b78-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b78-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b78-126">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="b7b78-126">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="b7b78-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b78-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b78-128">Идентифицирует и помечает сообщения электронной почты, которые предназначены для побудить получателей разглашение конфиденциальной информации (например, пароли и другие личные сведения) чтобы-надежного источника.</span><span class="sxs-lookup"><span data-stu-id="b7b78-128">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
<span data-ttu-id="b7b78-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b78-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b78-130">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b7b78-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7b78-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b7b78-131">Header files</span></span>

<span data-ttu-id="b7b78-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7b78-132">Mapitags.h</span></span>
  
> <span data-ttu-id="b7b78-133">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="b7b78-133">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="b7b78-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7b78-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7b78-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b7b78-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7b78-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b7b78-136">See also</span></span>



[<span data-ttu-id="b7b78-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b7b78-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7b78-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b7b78-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7b78-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b7b78-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


[<span data-ttu-id="b7b78-140">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="b7b78-140">About the Store API</span></span>](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

