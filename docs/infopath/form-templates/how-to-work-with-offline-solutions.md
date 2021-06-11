---
title: Работа с автономными решениями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- автономные решения [infopath 2007], решения [InfoPath 2007], автономные решения, InfoPath 2007, автономные решения
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
# <a name="work-with-offline-solutions"></a>Работа с автономными решениями

Объектная модель InfoPath предоставляет свойство [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) класса [Application,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) которое позволяет коду формы проверять, подключен ли компьютер пользователя к сети. Проверяя значение свойства **MachineOnlineState**, код формы может выполнять различные действия в зависимости от состояния подключения. 
  
## <a name="using-the-machineonlinestate-property"></a>Использование свойства MachineOnlineState

В приведенном далее примере демонстрируется, как можно добавить в код формы логику, определяющую способ отправки формы на основе наличия или отсутствия подключения компьютера пользователя к сети.
  
В этом примере предполагается, что вы создали форму для отправки отчета о продажах, который содержит период с именем поля, который указывает месяц и год, охватываемых отчетом. Также предполагается, что уже определено подключение к данным и создана логика для отправки отчета, когда пользователь подключен к сети. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Добавление подключения к данным, которое передает форму в виде вложения в сообщение электронной почты

1. Создайте шаблон формы InfoPath, используя шаблон **Пустой (редактор InfoPath)**. 
    
2. В режиме конструктора InfoPath выберите пункт **Подключения данных** на вкладке **Данные**. 
    
3. В диалоговом окне **Подключения данных** нажмите кнопку **Добавить**.
    
4. В **мастере подключения данных** щелкните **Отправка данных** и нажмите кнопку **Далее**.
    
5. На следующей странице мастера нажмите **кнопку Как сообщение** электронной почты, а затем нажмите **кнопку Далее**.
    
6. На следующей странице мастера введите адрес электронной почты в поле **To.** 
    
7. Чтобы объединить период продаж с текстом "Отчет о продажах", в поле **Тема** выполните следующие действия. 
    
   1. Нажмите **кнопку Формула** рядом с **полем Subject.** 
      
   2. В диалоговом окне **Вставка формулы** нажмите кнопку **Вставить функцию**.
      
   3. В диалоговом окне **Вставка функции** выберите вариант **Текст** в списке **Категории**, а затем дважды щелкните **объединить** в списке **Функции**. 
      
   4. Замените первую строку **дважды щелкните, чтобы вставить поле** на следующий текст (включая одинарные кавычки): 'Отчет о продажах: ' 
      
   5. Дважды щелкните вторую строку **дважды щелкните, чтобы вставить поле**.
      
   6. В диалоговом окне **Выбор поля или группы** выберите поле period. 
      
   7. Удалите последнюю строку **дважды щелкните, чтобы вставить поле** и нажмите кнопку **ОК**.
    
8. В мастере нажмите кнопку **Далее**.
    
9. На следующей странице мастера нажмите  кнопку Формула  рядом с полем Имя вложения, а затем повторите действия, которые были выше, чтобы создать формулу concat ("Отчет о продажах. - ", период"), а затем нажмите кнопку **Далее**.
    
10. На последней странице мастера введите отправку электронной почты в поле **Ввод** имени для этого окна подключения к данным, а затем нажмите **кнопку Готово**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Добавление логики для отправки формы в зависимости от наличия или отсутствия подключения пользовательского компьютера к сети

1. В режиме конструктора InfoPath выберите пункт **Параметры отправки** на вкладке **Данные**. 
    
2. В диалоговом окне **Параметры отправки** щелкните **Разрешить пользователям отправлять эту форму**, выберите **Выполнить пользовательское действие с использованием кода** и щелкните **Редактировать код**.
    
3. Добавьте следующие две функции ниже обработика [события Отправка:](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) 
    
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

4. Добавьте **следующее, если** заявление в функцию обработера событий [Отправка.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) 
    
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

### <a name="test-the-code"></a>Проверка кода

1. В меню **Отладка** выберите пункт **Начать отладку**.
    
2. Заполните форму.
    
3. Запустите браузер Microsoft Internet Explorer.
    
4. В браузере Internet Explorer выберите пункт **Работать автономно** в меню **Файл**. 
    
5. В приложении InfoPath щелкните **Отправка**. Вы должны видеть сообщение о том, что форма будет отправлена в виде сообщения электронной почты.
    
6. Щелкните **Отправить**. Должно появиться сообщение о том, что форма отправляется в автономном режиме и будет отправлена при подключении к сети.
    
## <a name="see-also"></a>См. также

- [Разработка шаблона форм для автономного использования](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

