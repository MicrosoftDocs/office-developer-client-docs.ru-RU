---
title: Сведения о регистрации хранилищ для индексирования
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 195812f53c4c0aaf20e4ed6e215d15b0295c9a07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584186"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="d241a-103">Сведения о регистрации хранилищ для индексирования</span><span class="sxs-lookup"><span data-stu-id="d241a-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="d241a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d241a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d241a-105">В этом разделе специально для мгновенного поиска в Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="d241a-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="d241a-106">Мгновенный поиск позволяет вам быстро находить элементы в Outlook.</span><span class="sxs-lookup"><span data-stu-id="d241a-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="d241a-107">Он использует компоненты Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="d241a-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="d241a-108">Обработчик протокола MAPI проверяет реестра Windows для хранилищ, которые следует индексации для поиска.</span><span class="sxs-lookup"><span data-stu-id="d241a-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="d241a-109">Поставщики хранилища, чтобы быть индексированы должна быть зарегистрирована в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="d241a-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="d241a-110">По умолчанию Windows Desktop Search добавляет следующие четыре типа поставщиков хранилища реестра Windows, чтобы разрешить индексирования:</span><span class="sxs-lookup"><span data-stu-id="d241a-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="d241a-111">Хранилище для файлов личных папок (. PST-ФАЙЛОВ).</span><span class="sxs-lookup"><span data-stu-id="d241a-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="d241a-112">Хранилище Microsoft Exchange, включая файлы автономной папки (OST-файлы).</span><span class="sxs-lookup"><span data-stu-id="d241a-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="d241a-113">Хранилище для общих папок.</span><span class="sxs-lookup"><span data-stu-id="d241a-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="d241a-114">Хранилище для Microsoft Office Outlook Connector для MSN.</span><span class="sxs-lookup"><span data-stu-id="d241a-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="d241a-115">Поставщики хранилища сторонних производителей, которые нужно индексировать необходимо регистрируются в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="d241a-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d241a-116">Администраторов и пользователей можно использовать параметр групповой политики, чтобы предотвратить индексирование элементов Outlook Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="d241a-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="d241a-117">Для получения дополнительных сведений см [Расширение Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d241a-117">For more information, see [Extending Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="d241a-118">Разделы реестра</span><span class="sxs-lookup"><span data-stu-id="d241a-118">Registry Keys</span></span>

<span data-ttu-id="d241a-119">На компьютере все поставщики хранилища, которые нужно индексировать должна быть зарегистрирована в разделе только один из следующих трех разделов реестра в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="d241a-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="d241a-120">Обработчик протокола MAPI выглядит в разделе каждого из этих параметров в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d241a-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="d241a-121">\Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="d241a-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="d241a-122">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="d241a-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="d241a-123">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]</span><span class="sxs-lookup"><span data-stu-id="d241a-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="d241a-124">Каждое значение в разделе соответствует поставщик хранилища, будут индексированы.</span><span class="sxs-lookup"><span data-stu-id="d241a-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="d241a-125">Имя значения — это глобальный уникальный идентификатор (GUID) поставщика хранилища, который типа **DWORD** и его шестнадцатеричное значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d241a-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="d241a-126">Идентификаторы GUID для поставщиков хранилища</span><span class="sxs-lookup"><span data-stu-id="d241a-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="d241a-127">Свойство MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** указывает идентификатор GUID для хранилища MAPI.</span><span class="sxs-lookup"><span data-stu-id="d241a-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="d241a-128">Идентификаторы GUID для поставщиков хранилища, что Outlook индексы описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d241a-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="d241a-129">**Тип поставщика хранилища**</span><span class="sxs-lookup"><span data-stu-id="d241a-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="d241a-130">**ИДЕНТИФИКАТОР GUID**</span><span class="sxs-lookup"><span data-stu-id="d241a-130">**GUID**</span></span> <br/> |<span data-ttu-id="d241a-131">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="d241a-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="d241a-132">Файлы личных папок (. PST-ФАЙЛОВ)</span><span class="sxs-lookup"><span data-stu-id="d241a-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="d241a-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="d241a-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="d241a-134">Идентификатор GUID описана в mspst.h общедоступных заголовок файл как **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="d241a-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="d241a-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="d241a-135">Exchange</span></span>  <br/> |<span data-ttu-id="d241a-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="d241a-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="d241a-137">Идентификатор GUID описана в edkmdb.h общедоступных заголовок файл как **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="d241a-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="d241a-138">Общедоступные папки</span><span class="sxs-lookup"><span data-stu-id="d241a-138">Public folders</span></span>  <br/> |<span data-ttu-id="d241a-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="d241a-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="d241a-140">Идентификатор GUID описана в edkmdb.h общедоступных заголовок файл как **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="d241a-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="d241a-141">Outlook Connector для MSN</span><span class="sxs-lookup"><span data-stu-id="d241a-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="d241a-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="d241a-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="d241a-143">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="d241a-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d241a-144">См. также</span><span class="sxs-lookup"><span data-stu-id="d241a-144">See also</span></span>



[<span data-ttu-id="d241a-145">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="d241a-145">About the Store API</span></span>](about-the-store-api.md)

