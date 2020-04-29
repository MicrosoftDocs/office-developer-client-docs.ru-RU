---
title: Работа с автономными решениями с помощью объектной модели InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- решения [InfoPath 2007], автономные, автономные решения [InfoPath 2007], InfoPath 2003 — шаблоны форм, шаблоны форм 2003 InfoPath, совместимые с InfoPath, автономные решения
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Объектная модель, совместимая с InfoPath 2003, предоставляет свойство MachineOnlineState объекта Application, которое позволяет коду формы проверить, подключен ли компьютер пользователя к сети. В зависимости от состояния подключения код формы может выполнять различные действия.
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429245"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="d34af-105">Работа с автономными решениями с помощью объектной модели InfoPath</span><span class="sxs-lookup"><span data-stu-id="d34af-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="d34af-106">Объектная модель, совместимая с InfoPath 2003, предоставляет свойство [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) объекта [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) , которое позволяет коду формы проверить, подключен ли компьютер пользователя к сети.</span><span class="sxs-lookup"><span data-stu-id="d34af-106">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="d34af-107">В зависимости от состояния подключения код формы может выполнять различные действия.</span><span class="sxs-lookup"><span data-stu-id="d34af-107">Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="d34af-108">Использование свойства MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="d34af-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="d34af-109">В приведенном далее примере демонстрируется, как можно добавить в код формы логику, определяющую способ отправки формы на основе наличия или отсутствия подключения компьютера пользователя к сети.</span><span class="sxs-lookup"><span data-stu-id="d34af-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="d34af-p103">В этом примере предполагается, что была создана форма для отправки отчета о продажах, содержащего поле "period", указывающее год и месяц, по которому создан отчет. Также предполагается, что уже определено подключение к данным и создана логика для отправки отчета, когда пользователь подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="d34af-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="d34af-112">Добавление подключения к данным, которое передает форму в виде вложения в сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="d34af-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="d34af-113">Создайте или откройте шаблон формы InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="d34af-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="d34af-114">В режиме конструктора InfoPath выберите пункт **Подключения данных** на вкладке **Данные**.</span><span class="sxs-lookup"><span data-stu-id="d34af-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="d34af-115">В диалоговом окне **Подключения данных** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d34af-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="d34af-116">В **мастере подключения данных** щелкните **Отправка данных** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d34af-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="d34af-117">На следующей странице мастера щелкните **как сообщение электронной почты**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d34af-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="d34af-118">На следующей странице мастера введите адрес электронной почты в поле " **Кому** ".</span><span class="sxs-lookup"><span data-stu-id="d34af-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="d34af-119">Чтобы объединить период продаж с текстом "Отчет о продажах", в поле **Тема** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d34af-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="d34af-120">Нажмите кнопку **Формула** рядом с полем **Тема** .</span><span class="sxs-lookup"><span data-stu-id="d34af-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="d34af-121">В диалоговом окне **Вставка формулы** нажмите кнопку **Вставить функцию**.</span><span class="sxs-lookup"><span data-stu-id="d34af-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="d34af-122">В диалоговом окне **Вставка функции** выберите вариант **Текст** в списке **Категории**, а затем дважды щелкните **объединить** в списке **Функции**.</span><span class="sxs-lookup"><span data-stu-id="d34af-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="d34af-123">Замените первую строку **дважды щелкните, чтобы вставить поле** на следующий текст (включая одинарные кавычки): 'Отчет о продажах: '</span><span class="sxs-lookup"><span data-stu-id="d34af-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="d34af-124">Дважды щелкните вторую строку **дважды щелкните, чтобы вставить поле**.</span><span class="sxs-lookup"><span data-stu-id="d34af-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="d34af-125">В диалоговом окне **Выбор поля или группы** выберите поле period.</span><span class="sxs-lookup"><span data-stu-id="d34af-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="d34af-126">Удалите последнюю строку **дважды щелкните, чтобы вставить поле** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d34af-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="d34af-127">В мастере нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d34af-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="d34af-128">На следующей странице мастера введите "Отправка электронной почты" в поле **введите имя для этого подключения к данным** , а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="d34af-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="d34af-129">Добавление логики для отправки формы в зависимости от наличия или отсутствия подключения пользовательского компьютера к сети</span><span class="sxs-lookup"><span data-stu-id="d34af-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="d34af-130">В режиме конструктора InfoPath выберите в меню **Данные** пункт **Параметры отправки**.</span><span class="sxs-lookup"><span data-stu-id="d34af-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="d34af-131">В диалоговом окне **Параметры отправки** щелкните **Разрешить пользователям отправлять эту форму**, а затем выберите **Выполнить пользовательское действие с использованием кода**.</span><span class="sxs-lookup"><span data-stu-id="d34af-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="d34af-132">Нажмите кнопку  **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="d34af-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="d34af-133">Добавьте следующие две функции ниже обработчика событий [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) :</span><span class="sxs-lookup"><span data-stu-id="d34af-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
   ```cs
    public void OnlineSubmit(DocReturnEvent e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmitX(DocReturnEvent e)
    {
      // Access and submit to the email adapter.
      DataAdaptersCollection myDataAdapters = 
          thisXDocument.DataAdapters;
      EmailAdapterObject submitAdapter = 
          (EmailAdapterObject) myDataAdapters["Email Submit"];
      submitAdapter.Submit();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder message = 
      new System.Text.StringBuilder();
      message.Append("You submitted your Sales Report offline. ");
      message.Append("Your Sales Report is in your outbox ");
      message.Append("and will be submitted when you connect to ");
      message.Append("the network.");
        thisXDocument.UI.Alert(message.ToString());
      // The submission was successful.
      e.ReturnStatus = true;
    }
   ```

5. <span data-ttu-id="d34af-134">Добавьте следующий оператор **if** в функцию обработчика событий **OnSubmitRequest**.</span><span class="sxs-lookup"><span data-stu-id="d34af-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
   ```cs
    // Check the computer's connection state.
    if (thisApplication.MachineOnlineState==XdMachineOnlineState.xdOnline)
    {
        OnlineSubmit(e);
    }
    else
    {
        OfflineSubmit(e);
    }
   ```

### <a name="test-the-code"></a><span data-ttu-id="d34af-135">Проверка кода</span><span class="sxs-lookup"><span data-stu-id="d34af-135">Test the code</span></span>

1. <span data-ttu-id="d34af-136">В конструкторе InfoPath нажмите кнопку **Просмотр** на вкладке **Главная**.</span><span class="sxs-lookup"><span data-stu-id="d34af-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="d34af-137">Заполните форму.</span><span class="sxs-lookup"><span data-stu-id="d34af-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="d34af-138">Запустите браузер Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d34af-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="d34af-139">В браузере Internet Explorer выберите пункт **Работать автономно** в меню **Файл**.</span><span class="sxs-lookup"><span data-stu-id="d34af-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="d34af-140">В приложении InfoPath щелкните **Отправка**.</span><span class="sxs-lookup"><span data-stu-id="d34af-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="d34af-141">Должно отобразиться сообщение о том, что форма будет отправлена в виде электронного сообщения.</span><span class="sxs-lookup"><span data-stu-id="d34af-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="d34af-142">Щелкните **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="d34af-142">Click **Send**.</span></span> <span data-ttu-id="d34af-143">Должно появиться сообщение, объявляющее, что форма отправлена автономно.</span><span class="sxs-lookup"><span data-stu-id="d34af-143">You should see a message stating that the form has been submitted offline.</span></span>
    

