---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Инициализирует объект IOlkApptRebaser для использования в модификации базового адреса встреч в календарях Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397543"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="8ecf3-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="8ecf3-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="8ecf3-104">Инициализирует объект [IOlkApptRebaser](iolkapptrebaser.md) для использования в модификации базового адреса встреч в календарях Outlook.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8ecf3-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8ecf3-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ecf3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8ecf3-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ecf3-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="8ecf3-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="8ecf3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8ecf3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ecf3-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="8ecf3-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="8ecf3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8ecf3-110">Called by:</span></span>  <br/> |<span data-ttu-id="8ecf3-111">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="8ecf3-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="8ecf3-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8ecf3-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="8ecf3-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="8ecf3-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="8ecf3-114">Точку входа:</span><span class="sxs-lookup"><span data-stu-id="8ecf3-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="8ecf3-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="8ecf3-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8ecf3-116">���������</span><span class="sxs-lookup"><span data-stu-id="8ecf3-116">Parameters</span></span>

<span data-ttu-id="8ecf3-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-117">_ulFlags_</span></span>
  
> <span data-ttu-id="8ecf3-118">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-118">[in] Required.</span></span> <span data-ttu-id="8ecf3-119">Битовая маска флаги, используемые для управления, как выполняется изменен базовый адрес.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="8ecf3-120">Следующие флаги можно задать и определяются в tzmovelib.h:</span><span class="sxs-lookup"><span data-stu-id="8ecf3-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="8ecf3-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — преобразовываются элементы встречи, в которых пользователь является организатором собрания.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="8ecf3-122">Обратите внимание, что по умолчанию, в результате Outlook для отправки обновлений собрания всем участникам собрания, любые модификации.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="8ecf3-123">Этот флаг можно объединить с **REBASE_FLAG_FORCE_NO_EX_UPDATES** или **REBASE_FLAG_FORCE_NO_UPDATES** , чтобы изменить порядок обработки обновлений встреч.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="8ecf3-124">**REBASE_FLAG_UPDATE_UNMARKED** — обновление элементов встречи, которые не были помечены часового пояса.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="8ecf3-125">Если этот флаг указан, значение *pTZMissing* используется как часовой пояс, создавшего элемент всех элементов, у которых нет данных часового пояса.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="8ecf3-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** — обновление только повторяющихся элементов встречи.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="8ecf3-127">**REBASE_FLAG_NO_UI** — без отображения пользовательского интерфейса (UI), включая диалоговые окна входа в систему, обычно отображается при открытии хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="8ecf3-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — не Смена базы элементы встреч, которые происходят в прошлом.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="8ecf3-129">**REBASE_FLAG_FORCE_REBASE** — не проверять Организатор для повторного размещения en решения, но Смена базы элементы встречи, в которых является пользователь.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="8ecf3-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** — отправить обновляет только в том случае, если пользователь является организатором и получатель не подключен к серверу Exchange.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="8ecf3-131">**REBASE_FLAG_FORCE_NO_UPDATES** — никогда не отправлять обновления.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="8ecf3-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — Перебазировка только элементы единичных встреч, созданные до исправления.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="8ecf3-133">**REBASE_FLAG_REPORTING_MODE** — фактически не rebase, только отчет о встрече элементы, может быть модификации базового адреса.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="8ecf3-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** — отправка обновлений встреч ресурсам.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="8ecf3-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-135">_pSession_</span></span>
  
> <span data-ttu-id="8ecf3-136">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-136">[in] Required.</span></span> <span data-ttu-id="8ecf3-137">Указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="8ecf3-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="8ecf3-139">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-139">[in] Required.</span></span> <span data-ttu-id="8ecf3-140">Указатель на сообщение хранилища, содержащего элементы встреч, чтобы быть модификации базового адреса.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="8ecf3-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="8ecf3-142">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-142">[in] Required.</span></span> <span data-ttu-id="8ecf3-143">Указатель на папку календаря, содержащую элементы встреч, чтобы быть модификации базового адреса.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="8ecf3-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="8ecf3-145">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-145">[in] Optional.</span></span> <span data-ttu-id="8ecf3-146">Указатель на строку, содержащую префикс, которые должны добавляться в начало на приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="8ecf3-147">Может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-147">May be NULL.</span></span>
    
<span data-ttu-id="8ecf3-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="8ecf3-149">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-149">[in] Optional.</span></span> <span data-ttu-id="8ecf3-150">Дата установки исправления часового пояса.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-150">The time zone patch install date.</span></span> <span data-ttu-id="8ecf3-151">Используется только в том случае, если установлен флаг **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** .</span><span class="sxs-lookup"><span data-stu-id="8ecf3-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="8ecf3-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="8ecf3-153">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-153">[in] Optional.</span></span> <span data-ttu-id="8ecf3-154">Глубина расширения при развертывании рассылки список для исключения получателей, подключенных к Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="8ecf3-155">Использовать, только если установлен флаг **REBASE_FLAG_FORCE_NO_EX_UPDATES** .</span><span class="sxs-lookup"><span data-stu-id="8ecf3-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="8ecf3-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-156">_pTZTo_</span></span>
  
> <span data-ttu-id="8ecf3-157">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-157">[in] Required.</span></span> <span data-ttu-id="8ecf3-158">Указатель на структуру **TZDEFINITION** , описывающее часовой пояс, который будет базовый адрес которого изменен.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="8ecf3-159">**TZDEFINITION** определен в tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="8ecf3-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="8ecf3-160">pTZMissing</span></span>
  
> <span data-ttu-id="8ecf3-161">[in] Required.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-161">[in] Required.</span></span> <span data-ttu-id="8ecf3-162">Указатель на структуру **TZDEFINITION** , описывающее часовой пояс, который будет предполагается, что если сведения о часовом поясе не указывается на элемент.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="8ecf3-163">Не должно быть значение NULL, но только если установлен флаг **REBASE_FLAG_UPDATE_UNMARKED** .</span><span class="sxs-lookup"><span data-stu-id="8ecf3-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="8ecf3-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-164">_ppError_</span></span>
  
> <span data-ttu-id="8ecf3-165">[out] Указатель на указатель на структуру **MAPIERROR** , содержащий версии, компонент и контекста сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="8ecf3-166">Может быть NULL, при необходимости не расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="8ecf3-167">Бесплатная загрузка с [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ecf3-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="8ecf3-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="8ecf3-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="8ecf3-169">[out] Указатель на указатель на возвращенный интерфейс **IOlkApptRebaser** .</span><span class="sxs-lookup"><span data-stu-id="8ecf3-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8ecf3-170">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8ecf3-170">Return values</span></span>

<span data-ttu-id="8ecf3-171">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ecf3-172">Remarks</span><span class="sxs-lookup"><span data-stu-id="8ecf3-172">Remarks</span></span>

<span data-ttu-id="8ecf3-173">При использовании [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) следует искать адреса этой функции tzmovelib.dll, укажите **HrCreateApptRebaser@44** в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="8ecf3-174">Не все флаги, допустимый в сочетании друг с другом.</span><span class="sxs-lookup"><span data-stu-id="8ecf3-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="8ecf3-175">Дополнительные сведения о различных параметрах, обратитесь к разделу «Глоссарий параметров командной строки для средства обновления данных часового пояса Outlook» в [931667 статья БАЗЫ знаний: как часовой пояс изменения адреса с помощью средства обновления данных часового пояса для Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="8ecf3-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ecf3-176">См. также</span><span class="sxs-lookup"><span data-stu-id="8ecf3-176">See also</span></span>

- [<span data-ttu-id="8ecf3-177">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="8ecf3-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

