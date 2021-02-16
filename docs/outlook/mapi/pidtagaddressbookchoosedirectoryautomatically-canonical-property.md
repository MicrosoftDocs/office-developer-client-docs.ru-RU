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
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="10457-103">Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="10457-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="10457-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10457-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10457-105">Позволяет Microsoft Outlook 2010, русская версия Microsoft Outlook 2013 выбрать наиболее подходящий глобальный список адресов (GAL) или папку контактов для текущего почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="10457-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10457-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="10457-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10457-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="10457-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="10457-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="10457-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10457-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="10457-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="10457-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="10457-110">Property type:</span></span>  <br/> |<span data-ttu-id="10457-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="10457-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="10457-112">Область:</span><span class="sxs-lookup"><span data-stu-id="10457-112">Area:</span></span>  <br/> |<span data-ttu-id="10457-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="10457-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10457-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="10457-114">Remarks</span></span>

<span data-ttu-id="10457-115">Это свойство соответствует параметру **"Выбор автоматически"** в диалоговом окте "Параметры адресной книги".</span><span class="sxs-lookup"><span data-stu-id="10457-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="10457-116">Если это свойство существует в разделе профиля IID_CAPONE_PROF и имеет значение **true,** диалоговое окно адресной книги больше не используется по умолчанию для контейнера, заданного методом [SetDefaultDir,](iaddrbook-setdefaultdir.md) но выбирает адресную книгу, которую Outlook 2010 или Outlook 2013 считает подходящей для контекста, в котором отобразилось диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="10457-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="10457-117">Обратите внимание, что это может привести к плохому опыту для сторонних поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="10457-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="10457-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="10457-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="10457-119">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="10457-119">Header files</span></span>

<span data-ttu-id="10457-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10457-120">Mapitags.h</span></span>
  
> <span data-ttu-id="10457-121">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="10457-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="10457-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10457-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="10457-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="10457-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10457-124">См. также</span><span class="sxs-lookup"><span data-stu-id="10457-124">See also</span></span>



[<span data-ttu-id="10457-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="10457-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10457-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="10457-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10457-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="10457-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="10457-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="10457-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10457-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="10457-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

