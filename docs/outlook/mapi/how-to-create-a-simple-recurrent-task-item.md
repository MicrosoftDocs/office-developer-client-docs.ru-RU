---
title: Создание простого элемента повторяющейся задачи
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345474"
---
# <a name="create-a-simple-recurrent-task-item"></a>Создание простого элемента повторяющейся задачи

**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI можно использовать для создания элементов задач. В этом разделе описывается создание простого элемента повторяющейся задачи.
  
Сведения о загрузке, просмотре и запуске кода из приложения MFCMAPI и проекта CreateOutlookItemsAddin, на которые ссылается этот раздел, см. в разделе ["Установка](how-to-install-the-samples-used-in-this-section.md)примеров, используемых в этом разделе".

### <a name="to-create-a-task-item"></a>Создание элемента задачи

1. Откройте хранилище сообщений. Сведения о том, как открыть хранилище сообщений, см. в [открываемом хранилище сообщений.](opening-a-message-store.md)
    
2. Откройте папку "Задачи" в хранилище сообщений. Дополнительные сведения **см. в PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId).](pidtagipmtaskentryid-canonical-property.md)
    
3. Вызовите [метод IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в папке Tasks, чтобы создать новый элемент задачи. 
    
4. Задайте свойство **dispidTaskRecur** ([PidLidTaskRecurrence)](pidlidtaskrecurrence-canonical-property.md)и другие связанные с задачами свойства, необходимые для создания повторяющейся задачи.
    
5. Сохраните новый элемент задачи.
    
Функция  `AddTask` в файле источника Tasks.cpp проекта CreateOutlookItemsAddin демонстрирует эти шаги. Функция принимает параметры в диалоговом окне "Добавление задачи", которое отображается при нажатии кнопки "Добавить задачу" в меню "Надстройки" в примере приложения `AddTask` MFCMAPI.    Функция в Tasks.cpp отображает диалоговое окно и передает значения из диалоговых окна  `DisplayAddTaskDialog`  `AddTask` функции. Функция  `DisplayAddTaskDialog` не связана напрямую с созданием элемента задачи с помощью MAPI, поэтому она не указана здесь. 
  
> [!IMPORTANT]
> Код в приложении MFCMAPI не гарантирует, что папка **"Задачи"** выбрана при нажатии команды "Добавить задачу" в меню  **"Надстройки".** Создание элементов задач в папке, не вложенной в папку **"Задачи",** может привести к неопределяемой поведению. Убедитесь, что папка **"Задачи"** выбрана перед использованием команды **"Добавить** задачу" в приложении MFCMAPI. 
  
Функция  `AddTask` приведена ниже. Обратите внимание, что параметр  _lpFolder,_ переданный функции, является указателем на  `AddTask` [интерфейс IMAPIFolder,](imapifolderimapicontainer.md) который представляет папку, в которой создается новая задача. С _учетом lpFolder,_ который представляет интерфейс **IMAPIFolder,** код вызывает метод [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) Метод **CreateMessage** возвращает код успешности и указатель на указатель на **интерфейс IMessage.** Большая часть кода функции обрабатывает работу по указанию свойств при подготовке к вызову метода `AddTask` [IMAPIProp::SetProps.](imapiprop-setprops.md) Если вызов метода **SetProps** будет успешным, будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для фиксации изменений в хранилище и создания нового элемента задачи. 
  
Функция  `AddTask` задает ряд именуемого свойства. For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx). Так как именуемые свойства, используемые для элементов задач, занимают несколько наборов свойств, при построении параметров, которые необходимо передать методу [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) необходимо быть очень внимательной. 
  
Функция использует helper function для создания структуры, представляющей повторение задачи для настройки `AddTask` `BuildWeeklyTaskRecurrencePattern` свойства **dispidTaskRecur.** Сведения о структуре повторения задачи, которую создает функция, см. в сведениях о каноническом свойстве `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) и [PidLidRecurrencePattern.](pidlidrecurrencepattern-canonical-property.md) 

Обратите внимание, что несмотря на то что возможно большое количество шаблонов повторения, функция создает только еженедельный  `BuildWeeklyTaskRecurrencePattern` шаблон повторения. Кроме того, он жестко задает код для ряда предположений, таких как тип календаря (григорианский), первый день недели (воскресенье) и количество измененных или удаленных экземпляров (нет). Функция создания шаблона повторения более общего назначения должна принимать эти виды переменных в качестве параметров. 
  
Ниже приводится полный список  `AddTask` функции. 
  
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

- [Использование MAPI для создания элементов Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

