---
title: Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810810"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="5642a-103">Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="5642a-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="5642a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5642a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5642a-105">Позволяет выбрать наиболее подходящую глобальном списке адресов (GAL) или папку "Контакты" для текущего почтового ящика Microsoft Outlook 2010 и Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="5642a-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5642a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5642a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5642a-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="5642a-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="5642a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5642a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5642a-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="5642a-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="5642a-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="5642a-110">Property type:</span></span>  <br/> |<span data-ttu-id="5642a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5642a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5642a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5642a-112">Area:</span></span>  <br/> |<span data-ttu-id="5642a-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="5642a-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5642a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5642a-114">Remarks</span></span>

<span data-ttu-id="5642a-115">Это свойство соответствует параметру **автоматически выбирать** в диалоговом окне параметры адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5642a-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="5642a-116">Когда это свойство в разделе профилей IID_CAPONE_PROF существует и имеет значение **true**, в адресной книге диалоговое окно больше не по умолчанию контейнер, указанный с помощью метода [SetDefaultDir](iaddrbook-setdefaultdir.md) , но выбирает к адресной книге, Outlook 2010 или Outlook 2013 рассматривает контексту, в котором диалоговое окно отображается.</span><span class="sxs-lookup"><span data-stu-id="5642a-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="5642a-117">Обратите внимание на то, что это может привести к низкого уровня качества для поставщиками сторонних производителей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5642a-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5642a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5642a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5642a-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5642a-119">Header files</span></span>

<span data-ttu-id="5642a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5642a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5642a-121">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="5642a-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="5642a-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5642a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5642a-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5642a-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5642a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5642a-124">See also</span></span>



[<span data-ttu-id="5642a-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5642a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5642a-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5642a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5642a-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="5642a-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5642a-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5642a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5642a-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5642a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

