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
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="6bd42-103">Создание простого элемента повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="6bd42-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="6bd42-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bd42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bd42-105">MAPI можно использовать для создания элементов задач.</span><span class="sxs-lookup"><span data-stu-id="6bd42-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="6bd42-106">В этом разделе описывается, как создать простой элемент повторяющихся задач.</span><span class="sxs-lookup"><span data-stu-id="6bd42-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="6bd42-107">Сведения о загрузке, просмотре и запуске кода из приложения MFCMAPI и проекта CreateOutlookItemsAddin, на которые ссылается в этом разделе, см. в статье [Install the Samples Used in This Section.](how-to-install-the-samples-used-in-this-section.md)</span><span class="sxs-lookup"><span data-stu-id="6bd42-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="6bd42-108">Создание элемента задачи</span><span class="sxs-lookup"><span data-stu-id="6bd42-108">To create a task item</span></span>

1. <span data-ttu-id="6bd42-109">Откройте хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6bd42-109">Open a message store.</span></span> <span data-ttu-id="6bd42-110">Сведения об открытии магазина сообщений см. в [сайте Opening a Message Store.](opening-a-message-store.md)</span><span class="sxs-lookup"><span data-stu-id="6bd42-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="6bd42-111">Откройте папку Задачи в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6bd42-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="6bd42-112">Дополнительные сведения см. **в PR_IPM_TASK_ENTRYID** [(PidTagIpmTaskEntryId).](pidtagipmtaskentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6bd42-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="6bd42-113">Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) в папке Задачи для создания нового элемента задачи.</span><span class="sxs-lookup"><span data-stu-id="6bd42-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="6bd42-114">Установите **свойство dispidTaskRecur** [(PidLidTaskRecurrence)](pidlidtaskrecurrence-canonical-property.md)и другие свойства, связанные с задачами, необходимые для создания повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="6bd42-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="6bd42-115">Сохраните новый элемент задачи.</span><span class="sxs-lookup"><span data-stu-id="6bd42-115">Save the new task item.</span></span>
    
<span data-ttu-id="6bd42-116">Функция  `AddTask` в файле источника Tasks.cpp проекта CreateOutlookItemsAddin демонстрирует эти действия.</span><span class="sxs-lookup"><span data-stu-id="6bd42-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="6bd42-117">Функция принимает параметры из диалогового окна Add Task, отображаемого при нажатии кнопки Добавить задачу в меню Addins в примере `AddTask` приложения MFCMAPI.   </span><span class="sxs-lookup"><span data-stu-id="6bd42-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="6bd42-118">Функция в Tasks.cpp отображает диалоговое окно и передает значения из диалогового окна  `DisplayAddTaskDialog` в  `AddTask` функцию.</span><span class="sxs-lookup"><span data-stu-id="6bd42-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="6bd42-119">Функция напрямую не связана с созданием элемента задачи с  `DisplayAddTaskDialog` помощью MAPI, поэтому он не указан здесь.</span><span class="sxs-lookup"><span data-stu-id="6bd42-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6bd42-120">Код в приложении MFCMAPI не гарантирует, что папка **Tasks** была выбрана при нажатии кнопки **Добавить** задачу в меню **Addins.**</span><span class="sxs-lookup"><span data-stu-id="6bd42-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="6bd42-121">Создание элементов задач в папке, помимо папки **Задачи,** может привести к неопределяемой модели поведения.</span><span class="sxs-lookup"><span data-stu-id="6bd42-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="6bd42-122">Убедитесь, что вы выбрали папку **Задачи** перед использованием команды **Добавить** задачи в приложении MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="6bd42-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="6bd42-123">Функция  `AddTask` приведена ниже.</span><span class="sxs-lookup"><span data-stu-id="6bd42-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="6bd42-124">Обратите внимание, что параметр  _lpFolder,_ переданный функции, представляет собой указатель  `AddTask` [интерфейса IMAPIFolder,](imapifolderimapicontainer.md) который представляет папку, в которой создается новая задача.</span><span class="sxs-lookup"><span data-stu-id="6bd42-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="6bd42-125">Учитывая _lpFolder,_ который представляет интерфейс **IMAPIFolder,** код вызывает [метод IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="6bd42-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="6bd42-126">Метод **CreateMessage** возвращает код успеха и указатель в указатель **интерфейса IMessage.**</span><span class="sxs-lookup"><span data-stu-id="6bd42-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="6bd42-127">Большая часть кода функции обрабатывает работу по указанию свойств при подготовке к вызову `AddTask` [метода IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="6bd42-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="6bd42-128">В случае успешного вызова метода **SetProps** используется метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для фиксации изменений в хранилище и создания нового элемента задачи.</span><span class="sxs-lookup"><span data-stu-id="6bd42-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="6bd42-129">Функция  `AddTask` задает ряд именных свойств.</span><span class="sxs-lookup"><span data-stu-id="6bd42-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="6bd42-130">Сведения о свойствах с именем и о том, как они создаются, см. в статьи Использование MAPI для создания Outlook [2007 элементов.](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bd42-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="6bd42-131">Так как названные свойства, используемые для элементов задач, занимают несколько наборов свойств, необходимо позаботиться о том, чтобы параметры здания прошли метод [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="6bd42-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="6bd42-132">Функция использует функцию помощника для создания структуры, представляющей повторение задач для настройки свойства `AddTask` `BuildWeeklyTaskRecurrencePattern` **dispidTaskRecur.**</span><span class="sxs-lookup"><span data-stu-id="6bd42-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="6bd42-133">Сведения о структуре повторения задач, создаваемой функцией, см. в рубрике Каноническое свойство  `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) и [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="6bd42-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="6bd42-134">Обратите внимание, что в то время как возможны различные шаблоны повторения, функция создает только недельный шаблон  `BuildWeeklyTaskRecurrencePattern` повторяемости.</span><span class="sxs-lookup"><span data-stu-id="6bd42-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="6bd42-135">Кроме того, трудно закодировать ряд предположений, таких как тип календаря (григорианский), первый день недели (воскресенье) и количество измененных или удаленных экземпляров (нет).</span><span class="sxs-lookup"><span data-stu-id="6bd42-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="6bd42-136">Чтобы принять эти параметры в качестве параметров, потребуется более общая функция создания шаблона повторяемого повторения.</span><span class="sxs-lookup"><span data-stu-id="6bd42-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="6bd42-137">Ниже приводится полный список  `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="6bd42-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="6bd42-138">См. также</span><span class="sxs-lookup"><span data-stu-id="6bd42-138">See also</span></span>

- [<span data-ttu-id="6bd42-139">Использование MAPI для создания элементов Outlook 2007 г.</span><span class="sxs-lookup"><span data-stu-id="6bd42-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

