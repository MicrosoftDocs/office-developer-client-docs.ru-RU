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
ms.openlocfilehash: ad81ac74f517b36029d29f8a6ed1e1dfcb28fade
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583668"
---
# <a name="create-a-complex-recurrent-appointment-item"></a>Создание сложных повторяющейся встречи
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
MAPI можно использовать для создания элементов повторяющейся встречи.
  
Сведения о загрузке, просмотр и запуск кода из приложения mfcmapi (en) и CreateOutlookItemsAddin проекта, указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-an-appointment-item"></a>Создание элемента встречи

1. Откройте хранилище сообщений. Сведения о том, как открыть хранилище сообщений содержатся [открытии хранилища сообщений](opening-a-message-store.md).
    
2. Откройте папку календаря в хранилище сообщений. В разделе **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).
    
3. Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в общей папке календаря для создания нового элемента встречи. 
    
4. Задайте свойство **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) и другие свойства, необходимые для создания повторяющейся встречи.
    
5. Сохраните новый элемент встречи.
    
`AddAppointment` Функции в исходном файле Appointments.cpp проекта CreateOutlookItemsAddin демонстрирует следующие действия. `AddAppointment` Функция принимает параметры в диалоговом окне **Добавление встречи** , которая отображается при нажатии кнопки **Добавить встречи** в меню **надстройки** в примере приложения mfcmapi (en). `DisplayAddAppointmentDialog` Функция Appointments.cpp отображает диалоговое окно и передает значения из диалогового окна `AddAppointment` функции. `DisplayAddAppointmentDialog` Функция не которые относятся непосредственно к созданию элемента встречи с помощью интерфейса MAPI, поэтому его нет в списке. 
  
> [!IMPORTANT]
> Код в приложении mfcmapi (en) не гарантирует, что при выборе команды **Добавить встречи** в меню **Addins** был выбран в папке **календаря** . Создание элемента встречи в папке, отличной от папки **календаря** может привести к непредвиденному поведению. Убедитесь в том, что выбрано в папке **календаря** перед использованием команды **Добавить встречи** в приложении mfcmapi (en). 
  
`AddAppointment` Метод приведены ниже. Обратите внимание, что параметр _lpFolder_ , передаваемый `AddAppointment` метод — это указатель на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , который представляет папку, где создается повторяющейся встречи. Учитывая параметр _lpFolder_ , который представляет интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Метод **CreateMessage** возвращает код успеха и указатель на указатель на интерфейс **IMessage** . Большая часть `AddAppointment` код функции управляет Указание свойств для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) подготовки. При вызове метода **SetProps** выполняется успешно, этот метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вызывается внести изменения в хранилище и создание нового элемента календаря. 
  
`AddAppointment` Функция задает число именованных свойств. Сведения об именованных свойств и как они создаются [С помощью интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)см. Так как именованные свойства, используемые для элементов встречи занимают несколько наборов свойств, необходимо соблюдать осторожность при создании параметров для передачи методу [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
`AddAppointment` Функция использует несколько вспомогательные функции для создания структуры для различных свойств, связанных с встречи. `BuildTimeZoneStruct` И `BuildTimeZoneDefinition` вспомогательные функции используются для построения структуры, указывающая свойства времени относящиеся к зоне. Свойства времени относящиеся к зоне, **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([ PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) и **dispidApptTZDefEndDisplay** ([ PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), и они рассматриваются в соответствующие разделы [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28v=EXCHG.80%29.aspx). 

`BuildGlobalObjectID` Функция используется для создания структуры, указывающее, **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) и **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) свойства, которые рассматриваются в соответствующие разделы [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28v=EXCHG.80%29.aspx). Структура, которая задает свойство **dispidApptRecur** построен с использованием `BuildWeeklyAppointmentRecurrencePattern` функции. 

Сведения о структуре, созданных с `BuildWeeklyAppointmentRecurrencePattern` работать, [Каноническое свойству PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)см. Обратите внимание, что при больших различные шаблоны повторения встречи возможны, `BuildWeeklyAppointmentRecurrencePattern` функции построения только еженедельно шаблона повторения встречи. Также использует несколько значений, жестко, такие как тип календаря (григорианский) с первого дня недели (воскресенье) и количество изменены или удалены экземпляры (нет). Более общего назначения необходимо принять следующие виды переменных в качестве параметров функции создания шаблона повторения встречи. 
  
Ниже приведен полный листинг `AddAppointment` функции. 
  
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

## <a name="see-also"></a>См. также

- [Использование интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

