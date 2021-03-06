---
title: Раздел Конфигурация формы [Описание]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433096"
---
# <a name="form-configuration-file-description-section"></a>Раздел Конфигурация формы [Описание]
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
В **разделе [Описание]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы. Записи **MessageClass,** **Clsid** и **DisplayName,** которые определяют имя класса сообщений формы, его GUID и отображаемого имени класса сообщений, соответственно, требуются записи, используемые для определения формы в библиотеке форм. Остальные записи необязательны. Формат раздела **[Описание]:** 
  
В **разделе [Описание]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы. Записи **MessageClass,** **Clsid** и **DisplayName,** которые определяют имя класса сообщений формы, его GUID и отображаемого имени класса сообщений, соответственно, требуются записи, используемые для определения формы в библиотеке форм. Остальные записи необязательны. Формат раздела **[Описание]:** 
  
 **[Описание] MessageClass**  =   _строка_
  
 **Clsid**  =   _guid_
  
 **DisplayName**  =   _displayedstring_
  
 **SmallIcon**  =   _путь_
  
 **LargeIcon**  =   _путь_
  
Необязательные записи:
  
 **Категория**  =   _отображаемая строка_
  
 **Subcategory**  =   _отображаемая строка_
  
 **Комментарий**  =   _отображаемая строка_
  
 **Владелец**  =   _отображаемая строка_
  
 **Номер**  =   _отображаемая строка_
  
 **Версия**  =   _integer_
  
 **Locale**  =   _строка_
  
 **Скрытые**  =   _integer_
  
 **DesignerToolName**  =   _строка_
  
 **DesignerToolGuid**  =   _clsid_
  
 **DesignerRuntimeGuid**  =   _clsid_
  
 **ComposeInFolder**  =   _0|1_
  
 **ComposeCommand**  =   _строка_
  
Записи **Category** и **Subcategory** используются установщиками форм для настройки классификации форм по умолчанию в пользовательском интерфейсе клиентского приложения. Например, можно настроить иерархию, в которой подкатегории — "Стол поддержки", а подкатегории — "Программное обеспечение" и "Оборудование". Эта классификация может использоваться приложениями просмотра для отображения сообщений более организованным образом. Записи **Comment,** **Owner** и **Number** — это строки комментариев, которые отображаются в пользовательском интерфейсе клиентского приложения. Это конкретные свойства форм, которые можно использовать по усмотрению разработчика форм. Например, запись **Comment** можно использовать для указать цель  формы, запись Владельца, используемую для указать лицо или организацию, ответственные за сохранение формы, и номер, используемый для отслеживания различных версий формы. Для **записи Комментарий** можно включить до десяти строк комментариев. В первой строке комментариев в качестве ключа используется слово "Комментарий", во второй строке в качестве ключа используется "Comment1" и так далее через "Comment9". 
  
Записи **LargeIcon** и SmallIcon используются для указания пути для ресурсов значков, используемых для отображения значков в пользовательском интерфейсе клиентского приложения, как правило, это для строк таблицы, которые включают **столбцы свойств PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)или **PR_MINI_ICON** [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md)  Имена файлов icon можно укаменовать как имена путей относительно каталога, в котором установлен файл конфигурации формы. Запись **Версия** используется для указать номер версии формы. **Locale** — это идентификатор языка с тремя буквами в библиотеке форм назначения. Список этих идентификаторов можно найти в справке  _программиста Win32_.
  
**Скрытая** запись указывает, должна ли форма отображаться в пользовательском интерфейсе поставщика библиотеки форм: 1 указывает, что файл скрыт, а 0 указывает, что форма видна. Пример файла конфигурации формы показан ниже. 
  
Запись **ComposeInFolder** контролирует, предназначена ли форма для размещения в текущей папке или в папке "Входящие" пользователя, когда пользователь сохраняет сообщение при его записи: 1 указывает, что форма должна идти в текущей папке, а 0 указывает, что она должна быть в папке "Входящие". 
  
Запись **ComposeCommand** — это строка, которая будет помещена в меню составить приложение клиента. Если это не указано, будет использоваться запись **DisplayName.** 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


