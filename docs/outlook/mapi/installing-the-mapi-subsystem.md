---
title: Установка подсистемы MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575352"
---
# <a name="installing-the-mapi-subsystem"></a>Установка подсистемы MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Поддерживаемые версии Windows Установка библиотеки заглушка MAPI, Mapi32.dll, в _ \<диск\>_ \Windows\System32 папки. 
  
Поддерживаемые версии Windows, как показано ниже:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Для правильной установки подсистемы MAPI установите приложения, содержащего подсистемы на основе MAPI, например Microsoft Outlook.
  
Сведения об установке подсистемы MAPI компьютера можно найти в системном реестре. Все значения в записях реестра: строк символов. 
  
Программы установки службы сообщений отвечают за создание сведения об установке в следующий раздел реестра системы: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Службы сообщений необходимо добавить записей системного реестра. 
  
В следующей таблице представлены как клиенты получить сведения о версии подсистемы MAPI на своем компьютере.
  
|**Для проверки**|**Реестра**|
|:-----|:-----|
|Доступность MAPI  <br/> |Найдите `MAPIX=1`.  <br/> |
|Доступная версия MAPI  <br/> |Найдите строку MAPIXVER формы « _x.x.x_».  <br/> |
   
## <a name="see-also"></a>См. также



[����� �������� � ���������������� MAPI](mapi-programming-overview.md)

