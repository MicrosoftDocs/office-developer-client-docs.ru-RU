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
# <a name="imapitablefindrow"></a><span data-ttu-id="be810-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="be810-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="be810-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be810-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be810-105">Находит следующую строку в таблице, которая соответствует определенным условиям поиска, и перемещает курсор в эту строку.</span><span class="sxs-lookup"><span data-stu-id="be810-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="be810-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be810-106">Parameters</span></span>

 <span data-ttu-id="be810-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="be810-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="be810-108">[in] Указатель на структуру [SRestriction,](srestriction.md) которая описывает условия поиска.</span><span class="sxs-lookup"><span data-stu-id="be810-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="be810-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="be810-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="be810-110">[in] Закладка, идентифицирующие строку, в которой должен начинаться поиск **FindRow.**</span><span class="sxs-lookup"><span data-stu-id="be810-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="be810-111">Закладку можно создать с помощью метода [IMAPITable::CreateBookmark](imapitable-createbookmark.md) или передать одно из следующих предварительно заранее задаваемых значений.</span><span class="sxs-lookup"><span data-stu-id="be810-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="be810-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="be810-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="be810-113">Выполняет поиск в начале таблицы.</span><span class="sxs-lookup"><span data-stu-id="be810-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="be810-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="be810-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="be810-115">Выполняет поиск по строке в таблице, в которой расположен курсор.</span><span class="sxs-lookup"><span data-stu-id="be810-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="be810-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="be810-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="be810-117">Выполняет поиск в конце таблицы.</span><span class="sxs-lookup"><span data-stu-id="be810-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="be810-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be810-118">_ulFlags_</span></span>
  
> <span data-ttu-id="be810-119">[in] Битоваяmas флагов, которая управляет направлением поиска.</span><span class="sxs-lookup"><span data-stu-id="be810-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="be810-120">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="be810-120">The following flag can be set:</span></span>
    
<span data-ttu-id="be810-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="be810-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="be810-122">Выполняет поиск в обратном направлении от строки, которая определена закладкой.</span><span class="sxs-lookup"><span data-stu-id="be810-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be810-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be810-123">Return value</span></span>

<span data-ttu-id="be810-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="be810-124">S_OK</span></span> 
  
> <span data-ttu-id="be810-125">Операция поиска прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="be810-125">The find operation was successful.</span></span>
    
<span data-ttu-id="be810-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="be810-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="be810-127">Закладка в  _параметре BkOrigin_ недействительна, так как она была удалена или находится за пределами последней запрашиваемой строки.</span><span class="sxs-lookup"><span data-stu-id="be810-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="be810-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="be810-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="be810-129">Строки, которые соответствуют ограничению, не найдены.</span><span class="sxs-lookup"><span data-stu-id="be810-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="be810-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="be810-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="be810-131">Вызов был успешным, но закладка, используемая в операции, больше не устанавливается в той же строке, что и при последнем вызове; если закладка не использовалась, она больше не находится в том положении, в который она была создана.</span><span class="sxs-lookup"><span data-stu-id="be810-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="be810-132">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="be810-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="be810-133">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="be810-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="be810-134">См. ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="be810-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be810-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="be810-135">Remarks</span></span>

<span data-ttu-id="be810-136">Метод **IMAPITable::FindRow** находит первую строку в таблице для соответствия набору критериев поиска, описанных в структуре **SRestriction,** на который указывает параметр _lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="be810-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="be810-137">Обычно **поиск в FindRow** выполняется из указанной закладки.</span><span class="sxs-lookup"><span data-stu-id="be810-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="be810-138">Вызываемая может настроить поиск для перемещения назад от закладки, установив флаг DIR_BACKWARD в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="be810-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="be810-139">Поиск вперед начинается с текущей закладки; поиск в обратном направлении начинается со строки перед закладкой.</span><span class="sxs-lookup"><span data-stu-id="be810-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="be810-140">End position of the search is just before the first row found that satisfied the restriction.</span><span class="sxs-lookup"><span data-stu-id="be810-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="be810-141">Если строка, на которую указывает закладка в параметре  _BkOrigin,_ больше не существует в таблице и в таблице не удается установить новое положение для закладки, **FindRow** возвращает MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="be810-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="be810-142">Если строка, на которую указывает  _BkOrigin,_ больше не существует и таблица может установить новое положение для закладки, **FindRow** возвращает MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="be810-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="be810-143">Если закладка, переданная  _в BkOrigin,_ BOOKMARK_BEGINNING или BOOKMARK_END, **FindRow** возвращает MAPI_E_NOT_FOUND если совпадающие строки не найдены.</span><span class="sxs-lookup"><span data-stu-id="be810-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="be810-144">Если закладка, используемая в  _BkOrigin,_ BOOKMARK_CURRENT, **FindRow** может возвращать MAPI_W_POSITION_CHANGED но не MAPI_E_INVALID_BOOKMARK, так как всегда имеется текущее положение курсора.</span><span class="sxs-lookup"><span data-stu-id="be810-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="be810-145">Столбец **свойства PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)требуется для всех таблиц, а все реализации **FindRow** необходимы для поддержки вызовов, ищите строку на основе PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="be810-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="be810-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="be810-146">Notes to implementers</span></span>

<span data-ttu-id="be810-147">Тип поиска префикса, выполняемого **FindRow,** полезен, только если поиск выполняется в том же направлении, что и организация таблицы.</span><span class="sxs-lookup"><span data-stu-id="be810-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="be810-148">Для достижения требуемого поведения функция сравнения,  подразумеваемая RELOP_GE, переданная в структуре ограничений свойств, должна быть той же функцией сравнения, на которой основан порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="be810-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="be810-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="be810-149">Notes to callers</span></span>

<span data-ttu-id="be810-150">С помощью **FindRow** можно поддерживать прокрутку на основе строк, введите их пользователем, особенно в полях со списками в диалоговом окке адреса.</span><span class="sxs-lookup"><span data-stu-id="be810-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="be810-151">В этом типе прокрутки пользователи постепенно введите более длинные префиксы нужного строковых значений, и вы можете периодически вызывать **FindRow,** чтобы перейти к первой строке, которая соответствует префиксу.</span><span class="sxs-lookup"><span data-stu-id="be810-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="be810-152">Направление перехода курсора зависит от того, в каком направлении будет запускаться поиск.</span><span class="sxs-lookup"><span data-stu-id="be810-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="be810-153">Чтобы использовать **FindRow,** необходимо установить закладку.</span><span class="sxs-lookup"><span data-stu-id="be810-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="be810-154">Поиск строк может происходить из любой закладки, в том числе из предустановленных закладок, указывающих текущую позицию, а также начало и конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="be810-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="be810-155">Если в таблице много строк, операция поиска может быть медленной.</span><span class="sxs-lookup"><span data-stu-id="be810-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="be810-156">Используйте ограничение, чтобы найти префикс строки для прокрутки следующим образом.</span><span class="sxs-lookup"><span data-stu-id="be810-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="be810-157">Для переадресации поиска в столбце, отсортженном по возрастанию, и для обратного поиска в столбце, отсортженном в порядке убывающего, передав структуру ограничений свойств в _параметре lpRestriction_ с отношением **RELOP_GE** и соответствующим тегом свойства и префиксом, используя префикс  **GE** тега формата _._</span><span class="sxs-lookup"><span data-stu-id="be810-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="be810-158">Дополнительные сведения об использовании структур ограничений для указания фильтра см. в [сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="be810-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="be810-159">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="be810-159">MFCMAPI reference</span></span>

<span data-ttu-id="be810-160">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="be810-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="be810-161">**Файл**</span><span class="sxs-lookup"><span data-stu-id="be810-161">**File**</span></span>|<span data-ttu-id="be810-162">**Функция**</span><span class="sxs-lookup"><span data-stu-id="be810-162">**Function**</span></span>|<span data-ttu-id="be810-163">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="be810-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be810-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="be810-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="be810-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="be810-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="be810-166">MFCMAPI использует метод **IMAPITable::FindRow** для поиска строк, которые соответствуют ограничению.</span><span class="sxs-lookup"><span data-stu-id="be810-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be810-167">См. также</span><span class="sxs-lookup"><span data-stu-id="be810-167">See also</span></span>



[<span data-ttu-id="be810-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="be810-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="be810-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="be810-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="be810-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="be810-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="be810-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be810-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="be810-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="be810-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

