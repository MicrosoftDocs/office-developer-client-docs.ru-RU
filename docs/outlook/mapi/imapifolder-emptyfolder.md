---
title: Имапифолдеремптифолдер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280108"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="c7cff-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="c7cff-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="c7cff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7cff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7cff-105">Удаляет все сообщения и вложенные папки из папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="c7cff-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c7cff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7cff-106">Parameters</span></span>

 <span data-ttu-id="c7cff-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="c7cff-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c7cff-108">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7cff-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="c7cff-109">Параметр _улуипарам_ игнорируется, если не установлен флаг фолдер_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c7cff-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c7cff-110">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="c7cff-110">_lpProgress_</span></span>
  
> <span data-ttu-id="c7cff-111">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7cff-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="c7cff-112">Если в _лппрогресс_переДАЕТСЯ значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="c7cff-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="c7cff-113">Параметр _лппрогресс_ игнорируется, если не установлен флаг фолдер_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c7cff-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c7cff-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c7cff-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c7cff-115">возврата Битовая маска флагов, которые управляют способом очистки папки.</span><span class="sxs-lookup"><span data-stu-id="c7cff-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="c7cff-116">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c7cff-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c7cff-117">ДЕЛ_АССОЦИАТЕД</span><span class="sxs-lookup"><span data-stu-id="c7cff-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="c7cff-118">Удаляет все вложенные папки, в том числе вложенные папки, содержащие сообщения с связанным контентом.</span><span class="sxs-lookup"><span data-stu-id="c7cff-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="c7cff-119">Флаг ДЕЛ_АССОЦИАТЕД имеет значение только для папки верхнего уровня, в которой работает вызов.</span><span class="sxs-lookup"><span data-stu-id="c7cff-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="c7cff-120">ДЕЛЕТЕ_ХАРД_ДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="c7cff-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="c7cff-121">Окончательно удаляет все сообщения, включая обратимо удаленные.</span><span class="sxs-lookup"><span data-stu-id="c7cff-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="c7cff-122">ФОЛДЕР_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="c7cff-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="c7cff-123">Отображает индикатор хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c7cff-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7cff-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7cff-124">Return value</span></span>

<span data-ttu-id="c7cff-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7cff-125">S_OK</span></span> 
  
> <span data-ttu-id="c7cff-126">Папка успешно очищена.</span><span class="sxs-lookup"><span data-stu-id="c7cff-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="c7cff-127">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="c7cff-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c7cff-128">Вызов выполнен успешно, но папка не была полностью очищена.</span><span class="sxs-lookup"><span data-stu-id="c7cff-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="c7cff-129">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="c7cff-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c7cff-130">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="c7cff-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c7cff-131">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c7cff-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7cff-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7cff-132">Remarks</span></span>

<span data-ttu-id="c7cff-133">Метод **IMAPIFolder:: EmptyFolder** удаляет все содержимое папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="c7cff-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="c7cff-134">При вызове **EmptyFolder** отправленные сообщения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="c7cff-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="c7cff-135">Содержимое, связанное с папкой, включает сообщения, которые используются для описания представлений, правил, настраиваемых форм и хранилища пользовательских решений, а также могут включать определения форм.</span><span class="sxs-lookup"><span data-stu-id="c7cff-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c7cff-136">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c7cff-136">Notes to implementers</span></span>

<span data-ttu-id="c7cff-137">Не вызывайте метод [IMsgStore:: абортсубмит](imsgstore-abortsubmit.md) для сообщений в папке, которые были отправлены.</span><span class="sxs-lookup"><span data-stu-id="c7cff-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="c7cff-138">Отправленные сообщения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="c7cff-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c7cff-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c7cff-139">Notes to callers</span></span>

<span data-ttu-id="c7cff-140">Эти возвращаемые значения следует ожидать при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="c7cff-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="c7cff-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="c7cff-141">**Condition**</span></span>|<span data-ttu-id="c7cff-142">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="c7cff-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7cff-143">**EmptyFolder** успешно очищает папку.</span><span class="sxs-lookup"><span data-stu-id="c7cff-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="c7cff-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7cff-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="c7cff-145">**EmptyFolder** не удалось полностью очистить папку.</span><span class="sxs-lookup"><span data-stu-id="c7cff-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="c7cff-146">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="c7cff-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="c7cff-147">**EmptyFolder** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="c7cff-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="c7cff-148">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="c7cff-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="c7cff-149">Если **EmptyFolder** не удается выполнить, не следует предполагать, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="c7cff-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="c7cff-150">Возможно, в **EmptyFolder** удалось удалить часть содержимого папки, прежде чем возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7cff-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c7cff-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c7cff-151">MFCMAPI reference</span></span>

<span data-ttu-id="c7cff-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c7cff-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c7cff-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c7cff-153">**File**</span></span>|<span data-ttu-id="c7cff-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c7cff-154">**Function**</span></span>|<span data-ttu-id="c7cff-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c7cff-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7cff-156">Мсгсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="c7cff-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="c7cff-157">Кмсгсторедлг:: Онемптифолдер</span><span class="sxs-lookup"><span data-stu-id="c7cff-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="c7cff-158">MFCMAPI использует метод **IMAPIFolder:: EmptyFolder** для удаления содержимого указанной папки.</span><span class="sxs-lookup"><span data-stu-id="c7cff-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7cff-159">См. также</span><span class="sxs-lookup"><span data-stu-id="c7cff-159">See also</span></span>



[<span data-ttu-id="c7cff-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="c7cff-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="c7cff-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c7cff-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="c7cff-162">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="c7cff-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c7cff-163">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="c7cff-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

