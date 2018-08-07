---
title: Каноническое свойство PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811570"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="47202-103">Каноническое свойство PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="47202-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="47202-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47202-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47202-105">Указывает сведения о версии Microsoft Exchange Server, к которому подключены учетных записей в профиле Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="47202-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="47202-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="47202-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47202-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="47202-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="47202-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="47202-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47202-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="47202-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="47202-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="47202-110">Property type:</span></span>  <br/> |<span data-ttu-id="47202-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47202-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47202-112">Область:</span><span class="sxs-lookup"><span data-stu-id="47202-112">Area:</span></span>  <br/> |<span data-ttu-id="47202-113">Настройки профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="47202-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47202-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="47202-114">Remarks</span></span>

<span data-ttu-id="47202-115">Профиль можно указать один или несколько учетных записей, которые подключаются к серверу Exchange, но они должна быть соединена с одного сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="47202-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="47202-116">Версии Outlook, предшествующие Microsoft Office Outlook 2007 можно создать для этого свойства для хранения сведений о версии Exchange Server, к которому подключен активного профиля.</span><span class="sxs-lookup"><span data-stu-id="47202-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="47202-117">Тем не менее формат сведений о версии зависит от различных версий Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="47202-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="47202-118">Например Outlook хранилищ в **PR_PROFILE_SERVER_VERSION** десятичное значение 6944 для представления только основной номер в идентификатор версии **6.5.6944.3** сборки для Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="47202-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="47202-119">Для подключения к Exchange 2007 Outlook хранит основной номер версии и основной номер в составное шестнадцатеричное представление эти номера в свойстве построения.</span><span class="sxs-lookup"><span data-stu-id="47202-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="47202-120">Идентификатор версии Exchange 2007 **8.0.685.24** имеет номер основной версии 8 и основной номер построения 685 в тип decimal.</span><span class="sxs-lookup"><span data-stu-id="47202-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="47202-121">Преобразование обоих чисел в шестнадцатеричном представлении, вы получите 0x8 и 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="47202-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="47202-122">Объединения этих двух чисел, Outlook сохраняет значение 0x82AD в **PR_PROFILE_SERVER_VERSION** в шестнадцатеричном представлении.</span><span class="sxs-lookup"><span data-stu-id="47202-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="47202-123">Outlook 2007 не чтение или запись с этим свойством.</span><span class="sxs-lookup"><span data-stu-id="47202-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="47202-124">Поддержка **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="47202-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="47202-125">Только один из **PR_PROFILE_SERVER_VERSION** или **PR_PROFILE_SERVER_FULL_VERSION** скорее всего, существуют в профиле, но не гарантируется, либо всегда существует в профиле.</span><span class="sxs-lookup"><span data-stu-id="47202-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="47202-126">Outlook не записывает либо свойством только после успешного подключения к серверу Exchange.</span><span class="sxs-lookup"><span data-stu-id="47202-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="47202-127">В объектной модели Outlook можно использовать свойство **ExchangeMailboxServerVersion** объекта **пространство имен** для поиска версии Exchange Server, на котором размещен почтовый ящик active.</span><span class="sxs-lookup"><span data-stu-id="47202-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="47202-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="47202-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47202-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="47202-129">Protocol specifications</span></span>

<span data-ttu-id="47202-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47202-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47202-131">Содержит определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="47202-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47202-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="47202-132">Header files</span></span>

<span data-ttu-id="47202-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47202-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="47202-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="47202-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="47202-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47202-135">Mapitags.h</span></span>
  
> <span data-ttu-id="47202-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="47202-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47202-137">См. также</span><span class="sxs-lookup"><span data-stu-id="47202-137">See also</span></span>



[<span data-ttu-id="47202-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="47202-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47202-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="47202-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47202-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="47202-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47202-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="47202-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

