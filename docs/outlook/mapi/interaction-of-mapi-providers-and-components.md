---
title: Взаимодействие компонентов и поставщиков MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cb0f8d5077b4851a50ceb8523943ae760a8ee5ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809475"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Взаимодействие компонентов и поставщиков MAPI

  
  
**Относится к**: Outlook 
  
Поставщиков служб MAPI никакой должны соответствовать определенным правилам для работы с другими компонентами MAPI. Каждый поставщик услуг выполнить следующие действия:
  
- Используйте соответствующие объекты поставщика и входа в систему для инициализации.
    
- Вернуться к системе обмена сообщениями при инициализации бездействия точек входа поставщика.
    
- Зарегистрируйте строки состояния MAPI для каждого ресурса, владельцем которого поставщика и вызовите метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) в соответствующие моменты. 
    
- Используйте метод [IMAPISupport::NewUID](imapisupport-newuid.md) для получения допустимого уникальных идентификаторов (UID). 
    
- Поддерживает общие интерфейсы MAPI на объекты, которые он возвращает.
    
- Использование функций выделения памяти MAPI для выделения памяти, возвращаемых для клиентских приложений и для освобождения памяти, выделенной с другими частями подсистемы MAPI.
    
- Ведение раздела профилей, если это необходимо для хранения учетных данных для базовой системы обмена сообщениями.
    
- Используйте метод [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) для регистрации любых сообщений о функции предварительной обработки. 
    
- Включить соответствующие файлы заголовков (включая mapispi.h), которые определяют распространенные константы, структуры, интерфейсы и возвращаемые значения.
    
- Формат соглашениям для распространенных типов адресов адрес.
    
