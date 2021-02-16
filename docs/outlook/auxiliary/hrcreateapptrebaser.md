---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект IOlkApptRebaser для использования при переоценке встреч в календарях Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317614"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="a53a1-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="a53a1-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="a53a1-104">Инициализирует [объект IOlkApptRebaser](iolkapptrebaser.md) для использования при переоценке встреч в календарях Outlook.</span><span class="sxs-lookup"><span data-stu-id="a53a1-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a53a1-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a53a1-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a53a1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a53a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="a53a1-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="a53a1-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="a53a1-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a53a1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a53a1-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="a53a1-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="a53a1-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a53a1-110">Called by:</span></span>  <br/> |<span data-ttu-id="a53a1-111">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="a53a1-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="a53a1-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a53a1-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="a53a1-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="a53a1-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="a53a1-114">Точка входа DLL:</span><span class="sxs-lookup"><span data-stu-id="a53a1-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="a53a1-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="a53a1-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a53a1-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="a53a1-116">Parameters</span></span>

<span data-ttu-id="a53a1-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a53a1-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a53a1-118">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="a53a1-118">[in] Required.</span></span> <span data-ttu-id="a53a1-119">Битоваяmas флагов, используемая для управления выполнением повторного использования.</span><span class="sxs-lookup"><span data-stu-id="a53a1-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="a53a1-120">Следующие флаги можно установить и определить в tzmovelib.h:</span><span class="sxs-lookup"><span data-stu-id="a53a1-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="a53a1-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — элементы встречи, в которых пользователь является организатором собрания, перенастрояются.</span><span class="sxs-lookup"><span data-stu-id="a53a1-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="a53a1-122">Обратите внимание, что по умолчанию outlook отправляет обновления собраний всем участникам перенаправляемого собрания.</span><span class="sxs-lookup"><span data-stu-id="a53a1-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="a53a1-123">Вы можете объединить этот флаг с REBASE_FLAG_FORCE_NO_EX_UPDATES **или** **REBASE_FLAG_FORCE_NO_UPDATES,** чтобы изменить лад обработку обновлений собраний.</span><span class="sxs-lookup"><span data-stu-id="a53a1-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="a53a1-124">**REBASE_FLAG_UPDATE_UNMARKED** — обновление элементов встреч, не помеченных часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="a53a1-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="a53a1-125">Если этот флаг указан, значение  *pTZMissing*  используется в качестве часового пояса, в который создается элемент для всех элементов без данных часового пояса.</span><span class="sxs-lookup"><span data-stu-id="a53a1-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="a53a1-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** — обновляют только элементы повторяющихся встреч.</span><span class="sxs-lookup"><span data-stu-id="a53a1-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="a53a1-127">**REBASE_FLAG_NO_UI** — не отображайте пользовательский интерфейс, включая диалоги для логотипа, которые обычно отображаются при открытии магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="a53a1-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="a53a1-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — не переназначить элементы встреч, которые происходят в прошлом.</span><span class="sxs-lookup"><span data-stu-id="a53a1-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="a53a1-129">**REBASE_FLAG_FORCE_REBASE** — не проверяйте организатора на предмет повторного принятия решений, а перенастройку элементов встреч, в которых пользователь является участником.</span><span class="sxs-lookup"><span data-stu-id="a53a1-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="a53a1-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** - отправлять обновления, только если пользователь является организатором и получатель не подключен к Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a53a1-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="a53a1-131">**REBASE_FLAG_FORCE_NO_UPDATES** — никогда не отправлять обновления.</span><span class="sxs-lookup"><span data-stu-id="a53a1-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="a53a1-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — повторное базовая база элементов встреч, созданных только для одного экземпляра до того, как исправление было применено.</span><span class="sxs-lookup"><span data-stu-id="a53a1-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="a53a1-133">**REBASE_FLAG_REPORTING_MODE** — не перебазделайте, просто делайте отчет об элементе встречи, которые будут перебазданы.</span><span class="sxs-lookup"><span data-stu-id="a53a1-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="a53a1-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** — отправка обновлений собрания на ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a53a1-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="a53a1-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="a53a1-135">_pSession_</span></span>
  
> <span data-ttu-id="a53a1-136">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="a53a1-136">[in] Required.</span></span> <span data-ttu-id="a53a1-137">Указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="a53a1-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="a53a1-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="a53a1-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="a53a1-139">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="a53a1-139">[in] Required.</span></span> <span data-ttu-id="a53a1-140">Указатель на хранилище сообщений, содержащее элементы встречи, которые необходимо переназначить.</span><span class="sxs-lookup"><span data-stu-id="a53a1-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="a53a1-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="a53a1-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="a53a1-142">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="a53a1-142">[in] Required.</span></span> <span data-ttu-id="a53a1-143">Указатель на папку календаря, содержащую элементы встреч, которые необходимо переназначить.</span><span class="sxs-lookup"><span data-stu-id="a53a1-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="a53a1-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="a53a1-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="a53a1-145">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="a53a1-145">[in] Optional.</span></span> <span data-ttu-id="a53a1-146">Указатель на строку, содержащую префикс, который должен быть в конце запроса на собрание.</span><span class="sxs-lookup"><span data-stu-id="a53a1-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="a53a1-147">Может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="a53a1-147">May be NULL.</span></span>
    
<span data-ttu-id="a53a1-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="a53a1-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="a53a1-149">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="a53a1-149">[in] Optional.</span></span> <span data-ttu-id="a53a1-150">Дата установки исправления часовой пояса.</span><span class="sxs-lookup"><span data-stu-id="a53a1-150">The time zone patch install date.</span></span> <span data-ttu-id="a53a1-151">Используется, только если **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** флага.</span><span class="sxs-lookup"><span data-stu-id="a53a1-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="a53a1-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="a53a1-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="a53a1-153">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="a53a1-153">[in] Optional.</span></span> <span data-ttu-id="a53a1-154">Глубина расширения при расширении списков рассылки для исключения получателей, подключенных к Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a53a1-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="a53a1-155">Используется, только если **REBASE_FLAG_FORCE_NO_EX_UPDATES** флага.</span><span class="sxs-lookup"><span data-stu-id="a53a1-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="a53a1-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="a53a1-156">_pTZTo_</span></span>
  
> <span data-ttu-id="a53a1-157">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="a53a1-157">[in] Required.</span></span> <span data-ttu-id="a53a1-158">Указатель на структуру **TZDEFINITION,** описывающий часовой пояс для перенастройки.</span><span class="sxs-lookup"><span data-stu-id="a53a1-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="a53a1-159">**TZDEFINITION** определяется в tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="a53a1-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="a53a1-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="a53a1-160">pTZMissing</span></span>
  
> <span data-ttu-id="a53a1-161">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="a53a1-161">[in] Required.</span></span> <span data-ttu-id="a53a1-162">Указатель на структуру **TZDEFINITION,** описывающий часовой пояс, который предполагается использовать, если сведения о часовом поясе не помеются в элементе.</span><span class="sxs-lookup"><span data-stu-id="a53a1-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="a53a1-163">Не должно быть NULL, но  используется, только если REBASE_FLAG_UPDATE_UNMARKED флага.</span><span class="sxs-lookup"><span data-stu-id="a53a1-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="a53a1-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="a53a1-164">_ppError_</span></span>
  
> <span data-ttu-id="a53a1-165">[out] Указатель на указатель на структуру **MAPIERROR,** содержащую сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="a53a1-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="a53a1-166">Может иметь NULL, если расширенные сведения об ошибке не нужны.</span><span class="sxs-lookup"><span data-stu-id="a53a1-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="a53a1-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a53a1-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="a53a1-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="a53a1-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="a53a1-169">[out] Указатель на указатель на возвращенный **интерфейс IOlkApptRebaser.**</span><span class="sxs-lookup"><span data-stu-id="a53a1-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a53a1-170">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a53a1-170">Return values</span></span>

<span data-ttu-id="a53a1-171">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="a53a1-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a53a1-172">Примечания</span><span class="sxs-lookup"><span data-stu-id="a53a1-172">Remarks</span></span>

<span data-ttu-id="a53a1-173">При использовании [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) для искомого адреса этой функции в tzmovelib.dll укажите HrCreateApptRebaser@44 **в** качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="a53a1-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="a53a1-174">Не все флаги допустимы в сочетании друг с другом.</span><span class="sxs-lookup"><span data-stu-id="a53a1-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="a53a1-175">Дополнительные сведения о различных параметрах см. в разделе "Глоссарий параметров командной строки для средства обновления данных часового пояса Outlook" в [KB 931667:](https://support.microsoft.com/kb/931667/en-us)как решить проблему изменения часового пояса с помощью средства обновления часового пояса для Microsoft Office Outlook .</span><span class="sxs-lookup"><span data-stu-id="a53a1-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a53a1-176">См. также</span><span class="sxs-lookup"><span data-stu-id="a53a1-176">See also</span></span>

- [<span data-ttu-id="a53a1-177">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="a53a1-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

