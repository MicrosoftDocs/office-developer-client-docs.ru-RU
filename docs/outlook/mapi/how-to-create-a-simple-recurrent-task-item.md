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
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="88339-103">Создание простого элемента повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="88339-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="88339-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88339-105">MAPI можно использовать для создания элементов задач.</span><span class="sxs-lookup"><span data-stu-id="88339-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="88339-106">В этом разделе описывается создание простого элемента повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="88339-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="88339-107">Сведения о загрузке, просмотре и запуске кода из приложения MFCMAPI и проекта CreateOutlookItemsAddin, на которые ссылается этот раздел, см. в разделе ["Установка](how-to-install-the-samples-used-in-this-section.md)примеров, используемых в этом разделе".</span><span class="sxs-lookup"><span data-stu-id="88339-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="88339-108">Создание элемента задачи</span><span class="sxs-lookup"><span data-stu-id="88339-108">To create a task item</span></span>

1. <span data-ttu-id="88339-109">Откройте хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="88339-109">Open a message store.</span></span> <span data-ttu-id="88339-110">Сведения о том, как открыть хранилище сообщений, см. в [открываемом хранилище сообщений.](opening-a-message-store.md)</span><span class="sxs-lookup"><span data-stu-id="88339-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="88339-111">Откройте папку "Задачи" в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="88339-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="88339-112">Дополнительные сведения **см. в PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId).](pidtagipmtaskentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88339-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="88339-113">Вызовите [метод IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в папке Tasks, чтобы создать новый элемент задачи.</span><span class="sxs-lookup"><span data-stu-id="88339-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="88339-114">Задайте свойство **dispidTaskRecur** ([PidLidTaskRecurrence)](pidlidtaskrecurrence-canonical-property.md)и другие связанные с задачами свойства, необходимые для создания повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="88339-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="88339-115">Сохраните новый элемент задачи.</span><span class="sxs-lookup"><span data-stu-id="88339-115">Save the new task item.</span></span>
    
<span data-ttu-id="88339-116">Функция  `AddTask` в файле источника Tasks.cpp проекта CreateOutlookItemsAddin демонстрирует эти шаги.</span><span class="sxs-lookup"><span data-stu-id="88339-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="88339-117">Функция принимает параметры в диалоговом окне "Добавление задачи", которое отображается при нажатии кнопки "Добавить задачу" в меню "Надстройки" в примере приложения `AddTask` MFCMAPI.   </span><span class="sxs-lookup"><span data-stu-id="88339-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="88339-118">Функция в Tasks.cpp отображает диалоговое окно и передает значения из диалоговых окна  `DisplayAddTaskDialog`  `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="88339-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="88339-119">Функция  `DisplayAddTaskDialog` не связана напрямую с созданием элемента задачи с помощью MAPI, поэтому она не указана здесь.</span><span class="sxs-lookup"><span data-stu-id="88339-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="88339-120">Код в приложении MFCMAPI не гарантирует, что папка **"Задачи"** выбрана при нажатии команды "Добавить задачу" в меню  **"Надстройки".**</span><span class="sxs-lookup"><span data-stu-id="88339-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="88339-121">Создание элементов задач в папке, не вложенной в папку **"Задачи",** может привести к неопределяемой поведению.</span><span class="sxs-lookup"><span data-stu-id="88339-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="88339-122">Убедитесь, что папка **"Задачи"** выбрана перед использованием команды **"Добавить** задачу" в приложении MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="88339-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="88339-123">Функция  `AddTask` приведена ниже.</span><span class="sxs-lookup"><span data-stu-id="88339-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="88339-124">Обратите внимание, что параметр  _lpFolder,_ переданный функции, является указателем на  `AddTask` [интерфейс IMAPIFolder,](imapifolderimapicontainer.md) который представляет папку, в которой создается новая задача.</span><span class="sxs-lookup"><span data-stu-id="88339-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="88339-125">С _учетом lpFolder,_ который представляет интерфейс **IMAPIFolder,** код вызывает метод [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="88339-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="88339-126">Метод **CreateMessage** возвращает код успешности и указатель на указатель на **интерфейс IMessage.**</span><span class="sxs-lookup"><span data-stu-id="88339-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="88339-127">Большая часть кода функции обрабатывает работу по указанию свойств при подготовке к вызову метода `AddTask` [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="88339-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="88339-128">Если вызов метода **SetProps** будет успешным, будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для фиксации изменений в хранилище и создания нового элемента задачи.</span><span class="sxs-lookup"><span data-stu-id="88339-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="88339-129">Функция  `AddTask` задает ряд именуемого свойства.</span><span class="sxs-lookup"><span data-stu-id="88339-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="88339-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="88339-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="88339-131">Так как именуемые свойства, используемые для элементов задач, занимают несколько наборов свойств, при построении параметров, которые необходимо передать методу [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) необходимо быть очень внимательной.</span><span class="sxs-lookup"><span data-stu-id="88339-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="88339-132">Функция использует helper function для создания структуры, представляющей повторение задачи для настройки `AddTask` `BuildWeeklyTaskRecurrencePattern` свойства **dispidTaskRecur.**</span><span class="sxs-lookup"><span data-stu-id="88339-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="88339-133">Сведения о структуре повторения задачи, которую создает функция, см. в сведениях о каноническом свойстве `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) и [PidLidRecurrencePattern.](pidlidrecurrencepattern-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88339-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="88339-134">Обратите внимание, что несмотря на то что возможно большое количество шаблонов повторения, функция создает только еженедельный  `BuildWeeklyTaskRecurrencePattern` шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="88339-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="88339-135">Кроме того, он жестко задает код для ряда предположений, таких как тип календаря (григорианский), первый день недели (воскресенье) и количество измененных или удаленных экземпляров (нет).</span><span class="sxs-lookup"><span data-stu-id="88339-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="88339-136">Функция создания шаблона повторения более общего назначения должна принимать эти виды переменных в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="88339-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="88339-137">Ниже приводится полный список  `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="88339-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="88339-138">См. также</span><span class="sxs-lookup"><span data-stu-id="88339-138">See also</span></span>

- [<span data-ttu-id="88339-139">Использование MAPI для создания элементов Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="88339-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

