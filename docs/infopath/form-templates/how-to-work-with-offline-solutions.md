---
title: Работа с автономными решениями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- автономные решения [infopath 2007],solutions [InfoPath 2007], offline,InfoPath 2007, автономные решения
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: Объектная модель InfoPath предоставляет свойство MachineOnlineState класса Application, которое позволяет коду формы проверять, подключен ли компьютер пользователя к сети. Проверяя значение свойства MachineOnlineState, код формы может выполнять различные действия в зависимости от состояния подключения.
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436141"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="c3b4c-105">Работа с автономными решениями</span><span class="sxs-lookup"><span data-stu-id="c3b4c-105">Work with offline solutions</span></span>

<span data-ttu-id="c3b4c-106">Объектная модель InfoPath предоставляет свойство [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) класса [Application,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) которое позволяет коду формы проверять, подключен ли компьютер пользователя к сети.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-106">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="c3b4c-107">Проверяя значение свойства **MachineOnlineState**, код формы может выполнять различные действия в зависимости от состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-107">By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="c3b4c-108">Использование свойства MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="c3b4c-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="c3b4c-109">В приведенном далее примере демонстрируется, как можно добавить в код формы логику, определяющую способ отправки формы на основе наличия или отсутствия подключения компьютера пользователя к сети.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="c3b4c-110">В этом примере предполагается, что вы создали форму для отправки отчета о продажах, который содержит поле с именем периода, которое указывает месяц и год, охватываемых отчетом.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-110">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report.</span></span> <span data-ttu-id="c3b4c-111">Также предполагается, что уже определено подключение к данным и создана логика для отправки отчета, когда пользователь подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-111">It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="c3b4c-112">Добавление подключения к данным, которое передает форму в виде вложения в сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="c3b4c-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="c3b4c-113">Создайте шаблон формы InfoPath, используя шаблон **Пустой (редактор InfoPath)**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="c3b4c-114">В режиме конструктора InfoPath выберите пункт **Подключения данных** на вкладке **Данные**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="c3b4c-115">В диалоговом окне **Подключения данных** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="c3b4c-116">В **мастере подключения данных** щелкните **Отправка данных** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="c3b4c-117">На следующей странице мастера щелкните **"Как сообщение** электронной почты", а затем нажмите кнопку **"Далее".**</span><span class="sxs-lookup"><span data-stu-id="c3b4c-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="c3b4c-118">На следующей странице мастера введите адрес электронной почты в поле **"В".**</span><span class="sxs-lookup"><span data-stu-id="c3b4c-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="c3b4c-119">Чтобы объединить период продаж с текстом "Отчет о продажах", в поле **Тема** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="c3b4c-120">Нажмите **кнопку "Формула"** рядом с полем **"Тема".**</span><span class="sxs-lookup"><span data-stu-id="c3b4c-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="c3b4c-121">В диалоговом окне **Вставка формулы** нажмите кнопку **Вставить функцию**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="c3b4c-122">В диалоговом окне **Вставка функции** выберите вариант **Текст** в списке **Категории**, а затем дважды щелкните **объединить** в списке **Функции**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="c3b4c-123">Замените первую строку **дважды щелкните, чтобы вставить поле** на следующий текст (включая одинарные кавычки): 'Отчет о продажах: '</span><span class="sxs-lookup"><span data-stu-id="c3b4c-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="c3b4c-124">Дважды щелкните вторую строку **дважды щелкните, чтобы вставить поле**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="c3b4c-125">В диалоговом окне **Выбор поля или группы** выберите поле period.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="c3b4c-126">Удалите последнюю строку **дважды щелкните, чтобы вставить поле** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="c3b4c-127">В мастере нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="c3b4c-128">На следующей странице мастера нажмите  кнопку "Формула" рядом с полем "Имя вложения", а затем повторите вышеперечисленные действия, чтобы создать конкату ("Отчет о продажах - ", точка") и нажмите кнопку  "Далее". </span><span class="sxs-lookup"><span data-stu-id="c3b4c-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="c3b4c-129">На последней странице мастера введите "Отправить по электронной почте" в поле "Введите имя для этого подключения к данным" и нажмите кнопку **"Готово".** </span><span class="sxs-lookup"><span data-stu-id="c3b4c-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="c3b4c-130">Добавление логики для отправки формы в зависимости от наличия или отсутствия подключения пользовательского компьютера к сети</span><span class="sxs-lookup"><span data-stu-id="c3b4c-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="c3b4c-131">В режиме конструктора InfoPath выберите пункт **Параметры отправки** на вкладке **Данные**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="c3b4c-132">В диалоговом окне **Параметры отправки** щелкните **Разрешить пользователям отправлять эту форму**, выберите **Выполнить пользовательское действие с использованием кода** и щелкните **Редактировать код**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="c3b4c-133">Добавьте следующие две функции под обработом событий [Отправка:](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3b4c-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
   ```cs
    public void OnlineSubmit(SubmitEventArgs e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmit(SubmitEventArgs e)
    {
      // Access and submit to the email connection.
      DataConnectionCollection myDataConnections =
          this.DataConnections;
      EmailSubmitConnection submitConnection =
          (EmailSubmitConnection)myDataConnections["Email Submit"];
      submitConnection.Execute();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder myMessage = 
          new System.Text.StringBuilder();
      myMessage.Append("You submitted your Sales Report offline. ");
      myMessage.Append("Your Sales Report is in your outbox ");
      myMessage.Append("and will be submitted when you connect to ");
      myMessage.Append("the network.");
        MessageBox.Show(myMessage.ToString());
      // The submission was successful.
      e.CancelableArgs.Cancel = false;
    }
   ```

   ```vb
    Public Sub OnlineSubmit(ByVal e As SubmitEventArgs)
      ' Logic for submitting online goes here.
    End Sub
    Public Sub OfflineSubmit(ByVal e As SubmitEventArgs)
      ' Access and submit to the email connection.
      Dim myDataConnections As DataConnectionCollection = _
          Me.DataConnections
      Dim submitConnection As EmailSubmitConnection = _
          DirectCast(myDataConnections("Email Submit"), _
          EmailSubmitConnection)
      submitConnection.Execute
      ' Notify the user that the form was submitted offline.
      Dim myMessage As System.Text.StringBuilder = _
          New System.Text.StringBuilder()
      myMessage.Append("You submitted your Sales Report offline. ")
      myMessage.Append("Your Sales Report is in your outbox ")
      myMessage.Append("and will be submitted when you connect to ")
      myMessage.Append("the network.")
        MessageBox.Show(myMessage.ToString())
      ' The submission was successful.
      e.CancelableArgs.Cancel = False
    End Sub
   ```

4. <span data-ttu-id="c3b4c-134">Добавьте следующий запрос **if** в [функцию обработера](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) событий Submit.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
   ```cs
    // Check the computer's connection state.
    if (this.Application.MachineOnlineState == MachineState.Online)
    {
      OnlineSubmit(e);
    }
    else
    {
      OfflineSubmit(e);
    }
   ```

   ```vb
    ' Check the computer's connection state.
    If (Me.Application.MachineOnlineState = MachineState.Online) Then
      OnlineSubmit(e)
    Else
    {
      OfflineSubmit(e)
    End If
   ```

### <a name="test-the-code"></a><span data-ttu-id="c3b4c-135">Проверка кода</span><span class="sxs-lookup"><span data-stu-id="c3b4c-135">Test the code</span></span>

1. <span data-ttu-id="c3b4c-136">В меню **Отладка** выберите пункт **Начать отладку**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="c3b4c-137">Заполните форму.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="c3b4c-138">Запустите браузер Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="c3b4c-139">В браузере Internet Explorer выберите пункт **Работать автономно** в меню **Файл**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="c3b4c-140">В приложении InfoPath щелкните **Отправка**.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="c3b4c-141">Должно отобраться сообщение о том, что форма будет отправлена в виде сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="c3b4c-p105">Щелкните **Отправить**. Должно появиться сообщение о том, что форма отправляется в автономном режиме и будет отправлена при подключении к сети.</span><span class="sxs-lookup"><span data-stu-id="c3b4c-p105">Click **Send**. You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3b4c-144">См. также</span><span class="sxs-lookup"><span data-stu-id="c3b4c-144">See also</span></span>

- [<span data-ttu-id="c3b4c-145">Разработка шаблона формы для автономного использования</span><span class="sxs-lookup"><span data-stu-id="c3b4c-145">Design a form template for offline use</span></span>](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

