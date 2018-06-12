---
title: Знакомство с Дополнительные справочные материалы по Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Дополнительные справочные материалы Outlook содержит концептуальное содержимое и справочные материалы по четыре наборов API, примеров кода и распространяемого установщика, который позволяет разработчикам для расширения и интеграции с Outlook. API-интерфейсы в этой справке, предоставляемые программой Outlook для расширения за пределами объектной модели Outlook.
ms.openlocfilehash: 5f289a1be8fe5d10ddac37394c940f2627415136
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807968"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Знакомство с Дополнительные справочные материалы по Outlook

Дополнительные справочные материалы Outlook содержит концептуальное содержимое и справочные материалы по четыре наборов API, примеров кода и распространяемого установщика, который позволяет разработчикам для расширения и интеграции с Outlook. API-интерфейсы в этой справке, предоставляемые программой Outlook для расширения за пределами объектной модели Outlook. 
  
Если вы не знакомы с разработкой решения для Outlook, статью [Выбор API или технологий для разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) для идентификации интерфейсы API и технологии, наиболее подходящие вашим потребностям. 

Подробные сведения об объектной модели Outlook содержатся в разделе [Справочник по VBA для Outlook](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

[Справочник по интерфейсу MAPI приложения Outlook](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)детальную информацию о системы обмена сообщениями API (MAPI) поддерживаются в Outlook, см.

## <a name="conceptual"></a>Концептуальная 

Общие обсуждения включает в себя следующие темы:
  
- [About anti-spam settings](about-anti-spam-settings.md)
    
- [Загружаемые файлы для управления сообщения для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Поиск журнала загрузки сообщений для учетной записи POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Синтаксический анализ журнала загрузки сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [О разрешения конфликтов для типов пользовательских элементов](about-conflict-resolution-for-custom-item-types.md)
    
- [О времени последнего обновления автономной адресной книги](about-the-last-update-time-of-an-offline-address-book.md)
    
- [О регистрации нового домена для автоматической настройки](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [О приглашений на собрания как информационные и полного обновления](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [О сдвига календарей программными средствами на летнее время](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (Имеется также распространяемого установщика средства сдвига календаря сторонних производителей, который работает с предыдущими версиями Outlook, начиная с Outlook 2010. Загрузить установщик [Outlook 2010: дополнительный распространяемого установщика ссылки и файл заголовка для повторного размещения en календарей](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [About persisting TZDEFINITION to a stream to commit to a binary property](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Справочные материалы

Содержимое справки включает в себя следующее:
  
- [API -интерфейсы экспортировать с Outlook](about-apis-exported-by-outlook.md) относятся функции и структуры данных, которые изначально были реализованы для внутреннего использования и теперь доступно для общедоступных использования. 
    
- [API управления учетными данными](about-the-account-management-api.md) предоставляет доступ к учетной записи пользователя и уведомления об изменениях учетной записи. 
    
- [API Layer уменьшение объема данных](about-the-data-degradation-layer-api.md) поддерживает клиенты, которые доступ к элементу Outlook, в предпочтительном символьном формате вместо формата внутреннего объекта. 
    
- [Свободен/Занят API](about-the-free-busy-api.md) предоставляет состояния занятости сведения о отдельным учетным записям пользователей в конкретный временной диапазон. 

## <a name="sample-tasks"></a>Примеры задач

Следующие примеры инструкциями задач в дополнительные справочные материалы по Outlook.
    
- [Определить, является ли элемент Outlook был изменен, но не сохраняются (Outlook дополнительные справочные материалы по)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Синтаксический анализ потока из двоичного свойства для чтения TZDEFINITION структуры](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Синтаксический анализ потока из двоичного свойства для чтения TZREG структуры](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Чтение свойств часового пояса из встречи](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Укажите, нужно ли отображать фотографии контакта в Outlook (Outlook дополнительные справочные материалы по)](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
    
- [Использование относительных времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)
    
Справочник по каждой API перечислены константы, определения типов и интерфейсы, которые разработчик должен реализовывать использовать дополнительные функциональные возможности.
  
> [!NOTE]
> Разработчикам необходимо реализовать эти интерфейсы API, только в том случае, как описано в этой справке. Некоторые элементы интерфейса и параметры метода присваиваются имена заполнителей так, как они зарезервированы для внутреннего использования Outlook и могут быть изменены без предварительного уведомления. 
  

