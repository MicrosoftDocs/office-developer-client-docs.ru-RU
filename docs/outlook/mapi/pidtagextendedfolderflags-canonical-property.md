---
title: Каноническое свойство PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 23c43586157806c603ad7fd8c146270a9d71170a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563788"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="c686e-103">Каноническое свойство PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="c686e-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="c686e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c686e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c686e-105">Содержит расширенные флаги о папке.</span><span class="sxs-lookup"><span data-stu-id="c686e-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c686e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c686e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c686e-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c686e-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c686e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c686e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c686e-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="c686e-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="c686e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c686e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c686e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c686e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c686e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c686e-112">Area:</span></span>  <br/> |<span data-ttu-id="c686e-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="c686e-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c686e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c686e-114">Remarks</span></span>

<span data-ttu-id="c686e-115">Это свойство соответствует двоичный поток, который содержит зашифрованный вложенные свойства папки.</span><span class="sxs-lookup"><span data-stu-id="c686e-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="c686e-116">В формате задано в формате переменной длины вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="c686e-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="c686e-117">Первые 8 бит элемент sub — это поле ID, который указывает, какие виды флаг представляет элемент sub.</span><span class="sxs-lookup"><span data-stu-id="c686e-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="c686e-118">Второй 8 бит — это число байт данных, выполните.</span><span class="sxs-lookup"><span data-stu-id="c686e-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="c686e-119">Возможные значения ID:</span><span class="sxs-lookup"><span data-stu-id="c686e-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="c686e-120">Invalid</span><span class="sxs-lookup"><span data-stu-id="c686e-120">Invalid</span></span>
    
   <span data-ttu-id="c686e-121">Это значение не используется</span><span class="sxs-lookup"><span data-stu-id="c686e-121">Do not use this value</span></span>
    
- <span data-ttu-id="c686e-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="c686e-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="c686e-123">Данные являются четыре байта в формате:</span><span class="sxs-lookup"><span data-stu-id="c686e-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="c686e-124">**Бит**</span><span class="sxs-lookup"><span data-stu-id="c686e-124">**Bits**</span></span>|<span data-ttu-id="c686e-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c686e-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="c686e-126">0-1</span><span class="sxs-lookup"><span data-stu-id="c686e-126">0-1</span></span>  <br/> |<span data-ttu-id="c686e-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c686e-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="c686e-128">2</span><span class="sxs-lookup"><span data-stu-id="c686e-128">2</span></span>  <br/> |<span data-ttu-id="c686e-129">Если приложение должно отобразиться описание политики значение 0.</span><span class="sxs-lookup"><span data-stu-id="c686e-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="c686e-130">3-5</span><span class="sxs-lookup"><span data-stu-id="c686e-130">3-5</span></span>  <br/> |<span data-ttu-id="c686e-131">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c686e-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="c686e-132">6-7</span><span class="sxs-lookup"><span data-stu-id="c686e-132">6-7</span></span>  <br/> |<span data-ttu-id="c686e-133">Определяет отображаемое количество сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="c686e-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="c686e-134">0 — использовать по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c686e-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="c686e-135">1 — используйте количество непрочитанных сообщений</span><span class="sxs-lookup"><span data-stu-id="c686e-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="c686e-136">3 - использовать общее число сообщений</span><span class="sxs-lookup"><span data-stu-id="c686e-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="c686e-137">8-31</span><span class="sxs-lookup"><span data-stu-id="c686e-137">8-31</span></span>  <br/> |<span data-ttu-id="c686e-138">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c686e-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="c686e-139">Зарезервированные элементов можно пропустить, однако существующие значения, которые необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="c686e-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="c686e-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="c686e-140">SearchFolderID</span></span>
    
   <span data-ttu-id="c686e-141">Поле данных является полем 16-битное.</span><span class="sxs-lookup"><span data-stu-id="c686e-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="c686e-142">Когда приложение создает папку сохраняемого поиска, его необходимо установить это поле в общей папке для совпадает со значением **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) двоичного свойства папки для поиска сообщения.</span><span class="sxs-lookup"><span data-stu-id="c686e-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="c686e-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="c686e-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="c686e-144">Поле 4-байтных является поля данных.</span><span class="sxs-lookup"><span data-stu-id="c686e-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="c686e-145">Когда приложение создает папку Поиск задачи, его необходимо задать значение этого поля в общей папке на прямом целое значение «0x000c0000»:</span><span class="sxs-lookup"><span data-stu-id="c686e-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c686e-146">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c686e-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c686e-147">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c686e-147">Protocol specifications</span></span>

<span data-ttu-id="c686e-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c686e-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c686e-149">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c686e-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c686e-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c686e-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c686e-151">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="c686e-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="c686e-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c686e-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c686e-153">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="c686e-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c686e-154">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c686e-154">Header files</span></span>

<span data-ttu-id="c686e-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c686e-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="c686e-156">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c686e-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="c686e-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c686e-157">Mapitags.h</span></span>
  
> <span data-ttu-id="c686e-158">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c686e-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c686e-159">См. также</span><span class="sxs-lookup"><span data-stu-id="c686e-159">See also</span></span>

- [<span data-ttu-id="c686e-160">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c686e-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="c686e-161">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c686e-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="c686e-162">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c686e-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="c686e-163">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c686e-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

