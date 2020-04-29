---
title: Добро пожаловать в вспомогательную ссылку Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Вспомогательная справочная информация Outlook содержит общие справочные материалы по четырем наборам API, примерам кода и распространяемому установщику, которые позволяют разработчикам расширять и интегрировать приложение в Outlook. API в этой ссылке предоставляются в Outlook для расширения возможностей вне объектной модели Outlook.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328986"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Добро пожаловать в вспомогательную ссылку Outlook

Вспомогательная справочная информация Outlook содержит общие справочные материалы по четырем наборам API, примерам кода и распространяемому установщику, которые позволяют разработчикам расширять и интегрировать приложение в Outlook. API в этой ссылке предоставляются в Outlook для расширения возможностей вне объектной модели Outlook. 
  
Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям. 

Конкретные сведения об объектной модели Outlook вы найдете в [справочном справочнике по VBA для Outlook](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Конкретные сведения об интерфейсе API обмена сообщениями (MAPI), поддерживаемом в Outlook, можно найти в статье [Справка по MAPI для Outlook](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Схемы 

Концептуальное обсуждение включает в себя следующие темы:
  
- [Сведения о параметрах защиты от нежелательной почты](about-anti-spam-settings.md)
    
- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Поиск журнала скачивания сообщений для учетной записи POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Анализ журнала скачивания сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Сведения о разрешении конфликтов для элементов пользовательских типов](about-conflict-resolution-for-custom-item-types.md)
    
- [Сведения о времени последнего обновления автономной адресной книги](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Сведения о регистрации нового домена для автоматической настройки](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Сведения о приглашениях на собрания в виде информационных или полных сообщений](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [Сведения о возможностях летнего времени на летнем календаре программным способом](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (Кроме того, существует распространяемый установщик для сторонних средств базового календаря, который работает с предыдущими версиями Outlook, так как Outlook 2010. Чтобы скачать установщик, ознакомьтесь со статьей [Outlook 2010: дополнительный справочный установщик и заголовочный файл для перебазового календаря](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Справочные материалы

Справочный контент включает следующее:
  
- [Интерфейсы API, экспортируемые в Outlook](about-apis-exported-by-outlook.md) , включают функции и структуры данных, изначально реализованные для внутреннего использования, и теперь доступны для использования в общедоступном виде. 
    
- [API управления учетными записями](about-the-account-management-api.md) предоставляет доступ к сведениям об учетной записи пользователя и уведомлениям об изменениях в учетной записи. 
    
- [API уровня ухудшения данных](about-the-data-degradation-layer-api.md) поддерживает клиенты, которые обращаются к элементу Outlook в предпочтительном символьном формате, а не в собственном формате символов объекта. 
    
- [API](about-the-free-busy-api.md) сведений о доступности предоставляет сведения о доступности для конкретных учетных записей пользователей в определенном диапазоне времени. 

## <a name="sample-tasks"></a>Примеры задач

Ниже приведены примеры задач, которые можно выполнить в вспомогательной справочной программе Outlook.
    
- [Определение того, был ли элемент Outlook изменен, но не сохранен (Вспомогательная справка по Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)  
    
- [Анализ потока из двоичного свойства для считывания структуры TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Анализ потока из двоичного свойства для считывания структуры TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Считывание свойств часового пояса встречи](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Указание на необходимость отображать изображение контакта в Outlook (Дополнительная справка по Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)
    
В справочных материалах для каждого API перечислены константы, определения типов и интерфейсы, которые разработчик должен реализовать, чтобы использовать дополнительные функции.
  
> [!NOTE]
> Разработчики должны реализовать эти API только в соответствии с инструкциями, приведенными в этом справочнике. Некоторые члены и параметры методов имеют имена заполнителей, так как они зарезервированы для внутреннего использования в Outlook и могут быть изменены без предварительного уведомления. 
  

