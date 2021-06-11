---
title: Новые возможности в этом выпуске
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Последние изменения: 09 февраля 2020 г.'
ms.openlocfilehash: 3a3d38d83311b63686a2379c3321194e538ff840
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061330"
---
# <a name="whats-new-in-this-edition"></a>Новые возможности в этом выпуске

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Ссылка microsoft Outlook MAPI была обновлена, чтобы включить документацию для различных новых функций. 
  
## <a name="new-content"></a>Новое содержимое

Добавлен контент для следующих функций:
  
- В разделе Начало работы с [ссылкой Outlook MAPI за 2013](getting-started-with-the-outlook-mapi-reference.md) г. была обновлена для ссылки на всеобъемлющую информацию о моделях программирования для ваших функций Outlook и MAPI, чтобы помочь вам определить API и технологии, наиболее подходящие для ваших потребностей. Ссылки на ссылки на техническую статью также были пересмотрены в следующих статьях: 
    
  - [Справочник по MAPI для Outlook](outlook-mapi-reference.md)
    
  - [Обзор справочника по MAPI для Outlook](outlook-mapi-reference-overview.md)
    
- **Пример поставщика магазина** сообщений — код поставщика магазина [PST](message-store-provider-sample.md) в примере был пересмотрен, чтобы распознать и Outlook 2013 г. Дополнительные сведения см. в разделе Ранее пересмотренный контент в этом разделе. 
    
- **Autocomplete Stream** [](nickname-cache.md) — тема кэша nickname, ранее формат **файла Nk2,** была обновлена с учетом изменений Outlook 2013 г., а также Outlook 2010 г. В настоящее время были пересмотрены следующие разделы, чтобы предоставить сведения о руководствах по разработчику формата файлов .nk2 для Microsoft Outlook 2003/Microsoft Office Outlook 2007 г. и двоичном размыве файлов. Дополнительные сведения см. в разделе Ранее пересмотренный контент в этом разделе.
    
  - [Профили MAPI](mapi-profiles.md)
    
  - [Кэш псевдонимов](nickname-cache.md)
    
  - [Поток автокомплетов](autocomplete-stream.md)
    
- **Интерфейсы** [-IAddrBook::OpenEntry](iaddrbook-openentry.md) документировать метод открытия записи адресной книги и возврата указателя в интерфейс, используемый для доступа к нему. Ранее он содержал флаг в параметре  *ulFlags* **MAPI_GAL_ONLY**, который можно было использовать для открытия глобального адресного списка (GAL), только, и был пересмотрен, чтобы включить его определение.
    
- **Свойства**— **PR_CONVERSATION_KEY** имени свойства [(PidTagConversationKey Canonical Property)](pidtagconversationkey-canonical-property.md)была добавлена и относится к **IPM. Сообщения MessageManager** только Outlook MAPI. Были пересмотрены следующие темы, связанные с Transport-Neutral форматом инкапсуляции (TNEF): 
    
  - [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Сопоставление атрибутов TNEF с свойствами MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID и attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>Монитор инициализации MAPI  

- Иногда приложение, которое потребляет MAPI, может потребовать знать, когда инициализация будет завершена. Например, он имеет несколько потоков, которые могли бы инициализировать MAPI, или в ответ на инициализацию MAPI приложение хотело бы выполнить некоторую работу, но не хочет всегда вращать стек MAPI.  Монитор инициализации предоставляет эту функцию с помощью функции (экспортируемой из OLMAPI32.DLL) и нескольких простых интерфейсов, описанных ниже. 

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor (IMAPIInitMonitor ppInitMonitor) 

- Это точка входа, экспортируемая из OLMAPI32.DLL это позволяет звонячему получить интерфейс для запроса текущего состояния инициализации, установки вызова для завершения инициализации или блокировки текущего потока до завершения.  Объект, возвращаемый из этого API, является многоразовым и безопасным для потока и может вызываться из любого потока, а не только из потока, который его извлек.  Кроме того, в отличие от других объектов, открытых в MAPI, этот объект действителен до тех пор, пока DLL загружен, его можно повторно использовать в сеансах инициализации и можно потреблять до или после того, как была вызвана MAPIInitialize. Возвращает успех или сбой с помощью стандартного HRESULT com и назначает параметр out экземпляру IMAPIInitMonitor. 

### <a name="interface-imapiinitmonitor"></a>Интерфейс: IMAPIInitMonitor 

**IFACEMETHODIMP_ (BOOL) IsInitialized()**
- Возвращает текущее состояние инициализации MAPI 

**IFACEMETHODIMP Wait(DWORD timeout)**
- Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI.  INFINITE можно использовать для бесконечного ожидания. 

**IFACEMETHODIMP BeginWait(DWORD timeout, IMAPIWaitResult ppResult)**
- Начните ожидание инициализации MAPI или указанного числа миллисекунд, которые должны сойти.   Это возвращает интерфейс IMAPIWaitResult, который должен иметь "End" для того, чтобы начать ожидание.  Это позволяет звонячему управлять тем, какой поток заблокирован во время ожидания. 

### <a name="interface-imapiwaitresult"></a>Интерфейс IMAPIWaitResult
**Переопределения IFACEMETHODIMP End()**
- Чтобы инициировать ожидание блокировки в потоке, где он называется, не требуется быть тем же потоком, который называется "BeginWait". 

    
## <a name="previously-revised-content"></a>Ранее пересмотренный контент

Содержимое было добавлено в предыдущих выпусках Outlook MAPI Reference для следующих функций:
  
- Microsoft Outlook 2013 для нестандартных сценариев развертывания, таких как бок о бок и Click-to-Run. Эти сценарии могут осложнить логику, используемую для загрузки соответствующей библиотеки MAPI. Теперь у разработчиков MAPI есть возможность прямой привязки к функциям MAPI, и они могут напрямую связаться с загоном MAPI клиента MAPI по умолчанию (например, Msmapi32.dll Outlook), не проехав библиотеку MAPI и Windows MAPI. Дополнительные сведения о явных связях по сравнению с неявными ссылками см. в ссылке [на MAPI Functions.](how-to-link-to-mapi-functions.md) Библиотека **stub MAPI,** размещенная на веб-сайте [CodePlex,](https://mapistublibrary.codeplex.com/) предоставляет замену для Mapi32.lib, которая поддерживает создание как 32-битных, так и 64-битных приложений MAPI. 
    
- **Поддержка 64-битных** microsoft Outlook — справочные темы для применимых элементов API были обновлены в соответствии с новыми файлами заголовки, поддерживаюющими 64-Outlook. Эти файлы заголовки доступны для скачивания в [Outlook 2010: MAPI Header Files](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). В "Проверить версию [Outlook"](how-to-check-the-version-of-outlook.md) был представлен новый пример кода, чтобы проверить, является ли установленная версия Outlook 64-Microsoft Outlook 2010, русская версия 64-Outlook 2013 года. Если существующее 32-битное приложение MAPI будет работать на 64-битной операционной системе с 64-битным Outlook, вам потребуется восстановить 32-битное приложение в качестве 64-битного приложения. Дополнительные сведения о поддержке MAPI для 64-битных Outlook см. в приложении mapi building [on 32-Bit и 64-Bit Platforms.](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)
    
- **Пример поставщика магазина сообщений**— поставщик пакетных [пакетов PST Store](message-store-provider-sample.md) ранее был обновлен для поддержки 64-битной архитектуры. В примере инициализация темы поставщика магазинов [PST](initializing-a-wrapped-pst-store-provider.md) теперь расширена, чтобы предоставить сведения о "Завернутые пути PST и Unicode". 
    
- **Autocomplete Stream** [](nickname-cache.md) — тема кэша nickname, ранее формат **файла Nk2,** была обновлена с учетом изменений Outlook 2013 г., а также Outlook 2010 г. Такие сведения, как список автокомплектов, который является списком имен, отображаемого в полях Редактирование **To**, **Cc** и [](autocomplete-stream.md) **Bcc** при составлении электронной почты, теперь сохраняются в потоке автокомплетов сообщения на локальном компьютере, а не сохраняются в файле, как в Outlook 2007 г. 
    
  - Взаимодействие с потоком автозаполнения
    
  - Загрузка потока автозаполнения
    
  - Сохранение потока автокомплетов
    
- Поддержка быстрого отключения для клиентов MAPI — теперь клиенты **MAPI** могут инициировать быстрое отключение, а подсистема MAPI уведомляет загруженных поставщиков, чтобы свести к минимуму потерю данных от быстрого отключения. Для поддержки быстрого отключения для клиента и поставщика были добавлены дополнительные интерфейсы. Дополнительные сведения о быстром закрытии см. в дополнительных сведениях о закрытии клиента [в MAPI.](client-shutdown-in-mapi.md)
    
- **Добавлена** структура потока для определений полей для элемента Outlook -Документация для двоичного потока для свойства [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) Это свойство указывает определения всех настраиваемого поля и параметров привязки данных для встроенных полей Outlook элемента. 
    
- **Переопределение** личного магазина — для поддержки переопределения политики поставщиков личных папок (PST) для поставщиков **магазинов PSTDisableGrow** были добавлены следующие интерфейсы и соответствующие методы: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **С помощью Exchange учетных записей** добавлена документация по [API адресной книги MAPI.](using-multiple-exchange-accounts.md) Этот API был расширен для поддержки нескольких Exchange учетных записей в Microsoft Outlook 2010, русская версия и теперь включает Microsoft Outlook 2013. ����� ��������� ������ ��������� � ����������� �������� �������� Exchange, ����������� ����� �������, ����������� �������� ������� ������, ����� ������ � �������� ����� ����� ���������� ������� ������ Exchange. 
    
- Сведения о конфигурации mapi File **Formats**—MAPI были расширены, чтобы объяснить, как можно использовать пути для регистрации служб и поставщиков услуг в [MapiSvc.inf.](registering-services-and-service-providers-in-mapisvc-inf.md)
    
- **Свойства**— в дополнение к документации по 38 другим помеченным свойствам и названным свойствам, которые были добавлены ранее, добавлены следующие свойства с тегами:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Константы MAPI**— расширены консолидированные [константы MAPI.](mapi-constants.md) В предыдущих выпусках они распространялись по ряду тем, но теперь собираются в одной теме, чтобы упростить их обнаружение и использование. Кроме того, они были расширены, чтобы обеспечить более широкий охват, включая следующие разделы: 
    
  - Определения кодов ошибок Exchange адресной книги и магазина сообщений
    
  - Определения квот Exchange Server кэширования режима почтовых ящиков
    
## <a name="see-also"></a>См. также



[Начало работы со справочником по MAPI для Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

