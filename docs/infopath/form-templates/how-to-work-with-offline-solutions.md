---
title: Работа с автономными решениями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- автономные решения [infopath 2007] решения [InfoPath 2007], автономный режим, InfoPath 2007, автономные решения
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: Объектная модель InfoPath предоставляет свойство MachineOnlineState класса приложения, которая позволяет код формы для проверки подключения компьютера пользователя к сети. Проверки значения свойства "MachineOnlineState", код формы позволяет выполнять разные действия в зависимости от состояния подключения.
ms.openlocfilehash: fcdaae31dd6a0c76cf1c453f267be430a2b34bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807501"
---
# <a name="work-with-offline-solutions"></a>Работа с автономными решениями

Объектная модель InfoPath предоставляет свойство [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , которая позволяет код формы для проверки подключения компьютера пользователя к сети. Проверки значения свойства " **MachineOnlineState"** , код формы позволяет выполнять разные действия в зависимости от состояния подключения. 
  
## <a name="using-the-machineonlinestate-property"></a>С помощью свойства "MachineOnlineState"

В приведенном далее примере демонстрируется, как можно добавить в код формы логику, определяющую способ отправки формы на основе наличия или отсутствия подключения компьютера пользователя к сети.
  
В этом примере предполагается, что созданы формы для отправки отчет о продажах, который содержит поле с именем периода времени, который указывает месяц и год, охватываемый в отчете. Также предполагается, что вы уже определенного подключения данных и логики для отправки отчета, когда пользователь находится в сети. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Добавление подключения к данным, который отправляет форму в виде вложения в сообщение электронной почты

1. Создание шаблона формы InfoPath на основе шаблона **пустой (редактор InfoPath)** . 
    
2. В режиме конструктора InfoPath выберите пункт **Подключения данных** на вкладке **данные** . 
    
3. В диалоговом окне **Подключения к данным** нажмите кнопку **Добавить**.
    
4. В окне **Мастера подключения данных**щелкните **Отправка данных**и нажмите кнопку **Далее**.
    
5. На следующей странице мастера щелкните **как сообщения электронной почты**и нажмите кнопку **Далее**.
    
6. На следующей странице мастера введите свой адрес электронной почты в поле **Кому** . 
    
7. В поле **Тема** выполните следующие действия, чтобы объединить период продаж с текстом отчета о продажах: 
    
   1. Нажмите кнопку **Формула** рядом с полем **Тема** . 
      
   2. В диалоговом окне **Вставка формулы** нажмите кнопку **Вставить функцию**.
      
   3. В диалоговом окне **Вставка функции** выберите вариант **текст** в списке **категории** и дважды щелкните **Объединить** в списке **функции** . 
      
   4. Замените первую строку **дважды щелкните, чтобы вставить поле** на следующий текст (включая одинарные кавычки): ' отчет о продажах: ' 
      
   5. Дважды щелкните вторую строку **дважды щелкните, чтобы вставить поле**.
      
   6. В диалоговом окне **Выбор поля или группы** выберите поле период. 
      
   7. Удалите последнюю строку **дважды щелкните, чтобы вставить поле**и нажмите кнопку **ОК**.
    
8. В окне мастера нажмите кнопку **Далее**.
    
9. На следующей странице мастера нажмите кнопку **Формула** рядом с полем **Имя вложения** и повторите описанные выше действия для создания формул объединить ("Отчет о продажах" -, период) и нажмите кнопку **Далее**.
    
10. На последней странице мастера введите отправка электронной почты в поле **Введите имя для этого подключения к данным** и нажмите кнопку **Готово**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Добавление логики для отправки формы в зависимости от наличия или отсутствия подключения пользовательского компьютера к сети

1. В режиме конструктора InfoPath выберите пункт **Параметры отправки** на вкладке **данные** . 
    
2. В диалоговом окне **Параметры отправки** щелкните **Разрешить пользователям отправлять эту форму**, выберите **выполнить пользовательское действие с использованием кода**и щелкните **Редактировать код**.
    
3. Добавьте следующие две функции обработчик события [отправки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) : 
    
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

4. Добавьте следующий оператор **if** в функцию обработчика событий [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) . 
    
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

1. В меню **Отладка** выберите **Начать отладку**.
    
2. Заполните форму.
    
3. Запустите браузер Microsoft Internet Explorer.
    
4. В Internet Explorer в меню **файл** щелкните **работы в автономном режиме** . 
    
5. В InfoPath нажмите кнопку **Отправить**. Должно появиться сообщение, что форма будет отправлено сообщение электронной почты.
    
6. Нажмите кнопку **Отправить**. Должно появиться сообщение о том, что в форме отправки в автономном режиме и будет отправлена при подключении к сети.
    
## <a name="see-also"></a>См. также

- [Разработка шаблона формы для автономного использования](http://office.microsoft.com/en-us/infopath/HA102117391033.aspx?pid=CH100341121033)

