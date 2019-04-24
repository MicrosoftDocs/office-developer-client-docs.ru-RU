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
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="ced6e-103">Создание простого элемента повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="ced6e-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="ced6e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced6e-105">С помощью MAPI можно создавать элементы задач.</span><span class="sxs-lookup"><span data-stu-id="ced6e-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="ced6e-106">В этом разделе описывается создание простой повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="ced6e-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="ced6e-107">Сведения о том, как скачать, просмотреть и запустить код из приложения MFCMAPI и проекта Креатеаутлукитемсаддин, указанного в этом разделе, приведены в статье [Установка примеров, используемых в этом разделе](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="ced6e-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="ced6e-108">Создание элемента задачи</span><span class="sxs-lookup"><span data-stu-id="ced6e-108">To create a task item</span></span>

1. <span data-ttu-id="ced6e-109">Откройте хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ced6e-109">Open a message store.</span></span> <span data-ttu-id="ced6e-110">Сведения о том, как открыть хранилище сообщений, можно найти в разделе [Открытие хранилища сообщений](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="ced6e-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="ced6e-111">Откройте папку Tasks в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ced6e-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="ced6e-112">Дополнительные сведения см. в статье **пр_ипм_таск_ентрид** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ced6e-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="ced6e-113">ВыЗовите метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) в папке Tasks, чтобы создать новый элемент задачи.</span><span class="sxs-lookup"><span data-stu-id="ced6e-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="ced6e-114">Задайте свойство **диспидтаскрекур** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) и другие свойства, связанные с задачами, необходимые для создания повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="ced6e-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="ced6e-115">Сохраните новый элемент Task.</span><span class="sxs-lookup"><span data-stu-id="ced6e-115">Save the new task item.</span></span>
    
<span data-ttu-id="ced6e-116">Эти `AddTask` шаги демонстрируются в функции в исходном файле Tasks. cpp проекта креатеаутлукитемсаддин.</span><span class="sxs-lookup"><span data-stu-id="ced6e-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="ced6e-117">Функция принимает параметры из диалогового окна **Добавление задачи** , которое отображается при выборе команды **Добавить задачу** в меню ADDIN примера приложения MFCMAPI. \*\*\*\* `AddTask`</span><span class="sxs-lookup"><span data-stu-id="ced6e-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="ced6e-118">`DisplayAddTaskDialog` Функция в файле Tasks. cpp отображает диалоговое окно и передает значения из диалогового окна `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="ced6e-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="ced6e-119">`DisplayAddTaskDialog` Функция не связана напрямую с созданием элемента задачи с помощью MAPI, поэтому она не указана здесь.</span><span class="sxs-lookup"><span data-stu-id="ced6e-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ced6e-120">Код в приложении MFCMAPI не гарантирует, что папка " **задачи** " была выбрана при выборе команды **Добавить задачу** в меню **ADDIN** .</span><span class="sxs-lookup"><span data-stu-id="ced6e-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="ced6e-121">Создание элементов задач в папке, отличной от папки **tasks** , может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="ced6e-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="ced6e-122">Прежде чем использовать команду **Добавить задачу** в \*\*\*\* приложении MFCMAPI, убедитесь, что вы выбрали папку Tasks.</span><span class="sxs-lookup"><span data-stu-id="ced6e-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="ced6e-123">`AddTask` Функция указана ниже.</span><span class="sxs-lookup"><span data-stu-id="ced6e-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="ced6e-124">Обратите внимание, что параметр _лпфолдер_ , `AddTask` переданный в функцию, является указателем на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , представляющий папку, в которой создается новая задача.</span><span class="sxs-lookup"><span data-stu-id="ced6e-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="ced6e-125">При наличии _лпфолдер_ , представляющего интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ced6e-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="ced6e-126">Метод **CreateMessage** возвращает код успешного выполнения и указатель на указатель на интерфейс **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="ced6e-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="ced6e-127">Большая часть кода `AddTask` функции обрабатывает работу по заданию свойств при подготовке к вызову метода [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="ced6e-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="ced6e-128">Если вызов метода **SetProps** выполнен успешно, вызывается метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для фиксации изменений в хранилище и создания элемента задачи.</span><span class="sxs-lookup"><span data-stu-id="ced6e-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="ced6e-129">`AddTask` Функция задает ряд именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="ced6e-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="ced6e-130">Сведения об именованных свойствах и способах их создания можно узнать [в статье использование MAPI для создания элементов Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ced6e-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="ced6e-131">Так как именованные свойства, используемые для элементов задач, занимают несколько наборов свойств, при построении параметров для передачи в метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) необходимо учитывать осторожность.</span><span class="sxs-lookup"><span data-stu-id="ced6e-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="ced6e-132">`AddTask` Функция использует `BuildWeeklyTaskRecurrencePattern` вспомогательную функцию для создания структуры, представляющей повторение задачи, для установки свойства **диспидтаскрекур** .</span><span class="sxs-lookup"><span data-stu-id="ced6e-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="ced6e-133">Сведения о структуре повторения задачи, которую создает `BuildWeeklyTaskRecurrencePattern` функция, приведены в статье [PidLidTaskRecurrence каноническое](pidlidtaskrecurrence-canonical-property.md) свойство и [PidLidRecurrencePattern каноническое свойство](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="ced6e-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="ced6e-134">Обратите внимание, что в то время как можно создать большое разнообразие `BuildWeeklyTaskRecurrencePattern` шаблонов повторения, функция выполняет построение только расписания повторения.</span><span class="sxs-lookup"><span data-stu-id="ced6e-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="ced6e-135">Это также жестко запрограммировано для ряда допущений, таких как тип календаря (григорианский), первый день недели (воскресенье), а также количество измененных или удаленных экземпляров (нет).</span><span class="sxs-lookup"><span data-stu-id="ced6e-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="ced6e-136">Более общая функция создания шаблона повторения должен принимать эти виды переменных в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="ced6e-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="ced6e-137">Ниже приведен полный список `AddTask` функции.</span><span class="sxs-lookup"><span data-stu-id="ced6e-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ced6e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="ced6e-138">See also</span></span>

- [<span data-ttu-id="ced6e-139">Использование MAPI для создания элементов Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="ced6e-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

