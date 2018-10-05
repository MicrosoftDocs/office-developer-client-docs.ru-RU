---
title: Интеграция приложений для обмена мгновенными сообщениями с приложениями Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: В этой статье описывается настройка клиентского приложения мгновенные сообщения (IM), чтобы он интегрируется с использованием социальных функций в Office 2013, включая отображение сведений о присутствии и отправлять мгновенные сообщения из карточки контакта.
ms.openlocfilehash: fbb3c68126b16e04cd00e950828fc67d16fc7669
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401740"
---
# <a name="integrating-im-applications-with-office"></a>Интеграция приложений для обмена мгновенными сообщениями с приложениями Office

В этой статье описывается настройка клиентского приложения мгновенные сообщения (IM), чтобы он интегрируется с использованием социальных функций в Office 2013, включая отображение сведений о присутствии и отправлять мгновенные сообщения из карточки контакта.
  
Если у вас есть вопросы или комментарии о данной технической статье или процессами, его описание, можно напрямую, отправив сообщение электронной почты для [docthis@microsoft.com](mailto:docthis@microsoft.com)обратитесь в Майкрософт.
  
## <a name="introduction"></a>Введение
<a name="off15_IMIntegration_Intro"> </a>

Office 2013 предоставляет приложениям, включая Lync 2013 расширенными возможностями интеграции с клиентом обмена мгновенными Сообщениями. В этом интеграции предоставляет пользователям возможности обмена мгновенными Сообщениями из в Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 и OneNote 2013, а также обеспечивает интеграцию присутствия на страницах SharePoint 2013. Пользователей можно увидеть фотографий, имя, состояние присутствия и контактных данных людей в свой список контактов. Их можно начать сеанс, видеозвонок или телефонный звонок обмена мгновенными Сообщениями непосредственно из карточки контакта (элемент пользовательского интерфейса в Office 2013, что параметры информации и связи контактов поверхности). Office 2013 упрощает Оставайтесь на связи контактам, без учета вы не из электронной почты или документов. 
  
> [!NOTE]
> В этой статье термин обмена мгновенными Сообщениями клиентского приложения для указания специально для приложения, установленные на компьютере пользователя, который подключается к службе обмена мгновенными Сообщениями. Например Lync 2013 считается клиентского приложения обмена мгновенными Сообщениями. В этой статье отсутствуют подробные сведения о взаимодействии клиентское приложение обмена мгновенными Сообщениями к службе обмена мгновенными Сообщениями или о самой службы обмена мгновенными Сообщениями. 
  
Клиентского приложения обмена мгновенными Сообщениями можно настроить таким образом, чтобы он взаимодействует с Office. В частности можно изменить приложение обмена мгновенными Сообщениями, чтобы она отображала следующие сведения в рамках пользовательского интерфейса Office:
  
- Фотография контакта.
    
- Имя контакта.
    
- Заметки о состоянии контакта личные.
    
- Состояние присутствия контакта.
    
- Обратитесь в доступности строка (например, «Доступен» или «нет на работе»).
    
- Обратитесь в строку возможность (например, «видео Готово»).
    
- Запуск обмена мгновенными Сообщениями одним щелчком мыши.
    
- Запуск видео звонка одним щелчком мыши.
    
- Запуск телефонного звонка одним щелчком мыши (включая SIP, номер телефона, голосовой почты и новый номер звонка).
    
- Управление контактами (Добавить группу обмена мгновенными Сообщениями).
    
- Обратитесь в расположение и часовой пояс.
    
- Контактные данные, номер телефона, адрес электронной почты, должность и название компании.
    
**На рисунке 1. Карточка контакта в Office 2013**

![Карточка контакта в Office 2013] (media/ocom15_peoplecard.png "Карточка контакта в Office 2013")
  
Чтобы включить этот интеграции с Office, клиентского приложения обмена мгновенными Сообщениями необходимо реализовать набор интерфейсов, предоставляемых Office, чтобы подключиться к ней. Интерфейсы API для интеграции включены в пространстве имен [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) , который содержится в файле Microsoft.Office.UC.dll, который устанавливается вместе с версиями Office 2013, включая Lync / Скайп для бизнеса. Пространство имен **UCCollaborationLib** включает в себя интерфейсы, которые должны быть реализованы для интеграции с Office. 
  
> [!IMPORTANT] 
> Библиотека типов для необходимых интерфейсов встраивается в Lync 2013/Скайп для бизнеса. Для интеграторов сторонних производителей это работает только в том случае, если на целевом компьютере установлены Lync 2013 и Скайп для бизнеса. Если вы реализуете интеграцию с помощью Office Standard, необходимо извлечь библиотеку типов и установить его на целевом компьютере. [Пакет SDK для Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) включает в себя файл Microsoft.Office.UC.dll. 
  
> [!NOTE]
>  Аналогичным образом интеграции небольшое количество приложений Office 2010 в приложение поставщика обмена мгновенными Сообщениями сторонних производителей: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 и SharePoint Server 2010 (с помощью элемента управления ActiveX). Многие из действий, необходимых для интеграции с Office 2013 относятся к Office 2010 также. Существует ряд ключевых различий в интеграции Office 2010 с помощью поставщика приложения обмена мгновенными Сообщениями: 
>  - Office 2010 не отображать фотографии контакта. 
>  - Файл Microsoft.Office.Uc.dll необходимо загрузить отдельно с Office 2010. [Пакет SDK для Lync 2010](https://www.microsoft.com/en-us/download/details.aspx?id=18898) включает в себя файл Microsoft.Office.UC.dll для Office 2010. 
>  - Когда приложение Office вызывает метод [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) в клиентском приложении обмена мгновенными Сообщениями, передается в строку «14.0.0.0». 
>  - Office 2010 перечисляет все группы или контактов сразу же подключается к клиентского приложения обмена мгновенными Сообщениями. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>Как Office интегрируется с клиентского приложения обмена мгновенными Сообщениями
<a name="off15_IMIntegration_How"> </a>

При запуске приложения Office 2013 проходит через процесс интеграции с клиентского приложения обмена мгновенными Сообщениями по умолчанию:
  
1. Он проверяет реестр, чтобы обнаружить клиентского приложения обмена мгновенными Сообщениями по умолчанию и затем подключается к нему.
    
2. Оно выполняет проверку подлинности с помощью клиентского приложения обмена мгновенными Сообщениями.
    
3. Осуществляет подключение к определенным интерфейсы, предоставляемые интерфейсом клиентское приложение обмена мгновенными Сообщениями.
    
4. Он определяет возможности вошедшего в систему пользователя (локальный), включая начало контактов пользователя, определения присутствия пользователя, а также для определения возможности обмена мгновенными Сообщениями пользователя (обмен мгновенными сообщениями, видео-чат, VOIP и т. п.).
    
5. Он получает сведения о присутствии для контактов с локального пользователя.
    
6. При завершении работы приложения клиент обмена мгновенными Сообщениями, приложение Office 2013 отключает без уведомления.
    
### <a name="discovering-the-im-application"></a>Обнаружение приложений обмена мгновенными Сообщениями

Приложение Office выполняет поиск для нескольких конкретных ключей и записей в реестр, чтобы обнаружить клиентского приложения обмена мгновенными Сообщениями по умолчанию. При обнаружении клиентского приложения обмена мгновенными Сообщениями по умолчанию она пытается подключиться к ней.
  
Процесс, который проходит приложение Office для обнаружения клиентского приложения обмена мгновенными Сообщениями по умолчанию выглядит следующим образом:
  
1. Приложение Office проверяет, если HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp раздел реестра имеет значение и считывает списке имя приложения.
    
2. Приложение Office выберите считывает ключа \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _имя приложения_и отслеживает значение для изменения.
    
3. Затем приложение Office считывает раздел реестра HKEY_LOCAL_MACHINE\Software\IM Providers\ _имя приложения_ и получает значения ID (CLSID) ProcessName и классов, хранящимся в нем. 
    
4. После клиентского приложения обмена мгновенными Сообщениями имеет успешно завершена последовательность start и зарегистрирован все классы для интеграции сведений о присутствии, он задает ключ \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _имя приложения_, «2» Указывает, клиентского приложения.
    
5. Когда приложение Office обнаруживает, что ключ \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _имя приложения_имеет значение «2», проверяет список выполняющихся процессов на компьютере для имя процесса клиентского приложения обмена мгновенными Сообщениями.
    
6. Когда приложение Office обнаруживает процесс, который использует клиентское приложение обмена мгновенными Сообщениями, приложение Office вызывает **CoCreateInstance** с помощью CLSID для соединения с клиентского приложения обмена мгновенными Сообщениями как сервер COM ожидания процесса. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Проверка подлинности подключения к приложению обмена мгновенными Сообщениями

После приложение Office устанавливает подключение к клиентское приложение обмена мгновенными Сообщениями, затем происходит следующее:
  
1. Приложение Office вызывает метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) для проверки для интерфейса [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) . 
    
2. Затем приложение Office вызывает метод **IUCOfficeIntegration.GetAuthenticationInfo** , передав в наибольший интеграции поддерживаемые версии (например, «15.0.0.0»). 
    
3. Если клиентское приложение обмена мгновенными Сообщениями поддерживает версии Office, переданное в качестве параметра, приложение возвращает следующую строку XML-кодом коду вызова:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > В целях прежних версий клиентского приложения обмена мгновенными Сообщениями должен возвращать значение `<authenticationinfo>` для вызова **GetAuthenticationInfo** если оно поддерживает версию Office переданную как параметр. 
  
4. Если клиентское приложение обмена мгновенными Сообщениями не возвращает значение, приложение Office вызывает метод **GetAuthenticationInfo** еще раз с помощью следующего наивысшей поддерживаемой версии Microsoft Office (например, «14.0.0.0»). 
    
5. Когда Office определяет, что клиентское приложение обмена мгновенными Сообщениями поддерживает интеграцию обмена мгновенными Сообщениями и присутствия, подключается к необходимый набор интерфейсов для завершения инициализации. (Для получения дополнительных сведений см [необходимых интерфейсов](#off15_IMIntegration_HowConnect).)
    
Если приложение Office возникает ошибка на каком указанные выше шаги, отклоняться и интеграции присутствия не установлено во время сеанса приложения Office. 
  
### <a name="connecting-to-required-interfaces"></a>Подключение к необходимых интерфейсов
<a name="off15_IMIntegration_HowConnect"> </a>

После проверки подлинности подключения к клиентскому приложению обмена мгновенными Сообщениями, приложение Office пытается подключиться к набор необходимых интерфейсов, которые должны предоставлять клиентское приложение обмена мгновенными Сообщениями. Приложение Office это достигается следующим образом:
  
- Приложение Office получает [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) объект путем вызова метода **IUCOfficeIntegration.GetInterface** , передав в **oiInterfaceLyncClient** константа из перечисления [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) . 
    
- Приложение Office получает [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) объект путем вызова метода **IUCOfficeIntegration.GetInterface** , передав в **oiInterfaceAutomation** константа из перечисления **OIInterface** . 
    
- Прослушиватель событий [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) устанавливает приложение Office. 
    
- Прослушиватель событий [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) устанавливает приложение Office. 
    
- Приложение Office получает состояние входа из клиентского приложения обмена мгновенными Сообщениями с помощью свойства **ILyncClient.State** . 
    
- Приложение Office получает возможности обмена мгновенными Сообщениями клиентского приложения путем вызова метода **IUCOfficeIntegration.GetSupportedFeatures** , который возвращает флаг из перечисления [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) . 
    
- Приложение Office обращается к свойству **ILyncClient.Self** , чтобы получить ссылку на объект [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) . 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Извлечение возможности локального пользователя
<a name="off15_IMIntegration_HowConnect"> </a>

Приложение Office возвращает сведения о возможностях локального пользователя, выполните следующее:
  
1. Если клиентское приложение обмена мгновенными Сообщениями поддерживает интерфейс **IClient2** , Office пытается получить объект [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) с помощью свойства **IClient2.PrivateContactManager** . 
    
2. Если приложение обмена мгновенными Сообщениями не поддерживает интерфейс **IClient2** , приложение Office возвращает объект **IContactManager** с помощью свойства **ILyncClient.ContactManager** . Клиентское приложение обмена мгновенными Сообщениями успешно должен возвращать объект **IContactManager** , прежде чем можно установить другие возможности обмена мгновенными Сообщениями. 
    
3. Приложение Office обращается к свойству **ILyncClient.Uri** и затем вызывает **IContactManager.GetContactByUri** для получения объекта [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) , связанный с локального пользователя. 
    
4. Затем приложение Office вызывает несколько **IContact.CanStart** для установления возможности локального пользователя, передав значения для **ModalityTypes.ucModalityInstantMessage** и **ModalityTypes.ucModalityAudioVideo** последовательно. 
    
### <a name="retrieving-contact-presence"></a>Получение контактных сведений о присутствии
<a name="off15_IMIntegration_HowConnect"> </a>

Приложение Office возвращает контактных сведений о присутствии, включая локального пользователя, выполните следующие действия: 
  
1. Приложение Office вызывает **IContact.GetContactInformation** для получения сведений о присутствии элемента с контактом. 
    
2. Затем приложение Office подписывается на изменения состояния присутствия контакта. Он вызывает **IContactManager.CreateSubscription** для получения объекта [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) . Он вызывает **IContactSubscription.AddContact** , чтобы добавить контакт с подпиской и затем вызывает **IContactSubscription.Subscribe** для получения изменений в состояние контакта. 
    
3. Если приложение обмена мгновенными Сообщениями поддерживает **IContact2**, Office пытается получить сведения о присутствии, вызвав **IContact2.BatchGetContactInformation2**.
    
4. Затем приложение Office получает свойства присутствия контакта путем вызова **IContact.BatchGetContactInformation**. Приложение Office можно получить, обратившись к свойству **IContact.Settings** второй набор свойств, сведения о присутствии. 
    
5. И, наконец приложение Office получает членство в группах контакта с помощью свойства **IContact.CustomGroups** . Возвращает коллекцию [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) , которая включает в себя все объекты [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) , к которым принадлежит контакт. 
    
### <a name="disconnecting-from-the-im-application"></a>Отключение от приложения обмена мгновенными Сообщениями
<a name="off15_IMIntegration_HowConnect"> </a>

Отключение когда приложение Office 2013 обнаруживает события **OnShuttingDown** из приложения обмена мгновенными Сообщениями, без уведомления. Тем не менее при завершении работы приложения Office перед приложения обмена мгновенными Сообщениями, приложение Office не гарантирует, очистки подключения. Приложение обмена мгновенными Сообщениями должен обрабатывать утечки подключения клиента. 
  
## <a name="setting-registry-keys-and-entries"></a>Параметр реестра и записей
<a name="off15_IMIntegration_SetRegistry"> </a>

Как уже было сказано ранее, приложения поддержкой обмена мгновенными Сообщениями Office 2013 найдите определенных разделов, записей и значений реестра для обнаружения клиентское приложение обмена мгновенными Сообщениями для подключения к. Если эти значения реестра предоставляют приложения Office с помощью имя процесса и CLSID класса, который выступает в качестве точки входа для объектной модели клиентское приложение обмена мгновенными Сообщениями (класс, реализующий интерфейс **IUCOfficeIntegration** ). Приложение Office совместно создает этот класс и подключается как клиент COM-сервер вне процесса в клиентском приложении обмена мгновенными Сообщениями. 
  
Используйте в таблице 1 для определения клавиши, записи и значения, которые должны быть записаны в реестр, чтобы интегрировать клиентского приложения обмена мгновенными Сообщениями с помощью приложений Office.
  
**В таблице 1. Параметры реестра для настройки клиентского приложения обмена мгновенными Сообщениями по умолчанию**

|**Key**|**Запись**|**Тип**|**Значение**|**Пример**|
|:-----|:-----|:-----|:-----|:-----|
|Поставщики HKEY_LOCAL_MACHINE\Software\IM\\< имя приложения\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |Имя клиентского приложения обмена мгновенными Сообщениями сторонних производителей.  <br/> |Обмен мгновенными Сообщениями Litware 2012 г.  <br/> |
||ProcessName  <br/> |REG_SZ  <br/> |Имя процесса клиентского приложения обмена мгновенными Сообщениями сторонних производителей.  <br/> |Litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Класс ID (CLSID) для корневого, создаваемых посредством функции CoCreateInstance класса в приложении обмена мгновенными Сообщениями (класс, реализующий интерфейс **IUCOfficeIntegration** ).  <br/> |(GUID)  <br/> |
|Поставщики HKEY_CURRENT_USER\Software\IM  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |Имя клиентского приложения обмена мгновенными Сообщениями. Это должен быть совпадает с именем в верхнего уровня реестра (куст) в разделе HKEY_LOCAL_MACHINE.  <br/> |Litware  <br/> |
|Поставщики HKEY_CURRENT_USER\Software\IM\\< имя приложения\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Целое число от 0 до 2:  <br/>  0 — не выполняется  <br/>  1 — Запуск  <br/>  2 — под управлением  <br/> <br/>**Примечание**: раздел реестра имя приложения должен совпадать с значение параметра DefaultIMApp.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Реализация необходимые интерфейсы для интеграции с Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Существует три интерфейса из пространства имен **UCCollaborationLib** , исполняемый файл (или COM-сервера) клиентского приложения обмена мгновенными Сообщениями необходимо применить, чтобы его можно интегрировать с Office. Если эти интерфейсы не реализованы, приложение Office отклоняться во время инициализации и не установить подключение с помощью клиентского приложения обмена мгновенными Сообщениями. 
  
Доступны следующие обязательные интерфейсы:
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration), но не требуется, интерфейс **_IUCOfficeIntegrationEvents** также должен быть реализован в одном производного класса. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient), но не требуется, интерфейс **_ILyncClientEvents** также должен быть реализован в одном производного класса. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>Интерфейс IUCOfficeIntegration
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

Интерфейс **IUCOfficeIntegration** предоставляет точки входа для приложения Office, чтобы подключиться к приложению клиент обмена мгновенными Сообщениями. Интерфейс определяет три метода, которые приложение Office вызывает как часть процесса осуществить соединение с клиентского приложения обмена мгновенными Сообщениями. Класс, реализующий интерфейс **IUCOfficeIntegration** должен быть совместного открыты, чтобы Office совместного можно создать его экземпляр. Кроме того он должен предоставлять CLSID, которое вводится как значение GUID запись в раздел реестра HKEY_LOCAL_MACHINE\Software\IM Providers\ _имя приложения_ . 
  
Класс, который наследует от **IUCOfficeIntegration** также требуется реализовать интерфейс **_IUCOfficeIntegrationEvents** . Интерфейс **_IUCOfficeIntegrationEvents** содержит элементы, которые предоставляют доступ к обработчики событий интерфейса **IUCOfficeIntegration** . 
  
В таблице 2 показаны элементы, которые должны быть реализованы в классе, который наследует от **IUCOfficeIntegration** и **_IUCOfficeIntegration**.
  
> [!NOTE]
> Дополнительные сведения о **IUCOfficeIntegration** и **_IUCOfficeIntegrationEvents** интерфейсы и их члены можно [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) и [UCCollaborationLib._IUCOfficeIntegrationEvents ](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**В таблице 2. Реализация интерфейсов IUCOfficeIntegration и _IUCOfficeIntegrationEvents**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |Метод **GetAuthenticationInfo**  <br/> |Получает строку, сведения о проверки подлинности.  <br/> |
||Метод **GetInterface**  <br/> |Получает интерфейс определенной версии.  <br/> |
||Метод **GetSupportedFeatures**  <br/> |Получает поддерживаемые функции интеграции с Office.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |Событие **OnShuttingDown**  <br/> |Событие, возникающее при попытке завершить работу клиентского приложения обмена мгновенными Сообщениями.  <br/> |
   
Используйте следующий код для определения класса, наследуемого от интерфейсов **IUCOfficeIntegration** и **_IUCOfficeIntegration** в приложении клиент обмена мгновенными Сообщениями. 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

Метод **GetAuthenticationInfo** принимает строку, в качестве аргумента для параметра _версии_ . Когда приложение Office вызывает этот метод, передается в одном из двух строк для аргумента, в зависимости от версии Office. Когда приложение Office предоставляет метод с версии Office, которая поддерживает клиентское приложение обмена мгновенными Сообщениями (то есть, поддерживает функциональные возможности), метод **GetAuthenticationInfo** возвращает строку XML-кодом `<authenticationinfo>`. 
  
Используйте следующий код для реализации метода **GetAuthentication** в код приложения клиент обмена мгновенными Сообщениями. 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

Метод **GetInterface** передвигаются ссылки на классы коду вызова, в зависимости от того, что передается в качестве аргумента для параметра _интерфейса_ . Когда приложение Office вызывает метод **GetInterface** , передается в одно из двух значений для параметра интерфейса: константа **oiInterfaceILyncClient** (1) или константа **oiInterfaceIAutomation** (2) из [ UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) перечисления. Если приложение Office передает **oiInterfaceILyncClient** константу, метод **GetInterface** возвращает ссылку на класс, реализующий интерфейс **ILyncClient** . Если приложение Office передает **oiInterfaceIAutomation** константу, метод **GetInterface** возвращает класс, реализующий интерфейс **IAutomation** . 
  
Используйте следующий пример кода для реализации метода **GetInterface** в код приложения клиент обмена мгновенными Сообщениями. 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

Метод **GetSupportedFeatures** возвращает сведения о функции обмена мгновенными Сообщениями, которые поддерживает клиентское приложение обмена мгновенными Сообщениями. Она принимает строку, для его единственный параметр _версии_. Когда приложение Office вызывает метод **GetSupportFeatures** , метод возвращает значение из перечисления [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) . Возвращаемое значение указывает возможности клиент обмена мгновенными Сообщениями, где каждой возможности обмена мгновенными Сообщениями клиентского приложения указывается в приложение Office, добавив флаг значение. 
  
> [!NOTE]
>  Приложения Office 2013 игнорировать следующие константы в перечислении **OIFeature** : 
> - **oiFeaturePictures** (2) 
> - **oiFeatureFreeBusyIntegration**
> - **oiFeaturePhoneNormalization**
  
Используйте следующий пример кода для реализации метода **GetSupportFeatures** в код приложения клиент обмена мгновенными Сообщениями. 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a>Интерфейс ILyncClient
<a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a>

Интерфейс **ILyncClient** сопоставляет возможности обмена мгновенными Сообщениями клиентского приложения. Она предоставляет свойства, связанные с человека, который вошел в приложении (локальный пользователь, представленный в интерфейсе [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf) ), состояние приложения, в списке контактов для локального пользователя и некоторые другие параметры. Когда она пытается подключиться к приложению клиент обмена мгновенными Сообщениями, приложение Office получает ссылку на объект, реализующий интерфейс **ILyncClient** . По этой ссылки Office может получить доступ практически возможности обмена мгновенными Сообщениями клиентского приложения. 
  
Кроме того класс, реализующий интерфейс **ILyncClient** также требуется реализовать интерфейс **_ILyncClientEvents** . Интерфейс **_ILyncClientEvents** предоставляет несколько событий, которые необходимы для отслеживания состояния клиентское приложение обмена мгновенными Сообщениями. 
  
В таблице 3 показаны элементы, которые должны быть реализованы в классе, который наследует от **ILyncClient** и **_ILyncClientEvents**.
  
> [!NOTE]
> Любой участник **ILyncClient** или ** \_ILyncClientEvents** интерфейс, не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызывать **NotImplementedException** или **E\_NOTIMPL** ошибка. 
> 
> Дополнительные сведения о **ILyncClient** и **_ILyncClientEvents** интерфейсы и их члены можно [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) и [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**В таблице 3. Реализация интерфейсов ILyncClient и ILyncClientEvents**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |Свойство **ContactManager**  <br/> |Возвращает диспетчер группы контактов.  <br/> |
||Свойство **ConversationManager**  <br/> |Возвращает диспетчер бесед.  <br/> |
||Свойство **SELF**  <br/> |Получает объект **Self** .  <br/> |
||Метод **Вход**  <br/> |Запускает обмена мгновенными Сообщениями клиентского приложения входа в процесс с определенным доступности.  <br/> |
||Свойство **состояний**  <br/> |Возвращает текущее состояние платформы.  <br/> |
||Свойство **URI**  <br/> |Возвращает URI клиентское приложение обмена мгновенными Сообщениями.  <br/> |
|**_ILyncClientEvents** <br/> |Событие **OnStateChanged**  <br/> |Возникает при изменении состояния приложения клиент обмена мгновенными Сообщениями. Необходимо обрабатывать и получить свойство **eventData.NewState** . Событие все процессы, привязанного к экземпляру клиентского приложения обмена мгновенными Сообщениями, когда все подсистемы в приложении вызывает изменение состояния.  <br/> |
   
Во время инициализации Office обращается к свойству **ILyncClient.State** . Это свойство должен возвращать значение из перечисления [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState) . 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

Свойство **State** сохраняет текущее состояние клиентского приложения обмена мгновенными Сообщениями. Необходимо установить и обновлено в течение всего сеанса обмена мгновенными Сообщениями клиентского приложения. Когда обмен мгновенными Сообщениями клиентское приложение входит в, выходит или завершает работу, его следует установить свойство **состояний** . Рекомендуется устанавливать это свойство в методы **ILyncClient.SignIn** и **ILyncClient.SignOut** , как показано в следующем примере. 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

В следующем примере кода показано, как настроить прослушиватель событий, с помощью _ **ILyncClientEvents** и _ **IUCOfficeIntegrationEvents** интерфейсов. 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a>Интерфейс IAutomation
<a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a>

Интерфейс **IAutomation** автоматизирует функции обмена мгновенными Сообщениями клиентского приложения. Его можно использовать для начало бесед, участвовать в конференциях и обеспечения расширяемости окно контекста. 
  
В таблице 4 показаны элементы, которые должны быть реализованы в классе, который наследует от **IAutomation**.
  
> [!NOTE]
> Любой элемент в интерфейсе **IAutomation** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** . 
> 
> Дополнительные сведения об интерфейсе **IAutomation** и его члены можно [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**В таблице 4. Реализация интерфейса IAutomation**

|**Элемент**|**Описание**|
|:-----|:-----|
|Метод **StartConversation**  <br/> |Запускает в беседе при помощи модальность указанного беседы. Экземпляр **IConversationWindow** возвращается.  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Реализация интеграции контактных сведений о присутствии
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

В дополнение к три необходимые интерфейсы, описанных ранее существует несколько интерфейсов, которые важны для включения функции контактных сведений о присутствии в Office. К ним относятся следующие:
  
- Интерфейс [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) или **IContact2** . 
    
- Интерфейс [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) . 
    
- Интерфейсы [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) и [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) . 
    
- Интерфейсы [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) и [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) . 
    
- Интерфейс [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) . 
    
- Интерфейс [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) . 
    
- Интерфейс [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) 
    
### <a name="icontact-interface"></a>Интерфейс IContact
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

Интерфейс **IContact** представляет пользователь приложения клиент обмена мгновенными Сообщениями. Интерфейс предоставляет сведения о присутствии, доступные модальности, членство в группах и свойства тип контакта для пользователя. Чтобы начать беседу с другим пользователем, необходимо предоставить экземпляр **IContact**этого пользователя.
  
В таблице 5 показаны элементы, которые должны быть реализованы в классе, который наследует от **IContact**.
  
> [!NOTE]
> Любой элемент в интерфейсе **IContact** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** . 
>
> Дополнительные сведения об интерфейсе **IContact** и его члены можно [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**В таблице 5. Реализация интерфейса IContact**

|**Элемент**|**Описание**|
|:-----|:-----|
|Метод **CanStart**  <br/> |Возвращает **значение true** , если заданного типа модальность может запускаться на контакт.  <br/> |
|Метод **GetContactInformation**  <br/> |Получает один элемент сведений о присутствии от публикации контакта.  <br/> |
|Метод **BatchGetContactInformation**  <br/> |Получает несколько элементов сведений о присутствии от публикации контакта.  <br/> |
|Свойства **параметров**  <br/> |Получает коллекцию свойства контакта.  <br/> |
|Свойство **CustomGroups**  <br/> |Получает коллекцию групп, которым принадлежит контакт.  <br/> |
   
Во время инициализации приложения Office вызывает метод **IContact.CanStart** для определения возможности обмена мгновенными Сообщениями для локального пользователя. Метод **CanStart** принимает флаг из перечисления [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) в качестве аргумента для параметра_modalityTypes_ _. Если текущий пользователь могли взаимодействовать в запрошенные модальности (то есть, пользователь способен обмена мгновенными сообщениями, аудио- и видеоконференций обмена мгновенными сообщениями или общего доступа к приложениям), метод **CanStart** возвращает **значение true**.
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

Метод **GetContactInformation** получает сведения о контакте из объекта **IContact** . Вызывающий код должен передать значение из перечисления [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) для параметра_contactInformationType_ _ указывает данные, которые нужно вернуть. 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

Как и **GetContactInformation**, метод **BatchGetContactInformation** получает несколько элементов сведений о присутствии о контакте из объекта **IContact** . Вызывающий код должен передать в массив значений из перечисления **ContactInformationType** для параметра_contactInformationTypes_ _. Метод возвращает объект [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) , содержащий запрошенные данные. 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

Свойство **IContact.Settings** возвращает объект **IContactSettingDictionary** , который содержит пользовательские свойства о контакте. 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

Свойство **IContact.CustomGroups** возвращает объект **IGroupCollection** , который включает в себя всех групп, членом которых является контактом. 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a>Интерфейс ISelf
<a name="off15_IMIntegration_ImplementRequired_ISelf"> </a>

Во время инициализации приложения Office с помощью свойства **ILyncClient.Self** , который должен возвращать объект **ISelf** получает данные для текущего пользователя. Интерфейс **ISelf** представляет локального, выполнившего вход пользователя клиентского приложения обмена мгновенными Сообщениями. 
  
В таблице 6 показаны элементы, которые должны быть реализованы в классе, который наследует от **ISelf**.
  
> [!NOTE]
> Любой элемент в интерфейсе **ISelf** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** . 
  
**В таблице 6. Реализация интерфейса ISelf**

|**Элемент**|**Описание**|
|:-----|:-----|
|Свойство **контакта**  <br/> |Возвращает объект **IContact** , связанный с локального пользователя.  <br/> |
   
Сведения о присутствии, доступные модальности, членство в группах и свойства тип контакта для локального пользователя, предоставляемые с помощью свойства **ISelf.Contact** (который возвращает объект **IContact** ). Во время инициализации приложения Office обращается к свойству **ISelf.Contact** для получения ссылки на контактные данные для локального пользователя. 
  
Используйте следующий код для определения класса, наследуемого от **ISelf** интерфейс, который реализует свойства **контакта** . 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a>Интерфейсы IContactManager и _IContactManagerEvents
<a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a>

Объект **IContactManager** управляет контакты для локального пользователя, включая контактные данные локального пользователя. Приложение Office использует объект **IContactManager** для доступа к объектам **IContact** , которые соответствуют контакты локального пользователя. 
  
В таблице 7 представлены элементы, которые должны быть реализованы в классе, который наследует от **IContactManager** и **_IContactManagerEvents**.
  
> [!NOTE]
> Любой элемент в интерфейсе **IContactManager** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызывать **NotImplementedException** или **E\_NOTIMPL** ошибка. 
>
> Дополнительные сведения о **IContactManager** и **_IContactManagerEvents** интерфейсы и их члены можно [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) и [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**В таблице 7. Реализация интерфейсов IContactManager и _IContactManagerEvents**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |Метод **GetContactByUri**  <br/> |Находит или создает новый экземпляр контакта с помощью контакта URI.  <br/> |
||Метод **CreateSubscription**  <br/> |Создает объект **ISubscription** , который может использоваться для пакетной обработки подписок или запросов.  <br/> |
||Метод **поиска**  <br/> |Поиск контакта или группы рассылки.  <br/> |
|**_IContactManagerEvents** <br/> |Событие **OnGroupAdded**  <br/> |Возникает при добавлении группы в семейство сайтов группы. Коллекции обновленные группы можно получить из свойства **IContactManager.Groups** .  <br/> |
||Событие **OnGroupRemoved**  <br/> |Возникает при удалении группы из коллекции группы. Коллекции обновленные группы можно получить из свойства **IContactManager.Groups** .  <br/> |
||Событие **OnSearchProviderStateChanged**  <br/> |Возникает при изменении состояния службы поиска.  <br/> |
   
Office вызывает **IContactManager.GetContactByUri** для получения сведений о присутствии контакта с помощью SIP-адрес контакта. Когда контакт, настроенный для SIP-адрес в Active Directory, Office определяет этот адрес контакта и вызовы **GetContactByUri**, передав SIP-адрес контакта в для параметра_contactUri_ _. 
  
Когда Office не может определить адрес SIP контакта, он вызывает метод **IContactManager.Lookup** для поиска SIP с помощью службы обмена мгновенными Сообщениями. Здесь Office передает в наиболее данных, его можно найти для контакта (например, просто адрес электронной почты контакта). Метод **поиска** асинхронно возвращает объект **AsynchronousOperation** . Когда он вызывает функцию обратного вызова, метод **поиска** должна вернуть успешное или неудачное выполнение операции в дополнение к URI контакта. 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

Подписаться на изменения сведений о присутствии для отдельного контакта требуются приложения Office. Таким образом, когда состояние присутствия контакта изменяется, обмен мгновенными Сообщениями сервера оповещений клиентское приложение обмена мгновенными Сообщениями, тем самым предупреждения приложения Office. Для этого приложения Office вызывает метод **IContactManager.CreateSubscription** для создания нового объекта **IContactSubscription** для этого запроса. 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a>Интерфейсы IGroup и IGroupCollection
<a name="off15_IMIntegration_ImplementRequired_IGroup"> </a>

Объект **IGroup** представляет набор контактов с помощью дополнительных свойств для идентификации коллекции контакта по имени общую группу. Объект **IGroupCollection** представляет коллекцию объектов **IGroup** , определенные в локальных пользователей и клиентское приложение обмена мгновенными Сообщениями. Приложения Office с помощью объектов **IGroupCollection** и **IGroup** доступ к контакты локального пользователя. 
  
В таблице 9 показаны элементы, которые должны быть реализованы в классы, наследующие от **IGroup** и **IGroupCollection** в следующей таблице. 
  
> [!NOTE]
> Любой элемент в интерфейсе **IGroup** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** . 
>
> Дополнительные сведения о **IGroup** и **IGroupCollection** интерфейсов и их члены можно [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) и [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**В таблице 9. Реализация интерфейсов IGroup и IGroupCollection**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |Свойство **Count**  <br/> |Возвращает число объектов **IGroup** в коллекции  <br/> |
||Свойство **Item**  <br/> |Возвращает объект **IGroup** по указанному индексу в коллекции.  <br/> |
|**IGroup** <br/> |Свойство **ID**  <br/> |Возвращает идентификатор группы.  <br/> |
   
Когда приложение Office возвращает сведения для локального пользователя, он обращается к членство в группах для контакта (локального пользователя), вызвав свойство **IContact.CustomGroups** , которое возвращает объект **IGroupCollection** . **IGroupCollection** должен содержать массив (или **списка**) **IGroup** объектов. Класс, производный от **IGroupCollection** должен предоставлять свойство **Count** , которое возвращает количество элементов в коллекции и метод проверки компонента индексирования **this(int)**, которое возвращает объект **IGroup** из коллекции. 
  
### <a name="icontactsubscription-interface"></a>Интерфейс IContactSubscription
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

Интерфейс **IContactSubscription** позволяет выбирать контакты для получения сведений о присутствии обновлять сведения о и типов сведений о присутствии, которые активируют уведомление. Приложения Office используйте объект **IContactSubscription** для регистрации изменений в состояние присутствия контакта. 
  
В таблице 10 показаны элементы, которые должны быть реализованы в классы, наследующие от **IContactSubscription**.
  
> [!NOTE]
> Любой элемент в интерфейсе **IContactSubscription** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .
>
> Дополнительные сведения об интерфейсе **IContactSubscription** и его члены можно [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**В таблице 10. Реализация интерфейса IContactSubscription**

|**Элемент**|**Описание**|
|:-----|:-----|
|Метод **AddContact**  <br/> |Добавляет объект подписки контакта.  <br/> |
|**Подписки на** метод  <br/> |Эта статья поможет клиентское приложение обмена мгновенными Сообщениями для отслеживания присутствия контакта.  <br/> |
   
Интерфейс **IContactSubscription** должен содержать ссылки на все объекты **IContact** , оно отслеживает, с помощью массив или **список**. Метод **IContactSubscription.AddContact** добавляет объект **IContact** для для структуры данных объекта **IContactSubscription** , тем самым Добавление нового контакта для наблюдения за изменения сведений о присутствии. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

Метод **IContactSubscription.Subscribe** позволяет клиентского приложения обмена мгновенными Сообщениями для доступа к наблюдатели присутствия контакта. Его можно использовать стратегию опроса для получения сведений о присутствии с сервера для контактов, которые подписана клиентское приложение обмена мгновенными Сообщениями. Метод **подписки на** полезно в тех случаях, когда запрашиваются сведения о присутствии для пользователя не из списка контактов пользователя (например, от большего публичная сеть). 
  
### <a name="icontactendpoint-interface"></a>Интерфейс IContactEndPoint
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

**IContactEndPoint** представляет телефонный номер из коллекции контакта телефонных номеров. 
  
В таблице 11 показаны элементы, которые должны быть реализованы в классы, наследующие от **IContactEndPoint**.
  
> [!NOTE]
> Любой элемент в интерфейсе **IContactEndPoint** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .
>
> Дополнительные сведения об интерфейсе **IContactEndPoint** и его члены можно [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**В таблице 11. Реализация интерфейса IContactEndPoint**

|**Элемент**|**Описание**|
|:-----|:-----|
|Свойство **DisplayName**  <br/> |Получает строку, отображение.  <br/> |
|Свойство **Type**  <br/> |Получает тип контакта конечной точки  <br/> |
|Свойство **URI**  <br/> |Получает контакт URI.  <br/> |
   
### <a name="ilocalestring-interface"></a>Интерфейс ILocaleString
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

**ILocaleString** — это структура локализованные строки, которая содержит локализованные строковые и код языка для локализации. Интерфейс **ILocaleString** используется для форматирования строку настраиваемой состояние в карточке контакта. 
  
В таблице 12 показаны элементы, которые должны быть реализованы в классы, наследующие от **ILocaleString**.
  
> [!NOTE]
> Любой элемент в интерфейсе **ILocaleString** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована. Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .
>
> Дополнительные сведения об интерфейсе **ILocalString** и его члены можно [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**В таблице 12. Реализация интерфейса ILocaleString**

|**Элемент**|**Описание**|
|:-----|:-----|
|Свойство **LocaleId**  <br/> |Получает идентификатор языка.  <br/> |
|Свойство **value**  <br/> |Получает строку.  <br/> |
   
## <a name="see-also"></a>См. также

- Пространство имен [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) 
    

