---
title: О регистрации хранилищ для индексации
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321828"
---
# <a name="about-registering-stores-for-indexing"></a>О регистрации хранилищ для индексации

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Этот раздел является специфическим для мгновенного поиска в Microsoft Office Outlook 2007.
  
Мгновенный поиск позволяет быстро находить элементы в Outlook. В нем используются компоненты windows Desktop Search.
  
Обработник протокола MAPI проверяет реестр Windows на наличие хранилищ, которые он должен индексировать в целях поиска. Поставщики магазина, которые хотят индексироваться, должны быть зарегистрированы в реестре Windows.
  
По умолчанию поиск на рабочем столе Windows добавляет в реестр Windows четыре типа поставщиков магазина, чтобы разрешить индексацию:
  
- Файлы личных папок в Хранилище (. PST).
    
-  Хранилище Microsoft Exchange, включая все файлы автономных папок (OST). 
    
-  Хранилище для общедоступных папок. 
    
-  Store для Microsoft Office Outlook connector для MSN. 
    
 Сторонние поставщики магазина, которые хотят индексироваться, должны зарегистрироваться в реестре Windows. 
  
> [!NOTE]
> Администраторы и пользователи могут использовать параметр групповой политики, чтобы запретить поиску windows desktop индексировать элементы Outlook. Дополнительные сведения см. в [расширенном поиске на рабочем столе Windows.](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx) 
  
## <a name="registry-keys"></a>Ключи реестра

На компьютере все поставщики store, которые нужно индексировать, должны быть зарегистрированы только в одном из следующих трех реестров в реестре Windows. Обработник протокола MAPI ищет каждый из этих ключей в следующем порядке:
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Каждое значение под ключом соответствует поставщику магазина, который будет индексироваться. Имя значения — это глобальный уникальный идентификатор (GUID) поставщика магазина, который имеет тип **DWORD** и имеет значение 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUID для поставщиков магазина

Свойство MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** guID для хранения MAPI. В следующей таблице описаны GUID для поставщиков магазина, индексы outlook. 
  
||||
|:-----|:-----|:-----|
|**Тип поставщика store** <br/> |**GUID** <br/> |**Примечания** <br/> |
|Файлы личных папок (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID задокументирован в файле общедоступных заговорок mspst.h **как MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID задокументирован в файле общедоступных заголовок edkmdb.h как **pbExchangeProviderPrimaryUserGuid** <br/> |
|Общедоступные папки  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID задокументирован в файле общедоступных заголовок edkmdb.h как **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector для MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Нет  <br/> |
   
## <a name="see-also"></a>См. также



[Сведения об API хранилищ](about-the-store-api.md)

