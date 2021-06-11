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

**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI можно использовать для создания элементов задач. В этом разделе описывается, как создать простой элемент повторяющихся задач.
  
Сведения о загрузке, просмотре и запуске кода из приложения MFCMAPI и проекта CreateOutlookItemsAddin, на которые ссылается в этом разделе, см. в статье [Install the Samples Used in This Section.](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-create-a-task-item"></a>Создание элемента задачи

1. Откройте хранилище сообщений. Сведения об открытии магазина сообщений см. в [сайте Opening a Message Store.](opening-a-message-store.md)
    
2. Откройте папку Задачи в хранилище сообщений. Дополнительные сведения см. **в PR_IPM_TASK_ENTRYID** [(PidTagIpmTaskEntryId).](pidtagipmtaskentryid-canonical-property.md)
    
3. Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в папке Задачи для создания нового элемента задачи. 
    
4. Установите **свойство dispidTaskRecur** [(PidLidTaskRecurrence)](pidlidtaskrecurrence-canonical-property.md)и другие свойства, связанные с задачами, необходимые для создания повторяющейся задачи.
    
5. Сохраните новый элемент задачи.
    
Функция  `AddTask` в файле источника Tasks.cpp проекта CreateOutlookItemsAddin демонстрирует эти действия. Функция принимает параметры из диалогового окна Add Task, отображаемого при нажатии кнопки Добавить задачу в меню Addins в примере `AddTask` приложения MFCMAPI.    Функция в Tasks.cpp отображает диалоговое окно и передает значения из диалогового окна  `DisplayAddTaskDialog` в  `AddTask` функцию. Функция напрямую не связана с созданием элемента задачи с  `DisplayAddTaskDialog` помощью MAPI, поэтому он не указан здесь. 
  
> [!IMPORTANT]
> Код в приложении MFCMAPI не гарантирует, что папка **Tasks** была выбрана при нажатии кнопки **Добавить** задачу в меню **Addins.** Создание элементов задач в папке, помимо папки **Задачи,** может привести к неопределяемой модели поведения. Убедитесь, что вы выбрали папку **Задачи** перед использованием команды **Добавить** задачи в приложении MFCMAPI. 
  
Функция  `AddTask` приведена ниже. Обратите внимание, что параметр  _lpFolder,_ переданный функции, представляет собой указатель  `AddTask` [интерфейса IMAPIFolder,](imapifolderimapicontainer.md) который представляет папку, в которой создается новая задача. Учитывая _lpFolder,_ который представляет интерфейс **IMAPIFolder,** код вызывает [метод IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) Метод **CreateMessage** возвращает код успеха и указатель в указатель **интерфейса IMessage.** Большая часть кода функции обрабатывает работу по указанию свойств при подготовке к вызову `AddTask` [метода IMAPIProp::SetProps.](imapiprop-setprops.md) В случае успешного вызова метода **SetProps** используется метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для фиксации изменений в хранилище и создания нового элемента задачи. 
  
Функция  `AddTask` задает ряд именных свойств. Сведения о свойствах с именем и о том, как они создаются, см. в статьи Использование MAPI для создания Outlook [2007 элементов.](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx) Так как названные свойства, используемые для элементов задач, занимают несколько наборов свойств, необходимо позаботиться о том, чтобы параметры здания прошли метод [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
  
Функция использует функцию помощника для создания структуры, представляющей повторение задач для настройки свойства `AddTask` `BuildWeeklyTaskRecurrencePattern` **dispidTaskRecur.** Сведения о структуре повторения задач, создаваемой функцией, см. в рубрике Каноническое свойство  `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) и [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md). 

Обратите внимание, что в то время как возможны различные шаблоны повторения, функция создает только недельный шаблон  `BuildWeeklyTaskRecurrencePattern` повторяемости. Кроме того, трудно закодировать ряд предположений, таких как тип календаря (григорианский), первый день недели (воскресенье) и количество измененных или удаленных экземпляров (нет). Чтобы принять эти параметры в качестве параметров, потребуется более общая функция создания шаблона повторяемого повторения. 
  
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

- [Использование MAPI для создания элементов Outlook 2007 г.](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

