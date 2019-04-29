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
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409666"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="9b6be-103">Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="9b6be-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="9b6be-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b6be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b6be-105">Позволяет Microsoft Outlook 2010 и Microsoft Outlook 2013 выбрать наиболее подходящий глобальный список адресов (GAL) или папку контактов для текущего почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="9b6be-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b6be-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9b6be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b6be-107">ПР_АБ_ЧУСЕ_ДИРЕКТОРИ_АУТОМАТИКАЛЛИ</span><span class="sxs-lookup"><span data-stu-id="9b6be-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="9b6be-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9b6be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b6be-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="9b6be-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="9b6be-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="9b6be-110">Property type:</span></span>  <br/> |<span data-ttu-id="9b6be-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9b6be-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9b6be-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9b6be-112">Area:</span></span>  <br/> |<span data-ttu-id="9b6be-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="9b6be-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b6be-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b6be-114">Remarks</span></span>

<span data-ttu-id="9b6be-115">Это свойство соответствует параметру **выбрать автоматический** параметр в диалоговом окне Параметры адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9b6be-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="9b6be-116">Если это свойство существует в разделе profile ИИД_КАПОНЕ_ПРОФ и имеет значение **true**, диалоговое окно адресной книги больше не будет использоваться по умолчанию в контейнере, указанном в методе [сетдефаултдир](iaddrbook-setdefaultdir.md) , но выбирает адресную книгу, которую outlook 2010 или Outlook 2013 подсчитается подходящим для контекста, в котором отображается диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9b6be-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="9b6be-117">Обратите внимание, что это может привести к неудовлетворительному взаимодействию сторонних поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="9b6be-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b6be-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9b6be-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9b6be-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9b6be-119">Header files</span></span>

<span data-ttu-id="9b6be-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9b6be-120">Mapitags.h</span></span>
  
> <span data-ttu-id="9b6be-121">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="9b6be-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="9b6be-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9b6be-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b6be-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9b6be-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b6be-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9b6be-124">See also</span></span>



[<span data-ttu-id="9b6be-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9b6be-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b6be-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9b6be-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b6be-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="9b6be-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9b6be-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9b6be-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b6be-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9b6be-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

