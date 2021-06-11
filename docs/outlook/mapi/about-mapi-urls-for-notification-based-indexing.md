---
title: О URL-адресах MAPI для Notification-Based индексации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422483"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a><span data-ttu-id="b50aa-103">О URL-адресах MAPI для Notification-Based индексации</span><span class="sxs-lookup"><span data-stu-id="b50aa-103">About MAPI URLs for Notification-Based Indexing</span></span>

<span data-ttu-id="b50aa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b50aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b50aa-105">Если поставщик магазина сообщает индексатору, что объект готов к индексации, он создает URL-адрес MAPI, который однозначно идентифицирует объект с обработщиком протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="b50aa-105">When a store provider notifies an indexer that an object is ready for indexing, it generates a MAPI URL that uniquely identifies the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="b50aa-106">URL-адреса MAPI кодируются в Unicode и имеют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="b50aa-106">MAPI URLs are encoded in Unicode, and have the following format:</span></span> 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

<span data-ttu-id="b50aa-107">В следующей таблице описываются различные части типичного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b50aa-107">The following table describes the various parts of a typical URL.</span></span>

|<span data-ttu-id="b50aa-108">Part</span><span class="sxs-lookup"><span data-stu-id="b50aa-108">Part</span></span> | <span data-ttu-id="b50aa-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b50aa-109">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="b50aa-110">*SID*</span><span class="sxs-lookup"><span data-stu-id="b50aa-110">*SID*</span></span> |<span data-ttu-id="b50aa-111">Идентификатор безопасности текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b50aa-111">The current user's security identifier.</span></span>| 
|<span data-ttu-id="b50aa-112">*StoreDisplayName*</span><span class="sxs-lookup"><span data-stu-id="b50aa-112">*StoreDisplayName*</span></span> |<span data-ttu-id="b50aa-113">Строка, которая указывает имя отображения пользователя в этом магазине.</span><span class="sxs-lookup"><span data-stu-id="b50aa-113">A string that specifies the display name of the user on that store.</span></span>|
|<span data-ttu-id="b50aa-114">*HashNumber*</span><span class="sxs-lookup"><span data-stu-id="b50aa-114">*HashNumber*</span></span> |<span data-ttu-id="b50aa-115">DWORD **в** hexadecimal представлении, которое рассчитывается на основе ID записи магазина или подписи сопоставления магазина.</span><span class="sxs-lookup"><span data-stu-id="b50aa-115">A **DWORD** in hexadecimal representation that is calculated based on the store entry ID or the store mapping signature.</span></span> <span data-ttu-id="b50aa-116">Это значение хранится в реестре и будет использоваться позже для идентификации магазина в обработнике протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="b50aa-116">This value is stored in the registry and will be used later to identify the store in the MAPI Protocol Handler.</span></span><br/><br/><span data-ttu-id="b50aa-117">Это число должно быть рассчитано таким образом, чтобы минимизировать столкновения с другими хранилищами.</span><span class="sxs-lookup"><span data-stu-id="b50aa-117">This number must be calculated in a way that minimizes collisions with other stores.</span></span> <span data-ttu-id="b50aa-118">Для алгоритма, Outlook для вычисления номера hash, см. в записи [Algorithm to Calculate the Store Hash Number.](algorithm-to-calculate-the-store-hash-number.md)</span><span class="sxs-lookup"><span data-stu-id="b50aa-118">For the algorithm that Microsoft Outlook uses to calculate the hash number, see [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).</span></span>|
|<span data-ttu-id="b50aa-119">*StoreType*</span><span class="sxs-lookup"><span data-stu-id="b50aa-119">*StoreType*</span></span> |<span data-ttu-id="b50aa-120">Номер, который идентифицирует тип магазина, который содержит объект, который будет индексироваться.</span><span class="sxs-lookup"><span data-stu-id="b50aa-120">A number that identifies the type of the store that contains the object to be indexed.</span></span> <span data-ttu-id="b50aa-121">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b50aa-121">The possible values are as follows:</span></span><br/><span data-ttu-id="b50aa-122">- 0 - Хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b50aa-122">- 0 - Default store.</span></span><br/><br/><span data-ttu-id="b50aa-123">- 1 - Хранилище Делегирования, используемого для элементов делегирования, кэшированных локально.</span><span class="sxs-lookup"><span data-stu-id="b50aa-123">- 1 - Delegate store, used for delegate items cached locally.</span></span><br/><br/><span data-ttu-id="b50aa-124">- 2 — общедоступные папки, используемые для избранных общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="b50aa-124">- 2 - Public folders, used for public folder favorites.</span></span><br/><br/><span data-ttu-id="b50aa-125">**ПРИМЕЧАНИЕ.** Если в магазине вместо нажатого обхода используется символ *X.*</span><span class="sxs-lookup"><span data-stu-id="b50aa-125">**NOTE**: If the store is being crawled instead of pushed, the value that is used is the character *X*.</span></span>| 
|<span data-ttu-id="b50aa-126">*FolderNameA/.../FolderNameN*</span><span class="sxs-lookup"><span data-stu-id="b50aa-126">*FolderNameA/…/FolderNameN*</span></span> |<span data-ttu-id="b50aa-127">Путь от корневого IPM_SUBTREE к папке или сообщению.</span><span class="sxs-lookup"><span data-stu-id="b50aa-127">The path from the root of the IPM_SUBTREE to the folder or message.</span></span> <span data-ttu-id="b50aa-128">Например, сообщение в папке **Family** в папке **"Входящие"** имеет для этого параметра папку **"Входящие" и** "Семейство".</span><span class="sxs-lookup"><span data-stu-id="b50aa-128">For example, a message in the **Family** folder under **Inbox** has **Inbox/Family** for this parameter.</span></span> |
|<span data-ttu-id="b50aa-129">*EntryIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="b50aa-129">*EntryIDEncoded*</span></span> |<span data-ttu-id="b50aa-130">Код входа MAPI для элемента, закодированного как строка Юникод.</span><span class="sxs-lookup"><span data-stu-id="b50aa-130">MAPI entry ID for the item encoded as a Unicode string.</span></span> <span data-ttu-id="b50aa-131">Сведения о том, как кодируются определенные специальные символы, см. в следующем разделе "Специальные символы".</span><span class="sxs-lookup"><span data-stu-id="b50aa-131">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="b50aa-132">Дополнительные сведения об алгоритме кодирования ID записи см. в приложении [Algorithm to Encode Entry IDs and Attachment IDs.](algorithm-to-encode-entry-ids-and-attachment-ids.md)</span><span class="sxs-lookup"><span data-stu-id="b50aa-132">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="b50aa-133">**ПРИМЕЧАНИЕ.** При просмотре в виде текста этот кодированный код записи отображается как случайные символы или поля Hangul в соответствии с алгоритмом в зависимости от доступных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="b50aa-133">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span>  |
|<span data-ttu-id="b50aa-134">*AttachIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="b50aa-134">*AttachIDEncoded*</span></span> |<span data-ttu-id="b50aa-135">Код вложения, закодированный как строка Unicode.</span><span class="sxs-lookup"><span data-stu-id="b50aa-135">Attachment ID encoded as a Unicode string.</span></span> <span data-ttu-id="b50aa-136">Сведения о том, как кодируются определенные специальные символы, см. в следующем разделе "Специальные символы".</span><span class="sxs-lookup"><span data-stu-id="b50aa-136">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="b50aa-137">Дополнительные сведения об алгоритме кодирования ID записи см. в приложении [Algorithm to Encode Entry IDs and Attachment IDs.](algorithm-to-encode-entry-ids-and-attachment-ids.md)</span><span class="sxs-lookup"><span data-stu-id="b50aa-137">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="b50aa-138">**ПРИМЕЧАНИЕ.** При просмотре в виде текста этот кодированный код записи отображается как случайные символы или поля Hangul в соответствии с алгоритмом в зависимости от доступных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="b50aa-138">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span> |
|<span data-ttu-id="b50aa-139">*FileName*</span><span class="sxs-lookup"><span data-stu-id="b50aa-139">*FileName*</span></span> |<span data-ttu-id="b50aa-140">Имя файла вложения, как оно отображается в сообщении.</span><span class="sxs-lookup"><span data-stu-id="b50aa-140">Name of the attachment file, as it appears in the message.</span></span>|
    
## <a name="examples-of-mapi-urls"></a><span data-ttu-id="b50aa-141">Примеры URL-адресов MAPI</span><span class="sxs-lookup"><span data-stu-id="b50aa-141">Examples of MAPI URLs</span></span>

<span data-ttu-id="b50aa-142">Ниже приводится несколько примеров URL-адресов MAPI.</span><span class="sxs-lookup"><span data-stu-id="b50aa-142">The following are some examples of MAPI URLs.</span></span>
  
- <span data-ttu-id="b50aa-143">URL-адрес MAPI для папки:</span><span class="sxs-lookup"><span data-stu-id="b50aa-143">MAPI URL for a folder:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- <span data-ttu-id="b50aa-144">URL-адрес MAPI для сообщения:</span><span class="sxs-lookup"><span data-stu-id="b50aa-144">MAPI URL for a message:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- <span data-ttu-id="b50aa-145">URL-адрес MAPI для вложения:</span><span class="sxs-lookup"><span data-stu-id="b50aa-145">MAPI URL for an attachment:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a><span data-ttu-id="b50aa-146">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="b50aa-146">Special characters</span></span>

<span data-ttu-id="b50aa-147">Определенные символы кодируются, если они отображаются в сообщении или вложении.</span><span class="sxs-lookup"><span data-stu-id="b50aa-147">Certain characters are encoded if they appear in the message or attachment.</span></span> <span data-ttu-id="b50aa-148">Ниже показано, какие символы закодированы в URL-адресе MAPI:</span><span class="sxs-lookup"><span data-stu-id="b50aa-148">The following shows which characters are encoded in a MAPI URL:</span></span>
  
- <span data-ttu-id="b50aa-149">% > %25</span><span class="sxs-lookup"><span data-stu-id="b50aa-149">% > %25</span></span>
    
- <span data-ttu-id="b50aa-150">/ > %2F</span><span class="sxs-lookup"><span data-stu-id="b50aa-150">/ > %2F</span></span> 
    
- <span data-ttu-id="b50aa-151">\ > %5C</span><span class="sxs-lookup"><span data-stu-id="b50aa-151">\ > %5C</span></span> 
    
- <span data-ttu-id="b50aa-152">\* > %2A</span><span class="sxs-lookup"><span data-stu-id="b50aa-152">\* > %2A</span></span> 
    
- <span data-ttu-id="b50aa-153">?</span><span class="sxs-lookup"><span data-stu-id="b50aa-153">?</span></span> <span data-ttu-id="b50aa-154">> %3F</span><span class="sxs-lookup"><span data-stu-id="b50aa-154">> %3F</span></span> 
    
## <a name="blob-associated-with-each-mapi-url"></a><span data-ttu-id="b50aa-155">Blob, связанный с каждым URL-адресом MAPI</span><span class="sxs-lookup"><span data-stu-id="b50aa-155">Blob associated with each MAPI URL</span></span>

<span data-ttu-id="b50aa-156">При нажатии URL-адреса MAPI для объекта, который будет индексироваться, поставщик магазинов также создает двоичный большой объект (BLOB), содержащий определенные сведения для обработчицы протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="b50aa-156">When pushing a MAPI URL for an object to be indexed, a store provider also creates a binary large object (BLOB) that contains certain information for the MAPI Protocol Handler.</span></span> <span data-ttu-id="b50aa-157">Поставщик магазина связывает этот BLOB с каждым URL-адресом MAPI и отправляет его при нажатии URL-адреса MAPI на индексер.</span><span class="sxs-lookup"><span data-stu-id="b50aa-157">The store provider associates this BLOB with each MAPI URL and sends it when pushing the MAPI URL to the indexer.</span></span> <span data-ttu-id="b50aa-158">Формат BLOB следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b50aa-158">The format of the BLOB is as follows:</span></span> 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

<span data-ttu-id="b50aa-159">Поставщик магазина должен записать эти значения в BLOB в показанном порядке.</span><span class="sxs-lookup"><span data-stu-id="b50aa-159">The store provider must write these values to the BLOB in the order shown.</span></span> <span data-ttu-id="b50aa-160">В следующей таблице описывается каждое поле BLOB.</span><span class="sxs-lookup"><span data-stu-id="b50aa-160">The following table describes each field of the BLOB.</span></span>

|<span data-ttu-id="b50aa-161">Part</span><span class="sxs-lookup"><span data-stu-id="b50aa-161">Part</span></span> | <span data-ttu-id="b50aa-162">Описание</span><span class="sxs-lookup"><span data-stu-id="b50aa-162">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="b50aa-163">*dwVersion*</span><span class="sxs-lookup"><span data-stu-id="b50aa-163">*dwVersion*</span></span> |<span data-ttu-id="b50aa-164">Это версия отосланных данных.</span><span class="sxs-lookup"><span data-stu-id="b50aa-164">This is the version of the data being sent.</span></span> <span data-ttu-id="b50aa-165">В настоящее время это значение 1.</span><span class="sxs-lookup"><span data-stu-id="b50aa-165">Currently this value is 1.</span></span>|
|<span data-ttu-id="b50aa-166">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b50aa-166">*dwFlags*</span></span> |<span data-ttu-id="b50aa-167">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="b50aa-167">Reserved for future use.</span></span> <span data-ttu-id="b50aa-168">В настоящее время это значение должно быть 0.</span><span class="sxs-lookup"><span data-stu-id="b50aa-168">Currently this value should be 0.</span></span>|
|<span data-ttu-id="b50aa-169">*cbProfileName*</span><span class="sxs-lookup"><span data-stu-id="b50aa-169">*cbProfileName*</span></span> |<span data-ttu-id="b50aa-170">Размер имени профиля в bytes.</span><span class="sxs-lookup"><span data-stu-id="b50aa-170">The size of the profile name, in bytes.</span></span> <span data-ttu-id="b50aa-171">Эта информация полезна обработчиве протокола MAPI, чтобы узнать, какой профиль использовать при индексации элемента.</span><span class="sxs-lookup"><span data-stu-id="b50aa-171">This information is useful for the MAPI Protocol Handler to know which profile to use when indexing the item.</span></span>|
|<span data-ttu-id="b50aa-172">*wszProfileName*</span><span class="sxs-lookup"><span data-stu-id="b50aa-172">*wszProfileName*</span></span> |<span data-ttu-id="b50aa-173">Null-terminated Unicode string that contains the profile name.</span><span class="sxs-lookup"><span data-stu-id="b50aa-173">Null-terminated Unicode string that contains the profile name.</span></span>|
|<span data-ttu-id="b50aa-174">*cbProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="b50aa-174">*cbProviderItemID*</span></span> |<span data-ttu-id="b50aa-175">Размер ID элемента поставщика в bytes.</span><span class="sxs-lookup"><span data-stu-id="b50aa-175">Size of the provider item ID, in bytes.</span></span> <span data-ttu-id="b50aa-176">Поставщик магазина должен отправлять только ID элемента поставщика для папок, чтобы предотвратить открытие дополнительных папок для получения этой информации.</span><span class="sxs-lookup"><span data-stu-id="b50aa-176">The store provider should send only the provider item ID for folders, to prevent opening additional folders to get this information.</span></span>|
|<span data-ttu-id="b50aa-177">*wszProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="b50aa-177">*wszProviderItemID*</span></span> |<span data-ttu-id="b50aa-178">Null-terminated Unicode string with the provider item ID that uniquely identifies the item in the store.</span><span class="sxs-lookup"><span data-stu-id="b50aa-178">Null-terminated Unicode string with the provider item ID that uniquely identifies the item in the store.</span></span>|
    
## <a name="see-also"></a><span data-ttu-id="b50aa-179">См. также</span><span class="sxs-lookup"><span data-stu-id="b50aa-179">See also</span></span>

- [<span data-ttu-id="b50aa-180">Индексация Notification-Based магазина</span><span class="sxs-lookup"><span data-stu-id="b50aa-180">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="b50aa-181">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b50aa-181">MAPI Constants</span></span>](mapi-constants.md)

