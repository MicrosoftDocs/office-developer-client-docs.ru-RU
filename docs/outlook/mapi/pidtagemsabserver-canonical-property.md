---
title: Каноническое свойство PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335800"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="efaff-103">Каноническое свойство PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="efaff-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="efaff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efaff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efaff-105">Указывает путь контейнера адресной книги в автономном сценарии или полное доменное имя сервера глобального каталога, где контейнер адресной книги находится в онлайн-сценарии.</span><span class="sxs-lookup"><span data-stu-id="efaff-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="efaff-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="efaff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efaff-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="efaff-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="efaff-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="efaff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efaff-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="efaff-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="efaff-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="efaff-110">Data type:</span></span>  <br/> |<span data-ttu-id="efaff-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="efaff-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="efaff-112">Область:</span><span class="sxs-lookup"><span data-stu-id="efaff-112">Area:</span></span>  <br/> |<span data-ttu-id="efaff-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="efaff-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efaff-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="efaff-114">Remarks</span></span>

<span data-ttu-id="efaff-115">Это свойство имеет сброс типа свойства **PT_UNICODE,** когда он компилирован с символом на платформе Unicode, и PT_STRING8, когда он не компилирован `UNICODE` с  `UNICODE` символом.</span><span class="sxs-lookup"><span data-stu-id="efaff-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="efaff-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="efaff-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="efaff-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="efaff-117">Protocol specifications</span></span>

<span data-ttu-id="efaff-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efaff-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efaff-119">Предоставляет определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="efaff-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="efaff-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="efaff-120">Header files</span></span>

<span data-ttu-id="efaff-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efaff-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="efaff-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="efaff-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="efaff-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="efaff-123">Mapitags.h</span></span>
  
> <span data-ttu-id="efaff-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="efaff-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efaff-125">См. также</span><span class="sxs-lookup"><span data-stu-id="efaff-125">See also</span></span>



[<span data-ttu-id="efaff-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="efaff-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efaff-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="efaff-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efaff-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="efaff-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efaff-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="efaff-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

