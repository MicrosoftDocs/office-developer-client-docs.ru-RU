---
title: О регистрации хранилищ для индексации
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321828"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="9c67e-103">О регистрации хранилищ для индексации</span><span class="sxs-lookup"><span data-stu-id="9c67e-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="9c67e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c67e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c67e-105">Этот раздел является специфическим для мгновенного поиска в Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="9c67e-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="9c67e-106">Мгновенный поиск позволяет быстро находить элементы в Outlook.</span><span class="sxs-lookup"><span data-stu-id="9c67e-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="9c67e-107">В нем используются компоненты windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="9c67e-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="9c67e-108">Обработник протокола MAPI проверяет реестр Windows на наличие хранилищ, которые он должен индексировать в целях поиска.</span><span class="sxs-lookup"><span data-stu-id="9c67e-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="9c67e-109">Поставщики магазина, которые хотят индексироваться, должны быть зарегистрированы в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="9c67e-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="9c67e-110">По умолчанию поиск на рабочем столе Windows добавляет в реестр Windows четыре типа поставщиков магазина, чтобы разрешить индексацию:</span><span class="sxs-lookup"><span data-stu-id="9c67e-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="9c67e-111">Файлы личных папок в Хранилище (. PST).</span><span class="sxs-lookup"><span data-stu-id="9c67e-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="9c67e-112">Хранилище Microsoft Exchange, включая все файлы автономных папок (OST).</span><span class="sxs-lookup"><span data-stu-id="9c67e-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="9c67e-113">Хранилище для общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="9c67e-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="9c67e-114">Store для Microsoft Office Outlook connector для MSN.</span><span class="sxs-lookup"><span data-stu-id="9c67e-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="9c67e-115">Сторонние поставщики магазина, которые хотят индексироваться, должны зарегистрироваться в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="9c67e-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9c67e-116">Администраторы и пользователи могут использовать параметр групповой политики, чтобы запретить поиску windows desktop индексировать элементы Outlook.</span><span class="sxs-lookup"><span data-stu-id="9c67e-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="9c67e-117">Дополнительные сведения см. в [расширенном поиске на рабочем столе Windows.](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c67e-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="9c67e-118">Ключи реестра</span><span class="sxs-lookup"><span data-stu-id="9c67e-118">Registry Keys</span></span>

<span data-ttu-id="9c67e-119">На компьютере все поставщики store, которые нужно индексировать, должны быть зарегистрированы только в одном из следующих трех реестров в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="9c67e-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="9c67e-120">Обработник протокола MAPI ищет каждый из этих ключей в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="9c67e-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="9c67e-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span><span class="sxs-lookup"><span data-stu-id="9c67e-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span></span>\
    
2. <span data-ttu-id="9c67e-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="9c67e-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
3. <span data-ttu-id="9c67e-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="9c67e-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
 <span data-ttu-id="9c67e-124">Каждое значение под ключом соответствует поставщику магазина, который будет индексироваться.</span><span class="sxs-lookup"><span data-stu-id="9c67e-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="9c67e-125">Имя значения — это глобальный уникальный идентификатор (GUID) поставщика магазина, который имеет тип **DWORD** и имеет значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="9c67e-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="9c67e-126">GUID для поставщиков магазина</span><span class="sxs-lookup"><span data-stu-id="9c67e-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="9c67e-127">Свойство MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** guID для хранения MAPI.</span><span class="sxs-lookup"><span data-stu-id="9c67e-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="9c67e-128">В следующей таблице описаны GUID для поставщиков магазина, индексы outlook.</span><span class="sxs-lookup"><span data-stu-id="9c67e-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="9c67e-129">**Тип поставщика store**</span><span class="sxs-lookup"><span data-stu-id="9c67e-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="9c67e-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="9c67e-130">**GUID**</span></span> <br/> |<span data-ttu-id="9c67e-131">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="9c67e-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="9c67e-132">Файлы личных папок (. PST)</span><span class="sxs-lookup"><span data-stu-id="9c67e-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="9c67e-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="9c67e-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="9c67e-134">GUID задокументирован в файле общедоступных заговорок mspst.h **как MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="9c67e-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="9c67e-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="9c67e-135">Exchange</span></span>  <br/> |<span data-ttu-id="9c67e-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="9c67e-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="9c67e-137">GUID задокументирован в файле общедоступных заголовок edkmdb.h как **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="9c67e-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="9c67e-138">Общедоступные папки</span><span class="sxs-lookup"><span data-stu-id="9c67e-138">Public folders</span></span>  <br/> |<span data-ttu-id="9c67e-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="9c67e-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="9c67e-140">GUID задокументирован в файле общедоступных заголовок edkmdb.h как **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="9c67e-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="9c67e-141">Outlook Connector для MSN</span><span class="sxs-lookup"><span data-stu-id="9c67e-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="9c67e-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="9c67e-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="9c67e-143">Нет</span><span class="sxs-lookup"><span data-stu-id="9c67e-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c67e-144">См. также</span><span class="sxs-lookup"><span data-stu-id="9c67e-144">See also</span></span>



[<span data-ttu-id="9c67e-145">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="9c67e-145">About the Store API</span></span>](about-the-store-api.md)

