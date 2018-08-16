---
title: Реализация разрешения имен
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4d55404149baca07a64b75d460bdfb2a8c541725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809313"
---
# <a name="implementing-name-resolution"></a>Реализация разрешения имен

  
  
**Относится к**: Outlook 
  
Отвечает за поддержку разрешения имен поставщиками адресной книги — процесс привязки идентификатор записи с отображаемым именем. Клиенты инициировать разрешение имен, когда он совершает вызов [IAddrBook::ResolveName](iaddrbook-resolvename.md) для того, чтобы каждый элемент списка получателей исходящих сообщений допустимый адрес. 
  
Ваш поставщик поддерживает разрешение имен с:
  
- Поддержка ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) является обязательным для всех контейнеров адресной книги.
    
- Реализация метода [IABContainer::ResolveNames](iabcontainer-resolvenames.md) параметр для всех контейнеров адресной книги. 
    
Если выбран для поддержки **IABContainer::ResolveNames**пытается найти точное совпадение в каждом нерешенные отображаемое имя структуры [ADRLIST](adrlist.md) , переданное с помощью параметра _lpAdrList_ . Можно identifiy нерешенные отображаемое имя, так как он отсутствует свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) в массиве значение свойства в его член **aEntries** структуры **ADRLIST** . Игнорируйте все записи, которые имеют ноль свойства, связанные с ними. 
  
Сообщить о результатах попытку с разрешением в параметре _lpFlagList_ массив флаги, соответствующий массива отображаемые имена в _lpAdrList_. Флаги позиционные таким образом, что соответствует первой флаг первый элемент **aEntries** в структуре **ADRLIST** , второй флаг, соответствует второй элемент **aEntries** и т. д. 
  
Существует три возможных результатов для каждой нерешенные записи.
  
- Не найден, что означает, что ни одна из записей в записях контейнер соответствует значению, указанному в структуре **ADRLIST** . Задайте соответствующие записи в параметре _lpFlagList_ MAPI_UNRESOLVED. 
    
- Несколько совпадений можно найти, что означает, что существует несколько записей контейнер, соответствующие записи в структуре **ADRLIST** . Задайте соответствующие записи в параметре _lpFlagList_ MAPI_AMBIGUOUS. Не изменяйте число записей в структуре **ADRLIST** . 
    
- Можно найти точное совпадение, что означает, что существует только один контейнер запись, которая соответствует записи в структуре **ADRLIST** . Укажите соответствующий элемент в параметре _lpFlagList_ MAPI_RESOLVED и добавьте идентификатор записи массива свойства, связанные с записью **ADRLIST** . 
    
Если вы решаете не поддерживает **IABContainer::ResolveNames**, возвращает MAPI_E_NO_SUPPORT от внедрения.
  
Все поставщиками адресных книг требуются для поддержки разрешения неоднозначных псевдонимов — ограничение свойства **PR_ANR** — на их контейнеров содержимое таблицы. Для поддержки, обработка ограничение PR_ANR в реализации [IMAPITable::Restrict](imapitable-restrict.md) , выполнив «лучше всего подбора» тип поиска, сравнение с одного или нескольких свойств конкретного, подходящие для поставщика. Вы можете использовать тот же свойства или свойства каждый раз, такие как **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) или **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), или разрешить администраторы могут выбирать из списка допустимых свойств. 
  
Хотя большинство поставщиков предоставить собственные реализации таблицы содержимого, можно настроить параметры реализации, предоставляемые MAPI через функции [CreateTable](createtable.md) . Тем не менее так как реализация MAPI не поддерживает ограничения любого типа, необходимо создать объект программы-оболочки для включения настроенную версию **Restrict** перехватывает вызов. 
  
