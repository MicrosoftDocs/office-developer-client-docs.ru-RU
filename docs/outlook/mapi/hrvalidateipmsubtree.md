---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436575"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="1a188-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="1a188-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="1a188-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a188-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a188-105">Добавляет папки стандартных сообщений взаимоконтактных сообщений (IPM) в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a188-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a188-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1a188-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a188-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="1a188-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1a188-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1a188-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a188-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1a188-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1a188-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1a188-110">Called by:</span></span>  <br/> |<span data-ttu-id="1a188-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="1a188-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="1a188-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a188-112">Parameters</span></span>

 <span data-ttu-id="1a188-113">_Лпмдб_</span><span class="sxs-lookup"><span data-stu-id="1a188-113">_lpMDB_</span></span>
  
> <span data-ttu-id="1a188-114">возврата Указатель на объект хранилища сообщений, в который добавляются папки.</span><span class="sxs-lookup"><span data-stu-id="1a188-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="1a188-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a188-115">_ulFlags_</span></span>
  
> <span data-ttu-id="1a188-116">возврата Битовая маска флагов, используемых для управления созданием папок.</span><span class="sxs-lookup"><span data-stu-id="1a188-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="1a188-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1a188-117">The following flags can be set:</span></span>
    
<span data-ttu-id="1a188-118">МАПИ_ФОРЦЕ_КРЕАТЕ</span><span class="sxs-lookup"><span data-stu-id="1a188-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="1a188-119">Папки следует проверить перед созданием, даже если свойства хранилища сообщений указывают, что они действительны.</span><span class="sxs-lookup"><span data-stu-id="1a188-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="1a188-120">Клиентское приложение обычно устанавливает этот флаг, если ошибка указывает на то, что структура существующей папки повреждена.</span><span class="sxs-lookup"><span data-stu-id="1a188-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="1a188-121">МАПИ_ФУЛЛ_ИПМ_ТРИ</span><span class="sxs-lookup"><span data-stu-id="1a188-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="1a188-122">Полный набор папок IPM должен быть создан в корневой папке хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a188-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="1a188-123">Названия папок в иерархии:</span><span class="sxs-lookup"><span data-stu-id="1a188-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="1a188-124">Представления папок</span><span class="sxs-lookup"><span data-stu-id="1a188-124">Folder Views</span></span>
    
    - <span data-ttu-id="1a188-125">Общие представления</span><span class="sxs-lookup"><span data-stu-id="1a188-125">Common Views</span></span>
    
    - <span data-ttu-id="1a188-126">Корень поиска\*</span><span class="sxs-lookup"><span data-stu-id="1a188-126">Search Root\*</span></span>
    
    - <span data-ttu-id="1a188-127">Поддерево IPM\*</span><span class="sxs-lookup"><span data-stu-id="1a188-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="1a188-128">Inbox;</span><span class="sxs-lookup"><span data-stu-id="1a188-128">Inbox</span></span>
    
    - <span data-ttu-id="1a188-129">Исходящие</span><span class="sxs-lookup"><span data-stu-id="1a188-129">Outbox</span></span>
    
    - <span data-ttu-id="1a188-130">Удаленные элементы\*</span><span class="sxs-lookup"><span data-stu-id="1a188-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="1a188-131">Отправленные</span><span class="sxs-lookup"><span data-stu-id="1a188-131">Sent Items</span></span>
    
    <span data-ttu-id="1a188-132">где три папки с \* пометкой — это минимальный набор, созданный даже в том случае, если не ЗАДАН флаг мапи_фулл_ипм_три.</span><span class="sxs-lookup"><span data-stu-id="1a188-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="1a188-133">Клиентское приложение обычно устанавливает этот флаг, когда хранилище сообщений, в котором будут создаваться папки, является хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a188-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="1a188-134">_Лпквалуес_</span><span class="sxs-lookup"><span data-stu-id="1a188-134">_lpcValues_</span></span>
  
> <span data-ttu-id="1a188-135">[вход, выход] Указатель на число структур [спропвалуе](spropvalue.md) в массиве, возвращаемом параметром _лпппропс_ .</span><span class="sxs-lookup"><span data-stu-id="1a188-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="1a188-136">Если _лпппропс_ имеет значение null, значение параметра _лпквалуес_ может быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1a188-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="1a188-137">_Лпппропс_</span><span class="sxs-lookup"><span data-stu-id="1a188-137">_lppProps_</span></span>
  
> <span data-ttu-id="1a188-138">[вход, выход] Указатель на указатель на массив структур **спропвалуе** , который содержит значения свойств для свойства **пр_валид_фолдер_маск** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)), а также для свойств соответствующего идентификатора записи папки.</span><span class="sxs-lookup"><span data-stu-id="1a188-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="1a188-139">Если **хрвалидатеипмсубтри** создает папку "Входящие" в хранилище сообщений, массив **спропвалуе** содержит идентификатор записи "Входящие" с особым тегом свойства, `PROP_TAG(PT_BINARY, PROP_ID_NULL)`закодированным как.</span><span class="sxs-lookup"><span data-stu-id="1a188-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="1a188-140">Параметр _лпппропс_ может иметь значение null, что указывает на то, что для вызывающей реализации не требуется возвратить массив **спропвалуе** .</span><span class="sxs-lookup"><span data-stu-id="1a188-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="1a188-141">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="1a188-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="1a188-142">вышли Указатель на указатель на структуру [мапиеррор](mapierror.md) , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="1a188-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="1a188-143">Параметр _лппмапиеррор_ имеет значение null, если структура **мапиеррор** не возвращается.</span><span class="sxs-lookup"><span data-stu-id="1a188-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a188-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a188-144">Return value</span></span>

<span data-ttu-id="1a188-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="1a188-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a188-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a188-146">Remarks</span></span>

<span data-ttu-id="1a188-147">MAPI использует функцию **хрвалидатеипмсубтри** для внутренних целей, чтобы построить стандартное поддерево IPM в хранилище сообщений при первом открытии хранилища, или когда хранилище по умолчанию создано.</span><span class="sxs-lookup"><span data-stu-id="1a188-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="1a188-148">Эта функция также может использоваться клиентскими приложениями для проверки или исправления стандартных папок сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a188-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="1a188-149">**Хрвалидатеипмсубтри** всегда создает папки корневОй папки поиска и поддерева IPM в корневой папке хранилища и в папке "Удаленные" в папке "ПОДдерево IPM".</span><span class="sxs-lookup"><span data-stu-id="1a188-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="1a188-150">Папка поддерева IPM является корневым каталогом иерархии IPM в этом хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a188-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="1a188-151">Корневую папку поиска можно использовать в качестве корня поддерева для папок результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="1a188-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="1a188-152">Клиенты IPM должны отображать свое представление папки, начиная с корневой папки поддерева IPM и отображая вложенные папки под ним.</span><span class="sxs-lookup"><span data-stu-id="1a188-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="1a188-153">Сведения в корневой папке хранилища сообщений не должны отображаться в пользовательском интерфейсе клиента.</span><span class="sxs-lookup"><span data-stu-id="1a188-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="1a188-154">Эта функция означает, что если клиент должен скрыть сведения, эти сведения можно поместить в корневой каталог дерева IPM, где они не видны пользователю.</span><span class="sxs-lookup"><span data-stu-id="1a188-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="1a188-155">В отличие от приложений, не связанных с IPM, которые требуют, чтобы сообщения и папки были невидимы для пользователя, например в серверном хранилище сообщений, их можно поместить вне иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="1a188-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="1a188-156">**Хрвалидатеипмсубтри** задает свойство **пр_валид_фолдер_маск** , которое указывает, содержит ли создаваемая папка IPM допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="1a188-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="1a188-157">Следующие свойства идентификатора записи в хранилище сообщений задаются идентификаторами записей соответствующих папок и возвращаются в параметре _лпппропс_ вместе с **пр_валид_фолдер_маск**:</span><span class="sxs-lookup"><span data-stu-id="1a188-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="1a188-158">**Пр_коммон_виевс_ентрид** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-159">**Пр_финдер_ентрид** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-160">**Пр_ипм_аутбокс_ентрид** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-161">**Пр_ипм_сентмаил_ентрид** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-162">**Пр_ипм_субтри_ентрид** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-163">**Пр_ипм_вастебаскет_ентрид** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-164">**Пр_виевс_ентрид** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a188-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1a188-165">Заполнитель [проп_таг](prop_tag.md) для папки "Входящие" IPM (ПТ_БИНАРИ, проп_ид_нулл).</span><span class="sxs-lookup"><span data-stu-id="1a188-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1a188-166">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1a188-166">MFCMAPI reference</span></span>

<span data-ttu-id="1a188-167">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1a188-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1a188-168">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1a188-168">**File**</span></span>|<span data-ttu-id="1a188-169">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1a188-169">**Function**</span></span>|<span data-ttu-id="1a188-170">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1a188-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a188-171">Мстсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="1a188-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="1a188-172">Кмсгсторедлг:: Онвалидатеипмсубтри</span><span class="sxs-lookup"><span data-stu-id="1a188-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="1a188-173">MFCMAPI использует метод **хрвалидатеипмсубтри** для добавления стандартных папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a188-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a188-174">См. также</span><span class="sxs-lookup"><span data-stu-id="1a188-174">See also</span></span>



[<span data-ttu-id="1a188-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1a188-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="1a188-176">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1a188-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

