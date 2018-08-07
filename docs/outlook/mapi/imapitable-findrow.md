---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809209"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="9f40a-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="9f40a-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="9f40a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f40a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f40a-105">Находит следующую строку в таблице, которая соответствует определенным условиям поиска и перемещает курсор в эту строку.</span><span class="sxs-lookup"><span data-stu-id="9f40a-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9f40a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f40a-106">Parameters</span></span>

 <span data-ttu-id="9f40a-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="9f40a-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="9f40a-108">[in] Указатель на структуру [SRestriction](srestriction.md) , описывающий условия поиска.</span><span class="sxs-lookup"><span data-stu-id="9f40a-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="9f40a-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="9f40a-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="9f40a-110">[in] Закладки, идентифицирующий строку, где **FindRow** должна начинать поиск.</span><span class="sxs-lookup"><span data-stu-id="9f40a-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="9f40a-111">Закладки можно создать с помощью метода [IMAPITable::CreateBookmark](imapitable-createbookmark.md) или один из следующих предварительно заданных значений может быть передан.</span><span class="sxs-lookup"><span data-stu-id="9f40a-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="9f40a-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="9f40a-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="9f40a-113">Поиск с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="9f40a-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="9f40a-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="9f40a-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="9f40a-115">Выполняет поиск строки в таблице, в котором находится курсор.</span><span class="sxs-lookup"><span data-stu-id="9f40a-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="9f40a-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="9f40a-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="9f40a-117">Поиск с конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="9f40a-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="9f40a-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f40a-118">_ulFlags_</span></span>
  
> <span data-ttu-id="9f40a-119">[in] Битовая маска флаги, определяющее направление поиска.</span><span class="sxs-lookup"><span data-stu-id="9f40a-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="9f40a-120">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9f40a-120">The following flag can be set:</span></span>
    
<span data-ttu-id="9f40a-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="9f40a-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="9f40a-122">Выполняет поиск строки, закладки.</span><span class="sxs-lookup"><span data-stu-id="9f40a-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f40a-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3">Return value</span></span>

<span data-ttu-id="9f40a-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9f40a-124">S_OK</span></span> 
  
> <span data-ttu-id="9f40a-125">Операция поиска успешно.</span><span class="sxs-lookup"><span data-stu-id="9f40a-125">The find operation was successful.</span></span>
    
<span data-ttu-id="9f40a-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="9f40a-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="9f40a-127">Закладки с помощью параметра _BkOrigin_ является недопустимым, так как он был удален или находится за последней строки запроса.</span><span class="sxs-lookup"><span data-stu-id="9f40a-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="9f40a-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9f40a-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9f40a-129">Не были найдены строки, соответствующие ограничение.</span><span class="sxs-lookup"><span data-stu-id="9f40a-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="9f40a-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="9f40a-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="9f40a-131">Вызов завершился успешно, но закладку, используемый в операции больше не устанавливаются в той же строке, что и при его последнего использования; Если закладка не используется, он больше не в той же позиции при его создании.</span><span class="sxs-lookup"><span data-stu-id="9f40a-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="9f40a-132">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="9f40a-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9f40a-133">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="9f40a-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9f40a-134">В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9f40a-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f40a-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f40a-135">Remarks</span></span>

<span data-ttu-id="9f40a-136">Метод **IMAPITable::FindRow** поиск первой строки в таблице в соответствии с набор условий поиска, описанного в структуре **SRestriction** указывает параметр _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="9f40a-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="9f40a-137">Как правило **FindRow** выполняет поиск вперед из указанной закладке.</span><span class="sxs-lookup"><span data-stu-id="9f40a-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="9f40a-138">Может задать поиск, чтобы переместить назад из закладки, установив флаг DIR_BACKWARD с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9f40a-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="9f40a-139">Поиск вперед начинается с текущей закладки; Поиск в обратном направлении начинается с строке до закладки.</span><span class="sxs-lookup"><span data-stu-id="9f40a-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="9f40a-140">Конечным поиска — непосредственно перед первой строки найдено, которое удовлетворены ограничение.</span><span class="sxs-lookup"><span data-stu-id="9f40a-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="9f40a-141">Если строка, на который указывает на закладку в параметре _BkOrigin_ более не существует в таблице и таблицы не удается установить новую позицию закладки, **FindRow** возвращает MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="9f40a-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="9f40a-142">Если строка, на который указывает _BkOrigin_ больше не существует и таблицу для установки в новое положение закладки, **FindRow** возвращает MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="9f40a-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="9f40a-143">При BOOKMARK_BEGINNING или BOOKMARK_END закладку, переданные в _BkOrigin_ **FindRow** возвращает MAPI_E_NOT_FOUND, если нет соответствующей строки не найден.</span><span class="sxs-lookup"><span data-stu-id="9f40a-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="9f40a-144">Если закладка, используемые в _BkOrigin_ BOOKMARK_CURRENT, **FindRow** может вернуть MAPI_W_POSITION_CHANGED, но не MAPI_E_INVALID_BOOKMARK, поскольку всегда текущей позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="9f40a-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="9f40a-145">Столбец **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) свойство является обязательным для всех таблиц и всех реализациях **FindRow** , необходимых для поддержки вызовов, поиск строки на основании PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="9f40a-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9f40a-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9f40a-146">Notes to implementers</span></span>

<span data-ttu-id="9f40a-147">Тип префикс поиска выполняется сервером **FindRow** полезен только поиска следует направлении организации в таблице.</span><span class="sxs-lookup"><span data-stu-id="9f40a-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="9f40a-148">Для достижения необходимых поведение функции сравнения, содержится в разрешении **RELOP_GE** передается в структуре ограничение свойства должен быть те же функции сравнения, на котором основано порядок сортировки в таблице.</span><span class="sxs-lookup"><span data-stu-id="9f40a-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9f40a-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9f40a-149">Notes to callers</span></span>

<span data-ttu-id="9f40a-150">**FindRow** можно использовать для поддержки прокрутки на основании строки, введенные в пользователем, особенно в списки в диалоговых окнах адрес.</span><span class="sxs-lookup"><span data-stu-id="9f40a-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="9f40a-151">В этом типе прокрутки пользователей введите постепенно больше префиксы желаемую строковое значение и периодически может выдавать **FindRow** звонка для перехода к первой строке, которая соответствует префикса.</span><span class="sxs-lookup"><span data-stu-id="9f40a-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="9f40a-152">Направление перескакивает курсора зависит от направление поиска установлен на выполнение.</span><span class="sxs-lookup"><span data-stu-id="9f40a-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="9f40a-153">Чтобы использовать **FindRow**, необходимо установить закладку.</span><span class="sxs-lookup"><span data-stu-id="9f40a-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="9f40a-154">Поиск строки может быть создано из любого закладку, включая из предварительно закладки, которое указывает текущую позицию и начала и окончания таблицы.</span><span class="sxs-lookup"><span data-stu-id="9f40a-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="9f40a-155">Если большое число строк в таблице, операции поиска может быть медленно.</span><span class="sxs-lookup"><span data-stu-id="9f40a-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="9f40a-156">Используйте ограничение для поиска строки префикс для прокрутки следующим образом.</span><span class="sxs-lookup"><span data-stu-id="9f40a-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="9f40a-157">При поиске вперед на столбец, сортировка в порядке возрастания и обратной поиска на столбец в порядке убывания передачи структуры ограничение свойства в параметр _lpRestriction_ с отношением **RELOP_GE** и соответствующей Свойство tag и префикса, с помощью **GE** формат _тега_ _префикса_.</span><span class="sxs-lookup"><span data-stu-id="9f40a-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="9f40a-158">Дополнительные сведения об использовании структур ограничение для указания фильтра, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="9f40a-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f40a-159">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="9f40a-159">MFCMAPI reference</span></span>

<span data-ttu-id="9f40a-160">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="9f40a-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f40a-161">**����**</span><span class="sxs-lookup"><span data-stu-id="9f40a-161">**File**</span></span>|<span data-ttu-id="9f40a-162">**�������**</span><span class="sxs-lookup"><span data-stu-id="9f40a-162">**Function**</span></span>|<span data-ttu-id="9f40a-163">**�����������**</span><span class="sxs-lookup"><span data-stu-id="9f40a-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f40a-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="9f40a-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="9f40a-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="9f40a-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="9f40a-166">Mfcmapi (en) использует метод **IMAPITable::FindRow** для поиска строк, которые соответствуют ограничению поиска.</span><span class="sxs-lookup"><span data-stu-id="9f40a-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f40a-167">См. также</span><span class="sxs-lookup"><span data-stu-id="9f40a-167">See also</span></span>



[<span data-ttu-id="9f40a-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="9f40a-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="9f40a-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="9f40a-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="9f40a-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9f40a-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="9f40a-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f40a-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="9f40a-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9f40a-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

