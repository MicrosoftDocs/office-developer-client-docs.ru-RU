---
title: Отображение стандартным диалоговым окном адрес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808338"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="e65d8-103">Отображение стандартным диалоговым окном адрес</span><span class="sxs-lookup"><span data-stu-id="e65d8-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="e65d8-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e65d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e65d8-105">Диалоговое окно MAPI распространенных адрес может использоваться для различных адресации задачи, такие как создание списка получателей.</span><span class="sxs-lookup"><span data-stu-id="e65d8-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="e65d8-106">Чтобы отобразить это диалоговое окно, вызовите **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="e65d8-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="e65d8-107">В зависимости от того, какой из много параметров, заданную вами и как задать можно ограничить экрана записи определенного типа из конкретного контейнера.</span><span class="sxs-lookup"><span data-stu-id="e65d8-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="e65d8-108">**Чтобы ограничить поле адрес для отображения только запись адресной книги (адресной книги)**</span><span class="sxs-lookup"><span data-stu-id="e65d8-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="e65d8-109">Вызовите [IAddrBook::GetPAB](iaddrbook-getpab.md) , чтобы получить идентификатор записи личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e65d8-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="e65d8-110">Создание ограничение свойство, которое использует RELOP_EQ для элемента **relop** структура [SPropertyRestriction](spropertyrestriction.md) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) в качестве член **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="e65d8-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="e65d8-111">Если вы используете **PR_ENTRYID**, передайте идентификатор записи, извлекается из **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="e65d8-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="e65d8-112">Если вы используете **PR_AB_PROVIDER_ID**, передайте значение, включенные в MSPAB. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="e65d8-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="e65d8-113">**PR_AB_PROVIDER_ID** — уникальный идентификатор для адресной книги, разработанная MAPI.</span><span class="sxs-lookup"><span data-stu-id="e65d8-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="e65d8-114">Вызов [IAddrBook::Address](iaddrbook-address.md) совместно с параметром _lpHierRestriction_ с указанием ограничении свойства.</span><span class="sxs-lookup"><span data-stu-id="e65d8-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

