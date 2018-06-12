---
title: Работа с автономными решениями, с помощью объектной модели InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- решения [infopath 2007], автономные, автономные решения [InfoPath 2007], шаблоны форм совместимых с InfoPath 2003, совместимых с InfoPath 2003 шаблонов форм, автономные решения
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Объектная модель совместимых с InfoPath 2003 предоставляет свойство MachineOnlineState объекта приложения, которое позволяет код формы для проверки подключения компьютера пользователя к сети. Код формы можно выполнять различные действия в зависимости от состояния подключения.
ms.openlocfilehash: 858b5d317cf5245dbfb447fa9e118a11ecbe7eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807497"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="d7ec2-105">Работа с автономными решениями, с помощью объектной модели InfoPath</span><span class="sxs-lookup"><span data-stu-id="d7ec2-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="d7ec2-106">Объектная модель совместимых с InfoPath 2003 предоставляет свойство [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) объекта [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) , которое позволяет код формы для проверки подключения компьютера пользователя к сети.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-106">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="d7ec2-107">Код формы можно выполнять различные действия в зависимости от состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-107">Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="d7ec2-108">С помощью свойства "MachineOnlineState"</span><span class="sxs-lookup"><span data-stu-id="d7ec2-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="d7ec2-109">В приведенном далее примере демонстрируется, как можно добавить в код формы логику, определяющую способ отправки формы на основе наличия или отсутствия подключения компьютера пользователя к сети.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="d7ec2-p103">В этом примере предполагается, что была создана форма для отправки отчета о продажах, содержащего поле "period", указывающее год и месяц, по которому создан отчет. Также предполагается, что уже определено подключение к данным и создана логика для отправки отчета, когда пользователь подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="d7ec2-112">Добавление подключения к данным, который отправляет форму в виде вложения в сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="d7ec2-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="d7ec2-113">Создайте или откройте шаблон формы InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="d7ec2-114">В режиме конструктора InfoPath выберите на вкладке **данные** щелкните **Подключения к данным**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="d7ec2-115">В диалоговом окне **Подключения к данным** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="d7ec2-116">В окне **Мастера подключения данных**щелкните **Отправка данных**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="d7ec2-117">На следующей странице мастера щелкните **как сообщения электронной почты**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="d7ec2-118">На следующей странице мастера введите свой адрес электронной почты в поле **Кому** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="d7ec2-119">В поле **Тема** выполните следующие действия, чтобы объединить период продаж с текстом отчета о продажах:</span><span class="sxs-lookup"><span data-stu-id="d7ec2-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="d7ec2-120">Нажмите кнопку **Формула** рядом с полем **Тема** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="d7ec2-121">В диалоговом окне **Вставка формулы** нажмите кнопку **Вставить функцию**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="d7ec2-122">В диалоговом окне **Вставка функции** выберите вариант **текст** в списке **категории** и дважды щелкните **Объединить** в списке **функции** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="d7ec2-123">Замените первую строку **дважды щелкните, чтобы вставить поле** на следующий текст (включая одинарные кавычки): ' отчет о продажах: '</span><span class="sxs-lookup"><span data-stu-id="d7ec2-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="d7ec2-124">Дважды щелкните вторую строку **дважды щелкните, чтобы вставить поле**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="d7ec2-125">В диалоговом окне **Выбор поля или группы** выберите поле период.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="d7ec2-126">Удалите последнюю строку **дважды щелкните, чтобы вставить поле**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="d7ec2-127">В окне мастера нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="d7ec2-128">На следующей странице мастера введите «Отправка электронной почты» в поле **Введите имя для этого подключения к данным** и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="d7ec2-129">Добавление логики для отправки формы в зависимости от наличия или отсутствия подключения пользовательского компьютера к сети</span><span class="sxs-lookup"><span data-stu-id="d7ec2-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="d7ec2-130">В режиме конструктора InfoPath выберите на вкладке **данные** щелкните **Параметры отправки**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="d7ec2-131">В диалоговом окне **Параметры отправки** щелкните **Разрешить пользователям отправлять эту форму**и затем выберите **выполнить пользовательское действие с использованием кода**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="d7ec2-132">Нажмите кнопку **Изменить** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="d7ec2-133">Добавьте обработчик события [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) следующие две функции:</span><span class="sxs-lookup"><span data-stu-id="d7ec2-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
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

5. <span data-ttu-id="d7ec2-134">Добавьте следующий оператор **if** в функцию обработчика событий **OnSubmitRequest** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="d7ec2-135">Проверка кода</span><span class="sxs-lookup"><span data-stu-id="d7ec2-135">Test the code</span></span>

1. <span data-ttu-id="d7ec2-136">В конструкторе InfoPath нажмите кнопку **Просмотр** на вкладке **Главная** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="d7ec2-137">Заполните форму.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="d7ec2-138">Запустите браузер Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="d7ec2-139">В Internet Explorer в меню **файл** щелкните **работы в автономном режиме** .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="d7ec2-140">В InfoPath нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="d7ec2-141">Должно появиться сообщение, что форма будет отправлено сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="d7ec2-142">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-142">Click **Send**.</span></span> <span data-ttu-id="d7ec2-143">Должно появиться сообщение о том, автономный режим отправлена форма.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-143">You should see a message stating that the form has been submitted offline.</span></span>
    

