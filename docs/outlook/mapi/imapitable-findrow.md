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
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429574"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="638eb-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="638eb-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="638eb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="638eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="638eb-105">Находит следующую строку в таблице, которая соответствует определенным критериям поиска и перемещает курсор в эту строку.</span><span class="sxs-lookup"><span data-stu-id="638eb-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="638eb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="638eb-106">Parameters</span></span>

 <span data-ttu-id="638eb-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="638eb-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="638eb-108">[in] Указатель на структуру [SRestriction,](srestriction.md) которая описывает критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="638eb-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="638eb-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="638eb-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="638eb-110">[in] Закладки, определяющие строку, в которой **FindRow** должен начать поиск.</span><span class="sxs-lookup"><span data-stu-id="638eb-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="638eb-111">Закладки можно создать с помощью [метода IMAPITable::CreateBookmark](imapitable-createbookmark.md) или передать одно из следующих предопределяемых значений.</span><span class="sxs-lookup"><span data-stu-id="638eb-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="638eb-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="638eb-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="638eb-113">Поиск с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="638eb-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="638eb-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="638eb-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="638eb-115">Поиск из строки в таблице, где расположен курсор.</span><span class="sxs-lookup"><span data-stu-id="638eb-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="638eb-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="638eb-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="638eb-117">Поиск в конце таблицы.</span><span class="sxs-lookup"><span data-stu-id="638eb-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="638eb-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="638eb-118">_ulFlags_</span></span>
  
> <span data-ttu-id="638eb-119">[in] Битмашка флагов, которые контролируют направление поиска.</span><span class="sxs-lookup"><span data-stu-id="638eb-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="638eb-120">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="638eb-120">The following flag can be set:</span></span>
    
<span data-ttu-id="638eb-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="638eb-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="638eb-122">Поиск в обратном направлении из строки, выделенной закладкой.</span><span class="sxs-lookup"><span data-stu-id="638eb-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="638eb-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="638eb-123">Return value</span></span>

<span data-ttu-id="638eb-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="638eb-124">S_OK</span></span> 
  
> <span data-ttu-id="638eb-125">Операция поиска прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="638eb-125">The find operation was successful.</span></span>
    
<span data-ttu-id="638eb-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="638eb-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="638eb-127">Закладки в  _параметре BkOrigin_ недействительны, так как она удалена или находится за пределами последней строки, запрашиваемой.</span><span class="sxs-lookup"><span data-stu-id="638eb-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="638eb-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="638eb-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="638eb-129">Строк, которые соответствуют ограничению, обнаружено не было.</span><span class="sxs-lookup"><span data-stu-id="638eb-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="638eb-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="638eb-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="638eb-131">Вызов удался, но закладки, используемые в операции, больше не устанавливаются в том же ряду, что и в последний раз; если закладка не была использована, она больше не находится в том же положении, что и при ее создания.</span><span class="sxs-lookup"><span data-stu-id="638eb-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="638eb-132">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="638eb-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="638eb-133">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="638eb-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="638eb-134">См. в руб. Использование [макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="638eb-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="638eb-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="638eb-135">Remarks</span></span>

<span data-ttu-id="638eb-136">Метод **IMAPITable::FindRow** находит первую строку в таблице, чтобы соответствовать набору критериев поиска, описанным в структуре **SRestriction,** на который указывает параметр _lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="638eb-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="638eb-137">Обычно **FindRow** выполняет поиск вперед из указанной закладки.</span><span class="sxs-lookup"><span data-stu-id="638eb-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="638eb-138">Вызываемая может настроить поиск для перемещения назад от закладки, установив флаг DIR_BACKWARD в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="638eb-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="638eb-139">Поиск вперед начинается с текущего закладки; поиск в обратном направлении начинается с строки до закладки.</span><span class="sxs-lookup"><span data-stu-id="638eb-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="638eb-140">End position of the search is just before the first row found that satisfied the restriction.</span><span class="sxs-lookup"><span data-stu-id="638eb-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="638eb-141">Если строка, на которую указывает закладки в параметре  _BkOrigin,_ больше не существует в таблице и таблица не может установить новое положение для закладки, **FindRow** возвращает MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="638eb-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="638eb-142">Если строка, на которую указывает  _BkOrigin,_ больше не существует и таблица может установить новую позицию для закладки, **FindRow** возвращает MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="638eb-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="638eb-143">Если закладки, переданные в  _BkOrigin,_ BOOKMARK_BEGINNING или BOOKMARK_END, **FindRow** возвращает MAPI_E_NOT_FOUND, если не найдена ни одна строка.</span><span class="sxs-lookup"><span data-stu-id="638eb-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="638eb-144">Если закладка, используемая в  _BkOrigin,_ BOOKMARK_CURRENT, **FindRow** может MAPI_W_POSITION_CHANGED, но не MAPI_E_INVALID_BOOKMARK, так как всегда имеется текущая позиция курсора.</span><span class="sxs-lookup"><span data-stu-id="638eb-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="638eb-145">Столбец **свойств PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)необходим для всех таблиц, а все реализации **FindRow** необходимы для поддержки вызовов, ищем строку на основе PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="638eb-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="638eb-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="638eb-146">Notes to implementers</span></span>

<span data-ttu-id="638eb-147">Тип поиска префикса, выполняемый **FindRow,** полезен только в том случае, если поиск выполняется в том же направлении, что и организация таблицы.</span><span class="sxs-lookup"><span data-stu-id="638eb-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="638eb-148">Для достижения требуемого поведения функция сравнения,  подразумеваемая RELOP_GE, переданной в структуре ограничений свойств, должна быть той же функцией сравнения, на которой основан порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="638eb-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="638eb-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="638eb-149">Notes to callers</span></span>

<span data-ttu-id="638eb-150">Вы можете использовать **FindRow** для поддержки прокрутки на основе строк, вбрасуемой пользователем, особенно в полях списков в диалоговом окантовке адресов.</span><span class="sxs-lookup"><span data-stu-id="638eb-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="638eb-151">В этом типе прокрутки пользователи введите постепенно более длинные префиксы нужного значения строки, и вы можете периодически выдавать вызов **FindRow,** чтобы перейти к первой строке, которая соответствует префиксу.</span><span class="sxs-lookup"><span data-stu-id="638eb-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="638eb-152">В каком направлении скачет курсор, зависит от того, в каком направлении будет запускаться поиск.</span><span class="sxs-lookup"><span data-stu-id="638eb-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="638eb-153">Чтобы использовать **FindRow,** необходимо установить закладки.</span><span class="sxs-lookup"><span data-stu-id="638eb-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="638eb-154">Поиск строки может происходить из любой закладки, в том числе из заранее закладки с указанием текущего положения и начала и конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="638eb-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="638eb-155">Если в таблице большое количество строк, операция поиска может быть медленной.</span><span class="sxs-lookup"><span data-stu-id="638eb-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="638eb-156">Используйте ограничение, чтобы найти префикс строки для прокрутки следующим образом.</span><span class="sxs-lookup"><span data-stu-id="638eb-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="638eb-157">Для переадресации поиска в столбце, отсортировали в порядке восходящего и для обратного поиска в столбце, отсортировали в порядке убывающего,  передать структуру ограничений свойств в _параметре lpRestriction_ с отношением **RELOP_GE** и соответствующим тегом свойства и префиксом, используя префикс **ge формат тега GE** _._</span><span class="sxs-lookup"><span data-stu-id="638eb-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="638eb-158">Дополнительные сведения об использовании структур ограничений для указания фильтра см. в дополнительных [сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="638eb-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="638eb-159">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="638eb-159">MFCMAPI reference</span></span>

<span data-ttu-id="638eb-160">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="638eb-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="638eb-161">**Файл**</span><span class="sxs-lookup"><span data-stu-id="638eb-161">**File**</span></span>|<span data-ttu-id="638eb-162">**Функция**</span><span class="sxs-lookup"><span data-stu-id="638eb-162">**Function**</span></span>|<span data-ttu-id="638eb-163">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="638eb-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="638eb-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="638eb-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="638eb-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="638eb-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="638eb-166">MFCMAPI использует **метод IMAPITable::FindRow** для поиска строк, которые соответствуют ограничению.</span><span class="sxs-lookup"><span data-stu-id="638eb-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="638eb-167">См. также</span><span class="sxs-lookup"><span data-stu-id="638eb-167">See also</span></span>



[<span data-ttu-id="638eb-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="638eb-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="638eb-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="638eb-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="638eb-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="638eb-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="638eb-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="638eb-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="638eb-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="638eb-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

