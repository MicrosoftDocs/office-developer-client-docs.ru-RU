---
title: Имапитаблефиндров
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329083"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="7ba4d-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="7ba4d-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="7ba4d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ba4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ba4d-105">Находит следующую строку в таблице, которая соответствует определенным условиям поиска, и перемещает курсор в эту строку.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7ba4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ba4d-106">Parameters</span></span>

 <span data-ttu-id="7ba4d-107">_Лпрестриктион_</span><span class="sxs-lookup"><span data-stu-id="7ba4d-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="7ba4d-108">возврата Указатель на структуру [срестриктион](srestriction.md) , которая описывает критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="7ba4d-109">_Бкоригин_</span><span class="sxs-lookup"><span data-stu-id="7ba4d-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="7ba4d-110">возврата Закладка, определяющая строку, в которой запрос **FindRow** должен начинаться.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="7ba4d-111">Можно создать закладку с помощью метода [IMAPITable:: креатебукмарк](imapitable-createbookmark.md) или одного из следующих предварительно заданных значений.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="7ba4d-112">БУКМАРК_БЕГИННИНГ</span><span class="sxs-lookup"><span data-stu-id="7ba4d-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="7ba4d-113">Выполняет поиск с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="7ba4d-114">БУКМАРК_КУРРЕНТ</span><span class="sxs-lookup"><span data-stu-id="7ba4d-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="7ba4d-115">Выполняет поиск из строки в таблице, в которой находится курсор.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="7ba4d-116">БУКМАРК_ЕНД</span><span class="sxs-lookup"><span data-stu-id="7ba4d-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="7ba4d-117">Выполняет поиск с конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="7ba4d-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ba4d-118">_ulFlags_</span></span>
  
> <span data-ttu-id="7ba4d-119">возврата Битовая маска флагов, которые управляют направлением поиска.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="7ba4d-120">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7ba4d-120">The following flag can be set:</span></span>
    
<span data-ttu-id="7ba4d-121">ДИР_БАККВАРД</span><span class="sxs-lookup"><span data-stu-id="7ba4d-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="7ba4d-122">Выполняет поиск в обратном направлении от строки, указанной закладкой.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ba4d-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ba4d-123">Return value</span></span>

<span data-ttu-id="7ba4d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ba4d-124">S_OK</span></span> 
  
> <span data-ttu-id="7ba4d-125">Операция поиска выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-125">The find operation was successful.</span></span>
    
<span data-ttu-id="7ba4d-126">МАПИ_Е_ИНВАЛИД_БУКМАРК</span><span class="sxs-lookup"><span data-stu-id="7ba4d-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="7ba4d-127">Закладка в параметре _бкоригин_ является недопустимой, так как она была удалена или находится за пределами последней запрошенной строки.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="7ba4d-128">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="7ba4d-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7ba4d-129">Не найдены строки, которые содержали ограничение.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="7ba4d-130">МАПИ_В_ПОСИТИОН_ЧАНЖЕД</span><span class="sxs-lookup"><span data-stu-id="7ba4d-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="7ba4d-131">Вызов выполнен успешно, но закладка, используемая в операции, больше не задается в той же строке, что и при ее последнем использовании; Если закладка не использовалась, она больше не находится в той же позиции, что и при ее создании.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="7ba4d-132">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7ba4d-133">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="7ba4d-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7ba4d-134">Просмотр и [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7ba4d-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ba4d-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ba4d-135">Remarks</span></span>

<span data-ttu-id="7ba4d-136">Метод **IMAPITable:: FindRow** ищет первую строку в таблице в соответствии с набором критериев поиска, описанным в структуре **срестриктион** , на которую указывает параметр _лпрестриктион_ .</span><span class="sxs-lookup"><span data-stu-id="7ba4d-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="7ba4d-137">Обычно поиск \*\*\*\* выполняется в перенаправлении с указанной закладки.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="7ba4d-138">Вызывающий абонент может задать перемещение в обратном направлении из закладки, установив флаг ДИР_БАККВАРД в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7ba4d-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="7ba4d-139">Поиск вперед начинается с текущей закладки; Поиск в обратном направлении начинается с строки, предшествующей закладке.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="7ba4d-140">Конечное положение поиска непосредственно перед найденной первой строкой, которая удовлетворяет ограничению.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="7ba4d-141">Если строка, указывающая на закладку в параметре _бкоригин_ , больше не существует в таблице, а в таблице не удается установить новую позицию для закладки, то методом **FindRow** возвращается мапи_е_инвалид_букмарк.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="7ba4d-142">Если строка, на которую указывает _бкоригин_ , больше не существует, а таблица может установить новую позицию для закладки, то **FindRow** возвращает мапи_в_поситион_чанжед.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="7ba4d-143">Если закладка, переданная в _бкоригин_ , имеет значение БУКМАРК_БЕГИННИНГ или букмарк_енд, то метод **FindRow** возвращает мапи_е_нот_фаунд, если соответствующая строка не найдена.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="7ba4d-144">Если закладка, используемая в _бкоригин_ , имеет значение букмарк_куррент, то **FindRow** может возвращать МАПИ_В_ПОСИТИОН_ЧАНЖЕД, но не мапи_е_инвалид_букмарк, так как всегда существует текущее положение курсора.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="7ba4d-145">Столбец свойства **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) является обязательным для всех таблиц, и все реализации метода **FindRow** должны поддерживать вызовы, обращающиеся к строке на основе пр_инстанце_кэй.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7ba4d-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7ba4d-146">Notes to implementers</span></span>

<span data-ttu-id="7ba4d-147">Тип поиска префикса, выполняемого методом **FindRow** , удобен только в том случае, если поиск соответствует тому же направлению, что и Организация таблицы.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="7ba4d-148">Для достижения требуемого поведения функция сравнения, которая подразумевается в **релоп_же** , переданной в структуру ограничения свойств, должна быть той же функцией сравнения, на которой основан порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7ba4d-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7ba4d-149">Notes to callers</span></span>

<span data-ttu-id="7ba4d-150">Можно использовать команду **FindRow** для поддержки прокрутки, основанной на строках, вводимых пользователем, особенно в полях списка в диалоговых окнах адресов.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="7ba4d-151">В этом типе прокрутки пользователи вводят более длительные префиксы строкового значения, и вы можете периодически выдать вызов **FindRow** , чтобы перейти к первой строке, которая соответствует префиксу.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="7ba4d-152">Направление перехода курсора зависит от направления, в котором будет выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="7ba4d-153">Для использования метода **FindRow**необходимо задать закладку.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="7ba4d-154">Поиск строки может исходить из любой закладки, в том числе из предварительно заданной закладки, указывающей текущую позицию, начало и конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="7ba4d-155">Если таблица содержит большое количество строк, операция поиска может выполняться медленно.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="7ba4d-156">Используйте ограничение, чтобы найти префикс строки для прокрутки, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="7ba4d-157">Для прямого поиска по столбцу, отсортированному по возрастанию, и для обратного поиска по столбцу, отсортированному по убыванию, передайте структуру ограниченного свойства в параметре _лпрестриктион_ с параметром relation **релоп_же** и соответствующим тег свойства и префикс, используя _префикс_GE _тега_ \*\*\*\* Format.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="7ba4d-158">Дополнительные сведения об использовании структур ограничений для указания фильтра можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7ba4d-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ba4d-159">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7ba4d-159">MFCMAPI reference</span></span>

<span data-ttu-id="7ba4d-160">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ba4d-161">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7ba4d-161">**File**</span></span>|<span data-ttu-id="7ba4d-162">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7ba4d-162">**Function**</span></span>|<span data-ttu-id="7ba4d-163">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7ba4d-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ba4d-164">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="7ba4d-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7ba4d-165">Двсреадфунклоадтабле</span><span class="sxs-lookup"><span data-stu-id="7ba4d-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="7ba4d-166">MFCMAPI использует метод **IMAPITable:: FindRow** для поиска строк, которые отвечают ограничению.</span><span class="sxs-lookup"><span data-stu-id="7ba4d-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ba4d-167">См. также</span><span class="sxs-lookup"><span data-stu-id="7ba4d-167">See also</span></span>



[<span data-ttu-id="7ba4d-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="7ba4d-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="7ba4d-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7ba4d-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="7ba4d-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7ba4d-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="7ba4d-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ba4d-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="7ba4d-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7ba4d-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

