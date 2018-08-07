---
title: Каноническое свойство PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811573"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="34767-103">Каноническое свойство PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="34767-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="34767-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34767-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34767-105">Указывает полные сведения о Microsoft Exchange Server, к которому подключены учетных записей в профиле версии и построения.</span><span class="sxs-lookup"><span data-stu-id="34767-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="34767-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="34767-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34767-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="34767-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="34767-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="34767-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34767-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="34767-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="34767-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="34767-110">Property type:</span></span>  <br/> |<span data-ttu-id="34767-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="34767-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="34767-112">Область:</span><span class="sxs-lookup"><span data-stu-id="34767-112">Area:</span></span>  <br/> |<span data-ttu-id="34767-113">Настройки профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="34767-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34767-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="34767-114">Remarks</span></span>

<span data-ttu-id="34767-115">Профиль можно указать один или несколько учетных записей, которые подключаются к серверу Exchange, но они должна быть соединена с одного сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="34767-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="34767-116">Версии Outlook, предшествующие Microsoft Office Outlook 2007 не поддерживают это свойство.</span><span class="sxs-lookup"><span data-stu-id="34767-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="34767-117">Эти версии Outlook Проверьте наличие **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** в профиле.</span><span class="sxs-lookup"><span data-stu-id="34767-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="34767-118">Как правило если active почтовый ящик подключен к серверу Exchange, Outlook 2007 сохраняется полный сведений о версии Exchange Server в свойстве **PR_PROFILE_SERVER_FULL_VERSION** в текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="34767-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="34767-119">Outlook хранит сведения в структуре **EXCHANGE_STORE_VERSION_NUM** , который содержит номера основной и дополнительный номер версии и номера основной и дополнительной сборок.</span><span class="sxs-lookup"><span data-stu-id="34767-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="34767-120">К примеру для хранения идентификатор версии Exchange Server **8.0.685.24**основной номер версии — 8 и дополнительный номер версии — 0 и 685 — номер основной сборки и дополнительный номер — номер сборки 24.</span><span class="sxs-lookup"><span data-stu-id="34767-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="34767-121">Только один из **PR_PROFILE_SERVER_VERSION** или **PR_PROFILE_SERVER_FULL_VERSION** скорее всего, существуют в профиле, но не гарантируется, либо всегда существует в профиле.</span><span class="sxs-lookup"><span data-stu-id="34767-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="34767-122">Outlook не записывает либо свойством только после успешного подключения к серверу Exchange.</span><span class="sxs-lookup"><span data-stu-id="34767-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="34767-123">В объектной модели Outlook можно использовать свойство **ExchangeMailboxServerVersion** объекта **пространство имен** для поиска версии Exchange Server, на котором размещен почтовый ящик active.</span><span class="sxs-lookup"><span data-stu-id="34767-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="34767-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="34767-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34767-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="34767-125">Protocol specifications</span></span>

<span data-ttu-id="34767-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34767-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34767-127">Содержит определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="34767-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34767-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="34767-128">Header files</span></span>

<span data-ttu-id="34767-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34767-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="34767-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="34767-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="34767-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34767-131">Mapitags.h</span></span>
  
> <span data-ttu-id="34767-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="34767-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34767-133">См. также</span><span class="sxs-lookup"><span data-stu-id="34767-133">See also</span></span>



[<span data-ttu-id="34767-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="34767-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34767-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="34767-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34767-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="34767-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34767-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="34767-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

