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
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="f38b6-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f38b6-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="f38b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f38b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f38b6-105">Добавляет стандартные папки межличностных сообщений (IPM) в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f38b6-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f38b6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f38b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="f38b6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f38b6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f38b6-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f38b6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f38b6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f38b6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f38b6-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f38b6-110">Called by:</span></span>  <br/> |<span data-ttu-id="f38b6-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="f38b6-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="f38b6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f38b6-112">Parameters</span></span>

 <span data-ttu-id="f38b6-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="f38b6-113">_lpMDB_</span></span>
  
> <span data-ttu-id="f38b6-114">[in] Указатель на объект хранения сообщений, в который необходимо добавить папки.</span><span class="sxs-lookup"><span data-stu-id="f38b6-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="f38b6-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f38b6-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f38b6-116">[in] Битоваяmas флагов, используемых для управления тем, как создаются папки.</span><span class="sxs-lookup"><span data-stu-id="f38b6-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="f38b6-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f38b6-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f38b6-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="f38b6-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="f38b6-119">Папки должны быть проверены перед созданием, даже если свойства хранения сообщений указывают, что они действительны.</span><span class="sxs-lookup"><span data-stu-id="f38b6-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="f38b6-120">Как правило, клиентские приложения устанавливают этот флаг, если ошибка указывает на то, что структура существующей папки повреждена.</span><span class="sxs-lookup"><span data-stu-id="f38b6-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="f38b6-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="f38b6-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="f38b6-122">Полный набор папок IPM должен быть создан в корневой папке хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="f38b6-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="f38b6-123">В иерархии имеются такие заголовки папок:</span><span class="sxs-lookup"><span data-stu-id="f38b6-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="f38b6-124">Представления папок</span><span class="sxs-lookup"><span data-stu-id="f38b6-124">Folder Views</span></span>
    
    - <span data-ttu-id="f38b6-125">Общие представления</span><span class="sxs-lookup"><span data-stu-id="f38b6-125">Common Views</span></span>
    
    - <span data-ttu-id="f38b6-126">Корень поиска\*</span><span class="sxs-lookup"><span data-stu-id="f38b6-126">Search Root\*</span></span>
    
    - <span data-ttu-id="f38b6-127">Подtree IPM\*</span><span class="sxs-lookup"><span data-stu-id="f38b6-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="f38b6-128">Inbox;</span><span class="sxs-lookup"><span data-stu-id="f38b6-128">Inbox</span></span>
    
    - <span data-ttu-id="f38b6-129">Исходящие</span><span class="sxs-lookup"><span data-stu-id="f38b6-129">Outbox</span></span>
    
    - <span data-ttu-id="f38b6-130">Удаленные элементы\*</span><span class="sxs-lookup"><span data-stu-id="f38b6-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="f38b6-131">Отправленные</span><span class="sxs-lookup"><span data-stu-id="f38b6-131">Sent Items</span></span>
    
    <span data-ttu-id="f38b6-132">где три помеченные папки являются минимальным набором, созданным, даже если MAPI_FULL_IPM_TREE \* флага не установлен.</span><span class="sxs-lookup"><span data-stu-id="f38b6-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="f38b6-133">Как правило, клиентские приложения устанавливают этот флаг, если хранилище сообщений, в котором будут созданы папки, является хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f38b6-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="f38b6-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="f38b6-134">_lpcValues_</span></span>
  
> <span data-ttu-id="f38b6-135">[in, out] Указатель на число структур [SPropValue](spropvalue.md) в массиве, возвращаемом в _параметре lppProps._</span><span class="sxs-lookup"><span data-stu-id="f38b6-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="f38b6-136">Значение параметра  _lpcValues_ может быть нулем, если  _lppProps_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f38b6-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="f38b6-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="f38b6-137">_lppProps_</span></span>
  
> <span data-ttu-id="f38b6-138">[in, out] Указатель на указатель на массив структур **SPropValue,** содержащий значения свойств для **свойства PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)и для соответствующих свойств идентификатора записи папки.</span><span class="sxs-lookup"><span data-stu-id="f38b6-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="f38b6-139">Если **HrValidateIPMSubtree** создает в хранилище сообщений почтовый ящик, массив **SPropValue** включает идентификатор записи "Входящие" со специальным тегом свойства, закодированные как  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` .</span><span class="sxs-lookup"><span data-stu-id="f38b6-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="f38b6-140">Параметр _lppProps_ может иметь параметр NULL, указывающий, что для реализации вызова не требуется возвращать массив **SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="f38b6-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="f38b6-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="f38b6-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="f38b6-142">[out] Указатель на указатель на структуру [MAPIERROR,](mapierror.md) которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="f38b6-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="f38b6-143">Если структура **MAPIERROR** не возвращается, для параметра _lppMAPIError_ задано NULL.</span><span class="sxs-lookup"><span data-stu-id="f38b6-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f38b6-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f38b6-144">Return value</span></span>

<span data-ttu-id="f38b6-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="f38b6-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f38b6-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="f38b6-146">Remarks</span></span>

<span data-ttu-id="f38b6-147">MAPI использует функцию **HrValidateIPMSubtree** внутри компании для создания стандартного поддерева IPM в хранилище сообщений при первом открытие магазина или при его встраии в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f38b6-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="f38b6-148">Эта функция также может использоваться клиентских приложений для проверки или восстановления стандартных папок сообщений.</span><span class="sxs-lookup"><span data-stu-id="f38b6-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="f38b6-149">**HrValidateIPMSubtree** всегда создает папки "Корень поиска" и "Поддерево IPM" в корневой папке магазина, а папка "Удаленные" в папке поддерева IPM.</span><span class="sxs-lookup"><span data-stu-id="f38b6-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="f38b6-150">Папка поддерево IPM является корневым корнем иерархии IPM в этом хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f38b6-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="f38b6-151">Корневую папку поиска можно использовать в качестве корня поддерево для папок результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="f38b6-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="f38b6-152">Клиенты IPM должны отображать представление папки, начиная с корневой папки поддеревого IPM и отображая под ней свои папки.</span><span class="sxs-lookup"><span data-stu-id="f38b6-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="f38b6-153">Сведения в корневой папке хранения сообщений не должны отображаться в пользовательском интерфейсе клиента.</span><span class="sxs-lookup"><span data-stu-id="f38b6-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="f38b6-154">Эта функция означает, что если клиенту необходимо скрыть сведения, эти сведения можно поместить в корневой каталог подстановки IPM, где они не видны пользователю.</span><span class="sxs-lookup"><span data-stu-id="f38b6-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="f38b6-155">С другой стороны, приложения, не вложенные в IPM, которые требуют, чтобы сообщения и папки были невидимыми для пользователя, например в серверном хранилище сообщений, могут поместить их за пределы иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="f38b6-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="f38b6-156">**HrValidateIPMSubtree** задает свойство **PR_VALID_FOLDER_MASK,** чтобы указать, имеет ли каждая создаемая папка IPM допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="f38b6-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="f38b6-157">Следующие свойства идентификатора записи в хранилище сообщений заданы для идентификаторов записей соответствующих папок и возвращаются в _параметре lppProps_ вместе с **PR_VALID_FOLDER_MASK:**</span><span class="sxs-lookup"><span data-stu-id="f38b6-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="f38b6-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId)](pidtagcommonviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f38b6-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f38b6-165">Замещего [PROP_TAG](prop_tag.md) для почтового ящика IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f38b6-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f38b6-166">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f38b6-166">MFCMAPI reference</span></span>

<span data-ttu-id="f38b6-167">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f38b6-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f38b6-168">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f38b6-168">**File**</span></span>|<span data-ttu-id="f38b6-169">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f38b6-169">**Function**</span></span>|<span data-ttu-id="f38b6-170">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f38b6-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f38b6-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f38b6-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f38b6-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f38b6-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="f38b6-173">MFCMAPI использует метод **HrValidateIPMSubtree** для добавления стандартных папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f38b6-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f38b6-174">См. также</span><span class="sxs-lookup"><span data-stu-id="f38b6-174">See also</span></span>



[<span data-ttu-id="f38b6-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f38b6-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="f38b6-176">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f38b6-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

