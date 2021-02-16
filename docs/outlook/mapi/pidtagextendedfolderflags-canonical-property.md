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
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316354"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="683a0-103">Каноническое свойство PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="683a0-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="683a0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="683a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="683a0-105">Содержит расширенные флаги о папке.</span><span class="sxs-lookup"><span data-stu-id="683a0-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="683a0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="683a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="683a0-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="683a0-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="683a0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="683a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="683a0-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="683a0-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="683a0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="683a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="683a0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="683a0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="683a0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="683a0-112">Area:</span></span>  <br/> |<span data-ttu-id="683a0-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="683a0-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="683a0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="683a0-114">Remarks</span></span>

<span data-ttu-id="683a0-115">Это свойство является двоичным потоком, который содержит закодированные вложенные свойства для папки.</span><span class="sxs-lookup"><span data-stu-id="683a0-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="683a0-116">Он отформатирован как ряд подустанавливных элементов переменной длины.</span><span class="sxs-lookup"><span data-stu-id="683a0-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="683a0-117">Первые 8 битов подгруппы — это поле ID, которое указывает, какой тип флага представляет подгруппа.</span><span class="sxs-lookup"><span data-stu-id="683a0-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="683a0-118">Вторые 8 битов — это количество последующих данных.</span><span class="sxs-lookup"><span data-stu-id="683a0-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="683a0-119">Возможные значения ID:</span><span class="sxs-lookup"><span data-stu-id="683a0-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="683a0-120">Invalid</span><span class="sxs-lookup"><span data-stu-id="683a0-120">Invalid</span></span>
    
   <span data-ttu-id="683a0-121">Не используйте это значение</span><span class="sxs-lookup"><span data-stu-id="683a0-121">Do not use this value</span></span>
    
- <span data-ttu-id="683a0-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="683a0-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="683a0-123">Данные отформатированы в формате 4-х битов:</span><span class="sxs-lookup"><span data-stu-id="683a0-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="683a0-124">**Биты**</span><span class="sxs-lookup"><span data-stu-id="683a0-124">**Bits**</span></span>|<span data-ttu-id="683a0-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="683a0-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="683a0-126">0-1</span><span class="sxs-lookup"><span data-stu-id="683a0-126">0-1</span></span>  <br/> |<span data-ttu-id="683a0-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="683a0-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="683a0-128">2 </span><span class="sxs-lookup"><span data-stu-id="683a0-128">2</span></span>  <br/> |<span data-ttu-id="683a0-129">Установите 0, если приложение должно показывать описание политики.</span><span class="sxs-lookup"><span data-stu-id="683a0-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="683a0-130">3-5</span><span class="sxs-lookup"><span data-stu-id="683a0-130">3-5</span></span>  <br/> |<span data-ttu-id="683a0-131">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="683a0-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="683a0-132">6-7</span><span class="sxs-lookup"><span data-stu-id="683a0-132">6-7</span></span>  <br/> |<span data-ttu-id="683a0-133">Управляет отображением количества сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="683a0-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="683a0-134">0 — использование параметра по умолчанию</span><span class="sxs-lookup"><span data-stu-id="683a0-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="683a0-135">1 — использование количества непрочитанные сообщения</span><span class="sxs-lookup"><span data-stu-id="683a0-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="683a0-136">3 . Использование общего количества сообщений</span><span class="sxs-lookup"><span data-stu-id="683a0-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="683a0-137">8-31</span><span class="sxs-lookup"><span data-stu-id="683a0-137">8-31</span></span>  <br/> |<span data-ttu-id="683a0-138">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="683a0-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="683a0-139">Зарезервированные элементы можно игнорировать, но существующие значения необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="683a0-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="683a0-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="683a0-140">SearchFolderID</span></span>
    
   <span data-ttu-id="683a0-141">Поле данных — это 16-byte field.</span><span class="sxs-lookup"><span data-stu-id="683a0-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="683a0-142">Когда приложение создает папку постоянного поиска, оно должно установить для этого поля в папке то же значение, что и двоичное свойство **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)в сообщении папки поиска.</span><span class="sxs-lookup"><span data-stu-id="683a0-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="683a0-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="683a0-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="683a0-144">Поле данных — это 4-byte field.</span><span class="sxs-lookup"><span data-stu-id="683a0-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="683a0-145">Когда приложение создает папку поиска "дела", оно должно установить для этого поля в ней значение, которое будет иметь малое конечное 0x000c0000":</span><span class="sxs-lookup"><span data-stu-id="683a0-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="683a0-146">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="683a0-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="683a0-147">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="683a0-147">Protocol specifications</span></span>

<span data-ttu-id="683a0-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683a0-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683a0-149">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="683a0-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="683a0-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683a0-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683a0-151">Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="683a0-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="683a0-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683a0-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683a0-153">Указывает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="683a0-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="683a0-154">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="683a0-154">Header files</span></span>

<span data-ttu-id="683a0-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="683a0-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="683a0-156">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="683a0-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="683a0-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="683a0-157">Mapitags.h</span></span>
  
> <span data-ttu-id="683a0-158">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="683a0-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="683a0-159">См. также</span><span class="sxs-lookup"><span data-stu-id="683a0-159">See also</span></span>

- [<span data-ttu-id="683a0-160">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="683a0-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="683a0-161">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="683a0-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="683a0-162">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="683a0-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="683a0-163">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="683a0-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

