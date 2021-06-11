---
title: Добро пожаловать в Outlook вспомогательную ссылку
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Вспомогательный справочник Outlook содержит концептуальное содержимое и справочную документацию для четырех наборов API, образцов кода и перераспределяемого установщика, который позволяет разработчикам расширять и интегрироваться с Outlook. API в этой ссылке Outlook для раздвивемости, за пределами Outlook объектной модели.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328986"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Добро пожаловать в Outlook вспомогательную ссылку

Вспомогательный справочник Outlook содержит концептуальное содержимое и справочную документацию для четырех наборов API, образцов кода и перераспределяемого установщика, который позволяет разработчикам расширять и интегрироваться с Outlook. API в этой ссылке Outlook для раздвивемости, за пределами Outlook объектной модели. 
  
Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям. 

Сведения о объектной модели Outlook см. в Outlook [VBA.](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) 

Сведения об API обмена сообщениями (MAPI), поддерживаемые Outlook, см. в Outlook [MAPI Reference.](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)

## <a name="conceptual"></a>Концептуальные 

Концептуальное обсуждение включает в себя следующие темы:
  
- [Сведения о параметрах защиты от нежелательной почты](about-anti-spam-settings.md)
    
- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Поиск журнала скачивания сообщений для учетной записи POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Анализ журнала скачивания сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Сведения о разрешении конфликтов для элементов пользовательских типов](about-conflict-resolution-for-custom-item-types.md)
    
- [О последнем времени обновления автономной адресной книги](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Сведения о регистрации нового домена для автоматической настройки](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Сведения о приглашениях на собрания в виде информационных или полных сообщений](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- О программном переопределении календарей для летнего времени [(существует](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) также перераспределяемый установщик для сторонних средств переопределяния календаря, который также работает для предыдущих версий Outlook, начиная с Outlook 2010 г. Чтобы скачать установщик, [см. Outlook 2010:](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)вспомогательный перераспределяемый установщик ссылок и файл загона для календарей повторного сбоя.)
    
- [Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Справочные материалы

Справочный контент включает в себя следующее:
  
- [API,](about-apis-exported-by-outlook.md) экспортируемая Outlook, включают функции и структуры данных, которые изначально были реализованы для внутреннего использования и теперь выставлены для общего использования. 
    
- API [управления учетной](about-the-account-management-api.md) записью предоставляет доступ к сведениям о учетных записях пользователей и уведомлениям об изменениях учетной записи. 
    
- API [уровня деградации](about-the-data-degradation-layer-api.md) данных поддерживает клиентов, которые Outlook элемент в предпочтительном формате символов, а не в формате родного символа объекта. 
    
- API [free/Busy предоставляет](about-the-free-busy-api.md) сведения о состоянии отдельных учетных записей пользователей в определенном диапазоне времени. 

## <a name="sample-tasks"></a>Примеры задач

Пример того, как выполнять задачи в Outlook вспомогательной ссылке, включает в себя следующее:
    
- [Определение того, был ли элемент Outlook изменен, но не сохранен (Вспомогательная справка по Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)  
    
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Анализ потока из двоичного свойства для считывания структуры TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Указание на необходимость отображать изображение контакта в Outlook (Дополнительная справка по Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)
    
В ссылке для каждого API перечислены константы, определения типов и интерфейсы, которые разработчик должен реализовать для использования дополнительных функций.
  
> [!NOTE]
> Разработчики должны реализовать эти API только в том случае, если они описаны в этой ссылке. Некоторые участники интерфейса и параметры метода называются в качестве держателей, так как они зарезервированы для внутреннего Outlook и могут изменяться без уведомления. 
  

