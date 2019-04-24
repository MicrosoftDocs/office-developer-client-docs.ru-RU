---
title: Работа с автономными решениями с помощью объектной модели InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- решения [InfoPath 2007], автономные, автономные решения [InfoPath 2007], InfoPath 2003 — шаблоны форм, шаблоны форм InfoPath, совместимые с InfoPath, автономные решения
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Объектная модель, совместимая с InfoPath 2003, предоставляет свойство MachineOnlineState объекта Application, которое позволяет коду формы проверить, подключен ли компьютер пользователя к сети. В зависимости от состояния подключения код формы может выполнять различные действия.
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303572"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Работа с автономными решениями с помощью объектной модели InfoPath

Объектная модель, совместимая с InfoPath 2003, предоставляет свойство [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) объекта [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) , которое позволяет коду формы проверить, подключен ли компьютер пользователя к сети. В зависимости от состояния подключения код формы может выполнять различные действия. 
  
## <a name="using-the-machineonlinestate-property"></a>Использование свойства MachineOnlineState

В приведенном далее примере демонстрируется, как можно добавить в код формы логику, определяющую способ отправки формы на основе наличия или отсутствия подключения компьютера пользователя к сети.
  
В этом примере предполагается, что была создана форма для отправки отчета о продажах, содержащего поле "period", указывающее год и месяц, по которому создан отчет. Также предполагается, что уже определено подключение к данным и создана логика для отправки отчета, когда пользователь подключен к сети.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Добавление подключения к данным, которое передает форму в виде вложения в сообщение электронной почты

1. Создайте или откройте шаблон формы InfoPath с управляемым кодом.
    
2. В режиме конструктора InfoPath выберите пункт **Подключения данных** на вкладке **Данные**.
    
3. В диалоговом окне **Подключения данных** нажмите кнопку **Добавить**.
    
4. В **мастере подключения данных** щелкните **Отправка данных** и нажмите кнопку **Далее**.
    
5. На следующей странице мастера щелкните **как сообщение электронной почты**, а затем нажмите кнопку **Далее**.
    
6. На следующей странице мастера введите адрес электронной почты в поле " **Кому** ". 
    
7. Чтобы объединить период продаж с текстом "Отчет о продажах", в поле **Тема** выполните следующие действия. 
    
   1. Нажмите кнопку **Формула** рядом с полем **Тема** . 
      
   2. В диалоговом окне **Вставка формулы** нажмите кнопку **Вставить функцию**.
      
   3. В диалоговом окне **Вставка функции** выберите вариант **Текст** в списке **Категории**, а затем дважды щелкните **объединить** в списке **Функции**. 
      
   4. Замените первую строку **дважды щелкните, чтобы вставить поле** на следующий текст (включая одинарные кавычки): 'Отчет о продажах: ' 
      
   5. Дважды щелкните вторую строку **дважды щелкните, чтобы вставить поле**.
      
   6. В диалоговом окне **Выбор поля или группы** выберите поле period. 
      
   7. Удалите последнюю строку **дважды щелкните, чтобы вставить поле** и нажмите кнопку **ОК**.
    
8. В мастере нажмите кнопку **Далее**.
    
9. На следующей странице мастера введите "Отправка электронной почты" в поле **введите имя для этого подключения к данным** , а затем нажмите кнопку **Готово**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Добавление логики для отправки формы в зависимости от наличия или отсутствия подключения пользовательского компьютера к сети

1. В режиме конструктора InfoPath выберите в меню **Данные** пункт **Параметры отправки**.
    
2. В диалоговом окне **Параметры отправки** щелкните **Разрешить пользователям отправлять эту форму**, а затем выберите **Выполнить пользовательское действие с использованием кода**.
    
3. Нажмите кнопку  **Изменить**. 
    
4. Добавьте следующие две функции ниже обработчика событий [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) : 
    
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

5. Добавьте следующий оператор **if** в функцию обработчика событий **OnSubmitRequest**. 
    
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

### <a name="test-the-code"></a>Проверка кода

1. В конструкторе InfoPath нажмите кнопку **Просмотр** на вкладке **Главная**. 
    
2. Заполните форму.
    
3. Запустите браузер Microsoft Internet Explorer.
    
4. В браузере Internet Explorer выберите пункт **Работать автономно** в меню **Файл**. 
    
5. В приложении InfoPath щелкните **Отправка**. Должно отобразиться сообщение о том, что форма будет отправлена в виде электронного сообщения.
    
6. Щелкните **Отправить**. Должно появиться сообщение, объявляющее, что форма отправлена автономно.
    

