---
title: Использование нескольких учетных записей Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329655"
---
# <a name="using-multiple-exchange-accounts"></a>Использование нескольких учетных записей Exchange

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживают интеграцию с несколькими учетными записями электронной почты Exchange. В Outlook 2010 и Outlook 2013 пользователь может добавить две учетные записи Exchange в один профиль, по-прежнему используя широкие возможности Exchange, такие как опубликованный глобальный список адресов (GAL), конфигурация отсутствия на рабочем месте в Exchange и общий доступ к папкам.
  
Те, кто знаком с разделами профиля MAPI для Microsoft Office Outlook 2007 и более ранних версий, знают, что параметры Exchange, такие как имя пользователя электронной почты и имя сервера, хранятся в фиксированном разделе глобального профиля Exchange — **pbGlobalProfileSectionGuid**. В Outlook 2010 и Outlook 2013 каждой учетной записи Exchange требуется собственный раздел профиля для хранения параметров, что избавляет от необходимости в **pbGlobalProfileSectionGuid**. 
  
Параметры Exchange в Outlook 2010 и Outlook 2013 по-прежнему хранятся в профиле, но уникальный идентификатор раздела профиля, содержащего эти параметры, динамически выделяется для каждого профиля. Расположение параметров Exchange в профиле указывается в свойстве [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), которое можно найти в разделе профиля службы сообщений для учетной записи Exchange. Это свойство также можно найти в разделе профиля для каждого поставщика в этой службе сообщений для учетной записи. Уникальный идентификатор не хранится на сервере и отличается от профиля к профилю.
  
Outlook 2010 и Outlook 2013 используют **PidTagExchangeProfileSectionId** в качестве уникального идентификатора для указания учетной записи Exchange. При таком использовании этот уникальный идентификатор называется **emsmdbUID**. Для некоторых операций MAPI и Outlook идентификатор **emsmdbUID** может быть необходим, чтобы указать учетную запись Exchange, которую следует использовать для выполнения операции. 
  
Для поддержки нескольких учетных записей Exchange необходимо использовать вызовы новых функций в коде. Замените любой вызов с использованием идентификатора **entryID** и метода [IAddrBook::OpenEntry](iaddrbook-openentry.md) или [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) в объектах [IMailUser : IMAPIProp](imailuserimapiprop.md) и [IDistList : IMAPIContainer](idistlistimapicontainer.md) одной из перечисленных ниже функций. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>Поддержка старых версий

Все клиенты MAPI, написанные до создания нового раздела **emsmdbUID**, по-прежнему поддерживаются. Эти клиенты продолжат получать старый глобальный раздел **pbGlobalProfileSectionGuid**. Запросы для этого раздела профиля будут перенаправляться в одну выделенную учетную запись Exchange, обрабатывающую старые запросы. Учетную запись, которая обрабатывает старые вызовы, можно определить, сверившись с таблицей служб сообщений и добавив столбец для PR_EMSMDB_LEGACY. Только в одной службе сообщений для этого свойства будет задано значение true, а его свойству **PidTagExchangeProfileSectionId** присваивается значение старого идентификатора **emsmdbUID**.
  
> [!NOTE]
> Настраиваемые параметры MAPI, такие как используемые по умолчанию хранилище и учетная запись, не влияют на то, какая учетная запись обрабатывает старые вызовы. Учетную запись, обрабатывающую старые вызовы, невозможно настроить. 
  
Свойство **emsmdbUID** старой учетной записи копируется в раздел глобального профиля Outlook. Если это свойство не существует, то с помощью таблицы служб сообщений можно определить, какая учетная запись обрабатывает старые запросы, и задать соответствующее значение в разделе глобального профиля Outlook. 
  
Для ясности, раздел глобального профиля Outlook отличается от аналогичного раздела в Exchange, а в Outlook 2010 и Outlook 2013 раздел глобального профиля Exchange больше не будет по-настоящему глобальным, так как у вас может быть несколько учетных записей Exchange. Раздел глобального профиля Outlook содержит свойства для Outlook, такие как состояние MRU папки или состояние глобального подключения.
  
## <a name="address-book-account-contexts"></a>Контексты учетных записей адресной книги

Чтобы правильно разрешать адреса с несколькими учетными записями Exchange, используйте новые функции, принимающие контекст учетной записи, чтобы при вызове адресной книги выполнялся поиск в правильной учетной записи Exchange.
  
Некоторые API адресной книги из предыдущих версий объявлены нерекомендуемыми, так как они не полностью поддерживали использование нескольких учетных записей Exchange. Как правило, этот контекст учетной записи представляется с помощью **emsmdbUID**.
  
Помимо **emsmdbUID**, у нескольких учетных записей Exchange также есть **emsabpUID**.
  
1. Значение **emsmdbUID** определяет контекст учетной записи. 
    
2. Значение **emsabpUID** определяет поставщика адресной книги Exchange. 
    
Значение **emsabpUID** обычно используется при разрешении получателя. При разрешении получателя с помощью [IAddrBook::ResolveName](iaddrbook-resolvename.md) строка получателя Exchange содержит свойство **PR_AB_PROVIDERS** (0x3D010102), которое включает значение **emsabpUID**. Это значение **emsabpUID** определяет поставщика адресной книги Exchange для конкретного получателя. 
  
Если вам нужно определить значение **emsabpUID** для идентификатора **emsmdbUID**, откройте раздел профиля для **emsmdbUID** и получите свойство **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
Если вы вызываете метод [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), убедитесь, что получатели Exchange в передаваемом списке содержат свойство **PR_AB_PROVIDERS** с идентификатором **emsabpUID**, соответствующим поставщику адресной книги, к которому относится получатель. Вызов метода [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) для строки, полученной из метода [IAddrBook::ResolveName](iaddrbook-resolvename.md), не требует дополнительных действий, но некоторые фрагменты кода будет вызывать метод [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) для строк, содержащих только свойство **PR_ENTRYID**. В этой и других подобных ситуациях строки должны содержать свойства **PR_ENTRYID** и **PR_AB_PROVIDERS** со свойством **PR_AB_PROVIDERS**, где задан правильный идентификатор **emsabpUID**.
  
Ниже представлено простое описание процесса разрешения нескольких учетных записей Exchange.
  
- Получив уникальный идентификатор службы, код ищет таблицу хранилища сообщений, соответствующую свойству **PR_SERVICE_UID**, совпадающему с вашим. После этого вы можете определить правильное свойство **PR_MDB_PROVIDER**. В этой строке указывается соответствующее хранилище.
    
- Получив **emsmdbUID**, код ищет в таблице служб сообщений строку, предоставляющую идентификатор **PidTagExchangeProfileSectionId**, который совпадает с **emsmdbUID**.
    
## <a name="see-also"></a>Дополнительные ресурсы



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[Каноническое свойство PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md)


[Как открыть раздел глобального профиля](https://support.microsoft.com/kb/188482)

