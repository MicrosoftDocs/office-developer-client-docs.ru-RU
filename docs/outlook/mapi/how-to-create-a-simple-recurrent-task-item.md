---
title: Создание элемента простой повторяющейся задачи
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 68d7472f993bcc35abbd4b733bae9f137b948608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576843"
---
# <a name="create-a-simple-recurrent-task-item"></a>Создание элемента простой повторяющейся задачи

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы создать для создания элементов задачи можно использовать MAPI. В этом разделе описывается, как создать элемент простого Повторяющаяся задача.
  
Сведения о загрузке, просмотр и запуск кода из приложения mfcmapi (en) и CreateOutlookItemsAddin проекта, указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-a-task-item"></a>Создание элемента задачи

1. Откройте хранилище сообщений. Сведения о том, как открыть хранилище сообщений содержатся [открытии хранилища сообщений](opening-a-message-store.md).
    
2. Откройте папку задачи в хранилище сообщений. Для получения дополнительных сведений см **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в общей папке задачи для создания нового элемента задачи. 
    
4. Задайте свойство **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) и другие свойства, связанные с задач, необходимые для создания Повторяющаяся задача.
    
5. Сохраните новый элемент задачи.
    
`AddTask` Функции в исходном файле Tasks.cpp проекта CreateOutlookItemsAddin демонстрирует следующие действия. `AddTask` Функция принимает параметры в диалоговом окне **Добавить задачу** , которая отображается при нажатии кнопки **Добавить задачу** в примере приложения mfcmapi (en) в меню **надстройки** . `DisplayAddTaskDialog` Функция Tasks.cpp отображает диалоговое окно и передает значения из диалогового окна `AddTask` функции. `DisplayAddTaskDialog` Функция не которые относятся непосредственно к Создание элемента задачи с помощью интерфейса MAPI, поэтому его нет в списке. 
  
> [!IMPORTANT]
> Код в приложении mfcmapi (en) не гарантирует, что при выборе команды **Добавить задачу** в меню **Addins** выбора папки **задач** . Создание элементов задачи в папке, отличной от папки **задач** может привести к непредвиденному поведению. Убедитесь в том, что выбрано папки **задач** перед использованием команды **Добавить задачу** в приложении mfcmapi (en). 
  
`AddTask` Функции приведены ниже. Обратите внимание, что параметр _lpFolder_ , передаваемый `AddTask` функции — указатель на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , который представляет папку, где создается новую задачу. Учитывая _lpFolder_ , который представляет интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Метод **CreateMessage** возвращает код успеха и указатель на указатель на интерфейс **IMessage** . Большая часть `AddTask` код функции управляет Указание свойств для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) подготовки. При вызове метода **SetProps** выполняется успешно, этот метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вызывается внести изменения в хранилище и создание нового элемента задачи. 
  
`AddTask` Функция задает число именованных свойств. Сведения об именованных свойств и как они создаются [С помощью интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)см. Так как именованные свойства, используемые для элементов задач занимают несколько наборов свойств, необходимо соблюдать осторожность при создании параметров для передачи методу [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
`AddTask` Функция использует `BuildWeeklyTaskRecurrencePattern` вспомогательная функция для создания структуры, представляющее Повторение задачи для установки свойства **dispidTaskRecur** . Сведения о структуре повторения задачи `BuildWeeklyTaskRecurrencePattern` работать построений, см [PidLidTaskRecurrence каноническое свойств](pidlidtaskrecurrence-canonical-property.md) и [PidLidRecurrencePattern каноническое](pidlidrecurrencepattern-canonical-property.md). 

Обратите внимание, что при больших различные шаблоны повторения возможны, `BuildWeeklyTaskRecurrencePattern` функции построения только еженедельно повторяющейся. Можно также жестко закодированные для целого ряда предположения, такие как тип календаря (григорианский) с первого дня недели (воскресенье) и число измененных или удаленных экземпляров (нет). Более общего назначения функции создания шаблона повторения необходимо принять следующие виды переменные как параметры. 
  
Ниже приведен полный листинг `AddTask` функции. 
  
```cpp
HRESULT AddTask(LPMAPIFOLDER lpFolder,
            SYSTEMTIME* lpstStart, // PidLidCommonEnd, PidLidTaskDueDate, PidLidTaskRecurrence
            SYSTEMTIME* lpstEnd, // PidLidTaskRecurrence
            SYSTEMTIME* lpstFirstDOW, // PidLidTaskRecurrence
            DWORD dwPeriod, // PidLidTaskRecurrence
            DWORD dwOccurrenceCount, // PidLidTaskRecurrence
            DWORD dwPatternTypeSpecific, // PidLidTaskRecurrence
            LPWSTR szSubject, // PR_SUBJECT_W
            LPWSTR szBody) // PR_BODY_W
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
      MAPINAMEID  rgnmid[ulTaskProps];
      LPMAPINAMEID rgpnmid[ulTaskProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulTaskProps ; i++)
      {
         if (i < ulFirstTaskProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Task;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulTaskProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulTaskProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidTaskMode].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskMode],PT_LONG);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidTaskStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskStatus],PT_LONG);
         spvProps[p_PidLidPercentComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidPercentComplete],PT_DOUBLE);
         spvProps[p_PidLidTaskState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskState],PT_LONG);
         spvProps[p_PidLidTaskRecurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskRecurrence],PT_BINARY);
         spvProps[p_PidLidTaskDeadOccurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDeadOccurrence],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwner].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwner],PT_UNICODE);
         spvProps[p_PidLidTaskFRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFRecurring],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwnership].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwnership],PT_LONG);
         spvProps[p_PidLidTaskAcceptanceState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskAcceptanceState],PT_LONG);
         spvProps[p_PidLidTaskFFixOffline].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFFixOffline],PT_BOOLEAN);
         spvProps[p_PidLidTaskDueDate].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDueDate],PT_SYSTIME);
         spvProps[p_PidLidTaskComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskComplete],PT_SYSTIME);
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag   = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag        = PR_ICON_INDEX;
         spvProps[p_PR_SUBJECT_W].ulPropTag         = PR_SUBJECT_W;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag     = PR_MESSAGE_FLAGS;
         spvProps[p_PR_BODY_W].ulPropTag            = PR_BODY_W;
         spvProps[p_PidLidTaskMode].Value.l = tdmtNothing;
         SYSTEMTIME stStartUTC = {0};
         TzSpecificLocalTimeToSystemTime(NULL,lpstStart,&stStartUTC);
         SystemTimeToFileTime(&stStartUTC,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidTaskStatus].Value.l = tsvNotStarted;
         spvProps[p_PidLidPercentComplete].Value.dbl = 0.0;
         spvProps[p_PidLidTaskState].Value.l = tdsOWNNEW;
         spvProps[p_PidLidTaskDeadOccurrence].Value.b = false;
         spvProps[p_PidLidTaskOwner].Value.lpszW = L"Unknown";
         spvProps[p_PidLidTaskFRecurring].Value.b = true;
         spvProps[p_PidLidTaskOwnership].Value.l = tovNew;
         spvProps[p_PidLidTaskAcceptanceState].Value.l = tdvNone;
         spvProps[p_PidLidTaskFFixOffline].Value.b = true;
         SystemTimeToFileTime(lpstStart,&spvProps[p_PidLidTaskDueDate].Value.ft);
         spvProps[p_PidLidTaskComplete].Value.b = false;
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Task";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x501; // Unassigned Recurring Task
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         spvProps[p_PR_BODY_W].Value.lpszW = szBody;
         hRes = BuildWeeklyTaskRecurrencePattern(
            lpstStart,
            lpstEnd,
            lpstFirstDOW,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.cb,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.lpb);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
            if (SUCCEEDED(hRes))
            {
               hRes = lpMessage->SaveChanges(FORCE_SAVE);
            }
         }
         if (spvProps[p_PidLidTaskRecurrence].Value.bin.lpb)
            delete[] spvProps[p_PidLidTaskRecurrence].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a>См. также

- [Использование интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

