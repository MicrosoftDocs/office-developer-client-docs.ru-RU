---
title: Интеграция приложений для обмена мгновенными сообщениями с приложениями Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: В этой статье описано, как настроить клиентское приложение для обмена мгновенными сообщениями так, чтобы интегрировать его с социальными функциями в Office 2013, включая отображение сведений о присутствии и отправку мгновенных сообщений из карточки контакта.
localization_priority: Priority
ms.openlocfilehash: b3add86f011e016b1b6ea1a74f425f3f1deab002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270120"
---
# <a name="integrating-im-applications-with-office"></a>Интеграция приложений для обмена мгновенными сообщениями с приложениями Office

В этой статье описано, как настроить клиентское приложение для обмена мгновенными сообщениями так, чтобы интегрировать его с социальными функциями в Office 2013, включая отображение сведений о присутствии и отправку мгновенных сообщений из карточки контакта.
  
Если у вас есть вопросы или комментарии к этой технической статье в отношении процессов, которые в ней описаны, вы можете обратиться напрямую в корпорацию Майкрософт, написав по адресу [docthis@microsoft.com](mailto:docthis@microsoft.com).
  
## <a name="introduction"></a>Введение
<a name="off15_IMIntegration_Intro"> </a>

Office 2013 располагает широкими возможностями интеграции с клиентскими приложениями для обмена мгновенными сообщениями, включая Lync 2013. Такая интеграция позволяет пользователям обмениваться мгновенными сообщениями из Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 и OneNote 2013, а также обеспечивает интеграцию сведений о присутствии на страницах SharePoint 2013. Пользователи могут просматривать фотографию, имя, состояние присутствия и контактные данные людей в своем списке контактов. Можно начать сеанс обмена мгновенными сообщениями, видеозвонок или телефонный звонок прямо из карточки контакта (элемент пользовательского интерфейса в Office 2013, содержащий контактную информацию и опции взаимодействия). Office 2013 позволяет легко поддерживать связь с пользователями из списка контактов, не откладывая работу с электронной почтой и документами. 
  
> [!NOTE]
> В этой статье используется термин "клиентское приложение для обмена мгновенными сообщениями", означающий конкретное приложение, установленное на компьютере пользователя, которое осуществляет взаимодействие со службой обмена мгновенными сообщениями. Например приложение Lync 2013 считается клиентским приложением для обмена мгновенными сообщениями. В этой статье не приводятся подробные сведения о том, как клиентское приложение для обмена мгновенными сообщениями взаимодействует со службой обмена мгновенными сообщениями, а также о самой службе обмена мгновенными сообщениями. 
  
Вы можете настраивать клиентское приложение для обмена мгновенными сообщениями таким образом, чтобы оно осуществляло взаимодействие с Office. В частности вы можете внести изменения в свое приложение для обмена мгновенными сообщениями так, чтобы оно отображало приведенные ниже сведения в пользовательском интерфейсе Office:
  
- фотография контакта;
    
- имя контакта;
    
- примечание о личном статусе контакта;
    
- состояние присутствия контакта;
    
- строка доступности контакта (например, "Доступен" или "Нет на месте");
    
- строка возможностей контакта (например, "Видео готово");
    
- запуск обмена мгновенными сообщениями одним щелчком;
    
- запуск видеозвонка одним щелчком;
    
- запуск телефонного звонка одним щелчком (в том числе SIP, номер телефона, голосовая почта и звонок на новый номер);
    
- управление контактами (добавление в группу обмена мгновенными сообщениями);
    
- местонахождение контакта и часовой пояс;
    
- данные контакта, номер телефона, адрес электронной почты, должность и название компании.
    
**Рис. 1. Карточка контакта в Office 2013**

![Карточка пользователя в Office 2013](media/ocom15_peoplecard.png "Карточка пользователя в Office 2013")
  
Чтобы сделать возможной такую интеграцию с Office, в клиентском приложении для обмена мгновенными сообщениями должен быть реализован набор интерфейсов, предоставляемых Office для подключения к нему. API для такой интеграции включены в пространство имен [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx), которое содержится в файле Microsoft.Office.UC.dll, установленном вместе с версиями Office 2013, которые включают Lync / Skype для бизнеса. Пространство имен **UCCollaborationLib** включает интерфейсы, которые следует реализовать для интеграции с Office. 
  
> [!IMPORTANT] 
> Библиотека типов обязательных интерфейсов встроена в Lync 2013 / Skype для бизнеса. Для сторонних интеграторов это применимо только в том случае, если и Lync 2013, и Skype для бизнеса установлены на целевой компьютер. Если вы выполняете интеграцию, используя Office стандартный, вам потребуется извлечь библиотеку типов и установить ее на целевой компьютер. [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) включает файл Microsoft.Office.UC.dll. 
  
> [!NOTE]
>  Некоторые приложения Office 2010 могут подобным образом интегрироваться со сторонним приложением для обмена мгновенными сообщениями: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 и SharePoint Server 2010 (используя элемент ActiveX). Многие действия, необходимые для интеграции с Office 2013, также применимы к Office 2010. Есть несколько важных различий в том, как Office 2010 интегрируется с приложением для обмена мгновенными сообщениями. 
>  - В Office 2010 фото контакта не отображается. 
>  - Необходимо скачать файл Microsoft.Office.Uc.dll отдельно от Office 2010. [Lync 2010 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=18898) включает файл Microsoft.Office.UC.dll для Office 2010. 
>  - Когда приложение Office вызывает метод [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) в клиентском приложении для обмена мгновенными сообщениями, оно передает строку "14.0.0.0". 
>  - Office 2010 перечисляет все группы и контакты, как только устанавливает подключение к клиентскому приложению для обмена мгновенными сообщениями. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>Как выполняется интеграция Office с клиентским приложением для обмена мгновенными сообщениями
<a name="off15_IMIntegration_How"> </a>

При запуске приложения Office 2013 выполняется указанный ниже порядок действий для интеграции с клиентским приложением для обмена мгновенными сообщениями по умолчанию.
  
1. Оно выполняет проверку реестра для обнаружения клиентского приложения для обмена мгновенными сообщениями по умолчанию, а затем подключается к нему.
    
2. Оно выполняете проверку подлинности с помощью клиентского приложения для обмена мгновенными сообщениями.
    
3. Оно подключается к определенным интерфейсам, которые отображаются клиентским приложением для обмена мгновенными сообщениями.
    
4. Оно определяет возможности пользователя, который в настоящий момент выполнил вход в систему (локальный пользователь), включая получение контактов пользователя, определение сведений о присутствии пользователя и определение возможностей пользователя в отношении обмена мгновенными сообщениями (обмен мгновенными сообщениями, видеочат, VOIP и т. д.).
    
5. Оно получает сведения о присутствии для контактов локального пользователя.
    
6. Когда клиентское приложение для обмена мгновенными сообщениями завершает работу, приложение Office 2013 отключается без уведомления.
    
### <a name="discovering-the-im-application"></a>Обнаружение приложения для обмена мгновенными сообщениями

Приложение Office выполняет поиск нескольких определенных разделов и записей в реестре, чтобы обнаружить клиентское приложение для обмена мгновенными сообщениями по умолчанию. Если оно находит клиентское приложение для обмена мгновенными сообщениями по умолчанию, выполняет попытку подключиться к нему.
  
Порядок действий, которые выполняет приложение Office, чтобы обнаружить клиентское приложение для обмена мгновенными сообщениями по умолчанию, приводится ниже.
  
1. Приложение Office выполняет поиск, чтобы выяснить, задан ли подраздел HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp в реестре и считывает ли он имя приложения, указанное в нем.
    
2. Затем приложение Office считывает раздел HKEY_CURRENT_USER\Software\IM Providers\ _Имя приложения_\UpAndRunning и отслеживает значение на предмет изменений.
    
3. Затем приложение Office считывает раздел реестра HKEY_LOCAL_MACHINE\Software\IM Providers\ _Имя приложения_ и получает значения ProcessName и идентификатор класса (CLSID), хранящиеся в нем. 
    
4. После того как клиентское приложение для обмена мгновенными сообщениями успешно завершит последовательность запуска и правильно зарегистрирует все классы для интеграции сведений о присутствии, оно задает для раздела HKEY_CURRENT_USER\Software\IM Providers\ _Имя приложения_\ UpAndRunning значение "2", указывая, что клиентское приложение выполняется.
    
5. Когда приложение Office обнаруживает, что для раздела HKEY_CURRENT_USER\Software\IM Providers\ _Имя приложения_\UpAndRunning задано значение "2", оно проверяет список выполняемых процессов на компьютере для выявления имени процесса клиентского приложения для обмена мгновенными сообщениями.
    
6. После того как приложение Office находит процесс, используемый клиентским приложением для обмена мгновенными сообщениями, оно вызывает **CoCreateInstance**, используя CLSID для установления подключения к клиентскому приложению для обмена мгновенными сообщениями, как внепроцессный сервер COM. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Аутентификация подключения к приложению для обмена мгновенными сообщениями

После того как приложение Office установит подключение к клиентскому приложению для обмена мгновенными сообщениями, оно выполняет указанные ниже действия.
  
1. Приложение Office вызывает метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) для выявления интерфейса [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). 
    
2. Затем приложение Office вызывает метод **IUCOfficeIntegration.GetAuthenticationInfo**, передавая самую последнюю поддерживаемую версию интеграции (например, "15.0.0.0"). 
    
3. Если клиентское приложение для обмена мгновенными сообщениями поддерживает версию, переданную приложением Office в качестве параметра, приложение возвращает следующую жестко заданную строку XML коду вызова:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > По причине возможного устаревания клиентское приложение для обмена мгновенными сообщениями должно вернуть точное значение `<authenticationinfo>` для вызова **GetAuthenticationInfo**, если оно поддерживает версию Office, переданную в качестве параметра. 
  
4. Если клиентское приложение для обмена мгновенными сообщениями не может вернуть значение, приложение Office вызывает метод **GetAuthenticationInfo** снова, используя следующую наиболее актуальную версию Office (например, "14.0.0.0"). 
    
5. После того как приложение Office определяет, что клиентское приложение для обмена мгновенными сообщениями поддерживает интеграцию обмена мгновенными сообщениями и сведений о присутствии, оно подключается к обязательному набору интерфейсов для завершения инициализации. (Для получения дополнительной информации см. статью [Подключение к обязательным интерфейсам](#off15_IMIntegration_HowConnect).)
    
Если приложение Office обнаруживает ошибку в ходе выполнения любого из описанных выше действий, оно отменяет выполненное ранее, и интеграция сведений о присутствии больше не будет устанавливаться во время сеанса приложения Office. 
  
### <a name="connecting-to-required-interfaces"></a>Подключение к обязательным интерфейсам
<a name="off15_IMIntegration_HowConnect"> </a>

После аутентификации подключения к клиентскому приложению для обмена мгновенными сообщениями приложение Office пытается подключиться к набору обязательных интерфейсов, которые клиентское приложение для обмена мгновенными сообщениями должно представлять. Приложение Office выполняет это в указанном ниже порядке.
  
- Приложение Office получает объект [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient), вызывая метод **IUCOfficeIntegration.GetInterface** посредством передачи константы **oiInterfaceLyncClient** из перечисления [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). 
    
- Приложение Office получает объект [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation), вызывая метод **IUCOfficeIntegration.GetInterface** посредством передачи константы **oiInterfaceAutomation** из перечисления **OIInterface**. 
    
- Приложение Office задает прослушиватель событий [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). 
    
- Приложение Office задает прослушиватель событий [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). 
    
- Приложение Office получает состояние выполнения входа из клиентского приложения для обмена мгновенными сообщениями, выполняя доступ к свойству **ILyncClient.State**. 
    
- Приложение Office получает возможности клиентского приложения для обмена мгновенными сообщениями, вызывая метод **IUCOfficeIntegration.GetSupportedFeatures**, который возвращает отметку из перечисления [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). 
    
- Приложение Office выполняет доступ к свойству **ILyncClient.Self**, чтобы получить ссылку на объект [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf). 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Получение возможностей локального пользователя
<a name="off15_IMIntegration_HowConnect"> </a>

Приложение Office получает возможности локального пользователя в указанном ниже порядке.
  
1. Если клиентское приложение для обмена мгновенными сообщениями поддерживает интерфейс **IClient2**, Office пытается получить объект [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager), выполняя доступ к свойству **IClient2.PrivateContactManager**. 
    
2. Если приложение для обмена мгновенными сообщениями не поддерживает интерфейс **IClient2**, приложение Office получает объект **IContactManager**, выполняя доступ к свойству **ILyncClient.ContactManager**. Клиентское приложение для обмена мгновенными сообщениями должно успешно вернуть объект **IContactManager**, прежде чем можно будет установить любую из других возможностей обмена мгновенными сообщениями. 
    
3. Приложение Office выполняет доступ к свойству **ILyncClient.Uri**, а затем вызывает **IContactManager.GetContactByUri**, чтобы получить объект [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact), связанный с локальным пользователем. 
    
4. Затем приложение Office выполняет несколько вызовов **IContact.CanStart**, чтобы установить возможности локального пользователя, последовательно передавая значения для **ModalityTypes.ucModalityInstantMessage** и **ModalityTypes.ucModalityAudioVideo**. 
    
### <a name="retrieving-contact-presence"></a>Получение сведений о присутствии контакта
<a name="off15_IMIntegration_HowConnect"> </a>

Приложение Office получает сведения о присутствии контакта, в том числе локального пользователя, выполняя указанные ниже действия. 
  
1. Приложение Office вызывает **IContact.GetContactInformation**, чтобы получить элемент сведений о присутствии от контакта. 
    
2. Затем приложение Office подписывается на получение сведений об изменении состояния присутствия от контакта. Оно вызывает **IContactManager.CreateSubscription**, чтобы получить объект [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription). Затем оно вызывает **IContactSubscription.AddContact**, чтобы добавить контакт в подписку, а после вызывает **IContactSubscription.Subscribe** для получения сведений об изменении статуса контакта. 
    
3. Если приложение для обмена мгновенными сообщениями поддерживает **IContact2**, приложение Office выполняет попытку получить сведения о присутствии, вызывая **IContact2.BatchGetContactInformation2**.
    
4. Затем приложение Office получает свойства присутствия для контакта, вызывая **IContact.BatchGetContactInformation**. Приложение Office может получить второй набор свойств присутствия, выполнив доступ к свойству **IContact.Settings**. 
    
5. И наконец, приложение Office получает сведения об участии контакта в группах, выполняя доступ к свойству **IContact.CustomGroups**. Это возвращает коллекцию [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup), которая включает все объекты [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup), которым принадлежит контакт. 
    
### <a name="disconnecting-from-the-im-application"></a>Отключение от приложения для обмена мгновенными сообщениями
<a name="off15_IMIntegration_HowConnect"> </a>

Когда приложение Office 2013 обнаруживает событие **OnShuttingDown** от приложения для обмена мгновенными сообщениями, оно отключается без уведомлений. Тем не менее, если приложение Office завершает работу раньше приложения для обмена мгновенными сообщениями, нет гарантий, что сведения о подключении и в приложении Office будут очищены. Приложение для обмена мгновенными сообщениями должно устранять возможность утечки сведений подключения клиента. 
  
## <a name="setting-registry-keys-and-entries"></a>Настройка записей и разделов реестра
<a name="off15_IMIntegration_SetRegistry"> </a>

Как уже было сказано, приложения Office 2013, поддерживающие обмен мгновенными сообщениями, выполняют поиск определенных разделов, записей и значений в реестре, чтобы обнаружить клиентское приложение для обмена мгновенными сообщениями, к которому следует подключиться. Такие значения реестра указывают приложению Office имя процесса и CLSID класса, выступающего в качестве точки входа в модель объекта клиентского приложения для обмена мгновенными сообщениями (т. е. класс, который реализует интерфейс **IUCOfficeIntegration**). Приложение Office воссоздает такой класс и устанавливает подключение в качестве клиента к внепроцессному серверу COM в клиентском приложении для обмена мгновенными сообщениями. 
  
Используйте Таблицу 1 для определения разделов, записей и значений, которые должны быть записаны в реестре для интеграции клиентского приложения для обмена мгновенными сообщениями с Office.
  
**Таблица 1. Разделы реестра, позволяющие задать клиентское приложение для обмена мгновенными сообщениями по умолчанию**

|**Раздел**|**Запись**|**Тип**|**Значение**|**Пример**|
|:-----|:-----|:-----|:-----|:-----|
|HKEY_LOCAL_MACHINE\Software\IM Providers\\<Имя приложения\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |Имя стороннего клиентского приложения для обмена мгновенными сообщениями.  <br/> |Litware IM 2012  <br/> |
||ProcessName  <br/> |REG_SZ  <br/> |Имя процесса стороннего клиентского приложения для обмена мгновенными сообщениями.  <br/> |litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Идентификатор класса (CLSID) для корневого, воссоздаваемого класса в приложении для обмена мгновенными сообщениями (класс, который реализует интерфейс **IUCOfficeIntegration**).  <br/> |(A GUID)  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |Имя клиентского приложения для обмена мгновенными сообщениями. Должно быть таким же, как и имя в разделе реестра верхнего уровня (куст) в HKEY_LOCAL_MACHINE.  <br/> |Litware  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers\\<Имя приложения\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Целое число от 0 до 2:  <br/>  0 — не выполняется;  <br/>  1 — выполняется запуск;  <br/>  2 — выполняется.  <br/> <br/>**ПРИМЕЧАНИЕ**: раздел реестра имени приложения должен быть таким же, как значение записи DefaultIMApp.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Реализация обязательных интерфейсов для интеграции с Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Существует три интерфейса из пространства имен **UCCollaborationLib**, которые исполняемый файл (или сервер COM) клиентского приложения для обмена мгновенными сообщениями должен реализовать, чтобы можно было выполнить интеграцию с Office. Если такие интерфейсы реализованы не будут, приложение Office отменяет выполненные действия во время процесса инициализации, и подключение к клиентскому приложению для обмена мгновенными сообщениями не устанавливается. 
  
Обязательные интерфейсы приведены ниже.
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) — несмотря на то, что данный интерфейс не является обязательным, интерфейс **_IUCOfficeIntegrationEvents** также следует реализовать в том же производном классе. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) — несмотря на то, что данный интерфейс не является обязательным, интерфейс **_ILyncClientEvents** также следует реализовать в том же производном классе. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>Интерфейс IUCOfficeIntegration
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

Интерфейс **IUCOfficeIntegration** обеспечивает точку входа для приложения Office, чтобы выполнить подключение к клиентскому приложению для обмена мгновенными сообщениями. Интерфейс определяет три метода, которые приложение Office вызывает в рамках процесса инициализации подключения к клиентскому приложению для обмена мгновенными сообщениями. Класс, который реализует интерфейс **IUCOfficeIntegration**, должен быть воспроизводимым, так чтобы приложение Office могло воссоздать его экземпляр. Кроме того, он должен отображать CLSID, который вводится как значение для записи GUID в разделе реестра HKEY_LOCAL_MACHINE\Software\IM Providers\  _Имя приложения_. 
  
Класс, наследуемый от **IUCOfficeIntegration**, также должен реализовать интерфейс **_IUCOfficeIntegrationEvents**. Интерфейс **_IUCOfficeIntegrationEvents** содержит элементы, которые отображают обработчики событий интерфейса **IUCOfficeIntegration**. 
  
В Таблице 2 показаны элементы, которые должны быть реализованы в классе, наследуемом от **IUCOfficeIntegration** и **_IUCOfficeIntegration**.
  
> [!NOTE]
> Для получения дополнительных сведений об интерфейсах **IUCOfficeIntegration** и **_IUCOfficeIntegrationEvents** и их элементах см. [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) и [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**Таблица 2. Реализация интерфейсов IUCOfficeIntegration и _IUCOfficeIntegrationEvents**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |Метод **GetAuthenticationInfo**  <br/> |Получает строку сведений аутентификации.  <br/> |
||Метод **GetInterface**  <br/> |Получает интерфейс определенной версии.  <br/> |
||Метод **GetSupportedFeatures**  <br/> |Получает поддерживаемые функции интеграции Office.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |Событие **OnShuttingDown**  <br/> |Событие, созданное, когда клиентское приложение для обмена мгновенными сообщениями пыталось завершить работу.  <br/> |
   
Используйте следующий код для определения класса, наследуемого из интерфейсов **IUCOfficeIntegration** и **_IUCOfficeIntegration** в пределах клиентского приложения для обмена мгновенными сообщениями. 
  
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

Метод **GetAuthenticationInfo** занимает строку в качестве аргумента для параметра _version_. Когда приложение Office вызывает этот метод, он передается в одну из двух строк для аргумента, в зависимости от версии Office. Когда приложение Office указывает методу версию Office, которую поддерживает клиентское приложение для обмена мгновенными сообщениями (а именно, поддерживает функционал), метод **GetAuthenticationInfo** возвращает жестко заданную строку XML `<authenticationinfo>`. 
  
Используйте следующий код для реализации метода **GetAuthentication** в пределах кода клиентского приложения для обмена мгновенными сообщениями. 
  
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

Метод **GetInterface** передает ссылки классам на вызывающий код, в зависимости от того, что передается в качестве аргумента для параметра _interface_. Когда приложение Office вызывает метод **GetInterface**, оно передает одно из двух значений для параметра интерфейса: либо константу **oiInterfaceILyncClient** (1), либо константу **oiInterfaceIAutomation** (2) перечисления [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). Если приложение Office передает константу **oiInterfaceILyncClient**, метод **GetInterface** возвращает ссылку на класс, который реализует интерфейс **ILyncClient**. Если приложение Office передает константу **oiInterfaceIAutomation**, метод **GetInterface** возвращает класс, который реализует интерфейс **IAutomation**. 
  
Используйте следующий пример кода для реализации метода **GetInterface** в пределах кода клиентского приложения для обмена мгновенными сообщениями. 
  
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

Метод **GetSupportedFeatures** возвращает сведения о возможностях обмена мгновенными сообщениями, которые поддерживает клиентское приложение для обмена мгновенными сообщениями. Он принимает строку для своего единственного параметра _version_. Когда приложение Office вызывает метод **GetSupportFeatures**, метод возвращает значение из перечисления [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). Возвращаемое значение указывает возможности клиента для обмена мгновенными сообщениями, где каждая возможность клиентского приложения для обмена мгновенными сообщениями указывается приложению Office добавлением отметки значению. 
  
> [!NOTE]
>  Приложения Office 2013 игнорируют следующие константы в перечислении **OIFeature**: 
> - **oiFeaturePictures** (2); 
> - **oiFeatureFreeBusyIntegration**;
> - **oiFeaturePhoneNormalization**.
  
Используйте следующий пример кода для реализации метода **GetSupportFeatures** в пределах кода клиентского приложения для обмена мгновенными сообщениями. 
  
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

Интерфейс **ILyncClient** сопоставляется с возможностями самого клиентского приложения для обмена мгновенными сообщениями. Он отображает свойства, которые относятся к пользователю, выполнившему вход в приложение (локальный пользователь, представленный интерфейсом [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), состояние приложения, список контактов локального пользователя и некоторые другие настройки. Когда он выполняет попытку подключиться к клиентскому приложению для обмена мгновенными сообщениями, приложение Office получает ссылку на объект, который реализует интерфейс **ILyncClient**. По такой ссылке приложение Office может получить доступ к большинству функций клиентского приложения для обмена мгновенными сообщениями. 
  
Кроме того, класс, который реализует интерфейс **ILyncClient**, также должен реализовать интерфейс **_ILyncClientEvents**. Интерфейс **_ILyncClientEvents** отображает несколько событий, которые являются обязательными для отслеживания состояния клиентского приложения для обмена мгновенными сообщениями. 
  
В Таблице 3 показаны элементы, которые должны быть реализованы в классе, наследуемом от **ILyncClient** и **_ILyncClientEvents**.
  
> [!NOTE]
> Любой элемент интерфейса **ILyncClient** или ** \_ILyncClientEvents**, не указанный в таблице, должен быть в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E\_NOTIMPL**. 
> 
> Дополнительные сведения об интерфейсах **ILyncClient** и **_ILyncClientEvents** и их элементах см. в статье [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) и [ UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**Таблица 3. Реализация интерфейсов ILyncClient и ILyncClientEvents**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |Свойство **ContactManager**  <br/> |Получает руководителя группы контактов.  <br/> |
||Свойство **ConversationManager**  <br/> |Получает руководителя беседы.  <br/> |
||Свойство **Self**  <br/> |Получает объект **Self**.  <br/> |
||Метод **SignIn**  <br/> |Запускает процесс выполнения входа в клиентское приложение для обмена мгновенными сообщениями с определенной доступностью.  <br/> |
||Свойство **State**  <br/> |Получает текущее состояние платформы.  <br/> |
||Свойство **Uri**  <br/> |Получает URI клиентского приложения для обмена мгновенными сообщениями.  <br/> |
|**_ILyncClientEvents** <br/> |Событие **OnStateChanged**  <br/> |Создается, когда изменяется состояние клиентского приложения для обмена мгновенными сообщениями. Это событие следует обработать и получить свойство **eventData.NewState**. Событие создается для всех процессов, связанных с экземпляром клиентского приложения для обмена мгновенными сообщениями, когда любая подсистема в приложении приводит к изменению состояния.  <br/> |
   
В ходе процесса инициализации приложение Office выполняет доступ к свойству **ILyncClient.State**. Этому свойству необходимо вернуть значение из перечисления [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState). 
  
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

Свойство **State** сохраняет текущий статус клиентского приложения для обмена мгновенными сообщениями. Его необходимо задать и обновить в сеансе клиентского приложения для обмена мгновенными сообщениями. Когда клиентское приложение для обмена мгновенными сообщениями выполняет вход, выход или завершает работу, оно должно задать свойство **State**. Лучше задать это свойство в методах **ILyncClient.SignIn** и **ILyncClient.SignOut**, как показано в примере ниже. 
  
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

В примере кода ниже показано, как задать прослушиватель событий, используя интерфейсы _ **ILyncClientEvents** и _ **IUCOfficeIntegrationEvents**. 
  
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

Интерфейс **IAutomation** автоматизирует функции клиентского приложения для обмена мгновенными сообщениями. Его можно использовать, чтобы начинать беседы, присоединяться к конференциям и указывать контекст окна расширяемости. 
  
В Таблице 4 показаны элементы, которые необходимо реализовать в классе, наследуемом от **IAutomation**.
  
> [!NOTE]
> Любой элемент интерфейса **IAutomation**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**. 
> 
> Дополнительные сведения об интерфейсе **IAutomation** и его элементах см. в статье [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**Таблица 4. Реализация интерфейса IAutomation**

|**Элемент**|**Описание**|
|:-----|:-----|
|Метод **StartConversation**  <br/> |Начинает беседу, используя указанную модальность беседы. Экземпляр **IConversationWindow** возвращается.  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Реализация интеграции сведений о присутствии контакта
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

Помимо трех обязательных интерфейсов, описанные ранее, существует несколько других интерфейсов, которые важны для функционального использования сведений о присутствии в Office. К ним относятся:
  
- интерфейс [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) или **IContact2**; 
    
- интерфейс [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf); 
    
- интерфейсы [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) и [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager); 
    
- интерфейсы [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) и [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup); 
    
- интерфейс [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription); 
    
- интерфейс [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint); 
    
- интерфейс [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString). 
    
### <a name="icontact-interface"></a>Интерфейс IContact
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

Интерфейс **IContact** представляет пользователя клиентского приложения для обмена мгновенными сообщениями. Интерфейс предоставляет сведения о присутствии, доступные модальности, участие в группах и свойства типа контакта определенного пользователя. Чтобы начать беседу с другим пользователем, укажите экземпляр **IContact** такого пользователя.
  
В Таблице 5 показаны элементы, которые необходимо реализовать в классе, наследуемом от **IContact**.
  
> [!NOTE]
> Любой элемент интерфейса **IContact**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**. 
>
> Дополнительные сведения об интерфейсе **IContact** и его элементах см. в статье [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**Таблица 5. Реализация интерфейса IContact**

|**Элемент**|**Описание**|
|:-----|:-----|
|Метод **CanStart**  <br/> |Возвращает **true**, если для контакта можно запустить указанный тип модальности.  <br/> |
|Метод **GetContactInformation**  <br/> |Получает один элемент сведений о присутствии от контакта публикации.  <br/> |
|Метод **BatchGetContactInformation**  <br/> |Получает несколько элементов сведений о присутствии от контакта публикации.  <br/> |
|Свойство **Settings**  <br/> |Получает коллекцию свойств контакта.  <br/> |
|Свойство **CustomGroups**  <br/> |Получает коллекцию групп, участником которых является контакт.  <br/> |
   
Во время процесса инициализации приложение Office вызывает метод **IContact.CanStart**, чтобы определить возможности обмена мгновенными сообщениями для локального пользователя. Метод **CanStart** получает отметку от перечисления [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) в качестве аргумента для параметра __modalityTypes_. Если текущий пользователь может взаимодействовать в запрашиваемой модальности (т. е. такой пользователь может обмениваться мгновенными, голосовыми и видеосообщениями или иметь общий доступ к приложениям), метод **CanStart** возвращает значение **true**.
  
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

Метод **GetContactInformation** получает информацию о контакте из объекта **IContact**. Код вызова должен передать значение из перечисления [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) для параметра __contactInformationType_, который обозначает получаемые данные. 
  
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

Также как и **GetContactInformation**, метод **BatchGetContactInformation** получает несколько элементов сведений о присутствии контакта из объекта **IContact**. Код вызова должен передать массив значений из перечисления **ContactInformationType** для параметра __contactInformationTypes_. Метод возвращает объект [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary), который содержит запрашиваемые данные. 
  
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

Свойство **IContact.Settings** возвращает объект **IContactSettingDictionary**, который содержит настраиваемые свойства контакта. 
  
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

Свойство **IContact.CustomGroups** возвращает объект **IGroupCollection**, который включает все группы, участником которых контакт является. 
  
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

Во время процесса инициализации приложение Office получает данные для текущего пользователя, выполняя доступ к свойству **ILyncClient.Self**, которое должно возвращать объект **ISelf**. Интерфейс **ISelf** представляет локального пользователя, выполнившего вход в клиентское приложение для обмена мгновенными сообщениями. 
  
В Таблице 6 показаны элементы, которые необходимо реализовать в классе, наследуемом от **ISelf**.
  
> [!NOTE]
> Любой элемент интерфейса **ISelf**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**. 
  
**Таблица 6. Реализация интерфейса ISelf**

|**Элемент**|**Описание**|
|:-----|:-----|
|Свойство **Contact**  <br/> |Получает объект **IContact**, связанный с локальным пользователем.  <br/> |
   
Сведения о присутствии, доступные модальности, участие в группах и свойства типа контакта для локального пользователя представлены через свойство **ISelf.Contact** (которое возвращает объект **IContact**). Во время процесса инициализации приложение Office выполняет доступ к свойству **ISelf.Contact** для получения ссылки на контактные данные для локального пользователя. 
  
Используйте следующий код для определения класса, наследуемого от интерфейса **ISelf**, который реализует свойство **Contact**. 
  
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

Объект **IContactManager** управляет контактами локального пользователя, включая собственные контактные данные локального пользователя. Приложение Office использует объект **IContactManager** для доступа к объектам **IContact**, которые соответствуют контактам локального пользователя. 
  
В Таблице 7 показаны элементы, которые необходимо реализовать в классе, наследуемом от **IContactManager** и **_IContactManagerEvents**.
  
> [!NOTE]
> Любой элемент интерфейса **IContactManager**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E\_NOTIMPL**. 
>
> Дополнительные сведения об интерфейсах **IContactManager** и **_IContactManagerEvents**, а также их элементах см. в статье [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) и [ UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**Таблица 7. Реализация интерфейсов IContactManager и _IContactManagerEvents**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |Метод **GetContactByUri**  <br/> |Находит или создает новый экземпляр контакта, используя URI контакта.  <br/> |
||Метод **CreateSubscription**  <br/> |Создает объект **ISubscription**, который можно использовать для пакетной обработки подписок или запросов.  <br/> |
||Метод **Lookup**  <br/> |Ищет контакт или группу рассылки.  <br/> |
|**_IContactManagerEvents** <br/> |Событие **OnGroupAdded**  <br/> |Создается, когда группа добавляется в коллекцию групп. Обновленную коллекцию групп можно получить из свойства **IContactManager.Groups**.  <br/> |
||Событие **OnGroupRemoved**  <br/> |Создается, когда группа удаляется из коллекции групп. Обновленную коллекцию групп можно получить из свойства **IContactManager.Groups**.  <br/> |
||Событие **OnSearchProviderStateChanged**  <br/> |Создается, когда изменяется статус поставщика поиска.  <br/> |
   
Office вызывает **IContactManager.GetContactByUri**, чтобы получить сведения контакта о присутствии, используя адрес SIP контакта. Когда контакт сконфигурирован для SIP-адреса в Active Directory, Office определяет такой адрес для контакта и вызывает **GetContactByUri**, передавая SIP-адрес контакта для параметра  __contactUri_. 
  
Если приложению Office не удается определить SIP-адрес для контакта, оно вызывает метод **IContactManager.Lookup**, чтобы найти SIP, используя службу обмена мгновенными сообщениями. Здесь Office передает оптимальные данные, которые удается найти для контакта (например, только адрес электронной почты для контакта). Метод **Lookup** асинхронно возвращает объект **AsynchronousOperation**. Когда он инициирует обратный вызов, метод **Lookup** должен вернуть сведения об успешном или неудачном выполнении операции, помимо URI контакта. 
  
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

Приложению Office необходимо подписаться на изменения сведений о присутствии для отдельного контакта. Таким образом, когда изменяется состояние сведений о присутствии контакта, сервер обмена мгновенными сообщениями оповещает клиентское приложение для обмена мгновенными сообщениями, тем самым оповещая приложение Office. Для этого приложение Office вызывает метод **IContactManager.CreateSubscription**, чтобы создать новый объект **IContactSubscription** для этого запроса. 
  
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

Объект **IGroup** представляет коллекцию контактов с дополнительными свойствами для определения коллекции контактов по имени группы. Объект **IGroupCollection** представляет коллекцию объектов **IGroup**, определенную локальным пользователем и клиентским приложением для обмена мгновенными сообщениями. Приложение Office использует объекты **IGroupCollection** и **IGroup**, чтобы получить доступ к контактам локального пользователя. 
  
В Таблице 9 показаны элементы, которые должны быть реализованы в классах, наследуемых от **IGroup** и **IGroupCollection** в приведенной ниже таблице. 
  
> [!NOTE]
> Любой элемент интерфейса **IGroup**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**. 
>
> Дополнительные сведения об интерфейсах **IGroup** и **IGroupCollection**, а также их элементах см. в статье [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) и [ UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**Таблица 9. Реализация интерфейсов IGroup и IGroupCollection**

|**Интерфейс**|**Элемент**|**Описание**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |Свойство **Count**  <br/> |Возвращает количество объектов **IGroup** в коллекции  <br/> |
||Свойство **Item**  <br/> |Возвращает объект **IGroup** в указанном индексе в коллекции.  <br/> |
|**IGroup** <br/> |Свойство **Id**  <br/> |Возвращает идентификатор группы.  <br/> |
   
Когда приложение Office получает сведения для локального пользователя, оно выполняет доступ к участию в группах контакта (локальный пользователь), вызывая свойство **IContact.CustomGroups**, которое возвращает объект **IGroupCollection**. Интерфейс **IGroupCollection** должен содержать массив (или **List**) объектов **IGroup**. Класс, который является производным от **IGroupCollection**, должен отображать свойство **Count**, которое возвращает количество элементов в коллекции, и метод индексатора, **this(int)**, который возвращает объект **IGroup** из коллекции. 
  
### <a name="icontactsubscription-interface"></a>Интерфейс IContactSubscription
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

Интерфейс **IContactSubscription** позволяет вам указать контакты для получения обновлений сведений о присутствии и типы сведений о присутствии, которые инициируют уведомление. Приложения Office используют объект **IContactSubscription** для регистрации изменений состояния присутствия контакта. 
  
В Таблице 10 показаны элементы, которые необходимо реализовать в классах, наследуемых от **IContactSubscription**.
  
> [!NOTE]
> Любой элемент интерфейса **IContactSubscription**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**.
>
> Дополнительные сведения об интерфейсе **IContactSubscription** и его элементах см. в статье [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**Таблица 10. Реализация интерфейса IContactSubscription**

|**Элемент**|**Описание**|
|:-----|:-----|
|Метод **AddContact**  <br/> |Добавляет контакт в объект подписки.  <br/> |
|Метод **Subscribe**  <br/> |Помогает клиентскому приложению для обмена мгновенными сообщениями отслеживать сведения о присутствии контакта.  <br/> |
   
Интерфейс **IContactSubscription** должен содержать ссылку на все объекты **IContact**, которые он отслеживает, используя массив или **List**. Метод **IContactSubscription.AddContact** добавляет объект **IContact** к базовой структуре данных объекта **IContactSubscription**, добавляя, таким образом, новый контакт для отслеживания изменений сведений о присутствии. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

Метод **IContactSubscription.Subscribe** позволяет клиентскому приложению для обмена мгновенными сообщениями выполнять доступ к наблюдателям присутствия контакта. Он может использовать стратегию опроса для получения сведений о присутствии от сервера для контактов, на которые подписано клиентское приложение для обмена мгновенными сообщениями. Метод **Subscribe** полезен в ситуациях, когда сведения о присутствии запрашиваются для кого-либо, кто отсутствует в списке контактов пользователя (например, из большой общедоступной сети). 
  
### <a name="icontactendpoint-interface"></a>Интерфейс IContactEndPoint
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

**IContactEndPoint** представляет номер телефона из коллекции телефонных номеров контакта. 
  
В Таблице 11 показаны элементы, которые необходимо реализовать в классах, наследуемых от **IContactEndPoint**.
  
> [!NOTE]
> Любой элемент интерфейса **IContactEndPoint**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**.
>
> Дополнительные сведения об интерфейсе **IContactEndPoint** и его элементах см. в статье [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**Таблица 11. Реализация интерфейса IContactEndPoint**

|**Элемент**|**Описание**|
|:-----|:-----|
|Свойство **DisplayName**  <br/> |Получает отображаемую строку.  <br/> |
|Свойство **Type**  <br/> |Получает тип конечной точки контакта  <br/> |
|Свойство **Uri**  <br/> |Получает URI контакта.  <br/> |
   
### <a name="ilocalestring-interface"></a>Интерфейс ILocaleString
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

**ILocaleString** — это структура локализованной строки, которая содержит локализованную строку и код языка локализации. Интерфейс **ILocaleString** используется для форматирования строки настраиваемого статуса в карточке контакта. 
  
В Таблице 12 показаны элементы, которые необходимо реализовать в классах, наследуемых от **ILocaleString**.
  
> [!NOTE]
> Любой элемент интерфейса **ILocaleString**, не указанный в таблице, должен иметься в наличии, но не обязательно должен быть реализован. Элементы, которые имеются в наличии, но не были реализованы, могут привести к возникновению ошибки **NotImplementedException** или **E_NOTIMPL**.
>
> Дополнительные сведения об интерфейсе **ILocalString** и его элементах см. в статье [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**Таблица 12. Реализация интерфейса ILocaleString**

|**Элемент**|**Описание**|
|:-----|:-----|
|Свойство **LocaleId**  <br/> |Получает код языка.  <br/> |
|Свойство **Value**  <br/> |Получает строку.  <br/> |
   
## <a name="see-also"></a>См. также

- Пространство имен [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) 
    

