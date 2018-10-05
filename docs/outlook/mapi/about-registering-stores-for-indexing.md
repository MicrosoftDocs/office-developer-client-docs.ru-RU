---
title: Сведения о регистрации хранилищ для индексирования
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386532"
---
# <a name="about-registering-stores-for-indexing"></a>Сведения о регистрации хранилищ для индексирования

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе специально для мгновенного поиска в Microsoft Office Outlook 2007.
  
Мгновенный поиск позволяет вам быстро находить элементы в Outlook. Он использует компоненты Windows Desktop Search.
  
Обработчик протокола MAPI проверяет реестра Windows для хранилищ, которые следует индексации для поиска. Поставщики хранилища, чтобы быть индексированы должна быть зарегистрирована в реестре Windows.
  
По умолчанию Windows Desktop Search добавляет следующие четыре типа поставщиков хранилища реестра Windows, чтобы разрешить индексирования:
  
- Хранилище для файлов личных папок (. PST-ФАЙЛОВ).
    
-  Хранилище Microsoft Exchange, включая файлы автономной папки (OST-файлы). 
    
-  Хранилище для общих папок. 
    
-  Хранилище для Microsoft Office Outlook Connector для MSN. 
    
 Поставщики хранилища сторонних производителей, которые нужно индексировать необходимо регистрируются в реестре Windows. 
  
> [!NOTE]
> Администраторов и пользователей можно использовать параметр групповой политики, чтобы предотвратить индексирование элементов Outlook Windows Desktop Search. Для получения дополнительных сведений см [Расширение Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Разделы реестра

На компьютере все поставщики хранилища, которые нужно индексировать должна быть зарегистрирована в разделе только один из следующих трех разделов реестра в реестре Windows. Обработчик протокола MAPI выглядит в разделе каждого из этих параметров в следующем порядке:
  
1. \Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]
    
2. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]
    
3. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]
    
 Каждое значение в разделе соответствует поставщик хранилища, будут индексированы. Имя значения — это глобальный уникальный идентификатор (GUID) поставщика хранилища, который типа **DWORD** и его шестнадцатеричное значение 0x00000001. 
  
## <a name="guids-for-store-providers"></a>Идентификаторы GUID для поставщиков хранилища

Свойство MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** указывает идентификатор GUID для хранилища MAPI. Идентификаторы GUID для поставщиков хранилища, что Outlook индексы описаны в следующей таблице. 
  
||||
|:-----|:-----|:-----|
|**Тип поставщика хранилища** <br/> |**GUID** <br/> |**Примечания** <br/> |
|Файлы личных папок (. PST-ФАЙЛОВ)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |Идентификатор GUID описана в mspst.h общедоступных заголовок файл как **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |Идентификатор GUID описана в edkmdb.h общедоступных заголовок файл как **pbExchangeProviderPrimaryUserGuid** <br/> |
|Общедоступные папки  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |Идентификатор GUID описана в edkmdb.h общедоступных заголовок файл как **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector для MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Отсутствует  <br/> |
   
## <a name="see-also"></a>См. также



[Сведения об API хранилищ](about-the-store-api.md)

