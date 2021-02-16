---
title: Новые возможности этого выпуска
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329549"
---
# <a name="whats-new-in-this-edition"></a>Новые возможности этого выпуска

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Справочник по MAPI для Microsoft Outlook 2013 был обновлен и включает документацию по различным новым функциям. 
  
## <a name="new-content"></a>Новое содержимое

Добавлен контент для следующих функций:
  
- The topic [Getting Started with the Outlook 2013 MAPI Reference](getting-started-with-the-outlook-mapi-reference.md) has been updated to reference comprehensive information about programming models for your Outlook and MAPI functionality to help you identify the APIs and technologies that are most appropriate for your needs. Ссылки на эту техническую статью также были изменены в следующих статьях: 
    
  - [Справочник по MAPI для Outlook](outlook-mapi-reference.md)
    
  - [Обзор справочника по MAPI для Outlook](outlook-mapi-reference-overview.md)
    
- **Пример поставщика для** магазина сообщений — пример кода поставщика упакованного [PST-магазина](message-store-provider-sample.md) теперь изменен для распознавания и размещения Outlook 2013. Дополнительные сведения см. в разделе "Ранее измененное содержимое" этой темы. 
    
- **Autocomplete Stream** [](nickname-cache.md) — раздел "Кэш псевдонимов" (прежнее название — формат файлов **Nk2)** был обновлен с учетом изменений в Outlook 2013 и Outlook 2010. Следующие разделы были изменены для предоставления сведений о руководствах разработчика по форматам файлов NK2 для Microsoft Outlook 2003/Microsoft Office Outlook 2007 и двоичном разбиение файлов. Дополнительные сведения см. в разделе "Ранее измененное содержимое" этой темы.
    
  - [Профили MAPI](mapi-profiles.md)
    
  - [Кэш псевдонимов](nickname-cache.md)
    
  - [Autocomplete Stream](autocomplete-stream.md)
    
- **Interfaces**-The [IAddrBook::OpenEntry](iaddrbook-openentry.md) topic documents a method of opening an address book entry and returning a pointer to the interface used to access it. Ранее он содержал флаг в параметре  *ulFlags* **MAPI_GAL_ONLY**, который можно было использовать только для открытия глобального списка адресов (GAL), и был изменен, чтобы включить его определение.
    
- **Свойства —** тема **PR_CONVERSATION_KEY** с именем [(каноническое свойство PidTagConversationKey)](pidtagconversationkey-canonical-property.md)добавлена и связана с **IPM. Сообщения MessageManager** только в Outlook MAPI. Изменены следующие разделы, связанные с ней, и документация по потоку Transport-Neutral формата инкапсуляции (TNEF): 
    
  - [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Сопоставление атрибутов TNEF со свойствами MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID и attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Ранее измененное содержимое

Содержимое было добавлено в предыдущих выпусках справочника по MAPI для Outlook для следующих функций:
  
- Microsoft Outlook 2013 позволяет использовать нестандартные сценарии развертывания, такие как "нажми и запускай". Эти сценарии могут усложнить логику, используемую для загрузки соответствующей библиотеки MAPI. Разработчики MAPI теперь могут явным образом связать функции MAPI и могут явно связать загон MAPI клиента MAPI по умолчанию (например, Msmapi32.dll Outlook), не перебирая библиотеку MAPI и загон Windows MAPI. Дополнительные сведения об явных связях по сравнению с неявными ссылками см. в ссылке [на функции MAPI.](how-to-link-to-mapi-functions.md) Библиотека **заглифов MAPI,** размещенная на веб-сайте [CodePlex,](https://mapistublibrary.codeplex.com/) предоставляет замену для Mapi32.lib, которая поддерживает создание 32- и 64-битных приложений MAPI. 
    
- **Поддержка 64-битной версии Microsoft Outlook**— справочные разделы для применимых элементов API были обновлены в соответствии с новыми файлами заголовок, которые поддерживают 64-битную версию Outlook. Эти файлы заголовок доступны для скачивания в [Outlook 2010: файлы заголовок MAPI.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1) Новый пример кода был представлен в версии [Outlook,](how-to-check-the-version-of-outlook.md) чтобы показать, является ли установленная версия Outlook 64-Microsoft Outlook 2010, русская версия и была изменена для Outlook 2013. Если существующее 32-битное приложение MAPI будет работать в 64-битной операционной системе с установленным 64-битным приложением Outlook, вам потребуется перестроить 32-битное приложение в качестве 64-битного приложения. Дополнительные сведения о поддержке MAPI для 64-битной платформы Outlook см. в подстройке приложений MAPI на [32- и 64-битных платформах.](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)
    
- **Пример поставщика магазина** сообщений — образец поставщика упакованного [PST-магазина](message-store-provider-sample.md) ранее был обновлен для поддержки 64-битной архитектуры. Раздел "Инициализация поставщика упакованного [PST-магазина"](initializing-a-wrapped-pst-store-provider.md) в примере теперь расширен для предоставления сведений о пути к оболочке PST и Юникод. 
    
- **Autocomplete Stream** [](nickname-cache.md) — раздел "Кэш псевдонимов" (прежнее название — формат файлов **Nk2)** был обновлен с учетом изменений в Outlook 2013 и Outlook 2010. Такие сведения, как список автозаполнений, который является списком имен, отображаемого в полях "Кому", "Ск" и "Ск" при составлении пользователем сообщения электронной почты, теперь сохраняются в потоке автозаполнений сообщения на локальном компьютере, а не сохраняются в файле, как в Outlook 2007.    [](autocomplete-stream.md) 
    
  - Взаимодействие с потоком автозаполнения
    
  - Загрузка потока автозаполнения
    
  - Сохранение потока автозаполнеия
    
- Поддержка быстрого завершения работы для клиентов MAPI — теперь клиенты **MAPI** могут инициировать быстрое завершение работы, а подсистема MAPI уведомляет загруженных поставщиков, чтобы свести к минимуму потерю данных после быстрого завершения работы. Для поддержки быстрого завершения работы были добавлены дополнительные интерфейсы для клиента и поставщика. Дополнительные сведения о быстром отключении см. в [этой теме.](client-shutdown-in-mapi.md)
    
- **Структура потока для определений** полей для элемента Outlook добавлена документация для двоичного потока для свойства [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) Это свойство определяет определения всех настраиваемые поля и параметры привязки данных для встроенных полей элемента Outlook. 
    
- **Переопределение** личного магазина : для поддержки переопределения политики **PST-файлов** PST-файлов были добавлены следующие интерфейсы и соответствующие методы: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Использование нескольких учетных записей Exchange**— добавлена документация для [API адресной книги MAPI.](using-multiple-exchange-accounts.md) Этот API был улучшен для поддержки нескольких учетных записей Exchange в Microsoft Outlook 2010, русская версия теперь включает Microsoft Outlook 2013. ����� ��������� ������ ��������� � ����������� �������� �������� Exchange, ����������� ����� �������, ����������� �������� ������� ������, ����� ������ � �������� ����� ����� ���������� ������� ������ Exchange. 
    
- **Форматы файлов MAPI**— сведения о конфигурации MAPI были расширены, чтобы пояснить, как можно использовать пути в службе регистрации и поставщиков услуг в [MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Свойства —** добавлены следующие помеченные свойства в дополнение к документации по 38 другим помеченным свойствам и именовамые свойства, которые были добавлены ранее:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI Constants**— были расширены консолидированные константы [MAPI.](mapi-constants.md) В предыдущих выпусках они были распределены по ряду тем, но теперь собраны в одном разделе, чтобы упростить их обнаружение и использование. Они также были расширены для более широкого охвата, включая следующие разделы: 
    
  - Определения для кодов ошибок адресной книги Exchange и магазина сообщений
    
  - Определения для Exchange Server режима кэширования почтовых ящиков
    
## <a name="see-also"></a>См. также



[Начало работы со справочником по MAPI для Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

