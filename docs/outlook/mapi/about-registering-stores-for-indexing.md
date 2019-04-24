---
title: Сведения о регистрации хранилищ для индексирования
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
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="e4c1d-103">Сведения о регистрации хранилищ для индексирования</span><span class="sxs-lookup"><span data-stu-id="e4c1d-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="e4c1d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4c1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4c1d-105">Эта статья относится к мгновенному поиску в Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="e4c1d-106">Мгновенный поиск позволяет быстро находить элементы в Outlook.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="e4c1d-107">Он использует компоненты панели поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="e4c1d-108">Обработчик протокола MAPI проверяет реестр Windows для хранения, который он должен индексировать для целей поиска.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="e4c1d-109">Поставщики хранилища, которые требуется индексировать, должны быть зарегистрированы в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="e4c1d-110">По умолчанию служба поиска на рабочем столе Windows добавляет следующие четыре типа поставщиков услуг хранения в реестр Windows, чтобы разрешить индексирование:</span><span class="sxs-lookup"><span data-stu-id="e4c1d-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="e4c1d-111">Хранение файлов личных папок (. PST).</span><span class="sxs-lookup"><span data-stu-id="e4c1d-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="e4c1d-112">Хранилище Microsoft Exchange, в том числе файлы автономных папок (OST).</span><span class="sxs-lookup"><span data-stu-id="e4c1d-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="e4c1d-113">Хранить для общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="e4c1d-114">Магазин для Microsoft Office Outlook Connector для MSN.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="e4c1d-115">Сторонние поставщики услуг хранения, которые необходимо индексировать, должны регистрироваться в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e4c1d-116">Администраторы и пользователи могут использовать параметр групповой политики, чтобы запретить индексирование элементов Outlook для поиска на рабочем столе Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="e4c1d-117">Дополнительные сведения см в разделе [расширение панели поиска Windows](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4c1d-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="e4c1d-118">Разделы реестра</span><span class="sxs-lookup"><span data-stu-id="e4c1d-118">Registry Keys</span></span>

<span data-ttu-id="e4c1d-119">На компьютере все поставщики магазинов, которые требуется индексировать, должны быть зарегистрированы только в одном из следующих разделов реестра в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="e4c1d-120">Обработчик протокола MAPI выполняет поиск в каждом из этих разделов в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="e4c1d-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="e4c1d-121">[HKLM] \Софтваре\полиЦиес\микрософт\виндовс\виндовс Поиск \\</span><span class="sxs-lookup"><span data-stu-id="e4c1d-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="e4c1d-122">[HKLM] \Софтваре\микрософт\виндовс\виндовс Сеарч\преференцес\\</span><span class="sxs-lookup"><span data-stu-id="e4c1d-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="e4c1d-123">[HKCU] \Софтваре\микрософт\виндовс\виндовс Сеарч\преференцес\\</span><span class="sxs-lookup"><span data-stu-id="e4c1d-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="e4c1d-124">Каждое значение в ключе соответствует поставщику услуг хранения, который будет индексироваться.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="e4c1d-125">Имя значения — это глобальный уникальный идентификатор (GUID) поставщика хранилища, имеющий тип **DWORD** и шестнадцатеричное значение 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="e4c1d-126">ИДЕНТИФИКАТОРы GUID для поставщиков услуг хранения</span><span class="sxs-lookup"><span data-stu-id="e4c1d-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="e4c1d-127">Свойство MAPI **[пр_мдб_провидер](pidtagstoreprovider-canonical-property.md)** указывает идентификатор GUID хранилища MAPI.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="e4c1d-128">В приведенной ниже таблице описаны ИДЕНТИФИКАТОРы GUID для поставщиков услуг хранения, для которых используются индексы Outlook.</span><span class="sxs-lookup"><span data-stu-id="e4c1d-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="e4c1d-129">**Тип поставщика услуг хранения**</span><span class="sxs-lookup"><span data-stu-id="e4c1d-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="e4c1d-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e4c1d-130">**GUID**</span></span> <br/> |<span data-ttu-id="e4c1d-131">**Notes**</span><span class="sxs-lookup"><span data-stu-id="e4c1d-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="e4c1d-132">Файлы личных папок (. ФОРМАТА</span><span class="sxs-lookup"><span data-stu-id="e4c1d-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="e4c1d-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="e4c1d-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="e4c1d-134">GUID задокументирован в файле общедоступных заголовков мспст. h как **мспст_уид_провидер**</span><span class="sxs-lookup"><span data-stu-id="e4c1d-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="e4c1d-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="e4c1d-135">Exchange</span></span>  <br/> |<span data-ttu-id="e4c1d-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="e4c1d-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="e4c1d-137">GUID задокументирован в файле общедоступных заголовков едкмдб. h как **пбексчанжепровидерпримарюсергуид**</span><span class="sxs-lookup"><span data-stu-id="e4c1d-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="e4c1d-138">Общедоступные папки</span><span class="sxs-lookup"><span data-stu-id="e4c1d-138">Public folders</span></span>  <br/> |<span data-ttu-id="e4c1d-139">{70fab278-f7af-CD11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="e4c1d-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="e4c1d-140">GUID задокументирован в файле общедоступных заголовков едкмдб. h как **пбексчанжепровидерпубликгуид**</span><span class="sxs-lookup"><span data-stu-id="e4c1d-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="e4c1d-141">Соединитель Outlook Connector для MSN</span><span class="sxs-lookup"><span data-stu-id="e4c1d-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="e4c1d-142">{c34f5c97-EB05-bb4b-B199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="e4c1d-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="e4c1d-143">Нет</span><span class="sxs-lookup"><span data-stu-id="e4c1d-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4c1d-144">См. также</span><span class="sxs-lookup"><span data-stu-id="e4c1d-144">See also</span></span>



[<span data-ttu-id="e4c1d-145">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="e4c1d-145">About the Store API</span></span>](about-the-store-api.md)

