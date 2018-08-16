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
ms.openlocfilehash: 4ffd92f44f1fe88b840e8f8119a92d2048f4f526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812590"
---
# <a name="whats-new-in-this-edition"></a>Новые возможности этого выпуска

 
  
**Относится к**: Outlook 
  
Справочник по интерфейсу MAPI Microsoft Outlook 2013 были добавлены документации по различные новые функции. 
  
## <a name="new-content"></a>Новое содержимое

Содержимое было добавлено следующие функции:
  
- Раздел, [Приступая к работе с Справочник по интерфейсу MAPI приложения Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) был обновлен для ссылки получить подробные сведения о программировании на базе модели для ваших функциональных возможностей Outlook и MAPI для идентификации интерфейсы API и технологии, которые являются большинство соответствующие вашим потребностям. Ссылки на который указывает ссылка технической статье также внесены изменения в следующих разделах: 
    
  - [Справочник по MAPI для Outlook](outlook-mapi-reference.md)
    
  - [Обзор справочника по MAPI для Outlook](outlook-mapi-reference-overview.md)
    
- **Пример поставщика хранилища сообщения**— код [Оболочку PST поставщик хранилища](message-store-provider-sample.md) теперь обновлен для распознавания и учета Outlook 2013. Для получения дополнительных сведений см раздел ранее в обновленной версии статьи контента в этом разделе. 
    
- **Автозаполнение потока**— раздел [кэш псевдонимов](nickname-cache.md) ранее **Формат файла Nk2**, обновлены сведения об изменениях в Outlook 2013, а также Outlook 2010. Следующие разделы теперь внесены изменения для предоставления сведений о рекомендации разработчикам формат файла .nk2 для Microsoft Outlook 2003 или Microsoft Office Outlook 2007 и анализа двоичных файлов. Для получения дополнительных сведений см раздел ранее в обновленной версии статьи контента в этом разделе.
    
  - [Профили MAPI](mapi-profiles.md)
    
  - [Кэш псевдонимов](nickname-cache.md)
    
  - [Поток автозаполнения](autocomplete-stream.md)
    
- **Интерфейсы**- [IAddrBook::OpenEntry](iaddrbook-openentry.md) разделе описано способ открытия записи адресной книги и возвращает указатель на интерфейс, используемый для доступа к нему. Ранее содержало флаг в параметре *ulFlags* **MAPI_GAL_ONLY**, который может использоваться для открытия глобальном списке адресов (GAL), только и была обновлена для включения его определение.
    
- **Свойства**— **PR_CONVERSATION_KEY** с именем раздел свойство ([Каноническое свойство PidTagConversationKey](pidtagconversationkey-canonical-property.md)) добавлена и связь со **IPM. MessageManager** только сообщений в Outlook MAPI. Внесены следующие статьи, посвященные документации потока Transport-Neutral Encapsulation формата TNEF () и его: 
    
  - [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Сопоставление атрибутов TNEF со свойствами MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID и attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Ранее изменение содержимого

Контент был добавлен в предыдущих выпусках Справочник по интерфейсу MAPI приложения Outlook следующие функции:
  
- Microsoft Outlook 2013 позволяет не традиционные сценарии, например рядом друг с другом и Click-to-Run. Эти сценарии может усложнить логика, используемая для загрузки в соответствующую библиотеку MAPI. MAPI разработчиков теперь существует возможность явно ссылки на функции MAPI и можно выбрать для явного связывания заглушку MAPI клиент MAPI по умолчанию (например, Msmapi32.dll из Outlook) без прохода через библиотеки MAPI и заглушка Windows MAPI. Дополнительные сведения о явного связывания по сравнению со неявное связывание можно [ссылка на функции MAPI](how-to-link-to-mapi-functions.md). В **Библиотеке заглушка MAPI**, размещенные на веб-сайте [CodePlex](http://mapistublibrary.codeplex.com/) , предоставляет замены сборка для Mapi32.lib, поддерживающего построение приложений MAPI в 32- и 64-разрядная версия. 
    
- **Поддержка 64-разрядная версия Microsoft Outlook**, ссылки на разделы для элементов, которые применяются API были обновлены в соответствии с новой файлы заголовков, которые поддерживают 64-разрядного приложения Outlook. Эти файлы заголовков, доступны для загрузки на [Outlook 2010: файлы заголовков MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Новые примеры кода было указано в [Проверка версии Outlook](how-to-check-the-version-of-outlook.md) , показано, как для проверки, является ли установленная версия Outlook 64-разрядная версия Microsoft Outlook 2010 и был обновлен для Outlook 2013. Если существующие приложения MAPI 32-разрядная версия будет выполняться в 64-разрядной операционной системе с 64-разрядного приложения Outlook установлен, необходимо перестроить приложения 32-разрядная версия как 64-разрядное приложение. Дополнительные сведения о поддержке MAPI для 64-разрядного приложения Outlook можно [Построение приложений MAPI на 32-разрядной и 64-разрядных платформах](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Пример поставщика хранилища сообщения**— [Оболочку PST поставщик хранилища](message-store-provider-sample.md) ранее был обновлен для поддержки 64-разрядную архитектуру. Пример [инициализации оболочку поставщика хранилища PST](initializing-a-wrapped-pst-store-provider.md) раздел теперь дополнены для предоставления сведений о «Wrapped PST-файлов и пути Юникод.» 
    
- **Автозаполнение потока**— раздел [кэш псевдонимов](nickname-cache.md) ранее **Nk2 формата файла**, обновлена для отражения изменений в Outlook 2013, а также в Outlook 2010. Сведения, такие как списки автозаполнения, которая список имен, которое отображает в **, **копия**и **СК Правка** **в то время как пользователь создает сообщение электронной почты, сохраненное в [потоке автозаполнения](autocomplete-stream.md) сообщения на локальном компьютере вместо сохранения его в файл, как и в Outlook 2007. 
    
  - Взаимодействие с потоком автозаполнения
    
  - Загрузка потока автозаполнения
    
  - Сохранение в потоке автозаполнения
    
- **Быстрое завершение работы поддержка клиентов MAPI**— клиентов MAPI теперь можно инициировать быстрого завершения работы и иметь Подсистема MAPI уведомить загруженных поставщиков для сведения к минимуму потерю данных из быстрое завершение работы. Дополнительные интерфейсы были добавлены для клиента и поставщика для поддержки быстрое завершение работы. Дополнительные сведения о быстрое завершение работы можно [Завершение работы клиента в MAPI](client-shutdown-in-mapi.md).
    
- **Структура потока для определения полей для элемента Outlook**— документации по двоичный поток для свойства [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) был добавлен. Это свойство определяет определения всех настраиваемых полей и параметров привязки данных для встроенных полей элемента Outlook. 
    
- **Переопределение личных хранения**— для поддержки переопределение личных папок (PST) хранилища поставщиков **PSTDisableGrow** политики файловой были добавлены следующие интерфейсы и их соответствующих методов: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Использование нескольких учетных записей Exchange**— документация по [API адресной книги MAPI](using-multiple-exchange-accounts.md) был добавлен. Этот интерфейс API был улучшен для поддержки нескольких учетных записей Exchange в Microsoft Outlook 2010 и теперь включает Microsoft Outlook 2013. ����� ��������� ������ ��������� � ����������� �������� �������� Exchange, ����������� ����� �������, ����������� �������� ������� ������, ����� ������ � �������� ����� ����� ���������� ������� ������ Exchange. 
    
- **Форматы файлов MAPI**— сведения о конфигурации MAPI расширена на объясняется, как можно использовать пути в [регистрации служб и поставщиков услуг в MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Свойства**— 38 других свойств с меткой и с именем свойства, которые ранее были добавлены следующие свойства с тегами были добавлены в дополнение к документации:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Константы MAPI**— дополнены консолидированной [Константы MAPI](mapi-constants.md) . В предыдущих выпусках они были распространяется на несколько разделов, но теперь собраны в одном разделе для упрощения их обнаружения и использования. Они также дополнены для предоставления расширенных покрытия, в том числе в следующих разделах: 
    
  - Определения для адресная книга Exchange и коды ошибок хранилища сообщений
    
  - Квоты режима кэширования данных определения для почтовых ящиков Exchange Server
    
## <a name="see-also"></a>См. также



[Начало работы со справочником по MAPI для Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex (en)](http://mapistublibrary.codeplex.com/)
