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
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341603"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="6034e-103">Каноническое свойство PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="6034e-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="6034e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6034e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6034e-105">Указывает полную версию и создает сведения о Microsoft Exchange Server, к которым подключены учетные записи в профиле.</span><span class="sxs-lookup"><span data-stu-id="6034e-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6034e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6034e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6034e-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="6034e-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="6034e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6034e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6034e-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="6034e-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="6034e-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="6034e-110">Property type:</span></span>  <br/> |<span data-ttu-id="6034e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6034e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6034e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6034e-112">Area:</span></span>  <br/> |<span data-ttu-id="6034e-113">Конфигурация профиля MAPI</span><span class="sxs-lookup"><span data-stu-id="6034e-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6034e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6034e-114">Remarks</span></span>

<span data-ttu-id="6034e-115">Профиль может указать одну или несколько учетных записей, которые подключаются к Exchange Server, но они должны быть подключены к одному Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6034e-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="6034e-116">Версии Outlook более ранних Microsoft Office Outlook 2007 года не поддерживают это свойство.</span><span class="sxs-lookup"><span data-stu-id="6034e-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="6034e-117">Для этих версий Outlook проверьте наличие PR_PROFILE_SERVER_VERSION **[в](pidtagprofileserverversion-canonical-property.md)** профиле.</span><span class="sxs-lookup"><span data-stu-id="6034e-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="6034e-118">Как правило, если активный почтовый ящик подключен к Exchange Server, Outlook 2007 г. Exchange Server  сведения о версии в свойстве PR_PROFILE_SERVER_FULL_VERSION в активном профиле.</span><span class="sxs-lookup"><span data-stu-id="6034e-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="6034e-119">Outlook хранит сведения в структуре **EXCHANGE_STORE_VERSION_NUM,** которая содержит основные и второстепенные номера версий, а также основные и второстепенные номера сборки.</span><span class="sxs-lookup"><span data-stu-id="6034e-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="6034e-120">Например, чтобы сохранить идентификатор Exchange Server версии **8.0.685.24,** основной номер версии — 8, а второстепенный — 0, а основной номер сборки — 685, а число сборки — 24.</span><span class="sxs-lookup"><span data-stu-id="6034e-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="6034e-121">Только один **PR_PROFILE_SERVER_VERSION** **или PR_PROFILE_SERVER_FULL_VERSION** может существовать в профиле, но нет никакой гарантии, что либо всегда существует в профиле.</span><span class="sxs-lookup"><span data-stu-id="6034e-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="6034e-122">Outlook не записыву в свойство, пока оно не будет успешно подключено к Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6034e-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="6034e-123">В Outlook объектной модели можно использовать свойство **ExchangeMailboxServerVersion** объекта **NameSpace,** чтобы найти версию Exchange Server, на которой расположен активный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="6034e-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6034e-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6034e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6034e-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6034e-125">Protocol specifications</span></span>

<span data-ttu-id="6034e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6034e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6034e-127">Предоставляет определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="6034e-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6034e-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6034e-128">Header files</span></span>

<span data-ttu-id="6034e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6034e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6034e-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6034e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="6034e-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6034e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="6034e-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6034e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6034e-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6034e-133">See also</span></span>



[<span data-ttu-id="6034e-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6034e-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6034e-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6034e-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6034e-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6034e-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6034e-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6034e-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

