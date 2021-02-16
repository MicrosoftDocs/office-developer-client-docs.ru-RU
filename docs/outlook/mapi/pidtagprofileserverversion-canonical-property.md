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
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286568"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="49f00-103">Каноническое свойство PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="49f00-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="49f00-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49f00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49f00-105">Указывает сведения о версии Microsoft Exchange Server, к которой подключены учетные записи в профиле Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="49f00-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="49f00-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="49f00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49f00-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="49f00-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="49f00-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="49f00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49f00-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="49f00-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="49f00-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="49f00-110">Property type:</span></span>  <br/> |<span data-ttu-id="49f00-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="49f00-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="49f00-112">Область:</span><span class="sxs-lookup"><span data-stu-id="49f00-112">Area:</span></span>  <br/> |<span data-ttu-id="49f00-113">Конфигурация профиля MAPI</span><span class="sxs-lookup"><span data-stu-id="49f00-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49f00-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="49f00-114">Remarks</span></span>

<span data-ttu-id="49f00-115">Профиль может указывать одну или несколько учетных записей, которые подключаются к Exchange Server, но они должны быть подключены к одной Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49f00-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="49f00-116">Версии Outlook более ранних Microsoft Office Outlook 2007 могут записывать в это свойство, чтобы хранить сведения о версии Exchange Server, к которой подключен активный профиль.</span><span class="sxs-lookup"><span data-stu-id="49f00-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="49f00-117">Однако формат сведений о версии зависит от Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49f00-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="49f00-118">Например, Outlook сохраняет **в PR_PROFILE_SERVER_VERSION** десятичной части значение 6944, чтобы представить только основной номер сборки в идентификаторе версии **6.5.6944.3** для Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="49f00-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="49f00-119">Для подключения Exchange 2007 Outlook сохраняет основной номер версии и основной номер сборки в совмещенном хронном представлении этих номеров в свойстве.</span><span class="sxs-lookup"><span data-stu-id="49f00-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="49f00-120">Идентификатор версии Exchange 2007 **версии 8.0.685.24** имеет основной номер версии 8 и основной номер сборки 685 в десятичной.</span><span class="sxs-lookup"><span data-stu-id="49f00-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="49f00-121">При преобразовании обоих чисел в дексекулярные значения 0x8 и 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="49f00-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="49f00-122">При совмещеании этих двух чисел Outlook сохраняет значение 0x82AD **в** PR_PROFILE_SERVER_VERSION в дексдетельном представлении.</span><span class="sxs-lookup"><span data-stu-id="49f00-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="49f00-123">Outlook 2007 не читает и не записи в это свойство.</span><span class="sxs-lookup"><span data-stu-id="49f00-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="49f00-124">Он поддерживает **[PR_PROFILE_SERVER_FULL_VERSION.](pidtagprofileserverfullversion-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="49f00-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="49f00-125">В профиле **PR_PROFILE_SERVER_VERSION** или **PR_PROFILE_SERVER_FULL_VERSION,** скорее всего, существует только один из них, но нет гарантии, что в профиле всегда существует любой из них.</span><span class="sxs-lookup"><span data-stu-id="49f00-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="49f00-126">Outlook не записи в ни в один из свойств, пока не будет успешно подключен к Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49f00-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="49f00-127">В объектной модели Outlook можно использовать свойство **ExchangeMailboxServerVersion** объекта **NameSpace,** чтобы найти версию Exchange Server, в которой находится активный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="49f00-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="49f00-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="49f00-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49f00-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="49f00-129">Protocol specifications</span></span>

<span data-ttu-id="49f00-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49f00-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49f00-131">Предоставляет определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="49f00-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49f00-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="49f00-132">Header files</span></span>

<span data-ttu-id="49f00-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49f00-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="49f00-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="49f00-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="49f00-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="49f00-135">Mapitags.h</span></span>
  
> <span data-ttu-id="49f00-136">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="49f00-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49f00-137">См. также</span><span class="sxs-lookup"><span data-stu-id="49f00-137">See also</span></span>



[<span data-ttu-id="49f00-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="49f00-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49f00-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="49f00-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49f00-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="49f00-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49f00-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="49f00-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

