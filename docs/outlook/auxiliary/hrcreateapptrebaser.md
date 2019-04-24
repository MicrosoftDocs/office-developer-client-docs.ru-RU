---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект Иолкапптребасер для использования в переиндексации встреч в календарях Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317614"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="eafd9-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="eafd9-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="eafd9-104">Инициализирует объект [иолкапптребасер](iolkapptrebaser.md) для использования в переиндексации встреч в календарях Outlook.</span><span class="sxs-lookup"><span data-stu-id="eafd9-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="eafd9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="eafd9-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eafd9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="eafd9-106">Header file:</span></span>  <br/> |<span data-ttu-id="eafd9-107">тзмовелиб. h</span><span class="sxs-lookup"><span data-stu-id="eafd9-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="eafd9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="eafd9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eafd9-109">тзмовелиб. dll</span><span class="sxs-lookup"><span data-stu-id="eafd9-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="eafd9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="eafd9-110">Called by:</span></span>  <br/> |<span data-ttu-id="eafd9-111">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="eafd9-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="eafd9-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="eafd9-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="eafd9-113">**ЛФРКРЕАТЕАППТРЕБАСЕР**</span><span class="sxs-lookup"><span data-stu-id="eafd9-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="eafd9-114">Точка входа DLL:</span><span class="sxs-lookup"><span data-stu-id="eafd9-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="eafd9-115">**Хркреатеапптребасер @ 44**</span><span class="sxs-lookup"><span data-stu-id="eafd9-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a><span data-ttu-id="eafd9-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="eafd9-116">Parameters</span></span>

<span data-ttu-id="eafd9-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eafd9-117">_ulFlags_</span></span>
  
> <span data-ttu-id="eafd9-118">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="eafd9-118">[in] Required.</span></span> <span data-ttu-id="eafd9-119">Битовая маска флагов, используемых для управления выполнением базового процесса.</span><span class="sxs-lookup"><span data-stu-id="eafd9-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="eafd9-120">Следующие флаги можно задать и определить в тзмовелиб. h:</span><span class="sxs-lookup"><span data-stu-id="eafd9-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="eafd9-121">**Ребасе_флаг_упдате_организед_митингс** — элементы встречи, в которых пользователь является организатором собрания, изменяются.</span><span class="sxs-lookup"><span data-stu-id="eafd9-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="eafd9-122">Обратите внимание, что по умолчанию Outlook отправляет обновления собраний всем участникам собрания, для которого выполняется перечисление.</span><span class="sxs-lookup"><span data-stu-id="eafd9-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="eafd9-123">Этот флаг можно сочетать с параметром **ребасе_флаг_форце_но_екс_упдатес** или **ребасе_флаг_форце_но_упдатес** для изменения способа обработки обновлений собраний.</span><span class="sxs-lookup"><span data-stu-id="eafd9-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="eafd9-124">**Ребасе_флаг_упдате_унмаркед** — обновление элементов встречи, которые не были помечены с помощью часового пояса.</span><span class="sxs-lookup"><span data-stu-id="eafd9-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="eafd9-125">Если этот флаг указан, то значение *птзмиссинг* используется как часовой пояс, в течение которого создается элемент для всех элементов, не имеющих данных о часовых поясах.</span><span class="sxs-lookup"><span data-stu-id="eafd9-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="eafd9-126">**Ребасе_флаг_упдате_онлирекурринг** — обновление только повторяющихся встреч.</span><span class="sxs-lookup"><span data-stu-id="eafd9-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="eafd9-127">**Ребасе_флаг_но_уи** — не отображать пользовательский интерфейс, включая диалоговые окна входа, которые обычно отображаются при открытии хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafd9-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="eafd9-128">**Ребасе_флаг_упдате_минимизеапптс** — не изменяйте базовые элементы встречи, которые происходят в прошлое.</span><span class="sxs-lookup"><span data-stu-id="eafd9-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="eafd9-129">**Ребасе_флаг_форце_ребасе** — не проверяйте организатора для принятия решений по обновлению, но изменяйте базовые элементы встречи, в которых пользователь является участником.</span><span class="sxs-lookup"><span data-stu-id="eafd9-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="eafd9-130">**Ребасе_флаг_форце_но_екс_упдатес** — Отправка обновлений только в том случае, если пользователь является организатором, а получатель не подключен к серверу Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="eafd9-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="eafd9-131">**Ребасе_флаг_форце_но_упдатес** — никогда не отправлять обновления.</span><span class="sxs-lookup"><span data-stu-id="eafd9-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="eafd9-132">**Ребасе_флаг_онли_креатед_пре_патч** — восстановление только тех элементов встречи с одним экземпляром, созданных до применения исправления.</span><span class="sxs-lookup"><span data-stu-id="eafd9-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="eafd9-133">**Ребасе_флаг_репортинг_моде** — не перестраивается, просто отчитываться об элементах встречи, которые будут передаваться в базовый.</span><span class="sxs-lookup"><span data-stu-id="eafd9-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="eafd9-134">**Ребасе_флаг_сенд_ресаурце_упдатес** — Отправка обновлений на собрания ресурсам.</span><span class="sxs-lookup"><span data-stu-id="eafd9-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="eafd9-135">_Псессион_</span><span class="sxs-lookup"><span data-stu-id="eafd9-135">_pSession_</span></span>
  
> <span data-ttu-id="eafd9-136">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="eafd9-136">[in] Required.</span></span> <span data-ttu-id="eafd9-137">Указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="eafd9-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="eafd9-138">_Пкалендармсгсторе_</span><span class="sxs-lookup"><span data-stu-id="eafd9-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="eafd9-139">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="eafd9-139">[in] Required.</span></span> <span data-ttu-id="eafd9-140">Указатель на хранилище сообщений, содержащее элементы встреч, которые необходимо перестроить.</span><span class="sxs-lookup"><span data-stu-id="eafd9-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="eafd9-141">_Пкалендарфолдер_</span><span class="sxs-lookup"><span data-stu-id="eafd9-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="eafd9-142">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="eafd9-142">[in] Required.</span></span> <span data-ttu-id="eafd9-143">Указатель на папку календаря, в которой содержатся элементы встречи, которые необходимо перестроить.</span><span class="sxs-lookup"><span data-stu-id="eafd9-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="eafd9-144">_Пвсзупдатепрефикс_</span><span class="sxs-lookup"><span data-stu-id="eafd9-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="eafd9-145">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="eafd9-145">[in] Optional.</span></span> <span data-ttu-id="eafd9-146">Указатель на строку, содержащую префикс, который будет добавлен в начало приглашений на собрание.</span><span class="sxs-lookup"><span data-stu-id="eafd9-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="eafd9-147">Может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="eafd9-147">May be NULL.</span></span>
    
<span data-ttu-id="eafd9-148">_Пфтинсталлдатеутк_</span><span class="sxs-lookup"><span data-stu-id="eafd9-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="eafd9-149">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="eafd9-149">[in] Optional.</span></span> <span data-ttu-id="eafd9-150">Дата установки исправления часового пояса.</span><span class="sxs-lookup"><span data-stu-id="eafd9-150">The time zone patch install date.</span></span> <span data-ttu-id="eafd9-151">Используется только в том случае, если установлен флаг **ребасе_флаг_онли_креатед_пре_патч** .</span><span class="sxs-lookup"><span data-stu-id="eafd9-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="eafd9-152">_Иекспансиондепс_</span><span class="sxs-lookup"><span data-stu-id="eafd9-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="eafd9-153">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="eafd9-153">[in] Optional.</span></span> <span data-ttu-id="eafd9-154">Глубина расширения при расширении списков рассылки для исключения получателей, подключенных к серверу Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="eafd9-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="eafd9-155">Используется только в том случае, если установлен флаг **ребасе_флаг_форце_но_екс_упдатес** .</span><span class="sxs-lookup"><span data-stu-id="eafd9-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="eafd9-156">_Птзто_</span><span class="sxs-lookup"><span data-stu-id="eafd9-156">_pTZTo_</span></span>
  
> <span data-ttu-id="eafd9-157">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="eafd9-157">[in] Required.</span></span> <span data-ttu-id="eafd9-158">Указатель на структуру **TZDEFINITION** , описывающую часовой пояс, в который будет выполняться перечисление.</span><span class="sxs-lookup"><span data-stu-id="eafd9-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="eafd9-159">**TZDEFINITION** определяется в тзмовелиб.</span><span class="sxs-lookup"><span data-stu-id="eafd9-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="eafd9-160">Птзмиссинг</span><span class="sxs-lookup"><span data-stu-id="eafd9-160">pTZMissing</span></span>
  
> <span data-ttu-id="eafd9-161">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="eafd9-161">[in] Required.</span></span> <span data-ttu-id="eafd9-162">Указатель на структуру **TZDEFINITION** , описывающую часовой пояс, который предполагается использовать, если сведения о часовом поясе не помечены для элемента.</span><span class="sxs-lookup"><span data-stu-id="eafd9-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="eafd9-163">ЗНАЧЕНИЕ не должно быть равно NULL, но используется только в том случае, если установлен флаг **ребасе_флаг_упдате_унмаркед** .</span><span class="sxs-lookup"><span data-stu-id="eafd9-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="eafd9-164">_Пперрор_</span><span class="sxs-lookup"><span data-stu-id="eafd9-164">_ppError_</span></span>
  
> <span data-ttu-id="eafd9-165">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="eafd9-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="eafd9-166">Может иметь значение NULL, если расширенные сведения об ошибке не требуются.</span><span class="sxs-lookup"><span data-stu-id="eafd9-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="eafd9-167">Бесплатно с [мапифрибуффер](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="eafd9-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="eafd9-168">_Ппапптребасе_</span><span class="sxs-lookup"><span data-stu-id="eafd9-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="eafd9-169">вышли Указатель на указатель на возвращенный интерфейс **иолкапптребасер** .</span><span class="sxs-lookup"><span data-stu-id="eafd9-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="eafd9-170">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="eafd9-170">Return values</span></span>

<span data-ttu-id="eafd9-171">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="eafd9-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eafd9-172">Замечания</span><span class="sxs-lookup"><span data-stu-id="eafd9-172">Remarks</span></span>

<span data-ttu-id="eafd9-173">При использовании [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) для поиска адреса этой функции в тзмовелиб. dll укажите в качестве имени процедуры **хркреатеапптребасер @ 44** .</span><span class="sxs-lookup"><span data-stu-id="eafd9-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="eafd9-174">Не все флаги являются допустимыми в сочетании друг с другом.</span><span class="sxs-lookup"><span data-stu-id="eafd9-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="eafd9-175">Дополнительные сведения о различных параметрах можно найти в разделе "Глоссарий по параметрам командной строки для средства обновления данных о часовых поясах Outlook" в статье [KB 931667: сведения об изменении часового пояса с помощью средства обновления данных часовых поясов для Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="eafd9-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eafd9-176">См. также</span><span class="sxs-lookup"><span data-stu-id="eafd9-176">See also</span></span>

- [<span data-ttu-id="eafd9-177">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="eafd9-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

