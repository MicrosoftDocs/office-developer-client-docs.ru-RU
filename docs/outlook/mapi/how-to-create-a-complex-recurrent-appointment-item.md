---
title: Создание сложных повторяющейся встречи
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da9626da-5ba5-4f18-954c-4e23971d23e8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 524fa44ddd1325b51a7389d712ac045afbefb8d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808593"
---
# <a name="create-a-complex-recurrent-appointment-item"></a><span data-ttu-id="03789-103">Создание сложных повторяющейся встречи</span><span class="sxs-lookup"><span data-stu-id="03789-103">Create a complex recurrent appointment item</span></span>
  
<span data-ttu-id="03789-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03789-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03789-105">MAPI можно использовать для создания элементов повторяющейся встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-105">MAPI can be used to create recurring appointment items.</span></span>
  
<span data-ttu-id="03789-106">Сведения о загрузке, просмотр и запуск кода из приложения mfcmapi (en) и CreateOutlookItemsAddin проекта, указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="03789-106">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-an-appointment-item"></a><span data-ttu-id="03789-107">Создание элемента встречи</span><span class="sxs-lookup"><span data-stu-id="03789-107">To create an appointment item</span></span>

1. <span data-ttu-id="03789-108">Откройте хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="03789-108">Open a message store.</span></span> <span data-ttu-id="03789-109">Сведения о том, как открыть хранилище сообщений содержатся [открытии хранилища сообщений](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="03789-109">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="03789-110">Откройте папку календаря в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="03789-110">Open a Calendar folder in the message store.</span></span> <span data-ttu-id="03789-111">В разделе **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03789-111">See **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="03789-112">Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в общей папке календаря для создания нового элемента встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-112">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Calendar folder to create the new appointment item.</span></span> 
    
4. <span data-ttu-id="03789-113">Задайте свойство **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) и другие свойства, необходимые для создания повторяющейся встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-113">Set the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property and other properties required to create a recurrent appointment.</span></span>
    
5. <span data-ttu-id="03789-114">Сохраните новый элемент встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-114">Save the new appointment item.</span></span>
    
<span data-ttu-id="03789-115">`AddAppointment` Функции в исходном файле Appointments.cpp проекта CreateOutlookItemsAddin демонстрирует следующие действия.</span><span class="sxs-lookup"><span data-stu-id="03789-115">The  `AddAppointment` function in the Appointments.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="03789-116">`AddAppointment` Функция принимает параметры в диалоговом окне **Добавление встречи** , которая отображается при нажатии кнопки **Добавить встречи** в меню **надстройки** в примере приложения mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="03789-116">The  `AddAppointment` function takes parameters from the **Add Appointment** dialog box that is displayed when you click **Add Appointment** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="03789-117">`DisplayAddAppointmentDialog` Функция Appointments.cpp отображает диалоговое окно и передает значения из диалогового окна `AddAppointment` функции.</span><span class="sxs-lookup"><span data-stu-id="03789-117">The  `DisplayAddAppointmentDialog` function in Appointments.cpp displays the dialog box and passes values from the dialog box to the  `AddAppointment` function.</span></span> <span data-ttu-id="03789-118">`DisplayAddAppointmentDialog` Функция не которые относятся непосредственно к созданию элемента встречи с помощью интерфейса MAPI, поэтому его нет в списке.</span><span class="sxs-lookup"><span data-stu-id="03789-118">The  `DisplayAddAppointmentDialog` function does not relate directly to creating an appointment item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="03789-119">Код в приложении mfcmapi (en) не гарантирует, что при выборе команды **Добавить встречи** в меню **Addins** был выбран в папке **календаря** .</span><span class="sxs-lookup"><span data-stu-id="03789-119">The code in the MFCMAPI application does not ensure that the **Calendar** folder has been selected when you click the **Add Appointment** command on the **Addins** menu.</span></span> <span data-ttu-id="03789-120">Создание элемента встречи в папке, отличной от папки **календаря** может привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="03789-120">Creating an appointment item in a folder other than the **Calendar** folder can cause undefined behavior.</span></span> <span data-ttu-id="03789-121">Убедитесь в том, что выбрано в папке **календаря** перед использованием команды **Добавить встречи** в приложении mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="03789-121">Make sure that you have selected the **Calendar** folder before using the **Add Appointment** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="03789-122">`AddAppointment` Метод приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="03789-122">The  `AddAppointment` method is listed below.</span></span> <span data-ttu-id="03789-123">Обратите внимание, что параметр _lpFolder_ , передаваемый `AddAppointment` метод — это указатель на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , который представляет папку, где создается повторяющейся встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-123">Note that the  _lpFolder_ parameter passed to the  `AddAppointment` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the recurrent appointment is created.</span></span> <span data-ttu-id="03789-124">Учитывая параметр _lpFolder_ , который представляет интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="03789-124">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="03789-125">Метод **CreateMessage** возвращает код успеха и указатель на указатель на интерфейс **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="03789-125">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="03789-126">Большая часть `AddAppointment` код функции управляет Указание свойств для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) подготовки.</span><span class="sxs-lookup"><span data-stu-id="03789-126">Most of the  `AddAppointment` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="03789-127">При вызове метода **SetProps** выполняется успешно, этот метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вызывается внести изменения в хранилище и создание нового элемента календаря.</span><span class="sxs-lookup"><span data-stu-id="03789-127">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new calendar item.</span></span> 
  
<span data-ttu-id="03789-128">`AddAppointment` Функция задает число именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="03789-128">The  `AddAppointment` function sets a number of named properties.</span></span> <span data-ttu-id="03789-129">Сведения об именованных свойств и как они создаются [С помощью интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="03789-129">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="03789-130">Так как именованные свойства, используемые для элементов встречи занимают несколько наборов свойств, необходимо соблюдать осторожность при создании параметров для передачи методу [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="03789-130">Because the named properties used for appointment items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="03789-131">`AddAppointment` Функция использует несколько вспомогательные функции для создания структуры для различных свойств, связанных с встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-131">The  `AddAppointment` function uses several helper functions to build a structure for various appointment-related properties.</span></span> <span data-ttu-id="03789-132">`BuildTimeZoneStruct` И `BuildTimeZoneDefinition` вспомогательные функции используются для построения структуры, указывающая свойства времени относящиеся к зоне.</span><span class="sxs-lookup"><span data-stu-id="03789-132">The  `BuildTimeZoneStruct` and  `BuildTimeZoneDefinition` helper functions are used to build a structure that specifies the time-zone-related properties.</span></span> <span data-ttu-id="03789-133">Свойства времени относящиеся к зоне, **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([ PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) и **dispidApptTZDefEndDisplay** ([ PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), и они рассматриваются в соответствующие разделы [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28v=EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="03789-133">The time-zone-related properties are **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)), and **dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), and they are discussed in the corresponding sections of [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> 

<span data-ttu-id="03789-134">`BuildGlobalObjectID` Функция используется для создания структуры, указывающее, **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) и **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) свойства, которые рассматриваются в соответствующие разделы [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28v=EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="03789-134">The  `BuildGlobalObjectID` function is used to build a structure that specifies the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) and **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) properties, which are discussed in the corresponding sections of [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> <span data-ttu-id="03789-135">Структура, которая задает свойство **dispidApptRecur** построен с использованием `BuildWeeklyAppointmentRecurrencePattern` функции.</span><span class="sxs-lookup"><span data-stu-id="03789-135">The structure that specifies the **dispidApptRecur** property is built using the  `BuildWeeklyAppointmentRecurrencePattern` function.</span></span> 

<span data-ttu-id="03789-136">Сведения о структуре, созданных с `BuildWeeklyAppointmentRecurrencePattern` работать, [Каноническое свойству PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)см.</span><span class="sxs-lookup"><span data-stu-id="03789-136">For information about the structure built by the  `BuildWeeklyAppointmentRecurrencePattern` function, see [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="03789-137">Обратите внимание, что при больших различные шаблоны повторения встречи возможны, `BuildWeeklyAppointmentRecurrencePattern` функции построения только еженедельно шаблона повторения встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-137">Note that while a large variety of appointment recurrence patterns are possible, the  `BuildWeeklyAppointmentRecurrencePattern` function only builds a weekly appointment recurrence pattern.</span></span> <span data-ttu-id="03789-138">Также использует несколько значений, жестко, такие как тип календаря (григорианский) с первого дня недели (воскресенье) и количество изменены или удалены экземпляры (нет).</span><span class="sxs-lookup"><span data-stu-id="03789-138">It also uses several hard-coded values, such as the calendar type (Gregorian), the first day of the week (Sunday), and number of modified or deleted instances (none).</span></span> <span data-ttu-id="03789-139">Более общего назначения необходимо принять следующие виды переменных в качестве параметров функции создания шаблона повторения встречи.</span><span class="sxs-lookup"><span data-stu-id="03789-139">A more general purpose appointment recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="03789-140">Ниже приведен полный листинг `AddAppointment` функции.</span><span class="sxs-lookup"><span data-stu-id="03789-140">The following is the complete listing of the  `AddAppointment` function.</span></span> 
  
```cpp
HRESULT AddAppointment(LPMAPIFOLDER lpFolder,
               SYSTEMTIME* lpstStartDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstEndDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstStartFirstUST, // PidLidAppointmentStartWhole, PidLidCommonStart, PR_START_DATE
               SYSTEMTIME* lpstEndFirstUST, // PidLidAppointmentEndWhole, PidLidCommonEnd, PR_END_DATE
               SYSTEMTIME* lpszClipStartUST, // PidLidClipStart
               SYSTEMTIME* lpstClipEndUST, // PidLidClipEnd
               SYSTEMTIME* lpstFirstDOW, // PidLidAppointmentRecur
               DWORD dwStartOffsetLocal, // PidLidAppointmentRecur
               DWORD dwEndOffsetLocal, // PidLidAppointmentRecur
               DWORD dwPeriod, // PidLidAppointmentRecur
               DWORD dwOccurrenceCount, // PidLidAppointmentRecur
               DWORD dwPatternTypeSpecific, // PidLidAppointmentRecur
               ULONG ulDuration, // PidLidAppointmentDuration
               LPWSTR szSubject, // PR_SUBJECT_W
               LPWSTR szLocation, // PidLidLocation
               LPWSTR szPattern) // PidLidRecurrencePattern
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulAppointmentProps];
      LPMAPINAMEID rgpnmid[ulAppointmentProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulAppointmentProps ; i++)
      {
         if (i < ulFirstMeetingProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Appointment;
         else if (i < ulFirstCommonProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Meeting;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulAppointmentProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulAppointmentProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidAppointmentSequence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentSequence],PT_LONG);
         spvProps[p_PidLidBusyStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidBusyStatus],PT_LONG);
         spvProps[p_PidLidLocation].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidLocation],PT_UNICODE);
         spvProps[p_PidLidAppointmentStartWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentStartWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentEndWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentEndWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentDuration].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentDuration],PT_LONG);
         spvProps[p_PidLidAppointmentColor].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentColor],PT_LONG);
         spvProps[p_PidLidResponseStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidResponseStatus],PT_LONG);
         spvProps[p_PidLidRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurring],PT_BOOLEAN);
         spvProps[p_PidLidClipStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipStart],PT_SYSTIME);
         spvProps[p_PidLidClipEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipEnd],PT_SYSTIME);
         spvProps[p_PidLidTimeZoneStruct].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneStruct],PT_BINARY);
         spvProps[p_PidLidTimeZoneDescription].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneDescription],PT_UNICODE);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].ulPropTag
           = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionRecur],
           PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionStartDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionEndDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentRecur].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentRecur],PT_BINARY);
         spvProps[p_PidLidRecurrenceType].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrenceType],PT_LONG);
         spvProps[p_PidLidRecurrencePattern].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrencePattern],PT_UNICODE);
         spvProps[p_PidLidIsRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidIsRecurring],PT_BOOLEAN);
         spvProps[p_PidLidGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCleanGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCleanGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCommonStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonStart],PT_SYSTIME);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidSideEffects].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidSideEffects],PT_LONG);
         spvProps[p_PR_SUBJECT_W].ulPropTag          = PR_SUBJECT_W;
         spvProps[p_PR_START_DATE].ulPropTag         = PR_START_DATE;
         spvProps[p_PR_END_DATE].ulPropTag           = PR_END_DATE;
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag    = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag         = PR_ICON_INDEX;
         spvProps[p_PR_CONVERSATION_INDEX].ulPropTag   = PR_CONVERSATION_INDEX;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag      = PR_MESSAGE_FLAGS;
         spvProps[p_PidLidAppointmentSequence].Value.l = 0;
         spvProps[p_PidLidBusyStatus].Value.l = olBusy;
         spvProps[p_PidLidLocation].Value.lpszW = szLocation;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidAppointmentStartWhole].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidAppointmentEndWhole].Value.ft);
         spvProps[p_PidLidAppointmentDuration].Value.l = ulDuration;
         spvProps[p_PidLidAppointmentColor].Value.l = 0; // No color
         spvProps[p_PidLidResponseStatus].Value.l = respNone;
         spvProps[p_PidLidRecurring].Value.b = true;
         SystemTimeToFileTime(lpszClipStartUST,&spvProps[p_PidLidClipStart].Value.ft);
         SystemTimeToFileTime(lpstClipEndUST,&spvProps[p_PidLidClipEnd].Value.ft);
         SYSTEMTIME stStandard = {0};
         stStandard.wMonth = 0xB;
         stStandard.wDay = 0x1;
         stStandard.wHour = 0x2;
         SYSTEMTIME stDaylight = {0};
         stDaylight.wMonth = 0x3;
         stDaylight.wDay = 0x2;
         stDaylight.wHour = 0x2;
         hRes = BuildTimeZoneStruct(
            300,
            0,
            (DWORD)-60,
            &stStandard,
            &stDaylight,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.cb,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb);
         spvProps[p_PidLidTimeZoneDescription].Value.lpszW = L"(GMT-05:00) Eastern Time (US & Canada)";
         SYSTEMTIME stRule1Standard = {0};
         stRule1Standard.wMonth = 0xA;
         stRule1Standard.wDay = 0x5;
         stRule1Standard.wHour = 0x2;
         SYSTEMTIME stRule1Daylight = {0};
         stRule1Daylight.wMonth = 0x4;
         stRule1Daylight.wDay = 0x1;
         stRule1Daylight.wHour = 0x2;
         if (SUCCEEDED(hRes)) hRes = BuildTimeZoneDefinition(
            L"Eastern Standard Time",
            0, // TZRule Flags
            2006, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stRule1Standard, // stStandardDate
            &stRule1Daylight, // stDaylightDate
            TZRULE_FLAG_EFFECTIVE_TZREG, // TZRule Flags
            2007, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stStandard, // stStandardDate
            &stDaylight, // stDaylightDate
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         if (SUCCEEDED(hRes)) hRes = BuildWeeklyAppointmentRecurrencePattern(
            lpstStartDateLocal,
            lpstEndDateLocal,
            lpstFirstDOW,
            dwStartOffsetLocal,
            dwEndOffsetLocal,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.lpb);
         spvProps[p_PidLidRecurrenceType].Value.l = rectypeWeekly;
         spvProps[p_PidLidRecurrencePattern].Value.lpszW = szPattern;
         spvProps[p_PidLidIsRecurring].Value.b = true;
         if (SUCCEEDED(hRes)) hRes = BuildGlobalObjectId(
            &spvProps[p_PidLidGlobalObjectId].Value.bin.cb,
            &spvProps[p_PidLidGlobalObjectId].Value.bin.lpb);
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.cb  = spvProps[p_PidLidGlobalObjectId].Value.bin.cb;
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.lpb = spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidCommonStart].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidSideEffects].Value.l
            = seOpenToDelete | seOpenToCopy | seOpenToMove | seCoerceToInbox | seOpenForCtxMenu;
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PR_START_DATE].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PR_END_DATE].Value.ft);
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Appointment";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x00000401; // Recurring Appointment
         if (SUCCEEDED(hRes)) hRes = BuildConversationIndex(
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         if (SUCCEEDED(hRes)) hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SaveChanges(FORCE_SAVE);
         }
         if (spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb)
            delete[] spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb;
         if (spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionStartDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionEndDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         if (spvProps[p_PidLidAppointmentRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentRecur].Value.bin.lpb;
         if (spvProps[p_PidLidGlobalObjectId].Value.bin.lpb)
            delete[] spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         // Do not delete p_PidLidCleanGlobalObjectId, it was borrowed from p_PidLidGlobalObjectId
         if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
            delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a><span data-ttu-id="03789-141">См. также</span><span class="sxs-lookup"><span data-stu-id="03789-141">See also</span></span>

- [<span data-ttu-id="03789-142">Использование интерфейса MAPI для создания элементов Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="03789-142">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

