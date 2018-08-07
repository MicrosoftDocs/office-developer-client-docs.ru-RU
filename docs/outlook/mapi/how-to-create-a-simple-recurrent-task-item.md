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
ms.openlocfilehash: 926b33fa3627461139362737f86248f217191534
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808597"
---
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="a8f48-103">Создание элемента простой повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="a8f48-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="a8f48-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8f48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8f48-105">Чтобы создать для создания элементов задачи можно использовать MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8f48-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="a8f48-106">В этом разделе описывается, как создать элемент простого Повторяющаяся задача.</span><span class="sxs-lookup"><span data-stu-id="a8f48-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="a8f48-107">Сведения о загрузке, просмотр и запуск кода из приложения mfcmapi (en) и CreateOutlookItemsAddin проекта, указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="a8f48-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="a8f48-108">Создание элемента задачи</span><span class="sxs-lookup"><span data-stu-id="a8f48-108">To create a task item</span></span>

1. <span data-ttu-id="a8f48-109">Откройте хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8f48-109">Open a message store.</span></span> <span data-ttu-id="a8f48-110">Сведения о том, как открыть хранилище сообщений содержатся [открытии хранилища сообщений](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="a8f48-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="a8f48-111">Откройте папку задачи в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8f48-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="a8f48-112">Для получения дополнительных сведений см **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8f48-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="a8f48-113">Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в общей папке задачи для создания нового элемента задачи.</span><span class="sxs-lookup"><span data-stu-id="a8f48-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="a8f48-114">Задайте свойство **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) и другие свойства, связанные с задач, необходимые для создания Повторяющаяся задача.</span><span class="sxs-lookup"><span data-stu-id="a8f48-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="a8f48-115">Сохраните новый элемент задачи.</span><span class="sxs-lookup"><span data-stu-id="a8f48-115">Save the new task item.</span></span>
    
<span data-ttu-id="a8f48-116">`AddTask` Функции в исходном файле Tasks.cpp проекта CreateOutlookItemsAddin демонстрирует следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a8f48-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="a8f48-117">`AddTask` Функция принимает параметры в диалоговом окне **Добавить задачу** , которая отображается при нажатии кнопки **Добавить задачу** в примере приложения mfcmapi (en) в меню **надстройки** .</span><span class="sxs-lookup"><span data-stu-id="a8f48-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="a8f48-118">`DisplayAddTaskDialog` Функция Tasks.cpp отображает диалоговое окно и передает значения из диалогового окна `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="a8f48-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="a8f48-119">`DisplayAddTaskDialog` Функция не которые относятся непосредственно к Создание элемента задачи с помощью интерфейса MAPI, поэтому его нет в списке.</span><span class="sxs-lookup"><span data-stu-id="a8f48-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a8f48-120">Код в приложении mfcmapi (en) не гарантирует, что при выборе команды **Добавить задачу** в меню **Addins** выбора папки **задач** .</span><span class="sxs-lookup"><span data-stu-id="a8f48-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="a8f48-121">Создание элементов задачи в папке, отличной от папки **задач** может привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="a8f48-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="a8f48-122">Убедитесь в том, что выбрано папки **задач** перед использованием команды **Добавить задачу** в приложении mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="a8f48-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="a8f48-123">`AddTask` Функции приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="a8f48-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="a8f48-124">Обратите внимание, что параметр _lpFolder_ , передаваемый `AddTask` функции — указатель на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , который представляет папку, где создается новую задачу.</span><span class="sxs-lookup"><span data-stu-id="a8f48-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="a8f48-125">Учитывая _lpFolder_ , который представляет интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f48-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="a8f48-126">Метод **CreateMessage** возвращает код успеха и указатель на указатель на интерфейс **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="a8f48-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="a8f48-127">Большая часть `AddTask` код функции управляет Указание свойств для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) подготовки.</span><span class="sxs-lookup"><span data-stu-id="a8f48-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="a8f48-128">При вызове метода **SetProps** выполняется успешно, этот метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вызывается внести изменения в хранилище и создание нового элемента задачи.</span><span class="sxs-lookup"><span data-stu-id="a8f48-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="a8f48-129">`AddTask` Функция задает число именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="a8f48-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="a8f48-130">Сведения об именованных свойств и как они создаются [С помощью интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="a8f48-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="a8f48-131">Так как именованные свойства, используемые для элементов задач занимают несколько наборов свойств, необходимо соблюдать осторожность при создании параметров для передачи методу [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f48-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="a8f48-132">`AddTask` Функция использует `BuildWeeklyTaskRecurrencePattern` вспомогательная функция для создания структуры, представляющее Повторение задачи для установки свойства **dispidTaskRecur** .</span><span class="sxs-lookup"><span data-stu-id="a8f48-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="a8f48-133">Сведения о структуре повторения задачи `BuildWeeklyTaskRecurrencePattern` работать построений, см [PidLidTaskRecurrence каноническое свойств](pidlidtaskrecurrence-canonical-property.md) и [PidLidRecurrencePattern каноническое](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="a8f48-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="a8f48-134">Обратите внимание, что при больших различные шаблоны повторения возможны, `BuildWeeklyTaskRecurrencePattern` функции построения только еженедельно повторяющейся.</span><span class="sxs-lookup"><span data-stu-id="a8f48-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="a8f48-135">Можно также жестко закодированные для целого ряда предположения, такие как тип календаря (григорианский) с первого дня недели (воскресенье) и число измененных или удаленных экземпляров (нет).</span><span class="sxs-lookup"><span data-stu-id="a8f48-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="a8f48-136">Более общего назначения функции создания шаблона повторения необходимо принять следующие виды переменные как параметры.</span><span class="sxs-lookup"><span data-stu-id="a8f48-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="a8f48-137">Ниже приведен полный листинг `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="a8f48-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a8f48-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a8f48-138">See also</span></span>

- [<span data-ttu-id="a8f48-139">Использование интерфейса MAPI для создания элементов Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="a8f48-139">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

