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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384981"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="2ae22-103">Каноническое свойство PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="2ae22-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="2ae22-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ae22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ae22-105">Задает путь контейнер адресной книги в автономном режиме сценарий или полное доменное имя сервера глобального каталога, где находится контейнер адресной книги в сети сценария.</span><span class="sxs-lookup"><span data-stu-id="2ae22-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="2ae22-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2ae22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ae22-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="2ae22-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="2ae22-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2ae22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ae22-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="2ae22-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="2ae22-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2ae22-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ae22-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="2ae22-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="2ae22-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2ae22-112">Area:</span></span>  <br/> |<span data-ttu-id="2ae22-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="2ae22-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ae22-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ae22-114">Remarks</span></span>

<span data-ttu-id="2ae22-115">Это свойство имеет тип свойства, сброс **PT_UNICODE** , при выполнении компиляции с `UNICODE` символ Unicode платформы, а также **PT_STRING8** , если он не компилируется с `UNICODE` символов.</span><span class="sxs-lookup"><span data-stu-id="2ae22-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ae22-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ae22-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ae22-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2ae22-117">Protocol specifications</span></span>

<span data-ttu-id="2ae22-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ae22-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ae22-119">Содержит определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="2ae22-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ae22-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2ae22-120">Header files</span></span>

<span data-ttu-id="2ae22-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ae22-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ae22-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2ae22-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ae22-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ae22-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2ae22-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2ae22-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ae22-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2ae22-125">See also</span></span>



[<span data-ttu-id="2ae22-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ae22-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ae22-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ae22-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ae22-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2ae22-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ae22-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2ae22-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

