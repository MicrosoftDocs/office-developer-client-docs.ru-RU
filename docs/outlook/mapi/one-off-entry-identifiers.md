---
title: Одноразовые идентификаторы записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411045"
---
# <a name="one-off-entry-identifiers"></a>Одноразовые идентификаторы записей
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Идентификаторы разовой записи создаются MAPI в методе **IAddrBook::CreateOneOff** и компонентами, которые не имеют доступа к подсистеме MAPI, например к компонентам шлюза. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). На следующей иллюстрации показан формат идентификатора одноавтной записи.
  
**Формат идентификатора единичных записей**
  
![Формат идентификатора одноавтной]записи(media/amapi_69.gif "формат идентификатора одноавтной записи")
  
Первое поле — это специальная [структура MAPIUID,](mapiuid.md) которая определяет идентификатор записи как представляющий настраиваемый получатель. Эта **структура MAPIUID** должна быть заданной для MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID определяется в файле header MAPIDEFS.H. 
  
Поля версии и флагов — это 16-битные слова в порядке byte Intel. Поле версии должно быть настроено на ноль. Поле флагов можно установить в следующих значениях:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
Флаг MAPI_ONE_OFF_NO_RICH_INFO, если получатель не должен получать содержимое сообщения в формате транспортной нейтральной инкапсуляции (TNEF). Этот флаг устанавливается, MAPI_SEND_NO_RICH_INFO передается [методу IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md) 
  
Флаг MAPI_ONE_OFF_UNICODE, если отображаемая фамилия и адрес электронной почты являются строками Юникод. Этот флаг устанавливается, когда MAPI_UNICODE передается **в IAddrBook::CreateOneOff**. Если флаг MAPI_UNICODE не передается **в CreateOneOff, MAPI** предполагает, что имя отображения и строки адресов электронной почты находятся в текущем наборе символов ANSI рабочей станции. Строки ANSI обычно не работают хорошо в сообщениях, которые отправляются между платформами с использованием различных наборов символов, так как страница кода не закодирована в идентификаторе записи. Чтобы защититься от этой потенциальной несовместимости, многие типы адресов ограничены только теми символами, которые являются общими для нескольких наборов символов. Однако для обеспечения совместимости набора символов и платформы клиенты должны использовать Юникод для строк символов в своих сообщениях.
  
Имя отображения — это строка с null-terminated,  соответствующая свойству [PR_DISPLAY_NAME (PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и _параметру lpszName,_ переданным **в IAddrBook::CreateOneOff.** Набор символов — Unicode, если MAPI_ONE_OFF_UNICODE флаг и ANSI, если он понятен. 
  
Тип адреса — это строка с null-terminated,  соответствующая свойству [PR_ADDRTYPE (PidTagAddressType)](pidtagaddresstype-canonical-property.md)и _параметру lpszAdrType,_ переданным **в IAddrBook::CreateOneOff**. 
  
Адрес электронной почты — это строка с null-terminated, соответствующая свойству [PR_EMAIL_ADDRESS (PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)и _параметру lpszAddress,_ переданным **в IAddrBook::CreateOneOff**.  
  
> [!NOTE]
> В одноавтных идентификаторах входных идентификаторов не существует заполнения; bytes packed exactly as indicated above and the entry identifier identifier length should not include any bytes beyond the terminating null character of the email address. 
  
Клиентам и поставщикам адресных книг, которые вручную создают идентификаторы одноразовой **записи,** также может потребоваться создать значения для свойств [PR_RECORD_KEY (PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и **PR_SEARCH_KEY** [(PidTagSearchKey).](pidtagsearchkey-canonical-property.md) Ключ записи идентичен идентификатору записи. Клавиша поиска должна быть сформирована путем укоренения следующих полей в следующем порядке:
  
1. Тип адреса, преобразованный в символы верхнего шкафа.
    
2. Двоеточие (:).
    
3. Адрес электронной почты, преобразованный в символы верхнего шкафа.
    
4. Завершающий null символ.
    
Преобразование набора символов при создании ключа поиска не должно производиться.
  

