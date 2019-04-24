---
title: Установка подсистемы MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Дата последнего изменения: 9 марта 2015 г.'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309641"
---
# <a name="installing-the-mapi-subsystem"></a>Установка подсистемы MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поддерживаемые версии Windows устанавливают библиотеки-заглушки MAPI (Mapi32.dll) в папку _\<ИмяДиска\>_ \Windows\System32. 
  
Ниже перечислены поддерживаемые версии Windows.
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Чтобы правильно установить подсистему MAPI, установите приложение, которое содержит подсистему на основе MAPI, например Microsoft Outlook.
  
Сведения об установленной подсистеме MAPI компьютера см. в системном реестре. Все значения в записях реестра представляют собой строки символов. 
  
Программы установки служб обмена сообщениями отвечают за создание сведений об установке в следующем разделе системного реестра: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Службы обмена сообщениями должны добавлять записи в системный реестр. 
  
В таблице ниже содержится информация о том, как клиенты получают сведения о версии для подсистемы MAPI на своих компьютерах.
  
|**Сведения, которые необходимо проверить**|**Реестр**|
|:-----|:-----|
|Доступность MAPI  <br/> |Найдите раздел реестра `MAPIX=1`.  <br/> |
|Доступная версия MAPI  <br/> |Найдите строку MAPIXVER вида _x.x.x_.  <br/> |
   
## <a name="see-also"></a>См. также



[Общие сведения о программировании MAPI](mapi-programming-overview.md)

