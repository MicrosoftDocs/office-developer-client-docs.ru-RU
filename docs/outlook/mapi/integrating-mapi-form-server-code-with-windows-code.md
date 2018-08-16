---
title: Интеграция серверного кода форм MAPI с кодом Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 31f09b1c2f7b23d63e17f59c28b7bcf377b769d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809445"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Интеграция серверного кода форм MAPI с кодом Windows

  
  
**Относится к**: Outlook 
  
Помните, что сервер формы — это приложение Win32. Таким образом существуют некоторые задачи, связанные с загрузки сервера формы в памяти и завершение работы приложения без ошибок. Как и все приложения Windows точка входа для сервера формы является функции **WinMain** . Эта функция является соответствующее место для выполнения следующих задач: 
  
- Создание и регистрация класса окна, чтобы сервер форм могут взаимодействовать с другими компонентами OLE.
    
- Создание и регистрация класса окна или классы для пользовательских интерфейсов объектам формы.
    
- Вызов функции [MAPIInitialize](mapiinitialize.md) . **MAPIInitialize** обрабатывает необходимые OLE инициализации, а также. Это необходимо выполнить один раз на каждый экземпляр сервера формы. 
    
- Регистрация глобального atom с строковое представление формы server идентификатор класса (CLSID). В этом atom должна существовать для жизненным циклом сервера форм.
    
- Вызов функции OLE [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) для регистрации фабрики классов сервера форм с OLE. 
    
- Создание главного окна для получения сообщений. Это окно, вероятно, не нужно быть видны, так как пользователь будет взаимодействует с определенным windows, связанные с объектами объединяемой формы. Тем не менее во время разработки, главного окна может быть удобно для отладки элемента управления сервера формы или вывода.
    
- Создание цикл обработки сообщений, на котором выполняется в течение времени жизни сервера формы, преобразования и отправки сообщений windows для активной формы объектов.
    
При выходе из сервера формы, его следует выполнить следующие задачи:
  
- Вызовите функцию OLE [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) для отмены регистрации OLE класс сообщения. 
    
- Вызовите **MAPIUninitialize** , чтобы должным образом закрыть подключения к серверу формы к MAPI. 
    
- Удаление глобального atom, содержащий строковое представление идентификатор класса.
    
## <a name="see-also"></a>См. также



[Написание серверного кода формы](writing-form-server-code.md)
